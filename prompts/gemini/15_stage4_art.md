# 15. 스테이지 4 그림 — 배경 7장 + 적·보스 시트 5장 (14-C, 칸 채운 판)

- 14-B 설계서(후보 B "청록빛 영혼석과 침수된 납골당")를 게임 규격에 맞춰 채운 프롬프트입니다. 그대로 복사해 붙이면 됩니다.
- **대화 2개**로 나눠 주세요: ① 배경 7장(같은 대화) ② 캐릭터 5장(같은 대화).
- 배경은 **움직이는 것이 빠진 판**입니다. 폭포·물방울·안개·이끼 빛·유령불·촛불·보라 사슬 전류는 따로 만들어 위에 얹습니다.
- 바닥 위 물건(석관·잔해·금 간 바닥·열쇠 상자)도 따로 만듭니다.
- ② 캐릭터는 **아트 검토 추천안**으로 썼습니다: 보스 = 선대 기사단장(약 2배, 2페이즈는 같은 그림에 유령빛), 융합 구울 = 부푼 구울 하나 + 팔 2개.
  Gemini 원안(1.3배 · 갑옷 파괴 본체 · 구울 3마리)으로 가려면 Claude에게 말해 주세요. 배경 ①은 어느 쪽이든 같습니다.

---

## ① 배경 (새 대화) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`

### 첫 메시지 (규칙 + 배경 1)
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.
The setting is a medieval fantasy world: a forgotten, half-flooded crypt of an ancient knight order, deep underground, lit by
dim teal soul-moss. Dark and eerie, but the walkable floor must stay bright and readable.

Rules for ALL backgrounds in this conversation:
- True pixel art with HARD EDGES: every pixel is a crisp square block (the same block size as the stage 1 references),
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- The aspect ratio is given per image. The walkable ground is seen from a slight high angle, fairly plain and EVENLY LIT
  (pale grey-blue stone or white marble) so characters and their shadows stay clearly readable, even though the walls are dark.
- Where the floor has shallow water, draw it as a thin, calm, flat reflective layer over the stone (no ripples, no splashes, no deep water).
- Exits stand on the ground line at the back edge.
- This is a STATIC PLATE: animated things are added later in the game, so draw them in their "off" state:
  NO lit flames (torches, braziers and candles unlit: only dark holders and cold candle stubs, no glow spots),
  NO ghosts, wisps or floating lights, NO fog or mist, NO falling water or drops, NO waterfalls (only the empty wet rock channel),
  glowing moss and magic runes drawn DIM (dull dark teal, no halo).
- NO objects on the walkable ground (no coffins, rubble, bone piles, barrels, crates) - those are added separately.
- NO characters, NO creatures, NO skeletons standing or lying on the floor (bones built into the walls are fine),
  NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1 - "Fallen Cave" (ULTRA-WIDE 21:9, for example 2520x1080): the bottom of a huge pit where the mine ceiling caved in from above.
