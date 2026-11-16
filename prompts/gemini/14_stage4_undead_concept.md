# 14. 6스테이지로 늘리기 + 언데드 던전 스테이지 구상 (뼈대 → 방향 → 설계·이야기 → 그림)

- 순서: **14-0 6스테이지 뼈대 → 14-A 방향 후보 → 14-B 상세 설계 + 이야기 → 14-C 그림**
  - 14-0·14-A·14-B: **스토리 대화**(1-1~1-3, 7·12번을 한 대화)에 이어서. 결과는 대화창(Claude)에 붙여 넣기
    (길면 `C:\GameDev\inbox\gemini\story\14_stage4.txt`)
  - 14-C: 14-B가 정해진 뒤 **새 대화 2개**(배경끼리 / 캐릭터끼리). `[ ]` 칸은 Claude가 14-B를 보고 채워 드립니다.
- 원래 뼈대는 5스테이지(4 공허의 탑 → 5 마계의 문)입니다. 여기에 **언데드·유령이 나오는 던전 스테이지**를 하나 끼워 6스테이지로 만듭니다.
  - Claude 추천 위치 = **스테이지 4**(3 광산 붕괴 → 4 언데드 던전 → 5 공허의 탑 → 6 마계의 문). 원래 스테이지 4에 있던 "해골 병사"가 던전으로 오고,
    탑은 가고일·마법 쪽으로 더 또렷해집니다. 다른 위치가 낫다면 Gemini가 이유와 함께 제안하게 했습니다.
  - 스테이지 1 샛길에 이미 "지하 묘실"이 있으니 그것과 겹치지 않게 요청했습니다.
- 스테이지 2·3에서 배운 것(12번과 같음): 움직이는 것(불·유령불·안개·떨어지는 물)은 배경에 그리지 않고 따로 얹는다 / 맵 모양을 처음부터 고른다 /
  캐릭터 실루엣은 굵고 단순하게, 공격 준비 때 무기는 몸 앞 / 기계·로봇 톤 대신 마석·마법 판타지.

---

## 14-0. 6스테이지 뼈대 (스토리 대화에 이어서)
```
게임을 5스테이지에서 6스테이지로 늘리려고 해. 언데드와 유령이 나오는 어두운 던전 스테이지를 하나 새로 넣고 싶어.
지금까지 만든 것: 스테이지 1 밤의 성 / 2 피의 숲 / 3 버려진 광산(유황 가스와 녹슨 기계의 광산, 보스 거한족 족장 골리앗, 폭약고를 터뜨려 붕괴)은 완성됐어.
원래 뼈대의 4 공허의 탑(흑주술사 본체, 해골 병사, 스톤 가고일), 5 마계의 문(심연 데몬 나이트, 헬 하운드, 정예 해골 기사·불꽃 정령)은 아직 안 만들었어.

1. 언데드 던전을 몇 번째에 넣을지 정해 줘. 내 생각은 4번째(광산 붕괴 → 언데드 던전 → 공허의 탑 → 마계의 문)인데,
   더 나은 자리가 있으면 이유와 함께 제안해 줘.
2. 6스테이지 뼈대 표를 다시 써 줘. 칸: 스테이지 / 흐름 한 줄 / 본길 3곳 / 샛길 분기와 중간 보스 / 비밀방(보상) / 스테이지 보스 / 새 적
   - 1~3은 이미 만든 대로 두고(표에는 한 줄 요약만), 4~6을 새로.
   - 해골 병사·정예 해골 기사처럼 원래 다른 스테이지에 있던 언데드를 던전으로 옮길지, 스테이지마다 새 적이 겹치지 않게 나눠 줘.
   - 비밀방 보상은 오래 쓰는 장비로(한 번 쓰는 물약 말고).
3. 스테이지 사이 연결 한 줄씩(3→4, 4→5, 5→6, 엔딩). 특히 광산이 무너진 뒤 어떻게 던전으로 가게 되는지.
4. 던전이 스테이지 1 샛길의 "지하 묘실"(환영 흑주술사가 나오는 작은 방)과 어떻게 다른 곳인지 한두 줄.
5. 던전의 주인(보스)이 데몬 나이트·흑주술사·마왕과 어떤 관계인지 한두 줄. 세 기사의 과거(옛 기사단)와 엮이면 더 좋아.
```
→ 뼈대가 마음에 들면 14-A로. 위치를 바꾸고 싶으면 같은 대화에서 고쳐 달라고 하면 됩니다.

