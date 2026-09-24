# 배경 프롬프트 — 대계단 홀 (스테이지1 신규 맵)

2026-09-24 작성. 맵 전환(페이드아웃/인) 구조로 바꾸기로 하면서, 스테이지1에서
**유일하게 비는 자리**를 채우기 위한 배경 1장이다.

## 왜 이 맵인가

현재 스테이지1의 장소는 4곳이다:

| # | 맵 | 그림 | 상태 |
|---|---|---|---|
| 1 | 성문 폐허 (노을, 야외) | `zone1_ruins.png` | 있음 |
| 2 | 문루 통로 (횃불, 실내) | `zone1_ruins_b.png` | 있음 |
| 3 | 밤 안뜰 (달빛, 야외) | `zone2_courtyard.png` | 있음 |
| — | **성 내부로 올라가는 계단 홀** | **없음** | **이 문서** |
| 4 | 왕좌의 방 (실내, 보스) | `zone3_throne.png` | 있음 |
| 샛길 | 보물방 | `vault_room.png` | 있음 |

**안뜰(야외 달빛)에서 곧장 왕좌의 방(성 깊은 실내)으로 넘어가는 게 유일하게 튀는
구간이다.** 1→2→3은 "바깥 → 문루 → 안뜰"로 빛이 이어지게 만들어뒀는데(S43), 3→4는
장소가 갑자기 바뀐다. 그 사이에 **성 안으로 들어가 위층으로 올라가는 계단 홀**이
들어가면 흐름이 완성되고, 보스방 직전의 "숨 고르는 구간"도 생긴다.

## 이전 프롬프트와 다른 점 — 이 맵은 이어붙이지 않는다

맵 전환이 페이드아웃/인이라 **이 그림은 앞뒤 어느 그림과도 맞물릴 필요가 없다.**
그래서 이음새 관련 요구(하늘 띠 잇기, 바닥 far edge 맞추기, 참고 이미지 복제 금지)가
전부 빠졌고, 대신 **독립된 한 화면으로서 완결성**을 요구한다.

## 크기

가로로 스크롤되는 한 화면이다. 기존 안뜰과 같은 계열인 **1774 x 887** (2:1)로 받으면
`scale=(0.564, 0.731)`로 그대로 들어간다. 정확히 못 맞춰도 되니 **2:1 비율만 지키고
실제 크기를 알려주면** 내가 맞춰서 줄인다(지난번에도 1409x1116로 와서 1120x888로
줄여 넣었다 — 비율만 맞으면 문제없다).

---

## 프롬프트 (아래 코드블록 전체를 복사)

**첨부할 이미지**: 왕좌의 방 (이 맵이 이어질 목적지 — 실내 톤을 여기에 맞춘다)
https://raw.githubusercontent.com/sodp57/BeltScrollGame-art-assets/main/reference/zone3_throne_ref.png

