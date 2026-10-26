# 2. 배경음악 8곡

- 지금 게임에 배경음악이 한 곡도 없습니다(재생 기능은 있음).
- Gemini에서 쓸 수 있는 음악 생성 기능으로 만들어 주세요. 구독에 음악 생성이 없으면 알려 주세요. 다른 방법을 찾겠습니다. 프롬프트는 영어라 다른 음악 생성 도구에도 그대로 쓸 수 있습니다.
- 곡마다 **새로 생성**하고, 마음에 드는 버전을 `C:\GameDev\inbox\gemini\bgm\번호_이름.mp3` 로 저장해 주세요. 예: `01_title.mp3`, `05_boss_demon_knight.mp3`
- 반복 재생 지점은 아트 세션이 맞춥니다. 끝이 자연스럽게 처음으로 이어지지 않아도 괜찮습니다.
- 한 곡이 너무 짧게 나오면(30초 미만) 같은 곡을 이어서 늘려 달라고 하거나 다시 생성해 주세요.

## 모든 곡에 공통으로 붙일 문장
매 곡 프롬프트 끝에 이 문장을 같이 붙여 주세요.
```
Style: 1990s arcade beat 'em up soundtrack (CPS2 / SNES era), punchy and catchy, sampled orchestra and synth instruments, clear strong melody, instrumental only, no vocals, no lyrics, loopable, around 90 seconds.
```

## 곡별 프롬프트

### 01_title — 타이틀 화면
```
Title screen theme for a dark medieval fantasy brawler. Majestic and ominous, slow 88 BPM, D minor. Opens with a deep church organ chord and timpani roll, then heroic brass melody over choir pads and tolling bells, building to a proud climax.
```

### 02_stage1_castle — 성문 통로·안뜰 (스테이지 1 일반 구간)
```
Stage theme for fighting through a moonlit castle at night. Driving and heroic but dark, 140 BPM, E minor. Punchy rock drums, slap bass, harpsichord ostinato, synth brass lead melody, short string stabs. Energetic enough to fight to for minutes without getting tiring.
```

### 03_crypt — 지하 묘실 (샛길)
```
Underground crypt exploration theme. Eerie and tense, 112 BPM, C minor. Low strings, pipe organ, music box motif, distant bells, heartbeat-like kick drum, occasional dissonant choir swell. Creepy but still rhythmic enough for combat.
```

### 04_midboss_sorcerer — 흑주술사 전투
```
Mid-boss battle against a dark sorcerer who summons stone gargoyles. Mystical and urgent, 150 BPM, F sharp minor. Fast arpeggiated synth, chanting choir "ah", tribal toms, eerie bell melody, a sinister motif that repeats and rises.
```

### 05_boss_demon_knight — 데몬 나이트 전투
```
Final boss battle against a demonic armored knight in a throne room. Heavy, aggressive and epic, 162 BPM, B minor. Pounding war drums, distorted guitar-like synth riffs, pipe organ, brass hits, full choir on the chorus. Relentless intensity with a memorable villain theme.
```

### 06_stage_clear — 스테이지 클리어 (짧은 곡)
```
Short victory fanfare after defeating a boss, 8 seconds long, triumphant brass and timpani ending on a bright major chord. Does not loop.
```

### 07_game_over — 게임 오버 (짧은 곡)
```
Short game over jingle, 6 seconds long, somber descending melody on strings and a low bell, ends quietly. Does not loop.
```

### 08_ending — 엔딩·스태프롤
```
Ending and credits theme after saving the castle. Warm, hopeful and slightly bittersweet, 96 BPM, G major. Strings and french horn melody, gentle harp, soft choir, building to a heroic final restatement of the title theme feeling, around 2 minutes.
```
