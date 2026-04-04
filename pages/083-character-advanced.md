# 70. 캐릭터 일관성 고급 전략

## 왜 캐릭터 일관성이 어려운가?

VEO 3는 매번 영상을 새롭게 생성합니다. "같은 캐릭터"를 다시 요청해도, AI는 이전에 만든 캐릭터를 "기억"하지 않습니다. 따라서 클립마다 얼굴형이 조금씩 다르거나, 헤어스타일이 바뀌거나, 키가 달라지는 현상이 생깁니다.

이것은 **AI 영상 제작의 가장 큰 도전 중 하나**이며, 완벽하게 해결하기는 어렵습니다. 하지만 고급 전략을 사용하면 일관성을 크게 높일 수 있습니다.

---

## 전략 1: 상세 묘사 반복 (Character Card)

캐릭터의 외형을 극도로 상세하게 묘사한 **"캐릭터 카드"**를 만들고, 모든 클립 프롬프트의 앞부분에 동일하게 붙여 넣습니다.

### 좋은 캐릭터 카드 예시

```
[CHARACTER: ELENA]
A young woman, mid-20s, approximately 165cm tall, athletic but slender build. Her face has high cheekbones, a slightly pointed chin, dark olive skin, and large almond-shaped dark brown eyes with thick natural brows. Her hair is dark black with a slight natural wave, cut in a blunt bob that falls just below her chin, with face-framing pieces. She has a small horizontal scar above her left eyebrow. She is wearing a worn brown leather jacket over a white fitted t-shirt, dark indigo jeans, and weathered brown ankle boots. She carries a worn leather messenger bag on her right shoulder.
```

이 텍스트를 모든 클립 프롬프트 앞에 추가합니다:

```
[CHARACTER: ELENA] A young woman, mid-20s... (위 전체 내용)
... [씬 내용] Elena walks through a crowded market, looking at a map in her hand.
```

---

## 전략 2: 핵심 구별 특징 설정

캐릭터에 VEO 3가 쉽게 포착할 수 있는 **독특한 특징**을 부여하면 일관성이 높아집니다:

### 효과적인 구별 특징

| 특징 유형 | 예시 | 효과 |
|---------|------|------|
| 신체적 특징 | 왼쪽 눈썹 위 흉터, 눈에 띄는 점 | 매우 효과적 |
| 특이한 헤어 | 분홍색 끝 염색, 특이한 색상 | 효과적 |
| 고정 의상 | 항상 같은 빨간 스카프 | 효과적 |
| 특이한 아이템 | 특별한 모자, 안경, 문신 | 효과적 |
| 체형 극단 | 매우 키가 크고 마른, 매우 근육질 | 중간 정도 효과 |

```
// 일관성을 높이는 특징 예시
"a young man with a distinctive bright red mohawk haircut and a wolf tattoo on his right forearm, always wearing an oversized olive military jacket"
```

---

## 전략 3: 의상으로 캐릭터 고정

사람의 얼굴보다 **의상**이 훨씬 일관되게 생성됩니다. 캐릭터를 설정할 때 의상을 매우 구체적으로 묘사하면, 얼굴이 약간 달라도 같은 캐릭터로 인식됩니다.

```
// 좋은 의상 묘사 예시
"always wearing: a distinctive deep teal kimono-style jacket with gold dragon embroidery on the back, black fitted pants, white Converse high-tops, and a single pearl earring in the left ear"
```

---

## 전략 4: 참조 이미지 + Imagen 3 연계 (가장 강력)

텍스트 묘사만으로는 얼굴을 완전히 고정하기 어렵습니다. **이미지를 시각적 기준점으로 제공하는 것이 가장 강력한 일관성 전략**입니다.

### Imagen 3로 캐릭터 이미지 만들기

Google AI Studio의 Imagen 3를 사용하면 Veo 3와 같은 Google 생태계 안에서 레퍼런스 이미지를 만들 수 있습니다.

**Imagen 3 캐릭터 이미지 생성 프롬프트 구조:**

```
Portrait of [나이+성별], [외형 상세 묘사],
photorealistic, neutral expression, front-facing,
clean studio background, character reference sheet style,
[조명 설명], high detail face
```

**실전 예시:**
```
Portrait of a 32-year-old Korean woman detective,
short straight black hair with blunt bangs just above eyebrows,
sharp defined jawline, narrow dark brown eyes, fair skin,
small nose, thin lips, neutral serious expression,
wearing a dark navy collared shirt,
photorealistic, front-facing portrait,
soft even studio lighting, white background,
character reference photo style, high detail
```