```
# ROLE

You are a senior pixel-art director reverse-engineering Capcom CPS-2 arcade
backgrounds. You are producing ONE stage-background image for a side-scrolling
belt-scroll beat-'em-up built in Godot 4. This is a real, already-playable game
and this image drops straight into it. It must look like it was painted by the
same artist, in the same session, as the attached reference — that consistency
is the primary success criterion, more important than the beauty of the image
on its own.

# THE ATTACHED IMAGE IS GROUND TRUTH FOR TECHNIQUE

Attached is an actual interior background from this game (the castle's throne
hall), at its native resolution. Match its technique exactly: outline weight,
value-step count, palette temperature, stone masonry treatment, how torch and
brazier light pools on the floor, how the walkable ground is kept readable and
uncluttered.

Copy the TECHNIQUE, not the content — this is a DIFFERENT room, earlier in the
castle. Do not reuse its throne, its dais, its green witch-fire, or its specific
banner arrangement.

# SETTING

A ruined border kingdom called IRONVALE, in the direct tradition of Dungeons &
Dragons — a close cousin to Capcom's "Dungeons & Dragons: Shadow over Mystara"
(CPS-2, 1996). Tattered heraldic banners bear a gold lion on crimson.

This image is THE GRAND STAIRCASE HALL. The player has just fought through a
moonlit outdoor courtyard and has now stepped INSIDE the keep proper. This is
the hall that climbs toward the throne room above. It is the calm before the
boss — grand, oppressive, and clearly "deeper in" than anywhere before it.

# COMPOSITION — three clear beats, left to right

The player enters from the LEFT and exits at the RIGHT. Give three readable
beats so they can tell how far through they are:

  1. LEFT (entry): a heavy doorway back out to the night — cold blue moonlight
     spilling in across the floor from behind the player, immediately swallowed
     by warm interior torchlight. Cracked flagstones, a fallen suit of armour.
  2. CENTRE: the hall itself at its widest — towering stone columns, a vaulted
     ceiling disappearing into darkness above, enormous tattered crimson-and-gold
     banners, iron chandeliers hanging on chains, wall torches. Keep this middle
     stretch of floor OPEN and uncluttered: this is where the fight happens.
  3. RIGHT (exit): the grand staircase — a wide stone stair rising and turning
     out of frame toward the upper floor, flanked by statues or column bases,
     with the brightest light at its foot. This reads as "the way onward."

# THE EXACT STYLE TO MATCH

1. OUTLINE. Selective outlining — a darker, more saturated version of the
   adjacent fill color, not a uniform black keyline. Near-black (#0d0a12) only
   where a form turns away from light.
2. SHADING. Three to four FLAT value steps per material plus one highlight. NO
   smooth continuous gradients, NO airbrush blending. Every value change is a
   deliberate, visible step. Key light from the UPPER LEFT, except where a torch
   or the doorway is itself the light source.
3. NO BLUR, NO PHOTOGRAPHIC TEXTURE, NO FILM GRAIN, NO LENS GLOW, NO
   DEPTH-OF-FIELD. These read as "AI concept art," which is the exact failure
   mode to avoid.
4. Crisp hard edges on every distinct object — no soft blending between an
   object and what is behind it.
5. COLOR DISCIPLINE. The background reads LOWER contrast and DARKER than the
   character sprites so they pop when standing in front — but still flat-shaded.

# MASTER PALETTE — use these exact hex values, do not invent new colors

OUTLINE / NEUTRAL  #0d0a12 #241d2b #3d3446 #5c5268 #8a8096 #b8b2c0 #e8e4ee
CRIMSON            #3d0a12 #7a1420 #b82936 #e04a4a #ff8a72
GOLD / BRASS       #3d2608 #7a5214 #c08a24 #e8bc4a #ffe89a
STEEL / COOL BLUE  #16203d #2e4470 #5878a8 #8fb0d0 #d0e4f4
GREEN              #0e2a1a #1e5236 #3a8a56 #6cba78 #b4e8a8
BROWN / WOOD       #2a1a0e #56341c #8a5a32 #b8875a #e0b88a

# OUTPUT SPEC — this drops straight into the game

- Resolution: 1774 x 887 pixels (2:1). If you cannot hit that exactly, KEEP THE
  2:1 ASPECT RATIO and state the size you produced — it will be resized.
- The game squeezes the image horizontally to about 0.56x and vertically to
  0.73x when drawing it, so the scene must be drawn roughly 23% WIDER than it
  should finally look. Draw round things (shield bosses, chandelier rings) as
  slightly WIDE ellipses so they become circles on screen. The attached
  reference is already drawn that way — match how wide its shapes look.
- Opaque PNG, full-bleed. No transparency, no border, no frame, no margin.
- ABSOLUTELY NO TEXT of any kind anywhere in the image — no title, no label, no
  watermark, no signature.
- The bottom ~50% is the GROUND PLANE (match where it starts in the attached
  reference — measure it, do not guess). Characters walk in the LOWER HALF of
  that ground plane. Keep it flat, uncluttered and readable; nothing there may
  visually compete with a character standing on it.

# THE FLOOR'S FAR EDGE MUST NOT BE A STRAIGHT HORIZONTAL LINE

Hard requirement, and the ONE thing the last batch got wrong — the throne hall
came back with an almost perfectly flat floor boundary, which makes the room
read as a plain rectangle.

The boundary between the walkable floor and the back of the room must VARY
ACROSS THE WIDTH by a clearly visible amount — think 60 to 100 pixels of
difference between its highest and lowest points, not 20. Concretely: let the
floor run DEEP (boundary high up) in the open centre of the hall, PINCH IN
(boundary low) where column bases and the fallen armour intrude, and step up
again at the foot of the staircase. Vary it at least four times across the
image. A viewer should be able to trace the ground boundary with a finger and
feel it rise and fall.

# KNOWN FAILURE MODE — READ BEFORE YOU START

We have run this request before and repeatedly got soft, airbrushed concept-art
paintings — beautiful, but continuous gradients and blurred edges, NOT hard-edge
pixel art — even when told "pixel art" and given a hex palette. Quantizing that
output afterward destroyed it (detail turned to mud) because there were no clean
flat-color regions to quantize into.

Self-check before delivering: (a) zoomed in 3x, do you see distinct flat color
bands with hard edges, or smooth gradients? If gradients, regenerate. (b) Does
the floor's far edge visibly rise and fall across the width, by tens of pixels?
If it is close to a straight line, redo it — this is the specific thing that
failed last time. (c) Is there any text anywhere? There must not be.

Before generating, state in one line: the palette subset you will use for
wall/floor/banner, the value-step count per material, and where along the width
you will place the four floor-boundary changes. Then generate.
```

---

## 받자마자 먼저 볼 것

1. **바닥 far edge가 실제로 오르내리는지** — 지난번 왕좌의 방이 여기서 걸렸다.
   격자를 씌워 최고점-최저점 차이를 재고, 60px 미만이면 재생성 요청.
2. **하드엣지** — 기존 배경과 고유 색 수 비교(기존 24~35만 대역).
3. **글자 없음**, **실내일 것**(하늘이 보이면 왼쪽 출입구 너머로만).
4. 비율이 2:1인지 — 아니면 알려준 크기로 `scale` 재계산.
