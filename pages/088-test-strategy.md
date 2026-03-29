# 74. 프롬프트 초안 테스트 전략

## 테스트 없이 생성하면 생기는 일

처음 VEO 3를 사용하는 분들이 가장 흔히 하는 실수는 긴 프롬프트를 작성하고 바로 High Quality로 생성하는 것입니다. 결과가 마음에 들지 않으면? 다시 100크레딧. 조금 수정해서 또 생성? 다시 100크레딧. 이 사이클이 반복되면 크레딧이 순식간에 사라집니다.

테스트 전략은 이 사이클을 근본적으로 바꿉니다.

---

## Fast Mode 먼저 테스트하는 방법

### 3단계 테스트 프로세스

**1단계: 핵심만 담은 초안 테스트 (15크레딧)**
프롬프트의 핵심 요소만 포함한 짧은 버전으로 Fast Mode 테스트:

```
// 원본 (복잡한) 프롬프트
"A tall elderly wizard with silver hair and long beard, wearing deep navy robes with gold star embroidery, standing in the center of a vast underground cavern filled with glowing crystals, lightning crackling from his outstretched hands, dramatic chiaroscuro lighting, slow orbiting camera, epic orchestral music, 8K, cinematic"

// 핵심 초안 테스트용 프롬프트
"Elderly wizard with silver beard, casting lightning in a dark crystal cave. Dramatic."
```

이 테스트로 기본 장면 구성이 원하는 방향인지 확인합니다.

**2단계: 수정 요소 추가 테스트 (15크레딧)**
초안에서 문제를 발견했다면 해당 부분만 수정 후 다시 Fast Mode 테스트:

```
// 문제: 마법사가 너무 어려 보임 → 나이 강조
"An OLD elderly wizard, 80 years old, very long white beard, wrinkled face, silver hair, casting lightning in a dark cave"
```

**3단계: 완성 프롬프트 검증 (15크레딧)**
모든 요소를 포함한 최종 프롬프트를 Fast Mode로 한 번 더 테스트:

완성 프롬프트가 의도한 대로 표현되는지 확인. OK라면 High Quality 생성.

**총 테스트 비용: 45크레딧**
**High Quality 생성: 100크레딧**
**전체: 145크레딧 (vs 테스트 없이 300크레딧)**

---

## 프롬프트 반복 개선 사이클

```
[초안 프롬프트 작성]
         ↓
[Fast Mode 생성] → 15크레딧
         ↓
[결과 분석]
    ├── 캐릭터/형태가 맞는가?
    ├── 조명이 맞는가?
    ├── 카메라 앵글이 맞는가?
    ├── 분위기가 맞는가?
    └── 움직임이 맞는가?
         ↓
[문제 요소 식별 및 프롬프트 수정]
         ↓
[Fast Mode 재생성] → 15크레딧
         ↓
[결과 분석 반복]
         ↓
[모든 요소 만족] → [High Quality 최종 생성] → 100크레딧
```

---

## 10크레딧으로 1000크레딧 아끼는 법

### 방법 1: 프롬프트 핵심 요소 분리 테스트

복잡한 프롬프트에서 문제가 생겼을 때, 어떤 요소가 문제인지 파악하기 어렵습니다. 요소를 분리해서 각각 테스트하세요:

```
테스트 A: 캐릭터만
"elderly wizard in navy robes" [Fast Mode]

테스트 B: 환경만
"underground crystal cave with dramatic lighting" [Fast Mode]

테스트 C: 조합
"elderly wizard in crystal cave" [Fast Mode]

→ 원하는 결과가 나오면 나머지 세부 요소 추가
```

### 방법 2: 변형 버전 Fast Mode 비교

같은 프롬프트의 여러 변형을 Fast Mode로 비교한 후 최고 버전만 High Quality 생성:

```
버전 A: "dramatic underlighting" [Fast]
버전 B: "natural window light" [Fast]
버전 C: "candlelight" [Fast]
→ 가장 좋은 버전 선택 → High Quality
```

---

## 테스트 체크리스트

Fast Mode 결과를 평가할 때 확인할 항목들:

**구성 체크:**
- [ ] 원하는 캐릭터/대상이 화면에 있는가?
- [ ] 원하는 환경이 설정되었는가?
- [ ] 카메라 앵글이 의도한 대로인가?

**품질 체크:**
- [ ] 조명이 원하는 분위기를 만드는가?
- [ ] 색상 팔레트가 맞는가?
- [ ] 움직임이 자연스러운가?

**내용 체크:**
- [ ] 원하는 행동이나 장면이 표현되었는가?
- [ ] 원하지 않는 요소가 포함되어 있지 않은가?
- [ ] 전체적인 분위기가 목표와 일치하는가?

모든 체크가 완료되면 High Quality로 최종 생성합니다.

---

## 테스트 결과 기록하기

테스트를 통해 발견한 것들을 기록해두세요:

```
[프롬프트 테스트 노트]

프롬프트: "elderly wizard in crystal cave..."
테스트 날짜: 2026-01-15
테스트 횟수: 3회 (Fast Mode)
최종 고품질 생성: 1회

발견사항:
- "elderly"만으로는 충분히 나이들어 보이지 않음 → "80 years old, deeply wrinkled" 추가 필요
- "crystal cave"가 좋은 결과를 냄 → 유지
- 조명은 "dramatic underlighting" > "backlight" 선호
```

이런 노트가 쌓이면 나만의 프롬프트 패턴 라이브러리가 만들어집니다.
