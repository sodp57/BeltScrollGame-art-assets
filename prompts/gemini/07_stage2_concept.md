# 7. 스테이지 2 구상 — 맵 · 샛길 · 비밀방 · 적 · 보스

- **1-3을 먼저** 끝내세요(5스테이지 뼈대가 거기서 정해짐).
- 순서: **7-A 방향 후보 → 7-B 상세 설계 → 7-C 컨셉 그림**
  - 7-A·7-B: 스토리 대화(1-1~1-3과 같은 대화)에 이어서. 결과를 대화창(Claude)에 붙여 넣기(길면 `C:\GameDev\inbox\gemini\story\7_stage2.txt`)
  - 7-C: 7-B 설계가 정해진 뒤 **새 대화**에서. 결과 그림을 대화창(Claude)에 첨부
- Claude가 7-B를 받으면 게임에 맞게 다듬어(만들 수 있는지, 기존 적 재사용, 크기) 작업 목록으로 바꾸고, 7-C에 붙여 넣을 칸을 채워 드립니다.

---

## 7-A. 방향 후보 (스토리 대화에 이어서)
```
이제 스테이지 2(피의 숲)를 구체적으로 설계하자. 먼저 방향 후보 3개만 짧게 줘.
- 후보마다: 한 줄 컨셉 / 분위기 키워드 3개 / 본길 지역 3곳 / 샛길과 중간 보스 / 비밀방 아이디어 / 보스 한 줄 / 이 후보만의 볼거리 하나
- 1-3에서 정리한 뼈대(데몬 나이트 추격, 용병단 매복, 거미 마수)를 지키되, 세 후보는 서로 느낌이 다르게.
- 마지막에 네 추천 하나와 이유.
```
→ 마음에 드는 후보(또는 섞을 부분)를 정해서 7-B로.

## 7-B. 상세 설계 (같은 대화)
`[고른 후보]` 칸을 바꿔 붙이세요(예: "2번 후보, 단 보스는 1번 것으로").
```
[고른 후보]로 스테이지 2 설계서를 써 줘. 이 게임에서 실제로 만들 수 있는 규칙을 먼저 알려 줄게. 규칙 안에서 설계해 줘.

[게임 규칙]
- 맵 하나 = 화면 한 장 크기의 배경 그림 한 장(가로로 조금만 스크롤된다). 맵과 맵 사이는 화면이 어두워졌다 밝아지며 넘어간다.
- 화면 위쪽 약 60%는 배경(벽·풍경), 아래쪽 약 40%가 캐릭터가 싸우는 바닥이다(위아래로도 움직이는 깊이 있는 띠).
  출구는 배경 벽에 그려진 문·동굴·길이고, 그 앞에서 위 방향키를 누르면 들어간다.
- 쓸 수 있는 장치: 레버로 여는 관문 / 주기적으로 켜지는 함정(가시·불길 등, 독·기절·둔화를 걸 수 있음) / 밟으면 숨어 있던 적이 튀어나오는 매복 /
  부서지는 상자·통(안에서 아이템) / 열쇠로 여는 보물상자 / 갈림길(문 두 개 중 고르기) / 보스를 쓰러뜨리면 열리는 문 / 들어갔다 나오는 옆방.
- 적 규칙: 주인공과 비슷한 크기(큰 적은 1.3배까지). 공격은 2개(근접 1 + 특기 1), 공격 전에 알아보기 쉬운 예고 동작. 한 화면에 적은 4~5명까지.
  이전 적(붉은 산적·붉은 궁수·검은 암살자·대머리 거한·돌 가고일)을 섞어 써도 된다. 새 적은 3종까지.
- 보스 규칙: 화면 높이의 1/3~1/2 크기. 패턴 3~4개 + 체력이 절반이 되면 2페이즈(패턴 하나가 세지거나 하나 추가). 졸개 소환 1개, 원거리 공격 가능
  (마법탄은 곧게 날아가고, 화살·투척물은 포물선). 참고로 스테이지 1 데몬 나이트 패턴은 내려찍기(바닥 충격파) / 돌진 / 졸개 소환 / 조준 마탄이다.
- 애니메이션은 뼈대(스켈레톤)로 움직여 만든다. 다리가 아주 많은 몸은 움직이기 어렵다. 거미라면 큰 몸통과 앞다리 위주로 움직이게 하거나,
  상체가 사람인 반인반거미처럼 읽기 쉬운 모양도 좋다.

[써 줄 것]
1. 맵 흐름: 본길 맵 3개 + 샛길 맵 1~2개 + 비밀방 + 보스 맵. 화살표로 이어진 흐름 한 줄, 그리고 맵마다 표로:
   이름(영어·한국어) / 배경에 보이는 것(벽·풍경, 3~4문장, 그림 프롬프트로 쓸 수 있게 구체적으로) / 바닥 재질 / 출구 모양과 위치 /
   장치 / 나오는 적 구성(웨이브 1~2개) / 분위기 색(주된 색 3개)
2. 갈림길: 어느 맵에서, 무엇으로(문·다리·덤불 사이 길 등) 갈라지는지. 샛길이 본길보다 어렵고 보상이 좋은 이유.
3. 비밀방: 찾는 방법(부서지는 벽·숨은 레버·조건 등, 위 장치 안에서), 안에 있는 것(보상 1~2개, 이름·한 줄 설명), 나가면 어디로 이어지는지.
4. 새 적(최대 3종) 표: 이름(영어·한국어) / 역할(근접·원거리·돌격·방해 중) / 생김새(색·무기·실루엣, 그림 프롬프트로 쓸 수 있게) /
   공격 2개(예고 동작 → 공격) / 상대하는 요령 / 처음 나오는 맵
5. 중간 보스(샛길): 이름 / 생김새 / 패턴 3개 / 등장 대사 2줄 · 쓰러질 때 2줄
6. 스테이지 보스(거미 마수 계열): 이름 / 생김새(크기 포함) / 보스방 모습 / 패턴 4개(예고 → 공격 → 빈틈) / 2페이즈 변화 / 소환 졸개 /
   대사(등장 2줄, 2페이즈 1줄, 쓰러질 때 2줄). 데몬 나이트가 이 스테이지 끝에 어떻게 얼굴을 비치는지(또는 안 비치는지) 한 줄.
7. 자막: 스테이지 시작 1장면(2줄) / 갈림길 앞 1줄(선택) / 비밀방 발견 1장면(2줄) / 클리어 3줄
8. 필요한 그림 목록: 배경(맵별 1장) / 적 · 중간 보스 · 보스 디자인 시트 / 기타(문·소품 등)
글자 수 규칙(한 줄 20자, 한 장면 2줄)은 대사·자막에만 적용.
```

