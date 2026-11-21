# 17. 방 맵 문 방향 고치기 + 높낮이 층 맵 2장 (11/20 아트)

16번으로 받은 방 8장은 모두 문이 뒷벽(북쪽)에 있습니다. 방 문은 **본길 맵에서 들어간 방향의 반대편**에 있어야 자연스럽습니다.

| 본길 맵에서 들어가는 곳 | 게임 방향 | 방 안의 문 |
|---|---|---|
| 뒷벽의 문 | 위(UP) | **앞쪽(화면 아래 가장자리)** — 남쪽 |
| 맵 왼쪽 끝 | 왼쪽(LEFT) | **오른쪽 벽** — 동쪽 |
| 바닥 앞 가장자리로 내려가는 길 | 아래(DOWN) | 뒷벽 — 북쪽(지금 그림 그대로) |
| 맵 오른쪽 끝 | 오른쪽 | 왼쪽 벽 — 본길 출구 자리라 이번엔 안 씀 |

## 방 배치안 (본길 맵 그림을 보고 고름)

| 방 | 들어가는 곳(본길 맵) | 방 안 문 | 그림 |
|---|---|---|---|
| 1-A 보물 창고 | 샛길(side_route) 왼쪽 위로 오르는 계단 | 오른쪽 벽(계단 꼭대기) | **다시** |
| 1-B 경비대 무기고 | 성문 통로(gate_passage) 뒷벽의 나무문 | 앞쪽 | **다시** |
| 2-A 사냥꾼의 오두막 | 안개 낀 입구 앞쪽으로 빠지는 오솔길 | 뒷벽 | 그대로 |
| 2-B 뿌리 아래 제단 → **야외 공터** | 안개 낀 입구 왼쪽 끝 | 오른쪽(숲길 틈) | **다시** |
| 3-A 광부 쉼터 | 용암 궤도 뒷벽의 나무틀 갱도 입구(소품 얹음) | 앞쪽 | **다시** |
| 3-B 수정 동굴 | 유황 펌프장 앞쪽 바닥의 부서진 쇠창살 구멍 | 뒷벽(레일 갱도) | 그대로 |
| 4-A 유골 예배실 | 납골당 회랑 왼쪽 끝 | 오른쪽 벽 | **다시** |
| 4-B 기사단 문서고 | 깊은 묘역 뒷벽(문 소품 얹음) | 앞쪽 | **다시** |

다시 그릴 것 6장. 같은 Gemini 대화에 이어서, 한 장씩. 먼저 "문 위치 규칙"을 한 번 보낸 뒤 각 방 메시지를 보냅니다.

## 문 위치 규칙 (먼저 한 번)
```
Correction for the side rooms: the doorway is NOT always in the back wall. From now on each room tells you where its ONE exit is.
Keep everything else the same (one screen 16:9, back wall about the top 40%, plain readable floor reaching the bottom, left and right edges).
- "EXIT SOUTH": the exit is behind the camera. The back wall has NO door and NO opening. At the bottom edge of the image,
  a little left of center, show the threshold of the exit: two short dark door-post stubs cut off by the bottom edge, a worn
  step between them, and a faint patch of lighter floor in front of it. The rest of the bottom edge is plain floor.
- "EXIT EAST": the exit is in the RIGHT side wall. The back wall has NO door. Show the right side wall a bit wider than the left
  (about the right 15% of the image, slanted in perspective) with one open dark doorway standing on the floor, at mid floor depth.
- "EXIT WEST": the same on the LEFT side wall.
- "OUTDOOR": no ceiling and no built walls; the room is an open clearing closed in by natural edges (cliffs, roots, thickets).
  The sky is dark and flat. The exit is a gap in those natural edges where the path continues.
```

## 1-A 보물 창고 — EXIT EAST (계단 꼭대기)
```
Redo "Royal Treasury" with EXIT EAST: same room and mood as before (iron-banded alcoves, looted bent bars, faded royal banner,
red carpet), but the back wall has no doorway. In the right side wall, the exit is the top of a stone staircase coming UP into
the room: an open arch with the first two or three steps visible going down out of sight. The red carpet runs from that arch
toward the left of the room.
```

