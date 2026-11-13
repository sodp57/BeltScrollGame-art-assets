# 12. 스테이지 3 구상 — 버려진 광산 (방향 → 설계·이야기 → 배경 · 적 시트)

- 순서: **12-A 방향 후보 → 12-B 상세 설계 + 이야기 → 12-C 그림**
  - 12-A·12-B: **스토리 대화**(1-1~1-3, 7-A·7-B를 한 대화)에 이어서. 결과는 대화창(Claude)에 붙여 넣기
    (길면 `C:\GameDev\inbox\gemini\story\12_stage3.txt`)
  - 12-C: 12-B가 정해진 뒤 **새 대화 2개**(배경끼리 / 캐릭터끼리). `[ ]` 칸은 Claude가 12-B를 보고 채워 드립니다.
- 스테이지 2에서 배운 것을 미리 넣었습니다:
  - **움직이는 것은 배경에 그리지 않습니다.** 불·광차·물방울·흔들리는 등불·빛나는 수정의 일렁임은 게임에서 따로 만들어 얹습니다.
    그래서 배경은 "불 꺼진 판"으로 받고, 12-B에서 맵마다 **움직이는 오브젝트 목록**을 따로 받습니다(아트가 그 목록대로 제작).
  - 맵 모양은 넓은 통로(21:9)·넓은 광장(1:1)·사선 비탈·깊은 아레나(4:3)를 처음부터 고르게 합니다(9번처럼 다시 그리지 않게).
  - 캐릭터는 단순한 실루엣으로(방패·가는 장식 많으면 애니메이션이 어려움, 11번 교훈), 공격 준비 때 무기는 몸 앞.

---

## 12-A. 방향 후보 (스토리 대화에 이어서)
```
이제 스테이지 3(버려진 광산)을 설계하자. 먼저 방향 후보 3개만 짧게 줘.
- 후보마다: 한 줄 컨셉 / 분위기 키워드 3개 / 본길 지역 3곳 / 샛길과 중간 보스 / 비밀방 아이디어 / 보스 한 줄 / 이 후보만의 볼거리 하나
- 1-3에서 정리한 뼈대(적의 자금줄인 마석 광산 습격, 대머리 거한 부대, 광차 전투, 폭약고를 터뜨려 광산 붕괴,
  중간 보스 트롤 광부, 보스 골리앗 브루트, 새 적 폭탄 고블린)를 지키되, 세 후보는 서로 느낌이 다르게.
- 스테이지 2(피의 숲: 붉은 달, 안개, 늪, 용병 야영지, 거미 둥지)와 색·분위기가 겹치지 않게. 
- 마지막에 네 추천 하나와 이유.
```
→ 마음에 드는 후보(또는 섞을 부분)를 정해서 12-B로.

