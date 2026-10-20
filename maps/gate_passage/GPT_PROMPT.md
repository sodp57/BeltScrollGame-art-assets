# 성문 통로 — ChatGPT 큰 배경 프롬프트

**첨부할 이미지 1장:** `gate_layout_guide.png` (같은 폴더) — 구도·크기 안내용. 회색 = 뒷벽, 파란 칸 = 밤하늘이 보이는 큰 아치,
갈색 = 바닥(밝은 띠 = 캐릭터가 걷는 곳), 검은 띠 = 잘려 나가는 부분. 기사·산적은 실제 게임 크기 기준.

**받는 법:** 아래 영어 프롬프트 전체를 복사 → 첨부와 함께 보내기 → 1536x1024 가로 그림 1장.
마음에 드는 걸 받으면 원본 PNG를 그대로 보내 주세요(축소·색 정리·격자 맞춤은 제가 합니다).

벽 횃불·불꽃·깃발·문·쇠창살은 **일부러 빼고** 그리게 했습니다 — 움직이는 부품이라 PixelLab으로 따로 만들어 위에 올립니다.

---

```
Create ONE wide 2D video game stage background, 1536x1024, landscape.

# GAME
A side-scrolling medieval-fantasy beat 'em up (arcade brawler, 1990s style). The camera looks at the
scene from the front and slightly above (3/4 front view): the back wall is seen straight on, and the
floor recedes upward from the bottom edge to the wall base. Characters walk left/right on the floor.
The attached guide image shows the exact layout and the size of the characters - follow it.

# SCENE: INSIDE A CASTLE GATEHOUSE PASSAGE AT NIGHT
- Back wall = massive grey castle masonry seen from inside the gatehouse: large cut stone blocks,
  heavy gothic arches and recessed vaulted bays along the wall, a few narrow arrow slits, iron rings
  and short hanging chains, moss and water stains, a worn stone bench or ledge at the base.
- On the RIGHT side (the blue box in the guide): one tall gothic archway opening to the outside -
  through it a deep night sky with a few stars, a pale moon glow, and the dark silhouette of distant
  castle towers. This arch is the brightest, coolest (blue) area of the image.
- Floor = wet stone flagstones, darker near the wall, with faint reflections. Keep the floor simple:
  it will be partly replaced by tiles. The wall base meets the floor at the height shown in the guide.
- The black strip at the top of the guide will be cropped: put only dark vaulted ceiling there,
  nothing important.

# LEAVE THESE OUT (they are separate animated parts added later)
No torches, no fire, no flames, no glowing light sources on the wall, no banners or flags, no doors,
no portcullis, no barrels or crates, no people, no characters, no creatures, NO TEXT of any kind.
Leave a few plain wall spaces at about chest height (left third, middle) where wall torches will hang.

# STYLE - VERY IMPORTANT
- True pixel art with HARD EDGES, drawn as if on a 384x256 pixel grid and enlarged 4x: every pixel
  is a crisp 4x4 square block, flat color clusters, no anti-aliasing, no blur, no soft gradients,
  no painterly brush strokes, no photographic texture, no noise or film grain.
- Dithering only where needed, in small clean patterns.
- Limited palette (about 32 colors): cool desaturated stone greys and blue-greys, deep navy for the
  night, a little dark moss green, dark brown wet floor. Darker and less saturated than the two
  characters in the guide so they stand out clearly in front of it.
- Lighting: dark moody night interior, dim cool ambient light; the outside arch gives soft blue
  moonlight on the floor near it. No warm light yet (torches are added later).
- Match the pixel size and shading style of the knight and the bandit in the guide (same chunkiness,
  dark outlines on major shapes, 3-4 tone shading per material).

# OUTPUT
One finished image, full frame, no border, no text, no watermark, no characters.
```