## 1-B 경비대 무기고 — EXIT SOUTH
```
Redo "Guard Armory" with EXIT SOUTH: same room and mood as before (weapon racks, cold stone fireplace, blank notice board,
plank floor), but the back wall has no doorway: fill that spot with a tall empty armor stand and more racks.
The exit threshold is at the bottom edge, a little left of center.
```

## 2-B 뿌리 공터 — OUTDOOR, EXIT EAST
```
Redo "Root Shrine" as an OUTDOOR room with EXIT EAST: a small hidden clearing in the cursed forest, walled in on the left and back
by the huge twisted dark-red roots of a dead giant tree (the roots arch over the top corners, but the middle of the sky is open,
dark blood-red and flat, no moon disc). The forgotten druid stone altar with spiral carvings (no letters) stands against the roots
of the back wall. On the right side, the roots part into a narrow gap where a dirt path leads out (the exit).
Floor of packed dark earth with flat stones, plain and readable. Mood: deep red-brown, moss green, blood-red sky.
```

## 3-A 광부 쉼터 — EXIT SOUTH
```
Redo "Miners' Rest" with EXIT SOUTH: same room and mood as before (rock walls with timber beams, bunk beds, helmets and pickaxes
on pegs, scribbled chalk board, unlit oil lamps), but the back wall has no tunnel or doorway: put a second bunk bed and a tool
shelf there instead. The exit threshold at the bottom edge is framed by two timber posts (cut off by the bottom edge).
```

## 4-A 유골 예배실 — EXIT EAST
```
Redo "Ossuary Chapel" with EXIT EAST: same room and mood as before (back wall of stacked skulls and bones, the old knight's helmet
in a stone niche, dull teal moss, unlit candle stubs), but the back wall has no doorway: continue the bone shelves there.
The exit is a pointed stone arch in the right side wall, open and dark, with a carved skull keystone.
```

## 4-B 기사단 문서고 — EXIT SOUTH
```
Redo "Order Archive" with EXIT SOUTH: same room and mood as before (stone bookshelves, scroll racks, torn teal banner with a silver
sword crest, reading desk, thin flat water only along the back edge of the floor), but the back wall has no doorway: put one more
bookshelf there. The exit threshold is at the bottom edge, a little left of center.
```

---

# 높낮이 층 맵 (HeightTier) — 2장

- 장치: 한 맵에 **낮은 바닥(앞)과 높은 단(뒤)**, 단 앞면의 턱에서만 점프로 오르고 끝을 밀어 뛰어내림(더블 드래곤식). 보스는 못 둠.
- 넣을 자리(추천): 두 스테이지 모두 **본1과 본2 사이**(갈림길 전이라 모든 플레이어가 지남).
  - 스테이지 2: 안개 낀 입구 → **가시등 벼랑**(오르내리기 둘 다) → 핏빛 늪지대
  - 스테이지 3: 녹슨 승강기 → **계단식 채굴장**(내려가기만 — 왼쪽 높은 단에서 시작, 단 끝에서 뛰어내려야 오른쪽으로 감) → 유황 펌프장
- 규격: 21:9(2520x1080). 높은 단의 앞면(턱) 높이 = 캐릭터 키 정도(그림 높이의 약 1/6).
- 같은 스테이지 배경을 만든 Gemini 대화에 이어서 보냅니다(없으면 16번의 "새 대화 첫 메시지" + 그 스테이지 배경 1~2장 첨부).

