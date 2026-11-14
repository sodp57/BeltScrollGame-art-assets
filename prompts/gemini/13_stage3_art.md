# 13. 스테이지 3 그림 — 배경 6장 + 적·보스 시트 5장 (12-C, 칸 채운 판)

- 12-B 설계서(후보 B "유황 가스와 녹슨 기계의 산업 광산")를 게임 규격에 맞춰 채운 프롬프트입니다. 그대로 복사해 붙이면 됩니다.
- **대화 2개**로 나눠 주세요: ① 배경 6장(같은 대화) ② 캐릭터 5장(같은 대화).
- 배경은 **움직이는 것이 빠진 판**입니다. 톱니·쇠사슬·광차·가스·증기·불·빛나는 마석은 아트가 따로 만들어 위에 얹습니다.
- 바닥 위 물건(나무통·화약통·바리케이드·금 간 바닥·열쇠 상자)도 따로 만듭니다.
- ② 캐릭터는 **아트 검토 추천안**(마석 동력 판타지: 기계병 → 녹슨 철골렘, 골리앗 → 거한족 족장 + 드릴 건틀릿)으로 썼습니다.
  Gemini 원안(로봇·양손 드릴)으로 가려면 Claude에게 말해 주세요. 배경 ①은 어느 쪽이든 같습니다.

---

## ① 배경 (새 대화) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`

### 첫 메시지 (규칙 + 배경 1)
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.
The setting is a medieval fantasy world: an old mine where enemies dig magic stones, with rusty iron machinery, pipes and sulfur.

Rules for ALL backgrounds in this conversation:
- True pixel art with HARD EDGES: every pixel is a crisp square block (the same block size as the stage 1 references),
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- The aspect ratio is given per image. The walkable ground is seen from a slight high angle, fairly plain and evenly lit
  so characters stay readable.
- Exits stand on the ground line at the back edge.
- This is a STATIC PLATE: animated things are added later in the game, so draw them in their "off" state:
  NO lit flames (lamps and torches unlit: only dark holders, no glow spots), NO mine carts (empty rails only),
  NO gas clouds, steam, smoke, falling water or dust, and magic crystals drawn DIM (dark purple, no halo).
- NO objects on the walkable ground (no barrels, crates, carts, rock piles, barricades, planks) - those are added separately.
- NO characters, NO creatures, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1 - "Rusted Elevator" (ULTRA-WIDE 21:9, for example 2520x1080): the upper shaft of the mine. Old rusted iron girder
scaffolding and a broken elevator frame with a big pulley wheel at the top (NO chains hanging - they are added later, leave open
air below the pulley). Rough rock walls cut by hand, with a few dull purple magic crystals stuck in the rock. A wide path of iron
plates and rock goes DOWN DIAGONALLY from the upper LEFT to the lower RIGHT, about one third of the image tall, at about 20 degrees.
At the bottom RIGHT end of the path, a dark mine tunnel opening (the exit, on the ground line). Main colors: dull grey, rust orange, dark brown.
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Background 2 - "Sulfur Pump" (SQUARE 1:1, for example 1920x1920): same rules. The camera is a little higher so the iron mesh grating
floor fills the LOWER 70% of the image - a wide, deep pump hall to fight in. Upper 30%: thick rusty pipes along the back wall, old valves
and round pressure gauges, a rusted iron grate ceiling, and in the CENTER of the back wall a large empty round socket in the wall where
a giant cogwheel will be placed later (draw only the round recess and its axle, NO cogwheel). No gas coming out of the pipes.
TWO exits on the far edge of the floor: on the upper LEFT an open iron mine door, on the upper RIGHT a dark open tunnel mouth.
Main colors: mustard yellow, rust orange, black iron.
```
```
Background 3 - "Magma Rails" (ULTRA-WIDE 21:9, for example 2520x1080): same rules. A long mine gallery along the edge of a deep pit;
far below at the back, a faint dull red glow of magma (dim, no bright light, no sparks). Shaky wooden support beams along the back wall,
a few dark unlit hanging lamps, dull purple crystals in the rock. Wooden plank floor with ONE straight mine cart rail track running
horizontally across the whole floor, in the middle of the walkable ground (no cart). At the far RIGHT end, a round tunnel opening (the exit).
Main colors: magma red, sooty black, orange.
```
```
Background 4 - "Gas Cavern" (16:9, for example 1920x1080): same rules. A natural dead-end cave where sulfur gas once gathered (draw NO gas,
only yellow-green sulfur stains on the rocks). Broken pickaxes, a toppled ore cart and abandoned mining tools piled in the back corners.
The back wall is solid bedrock; on the RIGHT side of the back wall a section of cracked rock (it will be blasted open later).
Floor: rough rock with a few thin cracks. Main colors: mustard yellow, dark moss green, black-grey.
```
```
Background 4b - "Gas Cavern, wall blasted": exactly the same image as Background 4, same size and composition, but the cracked rock section
on the right of the back wall is now blown open into a rough dark tunnel opening (the exit), with broken rock edges. Everything else identical.
```
```
Background 5 - "Overseer's Vault" (16:9, for example 1920x1080): same rules. A small secret iron room under the cave, lit only in dim red
(one dark emergency lamp housing on the wall, no glow halo). A desk with scattered papers, a huge round vault door standing open, gold bars
and stolen relics leaning against the walls. In the CENTER of the back wall, an iron ladder going up into a dark hatch (the exit).
Floor: smooth iron plates. Main colors: blood red, gold, deep shadow.
```
```
Background 6 - "Drill Chamber" (4:3, for example 2048x1536): same rules, boss arena. A huge round excavation pit; the walls show enormous
spiral drill marks, thick steel girders cross overhead. At the back, a mountain of stacked explosive crates and a big plunger detonator box
next to them. In the upper CENTER of the back wall, a large smooth flat rock face with nothing on it (a ghostly figure will appear there
later - keep it empty). The dug-up dirt floor fills the LOWER 55% of the image, with a few thin dark cracks (steam will come out later -
no steam). No exit. Main colors: dull grey, sulfur yellow, machine black.
```

---

## ② 적 · 보스 시트 (새 대화) — 첨부: `refs/enemy_lineup_ref.png`

### 첫 메시지 (규칙 + 캐릭터 1)
```
Design new enemies for a 2D pixel art beat 'em up set in a medieval fantasy world. The attached sheet shows the real in-game sprites
(the silver knight is the hero). Match that exact pixel art style, outline, shading, proportions and pixel size.

