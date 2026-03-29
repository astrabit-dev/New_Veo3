# 56. 다큐멘터리 스타일 템플릿

## 목표

다큐멘터리 스타일 영상은 **실제처럼 보이는 자연/도시 다큐멘터리**를 AI로 제작하는 템플릿입니다. BBC 자연 다큐멘터리나 National Geographic의 느낌을 VEO 3로 재현할 수 있습니다.

이 템플릿의 활용 사례:

- 실제로 촬영하기 어려운 야생동물 장면 (북극곰, 설표, 심해 생물)
- 여행 콘텐츠에서 B-roll로 사용
- 교육 콘텐츠의 시각 자료
- 자연 다큐 유튜브 채널 운영

### 공식

```
[핸드헬드/자연스러운 카메라] + [내레이션 스타일 대사 또는 자연음] + [아이레벨 촬영] + [자연 배경음] + [다큐 특유의 조명]
```

### 다큐 스타일의 핵심 특징

| 특징 | 일반 영화와의 차이 | 프롬프트 키워드 |
|------|------------------|----------------|
| 카메라 | 약간의 흔들림, 줌인/줌아웃 | "handheld, slight zoom", "natural camera movement" |
| 조명 | 인공 조명 없음, 자연광 | "natural lighting only", "overcast day" |
| 사운드 | 현장 소리 중심 | "ambient natural sound", "no music" |
| 편집 느낌 | 찾아낸 듯한 리얼함 | "documentary style", "raw footage feel" |

---

## 완성 예시 1: 야생 동물 다큐

### 시나리오
눈 덮인 산속에서 눈표범이 먹이를 사냥하기 위해 조심스럽게 이동하는 장면을 담은 자연 다큐멘터리 스타일의 영상입니다.

### 전체 프롬프트

```
Documentary-style footage of a snow leopard moving silently along a narrow rocky ridge in the Himalayan mountains in winter. The leopard is shot from a distance using a long telephoto lens — as if a wildlife camera crew is watching from a safe distance without disturbing the animal. The big cat moves with extraordinary grace and balance on a ledge barely wider than its paws, thick snow on the rocks below. Its breath creates small clouds in the frigid air. The camera follows its movement with gentle handheld adjustments, occasionally zooming in slightly to capture the detail of its spotted coat and pale green eyes. The leopard pauses, looks directly toward camera for one long moment — alert, assessing — then continues forward and disappears around a boulder. A calm, measured BBC-style narrator voice says softly: "After three weeks of tracking, we finally catch our first glimpse of the ghost of the mountains." Natural ambient sound only: wind across the mountain, distant eagle cry, the faint crunch of snow under the leopard's paws. Overcast natural lighting, cold blue-grey color palette, National Geographic quality.
```

### 왜 이 프롬프트가 효과적인가

- **"from a distance using a long telephoto lens"**: 다큐 특유의 관찰 카메라 설정
- **"without disturbing the animal"**: 야생 다큐의 윤리적 관찰 방식을 VEO 3에 전달
- **"looks directly toward camera for one long moment"**: 동물과 카메라 눈 맞춤의 극적 순간
- **BBC-style narrator**: 다큐 내레이션 스타일 지정
- **"cold blue-grey color palette"**: 히말라야의 차갑고 황량한 느낌을 색으로 설정

---

## 완성 예시 2: 도시 사람들 다큐

### 시나리오
서울의 새벽 시장에서 하루를 시작하는 상인들의 모습을 담은 인문 다큐멘터리 스타일의 영상입니다.

### 전체 프롬프트

```
Documentary-style footage at a bustling traditional Korean market at 4am as merchants set up for the day. Shot handheld, available light only — harsh fluorescent stall lights and the occasional glow of a phone screen in the pre-dawn darkness. An elderly woman in her 70s arranges fresh vegetables with practiced efficiency, her breath visible in the cold morning air. Nearby, a younger man unloads large cardboard boxes from a truck, moving quickly and quietly. The camera captures them from a respectful distance at eye level — observational style, not intrusive. Occasionally the subjects glance at the camera briefly, then return to their work naturally. The market gradually fills — more merchants arrive, lights flicker on, the hum of activity grows. A thoughtful narrator says quietly: "Every morning before the city wakes, the invisible labor begins." Sound design emphasizes the real ambiance: the slap of fish on ice, the rustling of packaging, whispered conversations, a radio playing old ballads softly in the background. No artificial lighting, no staged shots. Authentic, warm, respectful documentary filmmaking.
```

### 왜 이 프롬프트가 효과적인가

- **"available light only"**: 인공 조명을 배제한 다큐 특유의 현장감
- **"they glance at the camera briefly, then return naturally"**: 카메라를 의식하는 자연스러운 반응
- **"respectful distance at eye level"**: 인물 다큐의 윤리적 접근 방식
- **구체적인 소리 디테일**: "slap of fish on ice", "rustling of packaging"으로 청각 현실감 부여
- **"radio playing old ballads softly"**: 배경의 작은 디테일이 영상의 깊이를 더함

---

## 다큐 스타일 프롬프트 키워드 모음

**카메라 키워드:**
- `handheld documentary style` — 핸드헬드 다큐 스타일
- `telephoto lens observation` — 망원 렌즈 관찰
- `verité style` — 시네마 베리떼 (있는 그대로 포착)
- `observational filmmaking` — 관찰형 다큐 스타일

**조명 키워드:**
- `available light only` — 현장 자연광만 사용
- `overcast natural light` — 흐린 날의 자연광
- `golden hour` — 해뜰 때나 해질 때의 황금빛 빛

**소리 키워드:**
- `ambient natural sound` — 자연 환경음
- `no music, only ambient` — 음악 없이 현장음만
- `narrator voice-over` — 내레이션
- `diegetic sound only` — 화면 속 현장 소리만
