# 59. JSON 프롬프트란 무엇인가

## 일반 프롬프트의 한계

VEO 3를 처음 배울 때 우리는 자연어 프롬프트를 사용합니다. 이것은 직관적이고 빠르지만, 복잡한 요구 사항이 생길 때 한계를 드러냅니다.

### 일반 프롬프트의 문제점

**문제 1: 우선순위 불명확**
"A luxury perfume bottle with dramatic lighting and golden particles and smoke effects and a dark background with silk fabric"처럼 요소를 나열하면, VEO 3가 어떤 것에 집중해야 할지 스스로 결정합니다. 때로는 중요한 요소가 묻혀버립니다.

**문제 2: 수정 어려움**
클라이언트가 "조명은 유지하고 배경만 바꿔주세요"라고 할 때, 자연어 프롬프트에서는 전체 문장을 다시 써야 합니다.

**문제 3: 일관성 유지 곤란**
같은 제품으로 여러 버전을 만들 때, 매번 같은 내용을 다시 작성해야 하고 실수가 생기기 쉽습니다.

**문제 4: 팀 협업 어려움**
팀원들이 각자 다른 방식으로 프롬프트를 작성하면 결과물의 품질이 일정하지 않습니다.

---

## JSON이 해결하는 문제

JSON 프롬프트는 각 요소를 **키(key)**와 **값(value)** 쌍으로 분리해서 작성합니다. 이렇게 하면:

- 각 요소가 명확하게 독립되어 있어 VEO 3가 혼동하지 않음
- 특정 필드만 수정하면 되어 수정이 쉬움
- 같은 구조에 내용만 바꿔 여러 버전 제작 가능
- 팀원 누구나 구조를 이해하고 활용 가능

---

## 일반 프롬프트 vs JSON 프롬프트 비교

**일반 프롬프트 예시:**
```
A dark luxury energy drink can with glowing blue neon accents floats in mid-air surrounded by electric sparks and lightning bolts against a dark stormy background with dramatic theatrical lighting and a sense of extreme power and energy
```

**JSON 프롬프트 예시:**
```json
{
  "product_name": "Blaze Energy",
  "product_type": "energy drink can",
  "style": "dark luxury, extreme sports aesthetic",
  "camera": "slow orbit around product, close-up detail shots",
  "lighting": "dramatic underlighting, electric blue neon rim light",
  "location": "dark void background",
  "atmosphere": "powerful, electric, intense",
  "elements": ["lightning bolts", "electric sparks", "floating particles"],
  "motion": "can slowly rotating, sparks orbiting",
  "color_palette": "electric blue, deep black, silver chrome"
}
```

| 비교 항목 | 일반 프롬프트 | JSON 프롬프트 |
|-----------|-------------|--------------|
| 작성 속도 | 빠름 | 조금 느림 |
| 요소 제어 | 간접적 | 직접적 |
| 수정 용이성 | 전체 재작성 필요 | 특정 필드만 수정 |
| 팀 협업 | 어려움 | 쉬움 |
| 일관성 유지 | 어려움 | 쉬움 |
| 적합한 상황 | 빠른 실험 | 전문 광고, 반복 제작 |

---

## 언제 JSON을 써야 하는가?

**JSON 프롬프트를 사용해야 하는 경우:**
- 클라이언트에게 납품하는 브랜드/제품 광고
- 같은 제품의 10개 이상 버전 제작
- 팀원과 협업할 때
- 정확한 스타일 가이드를 따라야 할 때
- 나중에 재사용할 템플릿을 만들 때

**일반 프롬프트로 충분한 경우:**
- 빠른 아이디어 테스트
- 개인 창작 프로젝트
- 한 번만 쓸 클립
- 즉흥적인 영상 실험

---

## JSON 프롬프트의 3가지 장점

### 장점 1: 정밀한 제어
각 요소가 독립적인 필드로 분리되어 있어 VEO 3가 각각을 독립적으로 처리합니다. "style"을 바꾼다고 "lighting"이 영향받지 않습니다.

### 장점 2: 재사용성
한 번 만든 JSON 템플릿은 필드 값만 바꿔서 무한히 재활용할 수 있습니다. Blaze Energy 템플릿에서 `product_name`만 바꾸면 다른 음료 광고가 됩니다.

### 장점 3: 전문성
클라이언트에게 JSON 프롬프트를 보여주면 작업에 대한 신뢰감과 전문성을 전달할 수 있습니다. "이런 구조로 제어합니다"라고 설명할 수 있어 소통이 원활해집니다.

---

## JSON의 기본 문법

JSON은 중괄호 `{}` 안에 `"키": "값"` 쌍을 쉼표로 구분해서 작성합니다:

```json
{
  "키1": "값1",
  "키2": "값2",
  "키3": ["목록값1", "목록값2"]
}
```

- 키는 항상 큰따옴표 `"` 로 감쌉니다
- 값이 여러 개일 때는 대괄호 `[]`와 쉼표를 사용합니다
- 마지막 항목 뒤에는 쉼표를 넣지 않습니다

이게 전부입니다. 다음 챕터에서 실제 VEO 3 프롬프트에 사용하는 각 키를 하나씩 살펴보겠습니다.