For each character make ONE sheet:
- Left, large: idle battle stance, full body, three-quarter view facing RIGHT and slightly toward the viewer (same angle as the reference sprites).
- Right, smaller: two attack poses (the moment of the hit).
- Same character, same colors in all three poses. Poses must not overlap. Feet visible.
- Only this one view - no turnaround, no back or side views.
- Bold, simple, readable silhouette: no shields, no capes, few thin dangling parts.
- In the wind-up poses the weapon stays in FRONT of the body, never hidden behind the head or back.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1 - BOMB GOBLIN: a small wiry goblin about 0.7 times the hero's height, soot-blackened grey skin, big pointed ears,
brass wind goggles on the forehead, ragged leather apron, a big wicker basket full of round black bombs with fuses on its back, thin arms and legs.
It must look clearly different from a green poison goblin. Poses: idle crouch / holding a lit bomb up in front above the head, about to throw /
running forward hunched with the basket on fire (self-destruct charge).
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Character 2 - MASK ENFORCER: same rules. A stocky mine guard about 1.1 times the hero's height in a thick orange rubber protective suit,
a big round gas mask with two filters, a small oxygen tank on the back, a huge steel wrench held in both hands.
Poses: idle with the wrench held across the body / wide horizontal wrench swing (wrench pulled to the side at hip level, then swung) /
gripping the tank valve on his chest, releasing a short burst of gas around himself.
```
```
Character 3 - RUST GOLEM: same rules. An empty suit of heavy rusted iron armour about 1.2 times the hero's height, brought to life by a
glowing purple magic stone in its chest; one red glowing eye slit in the helmet; the right forearm is a thick iron piston ram, the left is
a big iron fist. Not a robot - a magic-powered armour golem. Poses: idle / piston arm pulled back at the side then punched straight forward
(long reach) / stepping forward with a fast left-right punch.
```
```
Character 4 - TROLL MINER (mid-boss): same rules. This is a mid-boss: about 1.6 times taller than the hero. A hulking grey-green troll
with a long nose, a too-small gas mask strapped over its face, two big yellow sulfur gas tanks strapped to its back, a rusty pickaxe as
big as a man. Poses: idle / two-handed pickaxe slam hitting the ground in front / hunched forward charging with gas jetting from the tanks.
```
```
Character 5 - GOLIATH BRUTE (stage boss): same rules. This is a boss: about 1.8 times taller than the hero. The chieftain of the bald brute
tribe (like the bald brute in the reference, but much bigger and heavier): huge bald muscular giant, thick lead apron, a welding mask pushed
up on the forehead, fur on the shoulders. His RIGHT arm ends in a giant iron drill gauntlet with a glowing purple magic stone engine;
the LEFT hand is a bare fist. Poses: idle / drill thrust forward at full spin (charge) / driving the drill down into the ground.
```

---

## Claude가 받은 뒤 하는 일
- 배경: 격자 재기 → 게임 배율로 맞춰 색 정리 → 맵 배치(바닥·사선·출구·카메라) → 게임 캡처. 4/4b는 겹쳐서 벽 뚫림만 따로 뺌.
- 움직이는 오브젝트: 톱니·쇠사슬·광차·마석 빛·비상등·등불 = PixelLab / 가스·증기·용암 불똥·흙먼지·폭약고 폭발 = 이펙트 세션 → 배경 위에 얹어 영상 확인
- 적·보스: 시트 대기 자세 → PixelLab 같은 화풍 생성 → 뼈대 애니메이션 → 이펙트 요청