## 12-B. 상세 설계 + 이야기 (같은 대화)
`[고른 후보]` 칸을 바꿔 붙이세요(예: "1번 후보, 단 보스방은 3번 것으로").
```
[고른 후보]로 스테이지 3 설계서를 써 줘. 이 게임에서 실제로 만들 수 있는 규칙을 먼저 알려 줄게. 규칙 안에서 설계해 줘.

[게임 규칙]
- 맵 하나 = 배경 그림 한 장. 맵과 맵 사이는 화면이 어두워졌다 밝아지며 넘어간다. 맵 모양은 넷 중 하나를 골라:
  (가) 가로로 긴 통로(21:9, 화면 약 2배 폭) (나) 위아래로 넓은 광장(1:1) (다) 한쪽 위로 올라가는 사선 비탈(21:9)
  (라) 바닥이 깊은 아레나(4:3, 보스방용) (마) 화면 한 장(16:9, 작은 방)
- 화면 위쪽은 배경(벽·풍경), 아래쪽이 캐릭터가 싸우는 바닥(위아래로도 움직이는 깊이 있는 띠).
  출구는 배경에 그려진 문·갱도·길이고, 그 앞에서 위 방향키를 누르면 들어간다.
- 쓸 수 있는 장치: 레버로 여는 관문 / 주기적으로 켜지는 함정(가시·불길·독 등, 독·기절·둔화를 걸 수 있음) / 매복 /
  부서지는 상자·통(아이템, 화약통은 터지며 주변 적에게 피해) / 열쇠 보물상자 / 갈림길(문 두 개 중 고르기) /
  부수면 길이 열리는 바리케이드 / 점프 공격으로 부서지는 바닥(아래 방으로 떨어짐) / 바닥에 남는 독 웅덩이 /
  보스를 쓰러뜨리면 열리는 문 / 보스방 배경에서 한 번 재생되는 연출(누가 나타났다 사라짐 등).
  새 장치는 2개까지 제안해도 된다(예: 화면을 가로지르는 광차). 대신 어떻게 피하는지 한 줄로.
- 적 규칙: 주인공과 비슷한 크기(큰 적은 1.3배까지). 공격은 2개(근접 1 + 특기 1), 공격 전에 알아보기 쉬운 예고 동작. 한 화면에 4~5명까지.
  이전 적을 섞어 써도 된다: 붉은 산적·붉은 궁수·검은 암살자·대머리 거한·돌 가고일·숲 늑대·맹독 고블린·중무장 용병.
  새 적은 3종까지(폭탄 고블린 포함). 맹독 고블린과 겹치지 않게 차별점을 줘.
- 보스 규칙: 화면 높이의 1/3~1/2. 패턴 3~4개(예고 → 공격 → 빈틈) + 체력 절반에서 2페이즈. 졸개 소환 1개, 원거리 가능
  (마법탄은 곧게, 투척물은 포물선). 지금 있는 보스 패턴: 내려찍기 충격파 / 돌진 / 소환 / 조준탄 / 거미줄 속박(연타로 풀기) /
  천장에서 덮치기(그림자 예고) / 전투 함성(주변 기절) / 독액 투척. 같은 것을 써도 되지만 이 보스만의 패턴 하나는 꼭 새로.
- 애니메이션은 뼈대로 만든다. 사람형이 가장 쉽다. 큰 방패·긴 망토·가는 장식이 많으면 어렵다. 실루엣은 굵고 단순하게.
- 움직이는 배경 오브젝트(불, 광차, 도르래, 떨어지는 물·흙먼지, 빛나는 마석 등)는 배경 그림과 따로 만들어 위에 얹는다.

[써 줄 것]
1. 맵 흐름: 본길 맵 3개 + 샛길 맵 1~2개 + 비밀방 + 보스 맵. 화살표 흐름 한 줄, 그리고 맵마다 표로:
   이름(영어·한국어) / 모양(가~마) / 배경에 보이는 것(3~4문장, 그림 프롬프트로 쓸 수 있게 구체적으로. 움직이는 것은 빼고) /
   바닥 재질 / 출구 모양과 위치 / 장치 / 적 구성(웨이브 1~2개) / 분위기 색(3개)
2. 움직이는 오브젝트 목록: 맵마다 3~6개. 표로: 무엇 / 어디(왼쪽 위, 뒷벽 가운데 등) / 어떻게 움직이나(반복 · 가끔 · 한 번) /
   배경 그림에서는 어떤 상태로 그려 둘지(예: 횃불은 불 꺼진 막대만, 광차는 그리지 않고 레일만, 수정은 어둡게).
   분위기를 살리는 것 위주로(먼지, 물방울, 매달린 등불, 굴러가는 광차, 연기, 빛나는 마석의 맥동 등).
3. 갈림길: 어느 맵에서 무엇으로 갈라지는지. 샛길이 더 어렵고 보상이 좋은 이유.
4. 비밀방: 찾는 방법(위 장치 안에서), 보상 1~2개(이름 · 한 줄 설명, 오래 쓰는 장비 위주. 한 번 쓰는 물약은 피해 줘),
   나가면 어디로 이어지는지.
5. 새 적(최대 3종) 표: 이름(영어·한국어) / 역할 / 생김새(색·무기·실루엣, 그림 프롬프트로) / 공격 2개(예고 → 공격) / 요령 / 첫 등장 맵
6. 중간 보스(샛길) TROLL MINER 계열: 생김새 / 패턴 3개 / 대사(등장 2줄, 쓰러질 때 2줄)
7. 스테이지 보스 GOLIATH BRUTE 계열: 생김새(크기 포함) / 보스방 모습 / 패턴 4개 / 2페이즈 / 소환 졸개 / 대사(등장 2줄, 2페이즈 1줄, 쓰러질 때 2줄)
8. 이야기: 스테이지 2 클리어("보급로가 광산에 있음을 알아냈다")에서 이어지게.
   - 광산이 누구 것이고 마석이 어디로 가는지 2~3문장(스테이지 4 공허의 탑, 흑주술사와 연결).
   - 데몬 나이트 또는 흑주술사(환영)가 이 스테이지에서 얼굴을 비치는 방법 한 줄(보스방 배경 연출로 가능).
   - 폭약고를 터뜨려 광산을 무너뜨리는 마무리를 어떻게 보여 줄지(보스 처치 뒤 자막 + 화면 흔들림·폭발 정도로).
9. 자막: 스테이지 시작 1장면(2줄) / 갈림길 앞 1줄 / 비밀방 발견 1장면(2줄) / 광산 붕괴 1장면(2줄) / 클리어 3줄(스테이지 4로 이어지게)
10. 필요한 그림 목록: 배경(맵별 1장) / 적 · 중간 보스 · 보스 시트 / 소품(문·광차·화약통 등)
글자 수 규칙(한 줄 20자, 한 장면 2줄)은 대사·자막에만 적용.
```