## 스테이지 2 — 가시등 벼랑 (Thornback Ridge)
```
Background - "Thornback Ridge" (ULTRA-WIDE 21:9, for example 2520x1080), same style and static-plate rules as this stage.
A forest path running along the foot of a rocky ridge in the cursed forest. This map has TWO WALKABLE LEVELS:
- LOWER PATH: wet dark earth along the bottom of the image, across the FULL width, plain and evenly lit.
- RAISED LEDGE: behind the lower path (higher in the image), from about 30% to 85% of the width, a flat-topped rock shelf
  with a plain walkable top of packed earth (deep enough for a person to stand and walk along it, about 1/8 of the image height).
  Its FRONT FACE is a clear vertical wall of dark rock and roots, about as tall as one person (about 1/6 of the image height),
  running straight and horizontal so it reads as a step people can jump up onto. Both short ends of the ledge are steep rock.
- Behind the ledge: dense bare blood-red trees, torn red cloth on branches, thorn bushes; left and right of the ledge the trees
  come down to the lower path. Dark red sky, no moon disc, no fog.
Keep both walkable surfaces plain (no rocks or bushes on them). Mood: dark brown earth, blood-red trees, grey rock.
```

## 스테이지 3 — 계단식 채굴장 (Terraced Dig)
```
Background - "Terraced Dig" (ULTRA-WIDE 21:9, for example 2520x1080), same style and static-plate rules as this stage.
An open-pit dig inside the mine, cut into big terraces. This map has TWO WALKABLE LEVELS:
- UPPER TERRACE: on the LEFT, from the left edge to about 60% of the width, a flat walkable shelf of iron plates and packed rock
  (higher in the image, deep enough to walk along, about 1/8 of the image height). Its FRONT FACE is a vertical rock cut reinforced
  with horizontal timber planks and posts, about as tall as one person (about 1/6 of the image height), straight and horizontal.
  The right end of the terrace stops at a timber railing that is broken open.
- LOWER FLOOR: packed dirt with a few planks along the bottom of the image across the FULL width; on the right side it is the only
  floor, continuing to a round tunnel mouth in the rock at the right edge.
- Behind: rough rock walls with dim mustard sulfur streaks, an idle wooden crane with a hanging hook, a winch, stacked timber.
Keep both walkable surfaces plain (no objects on them). Mood: rust orange, ochre dirt, black iron.
```

---

# 승강기 하강 맵 (스테이지 3, 수직 특이 맵) — 2장

- 흐름: 녹슨 승강기(본1) → **승강기 하강** → 계단식 채굴장(층 맵) → 유황 펌프장. 발판은 고정, 뒤 벽이 위로 흘러가며 적이 위에서 뛰어내림.
- 스테이지 3 대화에 이어서 한 장씩. 위아래 이음새는 아트가 가공으로 맞춥니다.

## A. 수직갱 벽 (세로로 반복되는 그림)
```
Background - "Lift Shaft Wall": a SEAMLESS VERTICAL LOOP, 16:9 width but TWO screens tall (for example 1920x2160), same style and
static-plate rules as this stage. It is the back wall of a deep vertical mine shaft seen while riding a lift down, and the image
will be repeated top-to-bottom, so the TOP EDGE AND BOTTOM EDGE MUST MATCH and nothing may be cut in half at those edges.
- Rough dark rock with dim mustard sulfur streaks, horizontal timber support frames, rusty pipes and thick cables running
  VERTICALLY through the whole height, small empty side tunnels in the rock, a few unlit hanging lamps.
- Two tall iron guide rails run straight down the full height near the left and right sides (the lift slides along them).
- No floor, no ground, no lift, no horizon: only wall from top to bottom. Evenly lit, slightly darker toward the left and right edges.
Mood: rust orange, ochre, black iron.
```

## B. 승강기 발판
```
Background - "Lift Platform" (16:9, for example 1920x1080), same style. A big rusty iron mine lift platform seen from the same slight
high angle as the floors of this stage. The platform's walkable top fills the bottom 55% of the image from the left edge to the
right edge: riveted iron plates, plain and evenly lit, a thin yellow-black hazard stripe only along its far (back) edge.
At the two back corners, thick iron posts with chains going straight up out of the top of the image. A low iron railing only on the
back edge (no railing at the front or sides). Everything above and behind the platform is a FLAT SOLID MAGENTA (#FF00FF) background
with no shading, so it can be cut out. No objects on the platform.
```
