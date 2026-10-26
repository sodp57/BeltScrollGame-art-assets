# 6. 타이틀 화면 (게임 전체 대표 그림 + 게임 이름)

- 03번 결과(아서와 성)는 오프닝 장면 3·5로 썼습니다. 타이틀은 5스테이지 전체를 대표하게 따로 만듭니다.
- 순서: **6-A 게임 이름 → 5번(가웨인·랜슬롯 디자인) → 6-B 타이틀 그림 → 6-C 로고**
- 6-A는 스토리 대화(1-1~1-3과 같은 대화)에서, 6-B·6-C는 새 대화에서 하세요.

## 6-A. 게임 이름 (스토리 대화에 이어서)
결과: 대화창(Claude)에 붙여 넣고 마음에 드는 이름을 알려 주세요.
```
이 게임의 제목을 정하고 싶어. 아케이드 벨트스크롤 타이틀 화면에 크게 박힐 이름으로 후보 6개를 줘.
- 후보마다: 로고용 영어 제목(1~3단어, 짧고 강하게) / 한국어 제목 / 부제(선택) / 한 줄 이유
- 서로 다른 느낌으로: 왕국 이름을 쓴 것, 기사들의 맹세를 쓴 것, 데몬 나이트를 쓴 것, 짧은 한 단어, 그 밖에 두 개
- 마지막에 네 추천 하나.
```

## 6-B. 타이틀 그림 (새 대화)
- 첨부 3개: `refs/title_style_refs.png`, 5번에서 받은 **가웨인 시트**, **랜슬롯 시트**
- 결과 2장을 대화창(Claude)에 첨부: 완성본 1장 + 같은 대화에서 "캐릭터를 뺀 배경만" 1장
```
Create ONE title screen illustration for a 2D pixel art beat 'em up, 16:9 landscape (1536x864 if possible).
Attached: (1) the real in-game sprite sheet — the silver knight with the gold-winged helmet is ARTHUR, the black-and-crimson horned knight is the DEMON KNIGHT;
(2) the design sheet of GAWAIN; (3) the design sheet of LANCELOT. Keep all three heroes exactly as designed.

Composition:
- The three knights stand together in the lower half, facing the viewer in heroic battle stances, weapons ready:
  ARTHUR in the center slightly forward, GAWAIN on the left, LANCELOT on the right. Strong rim light, readable silhouettes.
- Behind them, the giant ghostly face and horned helmet of the DEMON KNIGHT fills the upper background, made of crimson flame and shadow, glowing red eyes.
- Around the Demon Knight, small hints of the five lands of the journey blended into the background: a dark castle, a blood-red moon over a misty forest,
  a mine shaft with rails, a tall purple void tower, a burning gate of hell.
- Keep the TOP-CENTER area (about the top 30%, middle 60% of the width) calm and dark enough for a big logo to be placed on it later.

STYLE - VERY IMPORTANT
- True pixel art with HARD EDGES, drawn as if on a 384x216 pixel grid and enlarged 4x: every pixel is a crisp 4x4 block,
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- Limited palette (about 48 colors). Night blues, silver and gold for the heroes, deep red and bronze for Gawain, navy blue for Lancelot, crimson for the Demon Knight.
NO text, NO letters, NO logo, NO watermark, NO border, NO UI.
```
두 번째 메시지(같은 대화):
```
Now the exact same image with the three knights removed. Keep everything else exactly the same (Demon Knight face, the five lands, sky).
Same size, same pixel style, NO text.
```

## 6-C. 로고 (6-B와 같은 대화, 이름이 정해진 뒤)
- `[게임 영어 제목]`을 6-A에서 고른 이름으로 바꿔 붙이세요. 결과를 대화창(Claude)에 첨부.
```
Make a pixel art game logo that reads exactly "[게임 영어 제목]" in large letters, for the title screen of the illustration above.
- Heavy medieval blackletter-inspired pixel font, silver steel letters with gold rim and a thin crimson glow, a sword or the gold winged emblem worked into the logo.
- True pixel art, hard edges, no anti-aliasing, drawn as if on a 192x72 pixel grid enlarged 4x.
- On a plain flat pure black background, nothing else, no other text, no watermark.
- Spell the title exactly, letter by letter.
```
