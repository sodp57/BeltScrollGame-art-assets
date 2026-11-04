# 11. 스테이지 2 캐릭터 시트 고치기 — 중무장 용병(방패 빼기) · 아라크니드 퀸(간소화)

- **8번 캐릭터 대화에 이어서** 보내 주세요(같은 대화라야 화풍이 맞습니다). 새 대화라면 고칠 시트 그림을 같이 첨부하세요.
- 메시지 2개를 하나씩 보냅니다. 결과 그림은 Claude 대화창에 첨부해 주세요.
- 숲 늑대 · 맹독 고블린 · 블러드 오크는 그대로 씁니다(고칠 것 없음).

**왜 고치나:** 애니메이션은 뼈대(관절)로 움직입니다. 방패처럼 몸을 크게 가리는 판은 팔이 움직일 때 몸과 겹쳐 깨지기 쉽고,
거미 다리 8개가 가늘고 마디가 많으면 다리마다 따로 움직이기 어렵습니다.

---

## 11-1 중무장 용병 — 방패 없이 (8번 대화에서)
```
Redraw Character 3 - HEAVY MERC with ONE change: remove the tower shield completely from all three poses.
Keep everything else identical: same pixel art style and pixel size, same red hood and red tabard, same dark steel plate armour,
same heavy falchion, same proportions (about 1.2 times the hero's height), same three-quarter view facing RIGHT.
His left arm is now free: a heavy steel gauntlet, nothing in that hand, the whole arm visible (no object hiding the body).
Poses: idle guard (falchion held in front of the body at an angle, left fist raised beside it) /
armoured shoulder tackle forward (leaning in, left shoulder pauldron first) / overhead falchion chop.
Same sheet layout as before: large idle pose on the left, the two attack poses smaller on the right. Plain flat dark background (#14161E),
no text, no watermark. Poses must not overlap, feet visible.
```

## 11-2 아라크니드 퀸 — 단순하게 (같은 대화에서 이어서)
```
Redraw Character 5 - ARACHNID QUEEN as a SIMPLER version that is easy to animate. Same character, same colours, same pixel art style
and pixel size, same three-quarter view facing RIGHT, about 2 times the hero's height.
Simplify like this:
- Upper body: the same pale female knight, but hair tied back short and close to the head (no long loose strands),
  a simple crown helm with 3 spikes, a few large flat armour plates instead of many small pieces.
- Spider body: one big smooth glossy black abdomen with a single highlight and one red hourglass mark, a small plain front body
  under the knight's waist (no face, no fangs, no mouth parts, no extra eyes).
- Legs: 8 legs, but each leg is THICK and made of only TWO straight segments (upper leg going up to a clear knee, lower leg going down
  to a pointed tip). Legs evenly spaced, NOT crossing or overlapping each other or the body, all tips standing on one ground line.
  The two front legs are longer with a curved scythe blade at the end.
- Fewer highlights and fewer colours overall; clear dark outline around every part.
Poses: idle / one front blade-leg raised for a slash / rearing back to spit a web (the web itself is NOT drawn).
Same sheet layout as before (large idle on the left, two smaller poses on the right). Plain flat dark background (#14161E),
no text, no watermark. Poses must not overlap.
```

---

## Claude가 받은 뒤 하는 일
- 중무장 용병: 대기 자세를 기준으로 PixelLab 캐릭터 생성 → 뼈대 애니메이션. 방패가 없어졌으니 **정면 막기는 칼과 팔 갑옷으로 막는 자세**,
  **방패 밀치기는 어깨 들이받기(기절)** 로 바꿉니다(게임 장치는 그대로: 정면 공격은 막힘, 점프 공격으로 깸).
- 아라크니드 퀸: 상반신은 뼈대, 하반신은 몸통 고정 + 다리를 부품으로 잘라 직접 움직이는 조립식.
