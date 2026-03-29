# 프롬프트란 무엇인가

> **당신이 쓰는 문장이 감독의 지시서, 배우의 대본, 편집자의 노트가 됩니다**

---

## 프롬프트의 정의

**프롬프트(Prompt)**는 AI에게 내리는 지시입니다. 텍스트 형태의 명령어이며, AI는 이 프롬프트를 읽고 해석하여 영상을 생성합니다.

단순히 "이런 영상 만들어줘"라는 요청이 아닙니다. 프롬프트는 영상의 모든 요소 — 장면, 캐릭터, 카메라, 조명, 분위기, 소리 — 를 텍스트로 표현하는 완전한 창작 지시서입니다.

---

## 프롬프트의 4가지 역할

### 역할 1: 감독의 지시서

영화 감독은 배우와 스태프에게 "이 장면에서 카메라는 여기서 출발해서 천천히 피사체에 가까이 다가가면서…"라고 지시합니다. 프롬프트가 바로 이 감독의 지시입니다.

```
프롬프트 예시:
"Start with a wide aerial shot of the city at night,
slowly descend and zoom toward one lit window,
the movement should feel like a bird gliding silently..."
```

### 역할 2: 촬영 감독의 카메라 지시

어떤 카메라 앵글, 어떤 렌즈, 어떤 움직임을 사용할지 지정합니다.

```
"Close-up, shallow depth of field,
slow dolly forward toward the character's face..."
```

### 역할 3: 배우의 대본

캐릭터가 무엇을 하고, 어떤 표정을 짓고, 어떤 대사를 말하는지를 정의합니다.

```
"The detective leans back in the chair, looking exhausted,
rubs her temples, sighs deeply..."
```

### 역할 4: 편집자의 노트

전반적인 분위기, 색조, 페이스를 지시합니다.

```
"Slow and deliberate pacing, warm nostalgic color grade,
soft film grain, contemplative mood..."
```

---

## 왜 프롬프트가 중요한가

Veo 3는 놀랍도록 강력하지만, AI는 여러분의 마음을 읽을 수 없습니다. 여러분이 프롬프트에 쓴 것만 알 수 있습니다.

**실험:**

프롬프트 A:
```
A warrior
```

프롬프트 B:
```
A battle-hardened female warrior in her 30s,
scarred bronze armor, dark braided hair blowing in the wind,
stands alone on a cliff edge overlooking a burning city,
low angle shot from below, dramatic backlight from the flames,
epic fantasy style, sorrowful yet resolute expression.
```

두 프롬프트 모두 "전사"를 요청하지만, 결과물은 천지차이입니다.

프롬프트 A는 AI가 알아서 결정하기 때문에 예측 불가한 결과가 나옵니다. 프롬프트 B는 여러분이 원하는 정확한 장면을 전달합니다.

---

## 프롬프트와 결과물의 관계

```
프롬프트의 구체성 ∝ 결과물의 품질

모호한 프롬프트 → 평범하거나 예측 불가한 결과
구체적인 프롬프트 → 원하는 결과에 가까운 영상
```

단, "구체적"이 "길다"는 의미는 아닙니다. 200단어의 길고 혼란스러운 프롬프트보다 50단어의 명확하고 집중된 프롬프트가 더 좋은 결과를 냅니다.

---

## 좋은 프롬프트의 3요소

### 요소 1: 명확성 (Clarity)
- 무엇을 원하는지 명확하게 표현
- 모호한 단어 피하기 (예: "좋은" → "따뜻한 황금빛 색감의")
- 한 문장에 여러 모순된 지시 넣지 않기

### 요소 2: 구체성 (Specificity)
- 일반적인 설명 대신 구체적 세부사항
- "나무" 대신 "안개 속 고대 소나무"
- "여자" 대신 "30대 초반 붉은 머리 여성 탐정"

### 요소 3: 우선순위 (Priority)
- 가장 중요한 요소를 프롬프트 앞에 배치
- AI는 프롬프트 앞부분을 더 크게 반영하는 경향
- 핵심이 아닌 부가 설명은 뒤에

---

## 프롬프트 작성 마인드셋

프롬프트를 쓸 때 이렇게 생각해보세요.

**"나는 지금 AI라는 재능 있는 영상 제작팀에게 장면 지시를 내리고 있다. 그들은 영어를 완벽하게 이해하고 모든 영화 기법을 알지만, 내가 원하는 것을 직접 볼 수 없다. 그러므로 내가 상상하는 장면을 최대한 생생하게 언어로 그려야 한다."**

이 마인드셋으로 프롬프트를 쓰면, 자연스럽게 더 구체적이고 효과적인 프롬프트가 나옵니다.

---

## 첫 프롬프트 자체 진단

지금 머릿속에 만들고 싶은 장면이 있다면, 다음 질문에 답해보세요.

1. 주인공은 누구/무엇인가? (나이, 외모, 복장)
2. 무엇을 하고 있는가? (행동, 표정)
3. 어디에 있는가? (장소, 날씨, 시간)
4. 카메라는 어디에 있는가? (각도, 거리)
5. 조명은 어떤가? (자연광, 인공광, 색감)
6. 전반적인 분위기는? (감정, 장르)
7. 소리는 무엇이 들리는가? (대화, 자연음, 음악)

이 7가지 질문에 답하면 좋은 프롬프트의 뼈대가 만들어집니다. 이것이 PART 7에서 배울 8요소 공식의 기반입니다.
