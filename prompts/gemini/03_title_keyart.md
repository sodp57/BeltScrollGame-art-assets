# 3. 타이틀 화면 그림

- 첨부 2개:
  - `refs/title_style_refs.png`: 게임 안 실제 그림. 화풍·색·캐릭터 생김새 기준
  - `refs/title_layout_guide.png`: 화면 배치 가이드. 색 덩어리는 위치만 뜻함
- 16:9 가로 비율로 요청합니다. 다른 크기로 나와도 아트 세션이 맞춥니다.
- 결과 2장을 대화창(Claude)에 첨부해 주세요.
  1. 완성 그림
  2. 같은 그림에서 캐릭터를 뺀 배경만 있는 그림 (아래 두 번째 프롬프트를 같은 대화에서)
- 로고 글자는 넣지 않습니다. 게임 안에서 따로 올립니다.

## 복사할 프롬프트 (1장째)

```
Create ONE title screen illustration for a 2D pixel art beat 'em up game, 16:9 landscape (1536x864 if possible).

Use the two attached images:
- Image 1 shows the real in-game sprites and one in-game background. Match this exact pixel art style, palette and character designs:
  the silver knight hero with the gold-winged helmet and blue tabard, the red-hooded dark sorcerer, the stone gargoyle, and the black-and-crimson horned Demon Knight with the double axe.
- Image 2 is the layout guide. Follow the placement only (the flat colors are not the final colors):
  top-center gold box = keep this area EMPTY and calm (dark night sky only, a logo will be placed there later),
  white shape lower-left = the hero, seen from behind in a 3/4 back view, standing on a rocky ledge, sword in hand, looking at the castle,
  blue shape right = a dark gothic castle on a hill,
  red shape right = the Demon Knight looming huge behind the castle like a ghostly apparition made of crimson flame and shadow, his eyes glowing,
  pale circle = full moon behind clouds, brown band = rocky ground in the foreground.
- Add two or three small stone gargoyles perched on the castle battlements, and a tiny red-hooded figure (the sorcerer) on a tower balcony.

STYLE - VERY IMPORTANT
- True pixel art with HARD EDGES, drawn as if on a 384x216 pixel grid and enlarged 4x: every pixel is a crisp 4x4 block,
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly brush strokes, no photographic texture, no noise.
- Limited palette (about 40 colors): cold moonlit blues and greys for the night, silver and gold for the hero, crimson and black for the Demon Knight.
- Dramatic rim light from the moon on the hero's armor. Strong silhouette readability.

NO text, NO letters, NO logo, NO watermark, NO border, NO UI.
```

## 복사할 프롬프트 (2장째, 같은 대화에서)

```
Now give me the exact same image with every character removed: no hero, no Demon Knight apparition, no gargoyles, no sorcerer.
Keep the castle, sky, moon, clouds, ledge and ground exactly the same, and fill the empty spots naturally with background.
Same size, same pixel style, NO text.
```
