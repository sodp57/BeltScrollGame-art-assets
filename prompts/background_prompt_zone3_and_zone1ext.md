# 배경 추가 생성 프롬프트 — zone3 재생성 + 구역1 확장 패널

2026-09-24 작성. `docs/background_art_prompt_gpt.md`(3종 최초 생성용)의 후속이다.
이번엔 **새 배경 2장**이 필요하다.

## 왜 이 2장인가 (실측 근거)

| 노드 | 원본 크기 | scale | 화면 커버 | 문제 |
|---|---|---|---|---|
| ZoneBgRuins (노을) | 1783x882 | (0.589, 0.735) | -150~899 (1049px) | 정상. 단 구역1 경계(900)와 정확히 맞아떨어져 **더 늘릴 여유가 0** |
| ZoneBgCourtyard (밤) | 1774x887 | (0.564, 0.731) | 900~1900 (1000px) | 정상 |
| ZoneBgThrone (왕좌) | 2069x**335** | (0.314, **1.934**) | 1900~2549 (649px) | **세로를 1.934배로 늘려 쓰고 있다** — zone1/zone2(0.73배)보다 2.6배 낮은 해상도로 렌더링되는 셈 |

1. **zone3**: 원본 세로가 335px뿐이라 화면(648px)을 채우려고 1.934배 늘린다. 가로는
   0.314배로 줄이니 **가로:세로 왜곡비가 6.2:1** — 그림이 세로로 뭉개지고 가로로 눌린다.
   zone1/zone2와 같은 해상도 계열(세로 ~888px)로 다시 그려야 한다.
2. **구역1 확장**: 노을 배경이 x=899까지밖에 없어서 구역1 경계를 1500으로 넓히려면
   **x=900~1500 구간을 채울 배경이 새로 필요**하다. GPT 한 장의 최대 폭(~1792px)으로는
   전체(1650px 커버)를 한 장에 못 담으므로, **기존 그림에서 이어지는 두 번째 패널**로 만든다.

   **중요 — 무엇을 그릴지는 기존 그림이 정해준다.** 노을 배경의 오른쪽 끝을 실제로 열어
   보니 **이미 성벽 정문(고딕 아치 + 쇠창살 관문)에서 끝난다.** 그래서 이어지는 패널은
   "야외 폐허가 더 이어지는 그림"이 아니라 **성벽을 관통하는 문루 통로(barbican)** 여야
   한다. 이게 덤으로 오래된 문제 하나를 같이 푼다 — 지금은 노을 배경과 밤 배경이 x=900에서
   맞닿아 **노을|밤이 수직선으로 갈리는 이음새**가 보이는데, 사이에 어두운 통로가 들어가면
   "바깥(노을) → 통로(횃불) → 안뜰(달빛)"로 빛이 자연스럽게 넘어가서 이음새가 **장소로
   설명된다.**

   또한 구역1 폭이 1500이 되면 뷰포트(1152)보다 넓어지므로, 어제 사용자가 포기했던
   E1 옵션①(구역1에서 카메라가 안 움직이는 문제)이 `min_camera_span` 없이 저절로 풀린다.

## 목표 크기를 이렇게 정한 이유

zone1/zone2는 `scale.x ≈ 0.57`, `scale.y ≈ 0.73`이다. 즉 원본을 **가로로 23% 더 눌러서**
쓴다(그래서 GPT에는 "가로로 약간 넓게 그린 그림"을 요청하는 게 맞다 — 화면에서 압축되며
정상 비율이 된다). 새 배경도 이 비율을 유지해야 기존 두 구역과 디테일 밀도가 맞는다.

- **zone3**: 커버 649px / 화면높이 648px → 원본 **1120 x 888** (scale 0.579, 0.730)
- **구역1 패널2**: 커버 600px(x=900~1500) → 원본 **1070 x 887** (scale 0.561, 0.731)

크기가 정확히 안 나와도 된다 — GPT가 만든 실제 크기를 알려주면 `scale`을 다시 계산한다.

---

## 프롬프트 1 — zone3 왕좌의 방 재생성

