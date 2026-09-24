# 배경 프롬프트 — 왕좌의 방 (가로로 넓게 재생성)

2026-09-25 작성. 맵 전환 구조로 가면서 **왕좌의 방이 단독 맵이 되려면 더 넓어야** 해서
다시 받는다. 지금 그림(1120x888)은 버리지 않고 이 프롬프트의 참고 이미지로 쓴다 —
같은 방을 더 넓은 화각으로 다시 그리는 것이다.

## 왜 다시 받나

맵 전환(페이드) 구조에서는 **맵 하나가 화면(1152x648)을 스스로 다 채워야 한다.**
안 그러면 배경 바깥의 빈 공간이 화면에 보인다. 배경은 세로로 화면을 채우도록
`648/원본높이` 배율로 들어가므로, 가로로 화면을 채우려면 **원본 비율이 최소 1.78:1**
이어야 한다.

| 배경 | 원본 | 비율 | 화면 커버 | 단독 맵 |
|---|---|---|---|---|
| 성문 폐허 | 1783x882 | 2.02 | 1310px | 가능 |
| 밤 안뜰 | 1774x887 | 2.00 | 1296px | 가능 |
| 대계단 홀 | 1774x887 | 2.00 | 1296px | 가능 |
| 문루 통로 | 1070x887 | 1.21 | 782px | 불가(다른 맵에 붙여 씀) |
| **왕좌의 방** | **1120x888** | **1.26** | **817px** | **불가 ← 이번에 해결** |

보스방은 스테이지의 마지막 방이라 다른 그림에 붙여 쓸 수가 없다(붙일 상대가 없고,
대계단 홀에 붙여봤더니 홀의 주황 횃불빛과 왕좌의 방의 청록빛이 바닥에서 수직으로
끊겨 보인다). 그래서 **대계단 홀과 같은 2:1로** 다시 받는다.

## 지난번과 달라진 지시 두 가지 (중요)

**1. "가로로 23% 넓게 그려라"를 뺐다.** 지난 두 번의 프롬프트에 이 지시를 넣었는데
**GPT가 두 번 다 무시했고, 무시한 게 오히려 맞았다.** 확인 방법은 이랬다 — 밤 안뜰
원본에서 보름달을 잘라내 보니 **완벽한 원**이었고, 대계단 홀의 샹들리에 고리도
정상 비율이었다. 즉 그림은 처음부터 정상 비율로 그려져 있었다.

문제는 게임 쪽이었다. `main.tscn`이 배경을 가로 0.56배·세로 0.73배로 그리고 있어서
(구역 폭에 억지로 맞추느라 그렇게 잡힌 값이다) **화면에서는 배경이 가로로 23%
눌려 나오고 있었다.** 달이 세로로 긴 타원이 되고 있었던 것이다. 이건 게임 쪽에서
가로·세로 같은 배율로 고친다. 그러니 **그림은 정상 비율로 그리면 된다.**

**2. 바닥 far edge 요구를 더 세게 걸었다.** 지난번 왕좌의 방이 이것만 못 지켰다
(변화 26px — 거의 직선). 이번엔 수치와 위치를 지정했다.

---

## 프롬프트 (아래 코드블록 전체를 복사)

**첨부할 이미지**: 지금 쓰고 있는 왕좌의 방 (같은 방을 더 넓게 다시 그리는 것)
https://raw.githubusercontent.com/sodp57/BeltScrollGame-art-assets/main/reference/zone3_throne_ref.png

