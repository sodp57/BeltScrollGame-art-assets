# 16. 방 맵 배경 — 스테이지마다 2장, 모두 8장 (11/20 개발 세션 작성)

- **방 맵**은 본길 맵의 뒷벽 문으로 들어갔다가, 같은 문으로 다시 나오는 한 화면짜리 곁방입니다. 적이 남아 있어도 나올 수 있습니다(게임 장치는 11/20 완성).
  안에는 보물 상자·작은 매복·회복 아이템 같은 "들러 갈 이유"를 둡니다. 비밀방(바닥을 부수고 떨어져 보스로 가는 길)과는 다릅니다.
- 규격: 한 화면 **16:9(1920x1080)**. 아트가 384x216으로 맞춘 뒤 정확히 3배로 넣습니다.
- 방의 문은 **뒷벽 바닥선에 붙은 열린 문 하나**입니다. 들어올 때 그 문에서 걸어 나오고, 나갈 때 그 문으로 위 방향을 눌러 나갑니다.
- **대화**: 그 스테이지 배경을 만든 Gemini 대화가 남아 있으면 **그 대화에 이어서** 아래 "이어서 보낼 메시지"만 붙여 넣으세요(화풍이 가장 잘 맞습니다).
  대화가 없으면 새 대화에 "새 대화 첫 메시지"를 먼저 보내고, 첨부로 `refs/stage_bg_layout_guide.png`와 **그 스테이지의 완성 배경 1~2장**을 올리세요.
- 한 번에 한 장씩 보내고, 받은 그림은 Claude 대화창에 첨부해 주세요. 아트 세션이 가공·배치합니다.
- 본길 맵 쪽 "방으로 들어가는 문"(벽에 붙이는 문 그림)은 Gemini가 아니라 아트 세션이 PixelLab으로 따로 만듭니다.

---

## 새 대화 첫 메시지 (공통 — 이어서 쓰는 대화면 건너뜀)
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) finished backgrounds from this stage.
Match the attached pixel art style, detail level and color approach exactly, and follow the layout guide in every image.

Rules for ALL backgrounds in this conversation:
- True pixel art with HARD EDGES: every pixel is a crisp square block (the same block size as the references),
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- The walkable ground is seen from a slight high angle, fairly plain and EVENLY LIT so characters and their shadows stay readable.
- This is a STATIC PLATE: animated things are added later in the game, so draw them in their "off" state:
  NO lit flames (torches, braziers, candles unlit: dark holders only, no glow spots), NO fog, NO falling water, NO floating lights.
- NO objects on the walkable ground (no chests, barrels, crates, rubble, bones) - those are added separately.
- NO characters, NO creatures, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).
Reply "ready" and wait for the first room.
```

## 이어서 보낼 메시지 — 방 공통 규칙 (각 스테이지 첫 방 앞에 한 번)
```
Next I need small SIDE ROOMS for this stage, one image at a time. Same style and rules as before, plus:
- Size: exactly ONE SCREEN, 16:9 (for example 1920x1080). The whole room is visible at once; no wide panorama.
- Layout: the back wall fills roughly the top 40% of the image; the walkable floor fills the bottom 60% and reaches the left, right
  and bottom edges of the image (the side walls must NOT cover the floor - show them only as thin slanted edges at the top corners).
- ONE open doorway in the back wall, standing on the floor line, a little left of the center, about as tall as 1.6 people.
  Draw it OPEN with a dark interior (this is the way back out). No other doors, no stairs, no windows to the outside.
- Keep the floor plain and readable. Decorate only the back wall and the top corners.
```

---

## 스테이지 1 — 무너진 성 (방 2장)

### 1-A 보물 창고 (지금 깨져 있는 `TreasureRoom1`을 이걸로 바꿉니다)
```
Side room 1 - "Royal Treasury": a small vaulted stone treasury deep inside the castle. Back wall of large grey castle stone blocks with
two heavy iron-banded alcoves, empty weapon hooks and a faded royal banner (dark blue with a gold crest shape, no letters).
Iron bars on one alcove are bent open as if looted. Floor of worn grey flagstones with a faded red carpet runner leading from the
doorway toward the camera. Unlit iron wall sconces. Mood: cool grey and gold accents, quiet and abandoned.
```

### 1-B 경비대 무기고
```
Side room 2 - "Guard Armory": the castle guards' armory. Back wall of rough stone with wooden weapon racks (mostly empty, a few
spears and shields hanging), a stone fireplace with no fire, a wooden notice board with blank pinned papers (no writing).
Wooden plank floor with a few dark stains near the walls only (center of the floor plain). Unlit lanterns on hooks.
Mood: warm brown wood and grey stone, slightly messy as if the guards left in a hurry.
```

## 스테이지 2 — 저주받은 숲 (방 2장)

### 2-A 사냥꾼의 오두막
```
Side room 3 - "Hunter's Cabin": the inside of an abandoned hunter's log cabin in the cursed forest. Back wall of dark log beams with
hanging traps, antlers, dried herbs and an empty bow rack. A small cold stone hearth. A tiny window in the back wall shows only
a dark red night sky (no moon disc, no trees in detail). Floor of uneven wooden boards with a worn animal-hide rug shape
(flat, part of the floor). Mood: dark brown and blood-red accents, cramped and eerie.
```

### 2-B 뿌리 아래 제단
```
Side room 4 - "Root Shrine": a hollow under the roots of a giant dead tree. Thick twisted dark-red roots form the back wall and
the ceiling corners. In the back wall, a small forgotten druid stone altar with carved spiral patterns (no letters), dim.
Floor of packed dark earth and flat stones, plain and readable. Mood: deep red-brown and moss green, mysterious.
```

## 스테이지 3 — 버려진 광산 (방 2장)

### 3-A 광부 쉼터
```
Side room 5 - "Miners' Rest": a small rest room carved into the rock of the mine. Back wall of rough rock reinforced with wooden
beams, bunk beds built into the wall, hanging helmets and pickaxes on pegs, a chalk board with only scribbled lines (no letters).
Unlit oil lamps. Floor of flat packed dirt with a few wooden planks. Mood: dusty ochre and dark brown.
```

### 3-B 무너진 수정 동굴
```
Side room 6 - "Crystal Pocket": a natural cave pocket that miners broke into. Back wall of dark rock with clusters of pale crystals
(drawn DIM, flat colors, no glow), a broken mine-cart rail ending at the wall, a collapsed support beam leaning in a top corner.
Floor of smooth flat rock, plain and readable. Mood: dark blue-grey rock with pale violet crystal accents.
```

## 스테이지 4 — 침수된 납골당 (방 2장)

### 4-A 유골 예배실
```
Side room 7 - "Ossuary Chapel": a small chapel whose back wall is built from neatly stacked skulls and bones (built into the wall only),
with a stone niche holding an old knight's helmet. Dim teal soul-moss in the wall cracks (dull dark teal, no halo).
Unlit candle stubs on a stone ledge. Floor of pale grey-blue stone tiles, dry. Mood: bone white, grey-blue and dim teal.
```

### 4-B 기사단 문서고
```
Side room 8 - "Order Archive": the record room of the ancient knight order. Back wall of tall stone shelves with rotting books and scroll
racks, a faded order banner (teal with a silver sword crest shape, no letters), a stone reading desk built against the wall.
A thin, calm, flat layer of water covers only the back edge of the floor; the rest of the floor is dry pale stone, plain and readable.
Mood: grey-blue stone, faded teal and silver.
```