---

## 12-C. 그림 (새 대화 2개, 12-B가 정해진 뒤)

### 12-C-1. 배경 (새 대화 ①) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`
첫 메시지:
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.

Rules for ALL backgrounds in this conversation:
- True pixel art with HARD EDGES: every pixel is a crisp square block (the same block size as the stage 1 references),
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- The aspect ratio is given per image. The walkable ground is seen from a slight high angle, fairly plain and evenly lit
  so characters stay readable.
- Exits stand on the ground line at the back edge.
- This is a STATIC PLATE: animated things are added later in the game, so draw them in their "off" state:
  NO lit flames (torches and lamps unlit: only dark heads/holders, no glow spots), NO mine carts (draw the empty rails only),
  NO falling water, dust or smoke, and glowing crystals drawn DIM (dark purple, no halo).
- NO objects on the walkable ground (no barrels, crates, carts, rocks piles, barricades, planks) - those are added separately.
- NO characters, NO creatures, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1 - [12-B 맵 1 이름] ([비율]): [12-B 맵 1 묘사 + 그려 둘 상태]
```
다음 메시지(같은 대화)에서 하나씩:
```
Background [N] - [이름] ([비율]): same rules. [12-B 맵 N 묘사 + 그려 둘 상태]
```

### 12-C-2. 적 · 보스 시트 (새 대화 ②) — 첨부: `refs/enemy_lineup_ref.png`
첫 메시지:
```
Design new enemies for a 2D pixel art beat 'em up. The attached sheet shows the real in-game sprites (the silver knight is the hero).
Match that exact pixel art style, outline, shading, proportions and pixel size.

For each character make ONE sheet:
- Left, large: idle battle stance, full body, three-quarter view facing RIGHT and slightly toward the viewer (same angle as the reference sprites).
- Right, smaller: two attack poses (the moment of the hit).
- Same character, same colors in all three poses. Poses must not overlap. Feet visible.
- Only this one view - no turnaround, no back or side views.
- Bold, simple, readable silhouette: no large shields, no long capes, few thin dangling parts.
- In the wind-up poses the weapon stays in FRONT of the body, never hidden behind the head or back.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1 - [12-B 적 1 이름 · 생김새 · 대기 / 공격 2개]
```
다음 메시지(같은 대화)에서 하나씩:
```
Character [N] - [이름]: same rules. [12-B 생김새 · 포즈 3개]
```
- 중간 보스는 `This is a mid-boss: about 1.6 times taller than the hero.`, 보스는 `This is a boss: about 2 times taller than the hero.`를 덧붙입니다.

## Claude가 받은 뒤 하는 일
- 12-B: 게임으로 되는 것 / 개발이 새로 만들 것 / 아트 주의로 나눠 `art/story/stage3_design.md`에 정리, 자막·대사는 `game_text_ko.json`. 12-C 칸 채우기.
- 배경: 도트 격자 재기 → 게임 배율로 맞춰 색 정리 → 맵 배치(바닥·출구·카메라) → 게임 캡처
- 움직이는 오브젝트: 12-B 목록대로 아트(PixelLab)·이펙트 세션(불·먼지·빛)이 만들어 배경 위에 얹고 영상으로 확인
- 적·보스: 시트 대기 자세 → PixelLab 같은 화풍 생성 → 뼈대 애니메이션 → 이펙트 요청
