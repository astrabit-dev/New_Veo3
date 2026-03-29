# 65. TikTok / YouTube Shorts 최적화

## TikTok과 YouTube Shorts의 공통점

TikTok과 YouTube Shorts는 사실상 동일한 소비 방식을 가지고 있습니다:
- 세로형 9:16 화면
- 스와이프로 다음 영상으로 이동
- 앱이 알아서 추천 (발견성이 핵심)
- 첫 1-3초 안에 흥미를 잡지 못하면 스킵

이 두 플랫폼에서의 성공 공식은 **빠른 훅 + 완주율 극대화**입니다.

---

## 9:16 세로형 비율 설정법

VEO 3 (Google Flow)에서 영상을 생성할 때:

1. 생성 옵션에서 **세로형 (Portrait/Vertical)** 선택
2. 또는 프롬프트에 명시: `"vertical 9:16 format, portrait orientation"`

### 세로형 프롬프트 작성 시 주의사항

세로형은 가로형과 **구도가 달라야** 합니다:

```
가로형 구도: 주제가 화면 중앙에 배치, 좌우 공간 활용
세로형 구도: 주제가 상단 또는 하단에 배치, 위아래 공간 활용
```

세로형 프롬프트에서 추가할 키워드:
- `vertical composition, subject fills the frame from top to bottom`
- `portrait orientation, strong vertical movement`
- `close-up favoring vertical space`

---

## 8초 안에 훅 만드는 공식

TikTok 알고리즘은 **완주율**을 가장 중요하게 봅니다. 8초짜리 영상을 끝까지 보게 만들려면 처음 1-2초에 강렬한 훅이 필요합니다.

### 훅의 5가지 유형

| 훅 유형 | 방법 | 예시 프롬프트 키워드 |
|---------|------|-------------------|
| 비주얼 서프라이즈 | 황당하거나 예상치 못한 장면 시작 | "opens with Bigfoot holding a camera" |
| 움직임 훅 | 빠르거나 강렬한 첫 동작 | "starts with explosion, then..." |
| 클리프행어 | 결과부터 보여주기 | "crystal fractures in slow motion, then..." |
| 질문 유도 | "이게 뭐지?" 하는 궁금증 | "extremely close shot of unknown object" |
| 감각적 자극 | ASMR 소리나 시각 | "giant knife enters frame from above" |

---

## 트렌드 활용법

TikTok은 트렌드의 플랫폼입니다. 현재 인기 있는 오디오, 포맷, 챌린지를 VEO 3 영상에 접목하는 전략:

**사운드 트렌드 활용**: VEO 3로 영상 생성 후 TikTok에서 트렌드 오디오를 덧입히기
- 프롬프트에서는 `"no music, ambient sound only"` 설정
- TikTok 편집에서 트렌드 오디오 추가

**포맷 트렌드 활용**: 현재 유행하는 영상 스타일 참조
- POV 포맷이 유행 → POV 프롬프트 (챕터 54 참조)
- Day-in-life 포맷 → 빅풋 브이로그 (챕터 51 참조)
- "Is this real?" 포맷 → 다큐 스타일 (챕터 56 참조)

---

## 해시태그 전략

TikTok 해시태그는 **발견성**을 높입니다:

**조합 공식:**
- 대형 태그 1-2개 (100M+ 뷰): `#fyp`, `#viral`, `#asmr`
- 중형 태그 2-3개 (1M-100M): `#aiart`, `#veo3`, `#shortfilm`
- 소형 태그 2-3개 (100K 이하): 특정 주제 태그 `#crystalasmr`, `#bigfootvlog`

---

## 최적화된 프롬프트 예시: TikTok용

### 예시: 틱톡 바이럴 ASMR 세로형 영상

```
Vertical 9:16 format. Extreme close-up macro shot of a giant perfect sphere made of crystallized ocean water — deep blue at the core shifting to transparent ice blue at the edges — sitting on a clean white surface. From the top of frame, a large silver kitchen knife descends slowly and deliberately. The knife begins to cut through the crystal sphere from the top — the cutting creates an incredibly satisfying crackling and crystalline shattering sound, like thousands of tiny bells breaking at once. As the sphere splits in half, the interior reveals a miniature ocean scene — tiny waves, bioluminescent plankton, deep blue gradient. The two halves slowly separate to reveal the interior. Extreme macro detail, every crack and facet visible. Audio: the crystalline cut sound is the entire audio focus — sharp, satisfying, layered. No music. No voice. Bright clean studio lighting, pure white background. Hyper-real, 8K, made for vertical viewing, total runtime 8 seconds.
```

---

## Shorts vs TikTok 미묘한 차이

| 요소 | TikTok | YouTube Shorts |
|------|--------|----------------|
| 알고리즘 | 팔로워 없어도 바이럴 가능 | 기존 채널 시청자 우선 |
| 성장 속도 | 빠름 | 상대적으로 느림 |
| 수익화 | Creativity Program | YouTube Partner Program |
| 자막 | 앱 내 자동 자막 | 영상 내 자막 권장 |
| 연령대 | 젊은 층 (16-30) | 약간 더 넓은 층 |

**추천**: 같은 영상을 양쪽 모두에 업로드하세요. 각 플랫폼에서 서로 다른 알고리즘이 새로운 시청자에게 노출시킵니다. 업로드 시간 간격을 2-3일 두는 것이 좋습니다.
