# AI 도구 스택 조합 가이드

> **Veo 3 단독보다 훨씬 강력한 — AI 도구들의 시너지**

---

## 왜 AI 스택이 필요한가

Veo 3는 텍스트→영상 변환에서 세계 최고 수준입니다. 하지만 전문 콘텐츠를 만들려면 Veo 3 혼자서는 부족한 부분이 있습니다.

| Veo 3가 약한 부분 | 해결해주는 도구 |
|-----------------|--------------|
| 스크립트·기획 작성 | ChatGPT / Gemini |
| 레퍼런스 이미지 생성 | Imagen 3 / Midjourney |
| 고품질 AI 보이스오버 | ElevenLabs / Typecast |
| 배경음악 생성 | Suno / Udio |
| 최종 편집·자막 | CapCut / DaVinci Resolve |

이 챕터에서는 다섯 가지 도구를 Veo 3와 조합하는 실전 워크플로우를 소개합니다.

---

## 전체 AI 스택 구조

```
[기획·스크립팅]          [이미지 생성]
ChatGPT / Gemini    →   Imagen 3 / Midjourney
        ↓                        ↓
   프롬프트 초안          레퍼런스 이미지
        └──────────────────────┘
                    ↓
              [Veo 3 / Google Flow]
              영상 클립 생성
                    ↓
        ┌───────────┴───────────┐
   [ElevenLabs]           [Suno / Udio]
   보이스오버·나레이션      배경음악 생성
        └───────────┬───────────┘
                    ↓
              [CapCut / DaVinci]
              편집·자막·색보정·내보내기
```

---

## 도구 1: ChatGPT / Gemini — 기획 및 스크립팅

### 역할

- 영상 기획안 및 스토리보드 작성
- Veo 3용 프롬프트 초안 생성
- 씬(Scene) 분해 및 클립 구성 설계

### 실전 활용 프롬프트 (ChatGPT / Gemini에 입력)

**영상 기획 요청:**
```
다음 조건으로 60초짜리 YouTube Shorts 시나리오를 작성해줘.

주제: 새벽 도심 편의점의 외로운 직장인
장르: 감성 다큐멘터리 스타일
클립 수: 7~8개 (각 8초)
분위기: 잔잔하고 쓸쓸하지만 따뜻한 여운

각 클립에 대해:
1. 장면 묘사
2. Veo 3 영어 프롬프트
3. 필요한 오디오
를 각각 작성해줘.
```

**프롬프트 품질 개선 요청:**
```
아래 Veo 3 프롬프트를 더 영화적으로 개선해줘.
카메라 앵글, 조명, 오디오 묘사를 보강하고,
[Avoid] 블록도 추가해줘.

[원본 프롬프트 붙여넣기]
```

---

## 도구 2: Imagen 3 / Midjourney — 레퍼런스 이미지

### 역할

- 캐릭터 외모를 시각적으로 고정
- 원하는 색감·분위기 레퍼런스 제공
- 배경·세트 디자인 참고 이미지 생성

### 워크플로우

```
1. Imagen 3(Google AI Studio) 또는 Midjourney에서 캐릭터 이미지 생성
2. 생성된 이미지를 Google Flow의 Reference Image로 업로드
3. Veo 3가 해당 이미지를 기준으로 영상 생성
```

### Imagen 3 사용법 (Google AI Studio)

```
접속: aistudio.google.com
메뉴: Image 생성 탭 선택
프롬프트 예시:

"Portrait of a 30-year-old Korean woman detective,
short black hair, sharp eyes, navy trench coat,
photorealistic, studio lighting, neutral expression,
front-facing portrait for character reference"
```

### 캐릭터 고정 효과

레퍼런스 이미지를 사용하면 캐릭터 일관성이 크게 향상됩니다.

| 방법 | 캐릭터 일관성 |
|------|------------|
| 텍스트 프롬프트만 | 클립마다 외모 편차 발생 |
| 텍스트 + 상세 묘사 반복 | 개선되지만 완벽하지 않음 |
| **레퍼런스 이미지 사용** | **가장 안정적인 일관성** |

---

## 도구 3: ElevenLabs — AI 보이스오버

### 역할

- 나레이션, 해설, 더빙 음성 생성
- Veo 3의 내장 대사보다 더 정교한 음성 제어
- 한국어·영어 고품질 TTS

### 언제 사용하나

Veo 3의 내장 오디오는 대화 장면에 강하지만, 다음 상황에서는 ElevenLabs가 더 효과적입니다:

- 다큐멘터리 스타일 나레이션
- 특정 감정·톤을 세밀하게 조정해야 할 때
- 동일 목소리로 여러 영상에 걸쳐 일관성이 필요할 때
- 실제 대본 낭독이 필요한 광고·교육 영상

### 기본 워크플로우

```
1. elevenlabs.io 접속 (무료 플랜: 월 10,000자)
2. Voice Library에서 적합한 목소리 선택 또는 Voice Cloning
3. 스크립트 입력 → 음성 파일(MP3) 다운로드
4. CapCut에서 Veo 3 영상 클립과 합성
5. 볼륨 밸런싱 조정
```

