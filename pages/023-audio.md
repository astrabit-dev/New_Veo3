# 오디오 생성 완전 해설

> **Veo 3가 세상을 바꾼 가장 큰 이유 — 소리**

---

## 오디오 기능이 왜 혁명인가

Veo 3 이전의 모든 AI 영상 도구는 **묵음**이었습니다. 영상을 만들고 나서 별도로 음악, 효과음, 대사를 입혀야 했습니다. 영상 편집 경험이 없는 초보자에게는 큰 장벽이었습니다.

Veo 3는 처음으로 **영상과 오디오를 하나의 프롬프트에서 동시에 생성**합니다. 이것이 Veo 3를 단순한 업그레이드가 아닌 혁명으로 만드는 이유입니다.

---

## Veo 3 오디오의 3가지 종류

### 1. 음성 대화 (Dialogue)

캐릭터가 실제로 말하는 대사입니다. 입술 움직임(립싱크)도 자연스럽게 맞춰집니다.

**활용:**
- 뉴스 앵커가 뉴스를 읽는 장면
- 캐릭터 간의 대화 장면
- 인터뷰 형식 영상
- 내레이션

**프롬프트 작성 방법:**
```
A news anchor sitting at a desk in a modern studio,
speaking directly to camera: "Tonight, scientists have
discovered a new planet that may support life."
[Audio: professional news studio ambiance, slight echo]
```

**주의:** 따옴표 안에 대사를 넣으면 자막이 함께 생성될 수 있습니다. 자막을 원하지 않으면 대사를 자연어로 설명하는 방식을 사용하세요.

예: `speaking about a new planet discovery` (직접 대사 없이)

### 2. 환경음 (Ambient Sound)

장면의 배경이 되는 자연스러운 소리들입니다.

**카테고리별 환경음:**

**자연 환경음:**
- `birds chirping` (새 지저귐)
- `wind rustling through leaves` (나뭇잎 바람 소리)
- `gentle stream flowing` (시냇물 흐르는 소리)
- `ocean waves` (바다 파도)
- `thunderstorm` (천둥 폭풍)
- `rain on a rooftop` (지붕 위 빗소리)
- `crackling campfire` (장작불 타는 소리)

**도시 환경음:**
- `city traffic noise` (도시 교통 소음)
- `café ambiance, clinking cups` (카페 분위기)
- `crowd murmuring` (군중 웅성거림)
- `subway sounds` (지하철 소리)
- `church bells in the distance` (멀리서 들리는 종소리)

**실내 환경음:**
- `clock ticking` (시계 째깍거림)
- `fire crackling in a fireplace` (벽난로 불소리)
- `old wooden floor creaking` (낡은 목조 바닥 삐걱임)

**프롬프트 예시:**
```
An old scholar reads by candlelight in a dusty library,
late at night, shadows dancing on stone walls.
[Audio: crackling fireplace, wind howling outside,
pages turning softly, distant owl hooting]
```

### 3. 음악 및 사운드 효과 (Music & SFX)

배경 음악이나 특정 사운드 이펙트를 생성합니다.

**음악 스타일:**
- `orchestral score, dramatic` (오케스트라, 드라마틱)
- `soft piano melody` (부드러운 피아노 선율)
- `electronic ambient music` (전자 앰비언트 음악)
- `upbeat jazz` (경쾌한 재즈)
- `suspenseful strings` (긴장감 있는 현악)
- `epic battle music` (서사적 전투 음악)
- `gentle acoustic guitar` (부드러운 어쿠스틱 기타)

**사운드 이펙트:**
- `sword clashing` (검 부딪히는 소리)
- `magical sparkles` (마법 반짝임 소리)
- `explosion in the distance` (멀리서 폭발음)
- `heartbeat, slow and heavy` (느리고 무거운 심장 박동)

---

## 오디오 프롬프트 작성 공식

```
[기본 영상 프롬프트]
[Audio: 주요 소리1, 소리2, 소리3, 전반적인 음악 분위기]
```

**전체 예시:**

```
A lone wolf howls at the full moon from a mountain peak,
snow-covered landscape stretching endlessly below,
dramatic wide shot, blue and silver tones, epic and solitary mood.
[Audio: wolf howling, howling wind, distant echo,
faint orchestral score building slowly]
```

---

## 오디오와 영상의 시너지

오디오와 영상 프롬프트가 서로를 강화할 때 최고의 결과가 나옵니다.

**예시 1 — 공포 장면:**
```
영상: 어두운 복도, 끝에서 문이 천천히 열림, 극적인 로우앵글
오디오: 삐걱이는 문소리, 느린 발소리, 긴장감 있는 바이올린
결과: 영상과 오디오가 함께 공포 분위기를 극대화
```

**예시 2 — 광고 장면:**
```
영상: 우아한 향수 병, 보랏빛 빛, 클로즈업 달리샷
오디오: 부드러운 재즈 피아노, 향기가 퍼지는 듯한 공기 소리
결과: 고급 브랜드 이미지 강화
```

---

## 오디오 생성 시 주의사항

### 주의 1: 자막 방지
대사를 큰따옴표로 감싸면 화면 위에 자막이 생성될 수 있습니다. 자막을 원하지 않으면 대사를 자연어로 설명하거나, 대사 앞에 `(no subtitles, no captions)` 를 명시하세요.

### 주의 2: 언어 제한
Veo 3의 대화 생성은 **영어**에서 가장 자연스럽게 작동합니다. 한국어 대사는 결과가 불안정할 수 있습니다.

### 주의 3: 오디오는 Veo 3 전용
Fast Mode(Veo 2)에서는 오디오 생성이 지원되지 않습니다. 반드시 Veo 3 모드를 선택해야 오디오가 포함됩니다.

---

## 오디오 활용 고급 팁

### 팁 1: 레이어 구조로 설명
단순히 "배경음"이라고 하지 말고, 레이어를 나눠서 설명하면 더 풍부한 오디오가 생성됩니다.

```
[Audio:
  foreground: footsteps on gravel, labored breathing
  middle: distant crowd noise, street performer music
  background: city traffic hum, wind
]
```

### 팁 2: 오디오와 영상 분위기 일치
공포 장면에 경쾌한 음악, 광고 장면에 장례식 음악처럼 영상과 오디오가 충돌하면 기이한 결과가 납니다. 분위기를 일치시키세요.

### 팁 3: "No music" 옵션
배경음악 없이 순수한 환경음만 원한다면 `[Audio: natural ambiance only, no music]` 처럼 명시하세요.

Veo 3의 오디오 기능은 이 책에서 가장 중요하게 다루는 기능입니다. PART 8에서 오디오 전반을 더 심층적으로 다루니 꼭 확인하세요.
