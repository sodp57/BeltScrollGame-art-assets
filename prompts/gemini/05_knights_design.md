# 5. 가웨인 · 랜슬롯 디자인 시트

- 지금 게임의 세 플레이어 칸은 모두 아서 그림에 색만 바꿔 쓰고 있습니다. 두 기사의 생김새를 정하는 작업입니다.
- 받은 디자인은 아트 세션이 PixelLab으로 아서와 같은 화풍의 게임 캐릭터로 만듭니다(흑주술사·가고일과 같은 방법).
- **새 대화 하나**에서 두 장을 차례로 만드세요. 첨부: `refs/title_style_refs.png` (맨 왼쪽 은빛 기사가 아서)
- 결과 2장을 대화창(Claude)에 첨부해 주세요. 마음에 안 드는 부분은 같은 대화에서 "투구만 바꿔 줘"처럼 고쳐도 됩니다.

## 복사할 프롬프트 (가웨인 — 첫 메시지)

```
Design a playable character for a 2D pixel art beat 'em up. The attached sheet shows the real in-game sprites.
The leftmost silver knight is ARTHUR, the main hero. Design his comrade GAWAIN so the two clearly belong to the same game and the same knightly order.

GAWAIN: a battle-hardened giant warrior knight with monstrous strength, bold and fearless.
- Much broader and heavier than Arthur (about 1.2x as wide, slightly taller), same chunky readable proportions (about 4 heads tall).
- Heavy plate armor in dark steel with bronze trim, a deep red surcoat (his color is red), an open-faced helmet or no helmet with a short beard, scars.
- Weapon: a huge two-handed spiked mace.
- Same knightly order as Arthur: a small gold winged emblem on the chest.
- Must read clearly different from the black-and-crimson horned Demon Knight (no horns, no black armor, no crimson flames) and from the bald brute enemy.

Sheet layout:
- Show GAWAIN twice side by side at the same size: a front view, and a 3/4 view facing down-right (the same angle as the in-game sprites).
- Full body, neutral fighting stance, standing on the same ground line.
- Plain flat dark grey background, no shadows on the ground, no scenery.
- Exactly the same pixel art style as the in-game sprites: true pixel art with HARD EDGES, crisp pixel blocks, flat color clusters,
  no anti-aliasing, no blur, no painterly strokes. Limited palette.
- NO text, NO labels, NO letters, NO watermark.
```

## 복사할 프롬프트 (랜슬롯 — 같은 대화)

```
Now design LANCELOT in exactly the same sheet layout, style and rules.

LANCELOT: a swift assassin-style knight, cynical but warm-hearted.
- Slimmer and lighter than Arthur, agile stance, same height and proportions (about 4 heads tall).
- Light armor: leather and light plate in steel and dark navy, a flowing blue cape (his color is blue), a light half-helm or hood with a face mask.
- Weapons: twin short swords, plus throwing daggers strapped on his chest belt.
- Same knightly order: a small gold winged emblem on the cape clasp.
- Must read clearly different from the black-hooded assassin enemy (lighter colors, blue cape, knightly details).
```