## 14-A. 언데드 던전 방향 후보 (같은 대화)
```
14-0에서 정한 언데드 던전 스테이지의 방향 후보 3개만 짧게 줘.
- 후보마다: 한 줄 컨셉 / 분위기 키워드 3개 / 본길 지역 3곳 / 샛길과 중간 보스 / 비밀방 아이디어 / 보스 한 줄 /
  유령형 적을 어떻게 쓰는지 한 줄 / 이 후보만의 볼거리 하나
- 조건: 던전 느낌(돌 회랑, 지하 감옥, 납골당, 봉인된 문 같은 닫힌 공간). 언데드(해골·구울 같은 몸 있는 적)와 고스트(떠다니는 망령)를 둘 다.
- 스테이지 1(밤의 성: 달빛·석조 성), 2(피의 숲: 붉은 달·안개·늪), 3(광산: 유황 노랑·녹 주황·용암)과 색이 겹치지 않게.
  어두워도 바닥과 캐릭터는 잘 보여야 한다.
- 세 후보는 서로 느낌이 다르게(예: 차가운 감옥 / 왕가의 납골 묘역 / 물에 잠긴 지하 신전 같은 식으로).
- 마지막에 네 추천 하나와 이유.
```
→ 마음에 드는 후보(또는 섞을 부분)를 정해서 14-B로.