```
# ROLE

You are a senior pixel-art director reverse-engineering Capcom CPS-2 arcade
backgrounds. You are producing ONE stage-background image for a side-scrolling
belt-scroll beat-'em-up built in Godot 4. This is a real, already-playable game
and this image drops straight into it.

# WHAT THIS IS — A RE-FRAME, NOT A NEW ROOM

Attached is the SAME ROOM as it currently exists in the game: the Dread Knight's
throne hall, the final boss arena of stage 1. It works, but it is too narrow a
frame — the game needs this room drawn WIDER so it fills the screen on its own.

Your job: draw THIS SAME ROOM again, same architecture, same mood, same palette,
same rendering technique — but with a WIDER field of view, as if the camera
stepped back and took in more of the hall to the left and right. Keep the throne
and its dais as the destination on the RIGHT. Everything that made the attached
image work should still be there; there is simply more room around it.

Treat the attached image as ground truth for technique AND content. Match its
outline weight, value-step count, palette, stone masonry, the pale GREEN
witch-fire in the braziers, the crimson-and-gold banners, the red carpet, and
the way the paved floor is kept readable.

# SETTING

A ruined border kingdom called IRONVALE, in the direct tradition of Dungeons &
Dragons — a close cousin to Capcom's "Dungeons & Dragons: Shadow over Mystara"
(CPS-2, 1996). This is the throne hall at the heart of the usurped keep: cold,
enclosed, and final. Banners bear a gold lion on crimson.

# COMPOSITION — the extra width goes here

The player enters from the LEFT and the boss waits at the RIGHT.

  1. LEFT (new space): extend the hall backwards — more columns receding, a tall
     broken gothic archway the player came in through, deep shadow, rubble and a
     toppled brazier. This is where the player lands when the fight starts, so
     keep the floor here OPEN.
  2. CENTRE (the fight): the widest, most open stretch of floor in the room. This
     is where the boss fight actually happens, so it must be visually CALM —
     columns and banners along the back, nothing busy on the floor itself.
  3. RIGHT (the throne): the raised dais with the shattered iron throne, the
     largest banners, the brightest witch-fire — as in the attached image. Keep
     the ground directly in front of the dais clear so the fight reads there too.

# THE EXACT STYLE TO MATCH

1. OUTLINE. Selective outlining — a darker, more saturated version of the
   adjacent fill color, not a uniform black keyline. Near-black (#0d0a12) only
   where a form turns away from light.
2. SHADING. Three to four FLAT value steps per material plus one highlight. NO
   smooth continuous gradients, NO airbrush blending. Every value change is a
   deliberate, visible step.
3. NO BLUR, NO PHOTOGRAPHIC TEXTURE, NO FILM GRAIN, NO LENS GLOW, NO
   DEPTH-OF-FIELD. These read as "AI concept art," which is the exact failure
   mode to avoid.
4. Crisp hard edges on every distinct object — no soft blending between an
   object and what is behind it.
5. This room is an ENCLOSED INTERIOR. No sky, no moon, no outdoor view anywhere.

# MASTER PALETTE — use these exact hex values, do not invent new colors

OUTLINE / NEUTRAL  #0d0a12 #241d2b #3d3446 #5c5268 #8a8096 #b8b2c0 #e8e4ee
CRIMSON            #3d0a12 #7a1420 #b82936 #e04a4a #ff8a72
GOLD / BRASS       #3d2608 #7a5214 #c08a24 #e8bc4a #ffe89a
STEEL / COOL BLUE  #16203d #2e4470 #5878a8 #8fb0d0 #d0e4f4
GREEN              #0e2a1a #1e5236 #3a8a56 #6cba78 #b4e8a8
BROWN / WOOD       #2a1a0e #56341c #8a5a32 #b8875a #e0b88a

# OUTPUT SPEC

- Resolution: 1774 x 887 pixels (2:1). If you cannot hit that exactly, KEEP THE
  2:1 ASPECT RATIO and state the size you produced.
- Draw at NORMAL, natural proportions. Do not pre-stretch or pre-squash the
  scene in either direction — a circular object should be drawn as a circle.
  The game scales this image by the same factor horizontally and vertically.
- Opaque PNG, full-bleed. No transparency, no border, no frame, no margin.
- ABSOLUTELY NO TEXT of any kind anywhere in the image.
- The bottom ~50% is the GROUND PLANE (match where it starts in the attached
  reference). Characters walk in the LOWER HALF of it. Keep it flat, uncluttered
  and readable; nothing there may visually compete with a character standing on it.

# THE FLOOR'S FAR EDGE MUST NOT BE A STRAIGHT HORIZONTAL LINE

Read this twice — it is the ONE thing the attached image got wrong, and the
reason it looks like a plain rectangle. In the attached image the boundary
between the walkable floor and the back of the room varies by only about 26
pixels across the whole width. That is not enough.

In your version that boundary must vary by **60 to 100 pixels** between its
highest and lowest points, and must change direction **at least four times**
across the width. Concretely:
  - Let the floor run DEEP (boundary high up the image) in the open centre.
  - PINCH IN (boundary low) where column bases, rubble and brazier plinths
    intrude from the back.
  - Step UP at the dais so the throne sits clearly above the fighting floor.
  - Dip again at the left archway where the player enters.
A viewer should be able to trace the ground boundary with a finger and feel it
rise and fall several times.

# KNOWN FAILURE MODE — READ BEFORE YOU START

We have run this request before and repeatedly got soft, airbrushed concept-art
paintings — beautiful, but continuous gradients and blurred edges, NOT hard-edge
pixel art — even when told "pixel art" and given a hex palette.

Self-check before delivering: (a) zoomed in 3x, do you see distinct flat color
bands with hard edges, or smooth gradients? If gradients, regenerate. (b) Trace
the floor's far edge — does it rise and fall by tens of pixels, changing
direction at least four times? If it is close to a straight line, redo it.
(c) Is it recognisably the SAME room as the attached image, just wider? (d) Any
text anywhere? There must not be.

Before generating, state in one line: the palette subset for wall/floor/banner,
the value-step count per material, and the four x-positions where the floor
boundary changes direction. Then generate.
```

---

## 받은 뒤에

1. **바닥 far edge 변화량을 먼저 잰다** — 격자를 씌워 최고점-최저점 차이가 60px 이상인지.
   미달이면 재생성 요청(지난번에 이걸 그냥 받았다가 아쉬웠다).
2. 같은 방으로 보이는지 — 초록 위치불, 붉은 카펫, 부서진 철 왕좌가 다 있는지.
3. 하드엣지 — 기존 배경과 고유 색 수 비교(기존 21~35만 대역).
4. 실내일 것(하늘 금지), 글자 없을 것, 비율 2:1.
