# PART 11. JSON 프롬프트 고급 기법

## 이 파트에서 배울 것

지금까지 우리는 자연어로 프롬프트를 작성해왔습니다. "A man walks down a rainy street at night..." 형식의 자유로운 문장 프롬프트는 빠르고 직관적입니다. 하지만 전문적인 제품 광고나 브랜드 영상을 만들 때는 훨씬 더 정밀한 제어가 필요합니다.

이 파트에서는 **JSON 형식의 구조화된 프롬프트**를 사용해 VEO 3를 더욱 정밀하게 제어하는 방법을 배웁니다.

---

## JSON 프롬프트란?

JSON(JavaScript Object Notation)은 데이터를 구조화된 형식으로 표현하는 방법입니다. 프로그래밍에서 많이 쓰이지만, VEO 3 프롬프트에도 효과적으로 활용할 수 있습니다.

일반 프롬프트:
```
A luxury perfume bottle sits on a dark velvet surface with dramatic lighting and smoke effects
```

JSON 프롬프트:
```json
{
  "product_name": "Noir Bloom",
  "product_type": "luxury perfume",
  "style": "cinematic dark luxury",
  "lighting": "dramatic single source, rim lighting",
  "location": "dark velvet surface",
  "atmosphere": "mysterious, sensual",
  "elements": ["smoke effects", "rose petals", "crystal reflections"]
}
```

두 번째 방식이 훨씬 명확하고 각 요소를 독립적으로 제어할 수 있습니다.

---

## 왜 JSON 프롬프트가 고급 기법인가?

일반 텍스트 프롬프트는 VEO 3가 각 요소의 **우선순위**를 스스로 결정합니다. 때로는 우리가 원하는 부분이 무시되거나 다른 요소와 충돌이 생깁니다.

JSON 프롬프트는 각 요소를 **독립적인 필드**로 분리해서 명확하게 지시합니다. 마치 레스토랑에서 "아무거나 건강한 거 주세요"와 "닭가슴살 100g, 현미밥, 샐러드 드레싱은 발사믹으로"의 차이입니다.

### JSON이 특히 유용한 상황

- **제품 광고**: 정확한 제품 배치, 조명, 브랜드 무드 제어
- **반복 생산**: 같은 제품의 다양한 버전을 만들 때 필드만 변경
- **클라이언트 작업**: 수정 요청이 왔을 때 특정 필드만 수정하면 됨
- **팀 협업**: 팀원들이 각 필드의 역할을 쉽게 이해

---

## PART 11 챕터 구성

| 챕터 | 제목 | 핵심 내용 |
|------|------|-----------|
| 60 | JSON 프롬프트란 무엇인가 | 개념, 장점, 활용 시기 |
| 61 | JSON 구조 상세 해설 | 각 필드(키)의 의미와 사용법 |
| 62 | 인물 없는 제품 광고 JSON 템플릿 | 완전한 템플릿 코드블록 |
| 63 | 실전 예시 1 — Blaze Energy 드링크 | 에너지 드링크 광고 완성 예시 |
| 64 | 실전 예시 2 — Noir Bloom 향수 | 향수 광고 완성 예시 |
| 65 | 나만의 JSON 템플릿 만들기 | ChatGPT/Claude 활용, 커스터마이징 |

---

## 이 파트를 배우기 전에

JSON 프롬프트는 **프로그래밍 지식 없이도** 사용할 수 있습니다. 기본 구조만 이해하면 누구나 바로 활용할 수 있습니다. 코드처럼 보이지만, 실제로는 단순한 텍스트 형식입니다.

준비되셨나요? 다음 챕터에서 JSON의 기초부터 차근차근 배워봅시다.