## 14-B. 상세 설계 + 이야기 (같은 대화)
`[고른 후보]` 칸을 바꿔 붙이세요(예: "2번 후보, 단 보스방은 1번 것으로").
```
[고른 후보]로 언데드 던전 스테이지 설계서를 써 줘. 이 게임에서 실제로 만들 수 있는 규칙을 먼저 알려 줄게. 규칙 안에서 설계해 줘.

[게임 규칙]
- 맵 하나 = 배경 그림 한 장. 맵과 맵 사이는 화면이 어두워졌다 밝아지며 넘어간다. 맵 모양은 다섯 중 하나:
  (가) 가로로 긴 통로(21:9, 화면 약 2배 폭) (나) 위아래로 넓은 광장(1:1) (다) 위나 아래로 이어지는 사선 비탈(21:9)
  (라) 바닥이 깊은 아레나(4:3, 보스방용) (마) 화면 한 장(16:9, 작은 방)
- 화면 위쪽은 배경(벽·풍경), 아래쪽이 캐릭터가 싸우는 바닥(위아래로도 움직이는 깊이 있는 띠).
  출구는 배경에 그려진 문·계단·통로이고, 그 앞에서 위 방향키를 누르면 들어간다.
- 쓸 수 있는 장치: 레버로 여는 관문 / 주기적으로 켜지는 함정(가시·불길·독 등, 독·기절·둔화·화상을 걸 수 있음) / 매복 /
  부서지는 상자·통·관(아이템, 화약통은 터지며 주변 적에게 피해) / 열쇠 보물상자 / 갈림길(문 두 개 중 고르기) /
  부수면 길이 열리는 바리케이드·벽 / 점프 공격으로 부서지는 바닥(아래 방으로 떨어짐) / 바닥에 남는 독 웅덩이 /
  레일을 따라 화면을 가로지르는 돌진물(경고 뒤 지나감) / 바닥 표시 뒤 솟아 띄우는 분출 / 그림자 예고 뒤 떨어지는 낙석 /
  보스를 쓰러뜨리면 열리는 문 / 보스방 배경에서 한 번 재생되는 연출.
  새 장치는 2개까지 제안해도 된다. 대신 어떻게 피하는지 한 줄로.
- 적 규칙: 주인공과 비슷한 크기(큰 적은 1.3배까지). 공격은 2개(근접 1 + 특기 1), 공격 전에 알아보기 쉬운 예고 동작. 한 화면에 4~5명까지.
  이전 적을 섞어 써도 된다: 붉은 산적·붉은 궁수·검은 암살자·대머리 거한·돌 가고일·숲 늑대·맹독 고블린·중무장 용병·
  폭탄 고블린·방독면 집행관·녹슨 철골렘. 새 적은 3종까지.
- 유령형 적 규칙(이 스테이지의 핵심):
  - 떠다니며 움직여도 되지만 그림자는 바닥에 있어야 한다(어느 깊이에 있는지 보이게).
  - 반투명·벽 통과·잠깐 사라졌다 나타나기는 된다. 단 맞힐 수 없는 시간은 짧게, 다시 맞힐 수 있게 되는 순간이 눈에 보이게.
  - 몸 있는 언데드와 다르게 싸우는 이유를 하나씩 줘(예: 유령은 잡기·넘어뜨리기가 안 됨, 해골은 쓰러져도 한 번 다시 일어남).
- 보스 규칙: 화면 높이의 1/3~1/2. 패턴 3~4개(예고 → 공격 → 빈틈) + 체력 절반에서 2페이즈. 졸개 소환 1개, 원거리 가능
  (마법탄은 곧게, 투척물은 포물선). 지금 있는 보스 패턴: 내려찍기 충격파 / 돌진 / 소환 / 조준탄 / 거미줄 속박(연타로 풀기) /
  천장에서 덮치기(그림자 예고) / 전투 함성(주변 기절) / 독액 투척 / 무작위 낙석 / 졸개 집어 던지기.
  같은 것을 써도 되지만 이 보스만의 패턴 하나는 꼭 새로(유령·언데드다운 것으로).
- 애니메이션은 뼈대로 만든다. 사람형이 가장 쉽다. 큰 방패·긴 망토·너풀거리는 천·가는 장식이 많으면 어렵다.
  유령도 아래가 흐려지는 꼬리 정도로 단순하게. 실루엣은 굵고 단순하게, 공격 준비 때 무기는 몸 앞.
- 움직이는 배경 오브젝트(횃불·유령불·흔들리는 쇠사슬·떨어지는 물방울·깔리는 안개·빛나는 봉인 문양 등)는 배경 그림과 따로 만들어 위에 얹는다.
- 어두운 던전이지만 걸어 다니는 바닥은 고르게 밝아서 캐릭터가 잘 보여야 한다.

[써 줄 것]
1. 맵 흐름: 본길 맵 3개 + 샛길 맵 1~2개 + 비밀방 + 보스 맵. 화살표 흐름 한 줄, 그리고 맵마다 표로:
   이름(영어·한국어) / 모양(가~마) / 배경에 보이는 것(3~4문장, 그림 프롬프트로 쓸 수 있게 구체적으로. 움직이는 것은 빼고) /
   바닥 재질 / 출구 모양과 위치 / 장치 / 적 구성(웨이브 1~2개) / 분위기 색(3개)
2. 움직이는 오브젝트 목록: 맵마다 3~6개. 표로: 무엇 / 어디 / 어떻게 움직이나(반복 · 가끔 · 한 번) /
   배경 그림에서는 어떤 상태로 그려 둘지(예: 횃불은 불 꺼진 막대만, 유령불은 그리지 않음, 봉인 문양은 어둡게).
3. 갈림길: 어느 맵에서 무엇으로 갈라지는지. 샛길이 더 어렵고 보상이 좋은 이유.
4. 비밀방: 찾는 방법(위 장치 안에서), 보상 1~2개(이름 · 한 줄 설명, 오래 쓰는 장비 위주), 나가면 어디로 이어지는지.
5. 새 적(최대 3종, 몸 있는 언데드와 유령을 둘 다 포함) 표: 이름(영어·한국어) / 역할 / 생김새(색·무기·실루엣, 그림 프롬프트로) /
   공격 2개(예고 → 공격) / 요령(어떻게 상대하나) / 첫 등장 맵
6. 중간 보스(샛길): 생김새 / 패턴 3개 / 대사(등장 2줄, 쓰러질 때 2줄)
7. 스테이지 보스: 생김새(크기 포함) / 보스방 모습 / 패턴 4개 / 2페이즈 / 소환 졸개 / 대사(등장 2줄, 2페이즈 1줄, 쓰러질 때 2줄)
8. 이야기: 스테이지 3 클리어(광산 붕괴)에서 이어지게.
   - 이 던전이 무엇이고 왜 언데드가 일어났는지 2~3문장(흑주술사·마왕·다음 스테이지와 연결).
   - 데몬 나이트 또는 흑주술사(환영)가 이 스테이지에서 얼굴을 비치는 방법 한 줄(보스방 배경 연출로 가능).
   - 보스를 쓰러뜨린 뒤 마무리를 어떻게 보여 줄지(자막 + 화면 연출 정도로).
9. 자막: 스테이지 시작 1장면(2줄) / 갈림길 앞 1줄 / 비밀방 발견 1장면(2줄) / 보스 처치 뒤 1장면(2줄) / 클리어 3줄(다음 스테이지로 이어지게)
   그리고 스테이지 3 클리어 3줄째가 지금 "다음은 놈이 있는 공허의 탑이다."인데, 던전으로 이어지게 바꿀 문장 1줄.
10. 필요한 그림 목록: 배경(맵별 1장) / 적 · 중간 보스 · 보스 시트 / 소품(문·관·제단 등)
글자 수 규칙(한 줄 20자, 한 장면 2줄)은 대사·자막에만 적용.
```