Wrecked pieces of a wooden mine elevator and broken iron girders lie crumpled against the back wall (not on the walkway). A faint cold
shaft of pale light comes from a hole high above (drawn as a few lighter flat colour bands on the rock, no glow). Old bones and skulls
are embedded in the rock walls, with patches of dim teal moss. A wide path of pale grey rock goes DOWN DIAGONALLY from the upper LEFT
to the lower RIGHT, about one third of the image tall, at about 20 degrees. At the bottom RIGHT end, an old carved stone archway (the exit,
on the ground line). Main colors: dull black, ash grey, pale teal.
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Background 2 - "Crypt Corridor" (ULTRA-WIDE 21:9, for example 2520x1080): same rules. A long ancient stone corridor; the back wall
is lined with rows of burial niches holding old skulls, with dim teal moss in the cracks between the stones. A few broken stone pillars
stand half sunk at the back. Floor: pale flat stone slabs under a thin layer of calm ankle-deep water. Two exits on the back ground line:
at the far RIGHT end a huge open stone double door (dark inside); and on the RIGHT part of the back wall, a section of cracked, crumbling
stone wall (it will be broken open later - draw it closed but clearly cracked). Main colors: deep cyan, blue-grey, dark navy.
```
```
Background 2b - "Crypt Corridor, wall broken": exactly the same image as Background 2, same size and composition, but the cracked stone
section on the back wall is now smashed open into a rough dark passage (the exit), with broken stone edges. Everything else identical.
```
```
Background 3 - "Soul Fall" (SQUARE 1:1, for example 1920x1920): same rules. The camera is a little higher so the white marble floor fills
the LOWER 70% of the image - a wide, deep hall to fight in. Upper 30%: in the CENTER of the back wall a tall dark wet rock channel where a
huge waterfall will be added later (draw only the empty wet channel and a shallow basin at its foot, NO falling water). On both sides of the
channel, giant stone statues of armoured knights with their swords pointing down, black stains running from their eyes like tears.
ONE exit: on the upper RIGHT of the floor's far edge, an open carved stone door. Main colors: dull teal, water black, white.
```
```
Background 4 - "Sunken Tomb" (ULTRA-WIDE 21:9, for example 2520x1080): same rules. A cramped, low-ceilinged tomb hall; rows of stone
sarcophagi along the back wall, some lids cracked. A huge iron chandelier has fallen and lies crashed against the back wall (its chain
broken, NOTHING hanging from the ceiling - chains are added later). Floor: teal-tinted stone with old water stains under a thin calm layer
of water, still bright enough to read. At the far RIGHT end, a narrow dark passage (the exit). Main colors: dark teal, black-green, pale jade.
```
```
Background 5 - "Purified Altar" (16:9, for example 1920x1080): same rules. A small dry sacred chamber untouched by the curse. A pure white
stone angel statue with folded wings stands in the back, with a plain altar before it and rows of cold unlit candles (no flames).
Warm golden trim on the walls. In the CENTER of the back wall, the bottom of a golden spiral staircase going up (the exit).
Floor: dry white carpet over pale stone. Main colors: warm gold, pure white, soft teal.
```
```
Background 6 - "Abyssal Shrine" (4:3, for example 2048x1536): same rules, boss arena. The front of a giant royal tomb. The whole back wall
is one enormous sealed round stone door carved with knight crests, wrapped tightly in thick black iron chains (dark, no purple light - the
glow is added later). Above the door, a large smooth flat stone surface with nothing on it (a ghostly figure will appear there later - keep it
empty). The floor is a wide round stone platform under a thin calm layer of water, filling the LOWER 55% of the image. No open exit.
Main colors: deep purple, deep cyan, pitch black.
```
```
Background 6b - "Abyssal Shrine, door open": exactly the same image as Background 6, same size and composition, but the chains are gone
(a few broken links on the ground line at the door's foot) and the great stone door stands open, showing an endless stone spiral staircase
going up into darkness behind it (the exit). Everything else identical.
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
- Same character, same colors in all three poses. Poses must not overlap. Feet visible (for a floating ghost: the lowest tip of its body visible).
- Only this one view - no turnaround, no back or side views.
- Bold, simple, readable silhouette: no shields, no capes, no long flowing cloth, few thin dangling parts.
- In the wind-up poses the weapon stays in FRONT of the body, never hidden behind the head or back.
- Ghosts: draw them OPAQUE with solid pixel colors (transparency is added in the game), a simple short tapering tail, no glow halo.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1 - VENGEFUL WRAITH: a floating ghost about the hero's height, pale blue, a hooded skull-like face with two teal eye lights,
thin bony arms, the lower body tapering into a short simple tail that floats a little above the ground. It holds a long curved scythe.
Poses: idle hovering with the scythe held diagonally in front / scythe pulled back to the side then sweeping forward in a wide slash /
lunging forward stabbing with the scythe tip (appearing from behind the hero).
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Character 2 - SKELETON SOLDIER: same rules. A skeleton warrior about the hero's height, old white bones, a rusty iron helmet and a torn
chainmail shirt, teal light in the eye sockets, an old straight sword in one hand, no shield. Poses: idle guard stance with the sword
in front / sword raised high in front of the head then chopping down / crouching low then lunging forward with a straight sword thrust.
```
```
Character 3 - SLUDGE GHOUL: same rules. A bloated drowned corpse about 1.2 times the hero's height, heavy round body, dark blue-green
swollen skin, a jaw hanging grotesquely open, short thick arms, no clothes except a few rags. Poses: idle hunched / belly swollen huge,
leaning forward and vomiting a stream of dark teal sludge onto the ground in front / arms spread wide, falling forward in a belly-flop body press.
```
```
Character 4 - AMALGAM GHOUL (mid-boss): same rules. This is a mid-boss: about 1.6 times taller than the hero. One huge swollen drowned ghoul,
dark blue-green, with two extra arms growing out of its back (four arms in total, no other extra limbs), dripping teal sludge, a wide open jaw.
Keep the silhouette one simple round mass. Poses: idle / belly swollen, throwing a big ball of sludge from the mouth in an arc /
crouching, about to curl up into a ball for a rolling charge.
```
```
Character 5 - PHANTOM COMMANDER (stage boss): same rules. This is a boss: about 2 times taller than the hero. The ghost of an ancient knight
commander inside a heavily rusted silver plate armour with teal water stains running down it, a closed great helm with teal ghost-light
glowing from the eye slit, a huge moss-covered two-handed greatsword. No cape, no shield. Poses: idle with the greatsword held in front /
dragging the sword low then swinging it upward in front (charge attack) / driving the greatsword point-down into the floor in front of him.
```

---

## Claude가 받은 뒤 하는 일
- 배경: 격자 재기 → 게임 배율로 맞춰 색 정리 → 맵 배치(바닥·사선·출구·카메라) → 게임 캡처. 2/2b·6/6b는 겹쳐서 바뀐 부분만 따로 뺌.
- 움직이는 오브젝트: 사슬·관·촛불·석문 = PixelLab / 폭포·물방울·안개·이끼 맥동·유령불·사슬 전류 = 이펙트 세션 → 배경 위에 얹어 영상 확인
- 적·보스: 시트 대기 자세 → PixelLab 같은 화풍 생성 → 뼈대 애니메이션 → 이펙트 요청