---

## 7-C. 컨셉 그림 (새 대화, 7-B가 정해진 뒤)
대화 2개로 나눠서 하세요(배경끼리, 캐릭터끼리 같은 대화라야 화풍이 맞습니다).
`[ ]` 칸은 7-B 결과를 받은 뒤 Claude가 채워 드립니다.

### 7-C-1. 배경 (새 대화 ①) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`
첫 메시지:
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.

Rules for ALL backgrounds in this conversation:
- 16:9 landscape (1536x864 if possible).
- True pixel art with HARD EDGES, drawn as if on a 384x216 pixel grid and enlarged 4x: every pixel is a crisp 4x4 block,
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- Top ~62%: back wall / scenery. Bottom ~38%: walkable ground seen from a slight high angle, fairly plain and evenly lit so characters stay readable.
- The exit (door, cave mouth or path) is drawn closed on the back wall, standing on the ground line, if the map has one.
- NO characters, NO creatures, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1: [7-B 맵 1 묘사]
```
다음 메시지(같은 대화)에서 하나씩:
```
Background [N]: same rules. [7-B 맵 N 묘사]
```

### 7-C-2. 적 · 보스 디자인 시트 (새 대화 ②) — 첨부: `refs/enemy_lineup_ref.png`
첫 메시지:
```
Design new enemies for a 2D pixel art beat 'em up. The attached sheet shows the real in-game sprites (the silver knight is the hero).
Match that exact pixel art style, outline, shading, proportions and pixel size.

For each character make ONE sheet:
- Left, large: idle battle stance, full body, three-quarter view facing RIGHT and slightly toward the viewer (same angle as the reference sprites).
- Right, smaller: two attack poses (the moment of the hit).
- Same character, same colors in all three poses. Poses must not overlap. Feet visible.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1: [7-B 적 1 이름 · 생김새 · 공격 2개]
```
다음 메시지(같은 대화)에서 하나씩:
```
Character [N]: same rules. [7-B 적 N / 중간 보스 / 보스 생김새]
```
- 보스는 이렇게 덧붙이세요: `This is a boss: draw it about 1.6 times taller than the hero in the reference.`

## Claude가 받은 뒤 하는 일
- 배경: 384x216 도트로 맞춰 색 정리 → 맵에 넣고 바닥 범위·출구 위치 지정 → 게임 캡처
- 적·보스: 시트의 대기 자세를 기준으로 PixelLab에서 같은 화풍 캐릭터 생성 → 뼈대 애니메이션 → 이펙트 세션에 공격 이펙트 요청