---

## 14-C. 그림 (새 대화 2개, 14-B가 정해진 뒤 — `[ ]` 칸은 Claude가 채워 드립니다)

### 14-C-1. 배경 (새 대화 ①) — 첨부: `refs/stage_bg_layout_guide.png`, `refs/stage1_maps_ref.png`
첫 메시지:
```
I need background art for a 2D pixel art beat 'em up. Attached: (1) a layout guide, (2) four finished backgrounds from stage 1.
Match the stage 1 pixel art style, detail level and color approach exactly, and follow the layout guide in every image.

Rules for ALL backgrounds in this conversation:
- True pixel art with HARD EDGES: every pixel is a crisp square block (the same block size as the stage 1 references),
  flat color clusters, no anti-aliasing, no blur, no soft gradients, no painterly strokes, no photographic texture, no noise.
- The aspect ratio is given per image. The walkable ground is seen from a slight high angle, fairly plain and evenly lit
  so characters stay readable, even though the dungeon is dark.
- Exits stand on the ground line at the back edge.
- This is a STATIC PLATE: animated things are added later in the game, so draw them in their "off" state:
  NO lit flames (torches and braziers unlit: only dark heads/holders, no glow spots), NO ghost lights or wisps,
  NO fog or mist, NO falling water drops, and magic runes or seals drawn DIM (dark, no halo).
- NO objects on the walkable ground (no coffins, barrels, crates, bones piles, barricades) - those are added separately.
- NO characters, NO creatures, NO skeletons standing or lying on the ground, NO text, NO letters, NO UI, NO watermark, NO border.
- Limited palette (about 40 colors per image).

Background 1 - [14-B 맵 1 이름] ([비율]): [14-B 맵 1 묘사 + 그려 둘 상태]
```
다음 메시지(같은 대화)에서 하나씩:
```
Background [N] - [이름] ([비율]): same rules. [14-B 맵 N 묘사 + 그려 둘 상태]
```

### 14-C-2. 적 · 보스 시트 (새 대화 ②) — 첨부: `refs/enemy_lineup_ref.png`
첫 메시지:
```
Design new enemies for a 2D pixel art beat 'em up. The attached sheet shows the real in-game sprites (the silver knight is the hero).
Match that exact pixel art style, outline, shading, proportions and pixel size.

For each character make ONE sheet:
- Left, large: idle battle stance, full body, three-quarter view facing RIGHT and slightly toward the viewer (same angle as the reference sprites).
- Right, smaller: two attack poses (the moment of the hit).
- Same character, same colors in all three poses. Poses must not overlap. Feet visible (for a floating ghost: the lowest point of its body visible).
- Only this one view - no turnaround, no back or side views.
- Bold, simple, readable silhouette: no large shields, no long capes, no long flowing cloth, few thin dangling parts.
- In the wind-up poses the weapon stays in FRONT of the body, never hidden behind the head or back.
- Ghosts: draw them OPAQUE with solid pixel colors (transparency is added in the game), a simple tapering tail, no glow halo.
- Plain flat dark background (#14161E), NO text, NO letters, NO UI, NO watermark.
- True pixel art with hard edges, no anti-aliasing, no blur.

Character 1 - [14-B 적 1 이름 · 생김새 · 대기 / 공격 2개]
```
다음 메시지(같은 대화)에서 하나씩:
```
Character [N] - [이름]: same rules. [14-B 생김새 · 포즈 3개]
```
- 중간 보스는 `This is a mid-boss: about 1.6 times taller than the hero.`, 보스는 `This is a boss: about 2 times taller than the hero.`를 덧붙입니다.

## Claude가 받은 뒤 하는 일
- 14-0: 6스테이지 뼈대를 `art/story/story_bible.md`에 정리, 스테이지 4~6 `stage_intro`·`stage_clear` 자리 다시 맞춤(스테이지 3 클리어 문장 포함).
- 14-B: 게임으로 되는 것 / 개발이 새로 만들 것(유령의 반투명·통과, 해골 되살아나기 등) / 아트 주의로 나눠 `art/story/stage4_design.md`, 14-C 칸 채우기.
- 배경: 도트 격자 재기 → 게임 배율 → 맵 배치 → 캡처. 움직이는 오브젝트는 아트(PixelLab)·이펙트 세션(유령불·안개·빛)이 얹음.
- 적·보스: 시트 대기 자세 → PixelLab 같은 화풍 생성 → 뼈대 애니메이션 → 이펙트 요청.