**첨부할 이미지**: `zone2_style_ref.png`
(https://raw.githubusercontent.com/sodp57/BeltScrollGame-art-assets/main/reference/zone2_style_ref.png)

```
# ROLE

You are a senior pixel-art director reverse-engineering Capcom CPS-2 arcade
backgrounds. You are producing ONE stage-background image for a side-scrolling
belt-scroll beat-'em-up built in Godot 4. This image replaces an existing
background in a real, already-playable game. It must look like it was painted
by the same artist, in the same session, as the attached reference image —
that consistency is the primary success criterion, more important than the
beauty of the image on its own.

# THE ATTACHED IMAGE IS GROUND TRUTH

Attached is the ACTUAL zone-2 background currently running in this game, at its
native resolution. Match its technique exactly: outline weight, value-step
count, palette temperature, stone texture treatment, how torch/brazier light
falls, how the floor band is kept readable. Copy the TECHNIQUE, not the
content — this new image is a different room.

# SETTING

A ruined border kingdom called IRONVALE, in the direct tradition of Dungeons &
Dragons — a close cousin to Capcom's "Dungeons & Dragons: Shadow over Mystara"
(CPS-2, 1996). This image is ZONE 3: the Dread Knight's throne hall, the final
interior room of stage 1, where the boss fight happens.

# THE EXACT STYLE TO MATCH

1. OUTLINE. Selective outlining — a darker, more saturated version of the
   adjacent fill color, not a uniform black keyline. Near-black (#0d0a12) only
   where a form turns away from light.
2. SHADING. Three to four FLAT value steps per material plus one highlight. NO
   smooth continuous gradients, NO airbrush blending. Every value change is a
   deliberate, visible step. Key light from the UPPER LEFT, consistently.
3. NO BLUR, NO PHOTOGRAPHIC TEXTURE, NO FILM GRAIN, NO LENS GLOW, NO
   DEPTH-OF-FIELD. These read as "AI concept art," which is the exact failure
   mode to avoid.
4. Crisp hard edges on every distinct object (stone block, banner, brazier
   flame) — no soft blending between an object and what is behind it.
5. COLOR DISCIPLINE. Backgrounds read LOWER contrast and DARKER/cooler than the
   characters, so the sprites pop when standing in front — but still flat-shaded.

# MASTER PALETTE — use these exact hex values, do not invent new colors

OUTLINE / NEUTRAL  #0d0a12 #241d2b #3d3446 #5c5268 #8a8096 #b8b2c0 #e8e4ee
CRIMSON            #3d0a12 #7a1420 #b82936 #e04a4a #ff8a72
GOLD / BRASS       #3d2608 #7a5214 #c08a24 #e8bc4a #ffe89a
STEEL / COOL BLUE  #16203d #2e4470 #5878a8 #8fb0d0 #d0e4f4
GREEN              #0e2a1a #1e5236 #3a8a56 #6cba78 #b4e8a8
PURPLE (arcane)    #24103d #4a2078 #7a3cb8 #a878e0 #d8b8f8
BROWN / WOOD       #2a1a0e #56341c #8a5a32 #b8875a #e0b88a

# OUTPUT SPEC — read carefully, this is a drop-in replacement

- Resolution: 1120 x 888 pixels. This exact size matters: the game squeezes the
  image horizontally to 0.58x and vertically to 0.73x when drawing it, so the
  scene must be drawn roughly 23% WIDER than it should finally look. Draw with
  that in mind — a circular shield boss or a round brazier should be drawn as a
  slightly WIDE ellipse so it becomes a circle on screen.
- Opaque PNG, full-bleed. No transparency, no border, no frame, no margin.
- ABSOLUTELY NO TEXT of any kind anywhere in the image — no title, no label, no
  watermark, no signature.
- The bottom ~50% of the image is the GROUND PLANE (this matches the attached
  reference — measure it there, do not guess). Characters walk in the LOWER HALF
  of that ground plane. Keep the whole ground plane flat, uncluttered and
  readable — sprites are drawn on top of it and nothing there may visually
  compete with a character standing on it.

# DO NOT COPY THE REFERENCE'S CONTENT — ONLY ITS TECHNIQUE

The attached image is zone 2. This image is zone 3, a different room. Your output
must NOT contain the reference's subject matter: no fountain, no hooded stone
figure, no gargoyle statue, no moon, no sky at all, no ivy-covered outdoor
colonnade, no open-air courtyard. Zone 3 is an ENCLOSED INTERIOR — if sky is
visible anywhere in your image, you have drawn the wrong room. Take from the
reference only: outline weight, value-step count, palette, stone texture
treatment, how brazier light falls, how the ground plane is kept readable.

# COMPOSITION — three clear beats, left to right

This room is entered from the LEFT and the boss waits at the RIGHT. Give it
three readable beats so the player can tell how far in they are:

  1. LEFT (entry): a tall broken gothic archway the player walks in through,
     deep shadow, the first pair of braziers burning with pale GREEN witch-fire.
  2. CENTRE: the long hall — towering cracked pillars receding, enormous
     tattered crimson-and-gold banners hanging from an unseen ceiling, a worn
     red carpet running along the floor toward the throne.
  3. RIGHT (destination): a raised stone dais of two or three steps with a
     shattered, oversized iron throne on it, flanked by the largest banners and
     the brightest witch-fire. This is where the boss stands — keep the area
     directly in front of the dais visually CLEAR so the fight reads.

# THE FLOOR'S FAR EDGE MUST NOT BE A STRAIGHT HORIZONTAL LINE

This is a hard requirement, not a style note. The boundary between the walkable
floor and the back wall must VARY across the width — step up at the dais, dip
where the carpet passes between pillars, jog around the brazier plinths. The
game reads this edge and lets the player walk deeper where the floor is deeper,
so a flat line makes the room feel like a rectangle. Make the variation clearly
visible (tens of pixels, not a subtle wobble), and keep it readable as a single
continuous ground boundary.

# KNOWN FAILURE MODE — READ BEFORE YOU START

We have run this exact request before and repeatedly got soft, airbrushed
concept-art paintings — beautiful, but continuous gradients and blurred edges,
NOT hard-edge pixel art — even when the prompt explicitly said "pixel art" and
gave a hex palette. Running an automatic color-quantization pass on that output
destroyed it (detail turned to mud) because there were no clean flat-color
regions to quantize into.

Self-check before delivering: if you zoomed in 3x, would you see distinct flat
color bands with hard edges (like a Super Nintendo background), or smooth
gradients and soft transitions (like a matte painting)? If the latter,
regenerate before showing it to me and say what you corrected.

Before generating, state in one line: the palette subset you will use for
wall/floor/banner, and the value-step count per material. Then generate.
```

---

## 프롬프트 2 — 구역1 확장 패널 (노을 배경 이어그리기)

**첨부할 이미지**: `zone1_right_edge.png`
(https://raw.githubusercontent.com/sodp57/BeltScrollGame-art-assets/main/reference/zone1_right_edge.png)

```
# ROLE

You are a senior pixel-art director reverse-engineering Capcom CPS-2 arcade
backgrounds. You are extending an existing stage background for a side-scrolling
belt-scroll beat-'em-up built in Godot 4. The attached image is the RIGHT-HAND
EDGE of the background that is currently running in the game. Your job is to
draw the NEXT PANEL — the stretch of the same location that continues directly
to the right of it.

This is a continuation, not a new scene. Same location, same moment in time,
same light. If the two panels are placed side by side in the game, the join must
read as one continuous place.

# WHAT MUST CARRY OVER FROM THE ATTACHED IMAGE (hard requirements)

1. GROUND PLANE POSITION AND SCALE. In the attached image the paved ground plane
   begins roughly HALFWAY down the image and fills the bottom half. Measure that
   line on the attached image and start your ground plane at the SAME height.
   The paving stones must be the same size and use the same value steps — a
   character standing at the join must not appear to step onto bigger or smaller
   stones.
2. FLOOR FAR EDGE AT THE JOIN. Where your panel's LEFT edge meets the attached
   panel's right edge, the boundary between walkable floor and the background
   must line up exactly — no sudden step at the join.
3. STONE MATERIAL. Same masonry: same block size, same weathering, same moss and
   crack treatment, same warm-grey-to-violet stone ramp.
4. PALETTE, OUTLINE WEIGHT, VALUE-STEP COUNT. Identical. Copy the technique
   exactly — flat steps, selective darker-saturated outlines, hard edges,
   no gradients, no blur, no photographic texture.
5. LIGHT DIRECTION. Key light from the UPPER LEFT, as in the attached image —
   except where a torch or the far opening is itself the light source, which may
   locally light from its own direction.

Note: unlike the attached panel, YOUR panel is an interior and has almost no sky.
That is intended (see SETTING). Only the far opening at the right shows outside
light. Do not add a sunset sky across the top of your panel.

# YOUR OUTPUT MUST NOT CONTAIN ANY PART OF THE ATTACHED IMAGE

Read this carefully. The attached image is ALREADY in the game and is NOT being
replaced. You are drawing the panel that sits immediately to its RIGHT. Your
image begins exactly where the attached one ends. Do not reproduce, redraw,
extend-and-include, or partially repeat the attached image's content — no second
copy of its gatehouse facade, its portcullis archway, its lion banners or its
brazier plinths may appear in your output. If a viewer can point at any object
and say "that is also in the attached image," you have made a mistake.

# SETTING — what this new stretch contains

A ruined border kingdom called IRONVALE (Dungeons & Dragons tradition, close
cousin to Capcom's "Shadow over Mystara").

The attached panel ends AT the keep's gatehouse — its tall gothic archway with an
iron portcullis is visible at the right of the attached image. So your panel is
what lies immediately BEYOND that archway: **the gate passage through the keep
wall — a barbican tunnel.** The player has just stepped under the arch and is
walking through the thickness of the wall before the courtyard opens up ahead.

This is deliberately an ENCLOSED, TRANSITIONAL space, and that is the point: it
carries the player from the sunset outside to the night courtyard that follows,
so the change of light reads as a place, not as a seam. Three readable beats,
left to right:

  1. LEFT (continuing from the attached edge): still under the outer arch — the
     last of the sunset light spills in from behind the viewer, warm on the left
     faces of the stonework. The paving continues unbroken from the attached
     image. Murder-holes and a raised portcullis mechanism overhead.
  2. CENTRE: the deepest, darkest part of the tunnel — a CHOKE POINT. Massive
     ribbed vaulting, wall torches the only light, dark alcoves with rusted
     chains and a toppled guard bench. Narrowest walkable floor of the panel.
  3. RIGHT: the far mouth of the tunnel — a tall arch opening onto COOL BLUE
     moonlit air, a sliver of the night courtyard beyond it (do not draw the
     courtyard itself in detail, just the cold light and a suggestion of depth).
     The warm torchlight and the cold outside light meet here. Keep the ground in
     front of this opening visually CLEAR — the player fights here.

The light transition across the panel — warm sunset at the left, torchlight in
the middle, cold moonlight at the right — is the single most important thing in
this image. It is what makes the next zone's night courtyard believable.

# MASTER PALETTE — use these exact hex values, do not invent new colors

OUTLINE / NEUTRAL  #0d0a12 #241d2b #3d3446 #5c5268 #8a8096 #b8b2c0 #e8e4ee
CRIMSON            #3d0a12 #7a1420 #b82936 #e04a4a #ff8a72
GOLD / BRASS       #3d2608 #7a5214 #c08a24 #e8bc4a #ffe89a
STEEL / COOL BLUE  #16203d #2e4470 #5878a8 #8fb0d0 #d0e4f4
GREEN              #0e2a1a #1e5236 #3a8a56 #6cba78 #b4e8a8
BROWN / WOOD       #2a1a0e #56341c #8a5a32 #b8875a #e0b88a

# OUTPUT SPEC — read carefully, this is dropped straight into the game

- Resolution: 1070 x 887 pixels. This exact size matters: the game squeezes the
  image horizontally to 0.56x and vertically to 0.73x when drawing it, so the
  scene must be drawn roughly 23% WIDER than it should finally look — draw round
  things as slightly wide ellipses so they become circles on screen. The attached
  reference is already drawn that way; match how wide its shapes look.
- Opaque PNG, full-bleed. No transparency, no border, no frame, no margin.
- ABSOLUTELY NO TEXT anywhere in the image.
- The bottom ~50% is the GROUND PLANE (match where it starts in the attached
  reference — measure it, do not guess). Characters walk in the LOWER HALF of
  that ground plane. Keep it flat, uncluttered, readable. Nothing there may
  compete with a character standing on it.

# THE FLOOR'S FAR EDGE MUST NOT BE A STRAIGHT HORIZONTAL LINE

Hard requirement. The boundary between walkable floor and the background must
VARY across the width — pinch inward at the choke point, open out in the
forecourt, jog around the fallen masonry. The game reads this edge and lets the
player walk deeper where the floor is deeper, so a flat line makes the stage feel
like a rectangle. Make the variation clearly visible (tens of pixels, not a
subtle wobble) and keep it readable as one continuous ground boundary. Where your
panel's LEFT edge meets the attached panel, the far edge must line up with where
the attached image leaves it — no sudden step at the join.

# KNOWN FAILURE MODE — READ BEFORE YOU START

We have run this exact request before and repeatedly got soft, airbrushed
concept-art paintings — beautiful, but continuous gradients and blurred edges,
NOT hard-edge pixel art — even when told "pixel art" and given a hex palette.
Quantizing that output afterward destroyed it (detail turned to mud) because
there were no clean flat-color regions to quantize into.

Self-check before delivering: (a) zoomed in 3x, do you see distinct flat color
bands with hard edges, or smooth gradients? If gradients, regenerate. (b) Hold
your panel's left edge against the attached image's right edge — does the sky
band, the horizon line, and the floor's far edge continue without a visible
step? If not, fix it before delivering.

Before generating, state in one line: which sky bands and floor value steps you
measured off the attached image and will continue. Then generate.
```

---

## 받자마자 먼저 볼 것 (프롬프트로는 못 막는 것들)

프롬프트에 금지 문구를 넣어도 이미지 모델이 참고 이미지를 베끼는 건 완전히는 안 막힌다
(2026-09-24 jev로 검증: 금지 문구를 넣은 뒤에도 잔존 위험 0.74로 "여전히 남음"). 그래서
**받는 쪽에서 확인하는 절차**로 대신한다. 아래에 하나라도 걸리면 재생성 요청:

1. **참고 이미지 복제 여부** — 패널2에 성문 파사드·쇠창살 아치·사자 깃발·화로 받침이
   다시 나오면 실패. zone3에 분수·가고일·달·하늘이 보이면 실패(실내여야 함).
2. **하드엣지 여부** — 3배 확대해서 평평한 색 띠인지 그라데이션인지 본다. 정량으로는
   기존 배경과 프레임당 고유 색 수를 비교한다(zone1/zone2는 5.8만 색 수준).
3. **바닥 far edge가 직선인지** — 직선이면 FloorProfile을 넣을 게 없어진다. 재생성.
4. **이음선** — 패널2의 왼쪽 끝을 기존 노을 배경 오른쪽 끝에 붙여보고 바닥 경계·돌
   크기가 튀는지 본다.
5. **글자** — 이미지 안에 어떤 글자든 있으면 재생성(지우면 밑 픽셀이 상한다).

## 받은 뒤에 (Claude가 처리)

1. 이미지 2장을 `art_preview/backgrounds/`에 저장(`zone3_throne.png` 덮어쓰기,
   새 패널은 `zone1_ruins_b.png`).
2. `scenes/main.tscn`:
   - `ZoneBgThrone`의 `scale` 재계산
   - `ZoneBgRuins2` 노드 신설(position x=900), `ZoneBgCourtyard`를 x=1500으로 이동
   - `Zone1.lock_x` 900→1500, 그 뒤 구역·배치물 전부 +600 시프트
   - `SpawnPoint3Brute`를 플레이어 뒤에서 스폰되지 않도록 이동
   - `TreasureRoom1`(현재 x=3000~3400)을 새 zone3 구간과 겹치지 않게 이동
3. `FloorProfile` 제어점: 새 배경 2장에 격자를 그려 실측 후 제어점 추가·시프트.
4. `--headless --import` → QA 캡처로 구역별 정렬 확인.
