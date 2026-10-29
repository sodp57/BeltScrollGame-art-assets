# 9. 스테이지 2 맵 넓히기 — 긴 통로 · 넓은 광장 · 사선 비탈 · 깊은 아레나

- 8번 **배경 대화(①)에 이어서** 붙여 넣으세요. 같은 대화라야 화풍이 그대로 이어집니다.
- 결과 5장을 대화창(Claude)에 첨부해 주세요. 이음새·크기·색은 Claude가 맞춥니다.
- 맵 모양 그림: `review_1022/stage2_map_shapes_proposal.png`
- 지하 창고(5번 배경)는 그대로 씁니다.

| 순서 | 맵 | 모양 | 비율 |
|---|---|---|---|
| 9-1 | 안개 낀 입구 앞부분 | 가로로 긴 통로(지금 입구 그림 왼쪽에 붙음) | 21:9 |
| 9-2 | 핏빛 늪 | 위아래로 넓은 광장 | 1:1 |
| 9-3 | 함정 야영지 | 오른쪽 위 동굴까지 올라가는 사선 비탈 | 21:9 |
| 9-4 | 불타는 거목 | 조금 넓은 방(중간 보스 돌진 공간) | 21:9 |
| 9-5 | 마수의 둥지 | 바닥이 깊은 아레나 | 4:3 |

## 9-1. 입구 앞부분 (같은 대화)
```
New image, same style and rules as before, but ULTRA-WIDE 21:9 (for example 2520x1080), drawn as if on a 504x216 pixel grid
(every pixel block the same size as in the previous images).
This is the long approach to "Background 1 - Misty Entrance": the same cursed red forest at night under the blood-red moon, gaunt
dark-red trees in layers, grey fog between them, torn red banners, wet dark soil. NO thorn tunnel and NO exit here - this part comes
BEFORE Background 1. Its RIGHT edge must flow into the LEFT edge of Background 1: same horizon height, same fog band height,
same ground line, and a big dark tree trunk standing right at the right edge.
Keep the fog darker and less bright than in Background 1 (soft grey, not white), so characters stay readable in front of it.
Bottom ~38% = plain walkable ground. NO characters, NO text, NO watermark.
```

## 9-2. 핏빛 늪 — 넓은 광장 (같은 대화)
```
Redraw "Background 2 - Blood Swamp" as a SQUARE 1:1 image (for example 1920x1920), drawn as if on a 384x384 pixel grid
(same pixel block size as before). Same place, same style, but the camera is a little higher so the muddy swamp ground fills
the LOWER 70% of the image - a wide, deep clearing to fight in, with a few small blood-red puddles and mud patches spread around.
The upper 30% keeps the scenery: rotting trees with moss, torches on poles, and the TWO exits standing on the far edge of the
ground: on the LEFT the broken wooden palisade gate (closed), on the RIGHT the split hollow tree with the red glow inside.
No other objects on the ground. NO characters, NO text, NO watermark.
```

## 9-3. 함정 야영지 — 사선 비탈 (같은 대화)
```
Redraw "Background 3 - Trap Camp" as an ULTRA-WIDE 21:9 image (for example 2520x1080), drawn as if on a 768x329 pixel grid
(small pixel blocks, the same detail level as before). The mercenary camp is now built on a hillside: a wide packed-dirt path
climbs DIAGONALLY from the lower LEFT corner up to the huge skull-decorated cave mouth at the UPPER RIGHT (the exit, on the
ground line at the top of the path). Leather tents, weapon racks, banners and the cooking fire stand on both sides of the path,
on terraces above and below it. The path itself is plain, about one third of the image tall, and rises at about 20 degrees.
Outside the path: rock and earth slopes, no objects on the path. NO characters, NO text, NO watermark.
```

## 9-4. 불타는 거목 — 조금 넓게 (같은 대화)
```
Redraw "Background 4 - Burning Tree" as an ULTRA-WIDE 21:9 image (for example 2520x1080), drawn as if on a 504x216 pixel grid
(same pixel block size as before). Same hollow burning tree interior, just wider: more charred wall with crimson flames on both
sides so a large boss can charge across. Keep the meeting table in the back and the web-covered rock crevice exit on the right.
Bottom ~38% = plain wooden floor. NO characters, NO text, NO watermark.
```

## 9-5. 마수의 둥지 — 깊은 아레나 (같은 대화)
```
Redraw "Background 6 - Spider Nest" as a 4:3 image (for example 2048x1536), drawn as if on a 384x288 pixel grid
(same pixel block size as before). Same boss cave, but the rocky floor is deeper: the walkable ground fills the LOWER 55% of the image.
Keep the tall cliff ledge on the upper LEFT with EMPTY space on top. Make the webs and cocoons a little dimmer than before
(soft grey-green, not bright white) so the fighters stay readable. NO characters, NO text, NO watermark.
```

## Claude가 받은 뒤 하는 일
- 도트 격자 크기를 재서 기존 배경과 같은 배율로 맞추고(다르면 알려 드림), 색 보정·반짝이 마크 제거
- 입구: 9-1 + 기존 입구 그림을 이어 붙이고, 이음새는 앞쪽 나무 기둥 그림으로 가림(가로 약 2.3화면)
- 맵마다 걷는 바닥 범위(사선 포함)·출구·카메라 위아래 범위를 넣고 게임 캡처로 확인