### Google Flow에서 참조 이미지 사용하는 법

```
1. Google AI Studio (aistudio.google.com) 접속
2. Image 탭에서 위 프롬프트로 캐릭터 이미지 생성 (2~3장)
3. 가장 마음에 드는 이미지 다운로드
4. Google Flow 접속 → 새 프로젝트 생성
5. 영상 생성 패널에서 "참조 이미지(Reference Image)" 클릭
6. 다운로드한 캐릭터 이미지 업로드
7. 프롬프트 작성 시 "character matching the reference image" 포함
```

**참조 이미지 포함 프롬프트 구조:**
```
[Character matching the reference image],
[씬 설명 — 행동/배경/카메라/조명],
[오디오 if needed]
```

**실전 예시:**
```
Character matching the reference image,
walking confidently through a rain-soaked Seoul alley at night,
neon signs overhead, hands in coat pockets,
medium tracking shot from behind,
cinematic noir style, wet pavement reflections.
[Audio: rain, distant city sounds]
```

### 참조 이미지 효과 비교

| 방법 | 클립 간 얼굴 일치율 |
|------|-----------------|
| 텍스트 묘사만 | 40~60% |
| 텍스트 묘사 + 상세 반복 | 60~75% |
| **참조 이미지 사용** | **80~90%** |

### 같은 캐릭터 여러 각도 이미지 준비하기

더 높은 일관성을 위해 동일 캐릭터를 정면/측면/3/4 각도로 각각 생성해두고, 씬의 카메라 앵글에 맞는 이미지를 골라 업로드합니다.

```
참조 이미지 세트 권장 구성:
- 정면 초상 (Close-up, 직접 카메라 응시)
- 측면 초상 (Profile, 90도 각도)
- 3/4 각도 (Three-quarter, 자연스러운 포즈)
- 전신 이미지 (Full body, 의상 전체 확인용)
```

> **팁:** 같은 Imagen 3 프롬프트에 `"side profile view"`와 `"three-quarter view"`를 각각 사용하면 동일 인물의 다른 각도 이미지를 생성할 수 있습니다.

---

## 전략 5: 동일 프롬프트 재활용

성공한 클립의 프롬프트를 저장해두고, 다음 클립에서 캐릭터 묘사 부분을 그대로 복사해서 사용합니다. 새로 쓰지 않으면 미묘한 표현 차이가 생깁니다:

```
// 재활용 시스템 예시
[CHARACTER_BASE_PROMPT.txt 파일에 저장]
"Elena, a young woman in her mid-20s with olive skin, dark brown almond-shaped eyes, black chin-length bob hair, wearing a worn brown leather jacket over white t-shirt, indigo jeans, brown ankle boots, carrying a leather messenger bag"

// 클립 1 프롬프트
[Character base] + "Elena stands at a train station, looking at the departure board, slightly anxious"

// 클립 2 프롬프트
[Character base] + "Elena sits in a window seat on a train, watching the countryside pass by"
```

---

## 전략 6: 변화를 최소화하는 팁

| 상황 | 문제 | 해결책 |
|------|------|--------|
| 감정 변화 장면 | 표정이 바뀌면 얼굴 모양이 달라져 보임 | 클로즈업 대신 미디엄샷 활용 |
| 다른 조명 환경 | 조명이 바뀌면 피부색이 다르게 보임 | 같은 조명 조건 유지 |
| 격렬한 움직임 | 움직임 블러로 얼굴 디테일 손실 | 느린 움직임 선호 |
| 극단적 각도 | 정면/측면/후면이 다른 사람처럼 보일 수 있음 | 비슷한 앵글 유지 |

---

## 현실적인 기대치

VEO 3 (2026년 기준)에서 완벽한 캐릭터 일관성을 기대하는 것은 아직 어렵습니다. 현실적인 목표는:

- **같은 캐릭터임이 "충분히" 인식될 수 있는 수준**
- 의상, 헤어, 특이한 특징이 일치한다면 시청자는 같은 캐릭터로 인식
- 얼굴 클로즈업이 없는 씬에서는 거의 완벽한 일관성 가능

기술이 계속 발전하고 있어, 향후 버전에서는 캐릭터 잠금(Character Lock) 기능이 더 정교해질 것으로 예상됩니다.
