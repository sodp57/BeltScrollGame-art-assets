# 8. 스테이지 2 컨셉 그림 — 배경 6장 + 적·보스 시트 5장 (7-C, 칸 채운 판)

- 7-B 설계서(후보 B "전술적 게릴라전")를 게임 규격에 맞춰 채운 프롬프트입니다. 그대로 복사해 붙이면 됩니다.
- **대화 2개**로 나눠 주세요: ① 배경 6장(같은 대화) ② 캐릭터 5장(같은 대화). 같은 대화라야 화풍이 맞습니다.
- 결과 그림은 대화창(Claude)에 첨부해 주세요. 한 번에 몇 장씩 보내셔도 됩니다.
- 바닥에 놓이는 물건(바리케이드·판자·화약통·가시 함정·거미줄 덩어리)은 아트가 따로 만들어 올립니다. 그래서 배경의 바닥은 비워 두게 했습니다.

---

## ① 배경 (새 대화) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`

### 첫 메시지 (규칙 + 배경 1)
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.

Rules for ALL backgrounds in this conversation:
- 16:9 landscape (1536x864 if possible).
- True pixel art with HARD EDGES, drawn as if on a 384x216 pixel grid and enlarged 4x: every pixel is a crisp 4x4 block,
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- Top ~62%: back wall / scenery. Bottom ~38%: walkable ground seen from a slight high angle, fairly plain and evenly lit so characters stay readable.
- Exits stand on the ground line at the back edge.
- NO objects on the walkable ground (no barrels, crates, spikes, barricades, planks) - those are added separately.
- NO characters, NO creatures, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1 - "Misty Entrance": the edge of a cursed forest at night under a blood-red moon. Dense, gaunt, leafless dark-red trees with
twisted trunks fill the background in layers, thick grey-white fog drifting between them, torn red cloth banners of a mercenary band hanging
from the branches. On the far RIGHT, a huge wall of black thorn bushes with a dark tunnel opening at ground level (the exit).
Ground: wet dark soil with a few patches of grass and roots. Main colors: fog grey, dark crimson trees, brown ground.
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Background 2 - "Blood Swamp": same rules. A gloomy swamp clearing at night. Pools of blood-red water and rotting trees with hanging moss in
the background, crude wooden barricades and torches on poles set up by bandits along the back. TWO exits on the back edge, both standing on
the ground line: on the LEFT a broken wooden palisade gate (closed), on the RIGHT the split trunk of a gigantic hollow tree with a red glow
burning inside the crack. Ground: dark muddy swamp with a few shallow red puddles. Main colors: dark blood red, torch orange, deep moss green.
```
```
Background 3 - "Trap Camp": same rules. A mercenary war camp in a forest clearing at night. Large patched leather tents, weapon racks with
spears and axes, supply crates and a cooking fire in the background, red mercenary banners. In the CENTER of the back edge, a huge cave mouth
in a rock face decorated with animal skulls and bones (the exit). Ground: packed dry dirt. Main colors: dark brown tents, yellow firelight, grey rock.
```
```
Background 4 - "Burning Tree": same rules. The inside of a gigantic hollow ancient tree. Curved walls of charred wood with glowing cracks and
eerie crimson flames licking up the walls, roots hanging overhead, traces of a secret mercenary meeting in the background (a rough table,
maps, candles). On the RIGHT of the back wall, a narrow rock crevice covered in thick spider webs (the exit).
Ground: dark wooden floor with a few scattered embers. Main colors: orange flame, black soot, red blood stains.
```
```
Background 5 - "Hidden Cellar": same rules. A small secret storeroom under the tree. Old stone and timber walls, wall torches, shelves with
dusty barrels and sacks, piles of gold coins and old treasure chests along the back wall. On the RIGHT of the back wall, a dark cave tunnel
opening (the exit). Ground: old flagstones with dirt. Warm torchlight against dark blue shadows.
```
```
Background 6 - "Spider Nest" (boss arena): same rules. A huge cave, the lair of a giant spider queen. The whole background is covered by
enormous white spider webs, silk cocoons with victims hanging from the ceiling, bones scattered at the base of the walls. On the upper LEFT,
a tall rock cliff ledge high above the ground with EMPTY space on top (a character will be added there later - keep it empty).
No exit. Ground: wide rocky cave floor dusted with old web strands. Main colors: pale white webs, deep purple-black cave, sickly green glow.
```

---

## ② 적 · 보스 시트 (새 대화) — 첨부: `refs/enemy_lineup_ref.png`

### 첫 메시지 (규칙 + 캐릭터 1)
```
Design new enemies for a 2D pixel art beat 'em up. The attached sheet shows the real in-game sprites (the silver knight is the hero).
Match that exact pixel art style, outline, shading, proportions and pixel size.

For each character make ONE sheet:
- Left, large: idle battle stance, full body, three-quarter view facing RIGHT and slightly toward the viewer (same angle as the reference sprites).
- Right, smaller: two attack poses (the moment of the hit).
- Same character, same colors in all three poses. Poses must not overlap. Feet visible.
- Only this one view - no turnaround, no back or side views.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1 - FOREST WOLF: a large grey forest wolf with glowing red eyes, ragged dark-grey fur with a darker stripe along the back, scars,
low prowling stance on four legs. Body length about the hero's height. Poses: idle prowl / lunging bite in mid-air / howling with the head raised.
```

### 다음 메시지들 (같은 대화에서 하나씩)
```
Character 2 - POISON GOBLIN: same rules. A small hunched green goblin about 0.7 times the hero's height, big pointed ears, ragged brown hood
and loincloth, a lumpy sack full of glowing green poison bottles on its back, a rusty dagger.
Poses: idle crouch / throwing a green bottle overhand / short dagger stab.
```
```
Character 3 - HEAVY MERC: same rules. A heavily armoured mercenary about 1.2 times the hero's height, dark steel plate armour with a red hood
and a red cloth tabard (the same red mercenary band as the red bandits in the reference), a huge rectangular iron tower shield held in front,
a heavy broad falchion in the other hand. Poses: idle guard behind the shield / shield bash forward / overhead falchion chop.
```
```
Character 4 - BLOOD ORC (mid-boss): same rules. A huge red-skinned orc warlord about 1.6 times the hero's height, big tusks, spiked iron
armour plates on the shoulders and belt, scars, a giant butcher's cleaver.
Poses: idle / two-handed overhead cleaver slam hitting the ground / war cry, roaring and beating his chest.
```
```
Character 5 - ARACHNID QUEEN (stage boss): same rules. A half-woman half-spider boss about 2 times the hero's height. Upper body: a pale
female knight in black-and-silver armour with a spiked crown helm and long white hair. Lower body: a giant black widow spider with a glossy
black abdomen and a red hourglass mark, eight legs, the two front legs long and blade-like. Keep the spider body large and simple and the
legs readable. Poses: idle / front blade-leg raised for a slash / rearing back to spit a web.
```

---

## Claude가 받은 뒤 하는 일
- 배경: 384x216 도트로 맞춰 색 정리(fit_opening 방식) → 맵 6개 배치(바닥 범위·출구·갈림길) → 게임 캡처
- 적: 시트의 대기 자세를 기준으로 PixelLab에서 같은 화풍 캐릭터 생성 → 뼈대 애니메이션(늑대는 네발 템플릿) → 이펙트 세션에 공격 이펙트 요청
- 보스: 오크는 데몬 나이트와 같은 방식, 퀸은 상반신 뼈대 + 하반신 조립식
- 소품(바리케이드·판자·화약통·벽 불기둥·거미줄·고치)은 아트가 PixelLab으로 만든다