### 한국어 음성 추천 설정

```
Language: Korean
Style: Narrative (나레이션) / Conversational (대화)
Stability: 0.5~0.7 (너무 높으면 단조로움)
Clarity: 0.75~0.85
```

---

## 도구 4: Suno / Udio — AI 배경음악

### 역할

- 장면 분위기에 맞는 오리지널 배경음악 생성
- 저작권 문제 없는 BGM 확보
- Veo 3 내장 음악보다 더 긴 트랙(1~3분) 생성

### 언제 사용하나

- Veo 3가 생성한 배경음악의 길이나 반복이 맞지 않을 때
- 여러 클립을 이어붙인 영상 전체에 하나의 BGM을 깔 때
- 특정 장르(재즈, 오케스트라, 로파이 등)의 정교한 음악이 필요할 때

### Suno 사용법

```
접속: suno.com (무료 플랜: 일 5곡)
프롬프트 예시:

"melancholic lo-fi piano, slow tempo 70BPM,
rainy night city atmosphere, no vocals,
cinematic instrumental, 2 minutes"

"upbeat corporate background music,
clean and professional, no lyrics,
motivational tone, 90 seconds"
```

### Udio 사용법

```
접속: udio.com
Suno보다 더 복잡한 구조의 음악 생성에 강함
장르·악기 조합을 세밀하게 지정 가능
```

### BGM 합성 팁

```
CapCut에서 오디오 레이어 구성:
- Layer 1: Veo 3 원본 오디오 (환경음·대화)
- Layer 2: Suno/Udio 생성 BGM (볼륨 20~40%)
- Layer 3: ElevenLabs 나레이션 (볼륨 90~100%)

우선순위: 나레이션 > 원본 오디오 > BGM
```

---

## 도구 5: CapCut — 최종 편집

기본 편집 워크플로우는 부록 E에서 상세히 다루고 있습니다. 여기서는 AI 스택 조합 시 추가되는 작업에 집중합니다.

### AI 스택 사용 시 추가 작업

```
1. Veo 3 클립 임포트
2. ElevenLabs 나레이션 파일 임포트 → 타이밍 맞추기
3. Suno BGM 임포트 → 볼륨 밸런싱
4. 세 레이어 오디오 믹싱
5. 자막 추가 (CapCut 자동 자막 또는 수동)
6. 최종 내보내기
```

---

## 완성 워크플로우 — 실전 예시

**목표:** 60초 감성 다큐멘터리 YouTube Shorts

```
STEP 1 (ChatGPT, 10분)
→ 7개 씬 구성 및 Veo 3 프롬프트 7개 초안 작성

STEP 2 (Imagen 3, 5분)
→ 주인공 캐릭터 레퍼런스 이미지 2~3장 생성

STEP 3 (Google Flow, 30분)
→ 레퍼런스 이미지 업로드 후 Veo 3.1로 7개 클립 생성
→ Fast Mode로 먼저 테스트, 방향 확인 후 고품질로 최종 생성

STEP 4 (ElevenLabs, 10분)
→ 30초 나레이션 스크립트 작성 후 음성 생성

STEP 5 (Suno, 5분)
→ "melancholic piano lo-fi 60 seconds no vocals" 생성

STEP 6 (CapCut, 20분)
→ 클립 편집 + 오디오 3레이어 믹싱 + 자막 + 내보내기

총 소요 시간: 약 1시간 20분
```

---

## 도구별 무료 플랜 한계

| 도구 | 무료 제공 | 유료 기준 |
|------|---------|---------|
| ChatGPT | 무료 (GPT-4o 제한) | $20/월 |
| Gemini | 무료 (Gemini 1.5 Flash) | Google One AI 요금제 |
| Imagen 3 | Google AI Studio 무료 | 사용량 제한 있음 |
| Midjourney | 없음 (유료만) | $10/월~ |
| ElevenLabs | 월 10,000자 | $5/월~ |
| Suno | 일 5곡 | $8/월~ |
| Udio | 일 10곡 | $10/월~ |
| CapCut | 무료 (워터마크 없음) | 선택적 유료 |

> **초보자 추천 스택:** Gemini(무료) + Imagen 3(무료) + Veo 3 + Suno(무료) + CapCut(무료)
> 추가 비용 없이 전문적인 워크플로우 구성이 가능합니다.

---

## 요약

| 단계 | 도구 | 역할 |
|------|------|------|
| 기획·스크립팅 | ChatGPT / Gemini | 씬 구성, 프롬프트 초안 |
| 레퍼런스 이미지 | Imagen 3 / Midjourney | 캐릭터 외모 고정, 스타일 가이드 |
| 영상 생성 | Google Flow (Veo 3) | 핵심 클립 생성 |
| 보이스오버 | ElevenLabs | 나레이션, 정교한 음성 |
| 배경음악 | Suno / Udio | 오리지널 BGM, 저작권 해결 |
| 편집 | CapCut | 최종 합성, 자막, 내보내기 |
