# 61. 인물 없는 제품 광고 JSON 템플릿

## 왜 인물 없는 광고인가?

제품 광고에서 인물을 포함하면 AI가 생성하는 얼굴, 손, 움직임의 부자연스러움이 광고 품질을 저하시킬 수 있습니다. 반면 **인물 없는 제품 광고**는:

- VEO 3가 가장 잘 생성하는 유형
- 제품 자체에 집중해서 메시지가 명확
- 현실적인 저작권/초상권 이슈 없음
- 브랜드 아이덴티티를 직접 전달

많은 고급 향수, 음료, 시계, 자동차 광고가 인물 없이 제품만으로 강력한 영상을 만듭니다.

---

## 완전한 JSON 템플릿 코드블록

다음은 모든 종류의 제품 광고에 적용할 수 있는 기본 템플릿입니다. 대괄호 `[...]` 부분을 실제 내용으로 채우세요.

```json
{
  "product_name": "[제품명]",
  "product_type": "[제품 유형 및 형태]",
  "description": "[제품의 시각적 외형 묘사: 색상, 재질, 로고, 크기]",
  "brand_style": "[브랜드 포지셔닝: 명품/대중적/스포티/친환경 등]",
  "style": "[영상 스타일: cinematic dark / bright minimal / natural organic 등]",
  "camera": "[카메라 움직임: orbit / push in / low angle tracking 등]",
  "lighting": "[조명 설정: 방향, 색상, 강도, 특수 효과]",
  "location": "[배경: dark void / marble surface / natural environment 등]",
  "time_of_day": "[시간대: night / golden hour / midday 등]",
  "atmosphere": "[분위기: powerful / elegant / fresh / mysterious 등]",
  "elements": [
    "[추가 시각 요소 1]",
    "[추가 시각 요소 2]",
    "[추가 시각 요소 3]"
  ],
  "motion": "[제품 및 주변 요소의 움직임]",
  "cta_motion": "[광고 후반 클라이맥스 움직임]",
  "ending": "[영상 마무리 방식]",
  "text": "[화면 텍스트 (선택 사항)]",
  "keywords": [
    "no humans",
    "product hero shot",
    "photorealistic",
    "8K quality",
    "professional commercial"
  ]
}
```

---

## 각 필드 작성 가이드

### `description` 필드 — 가장 중요

제품의 외형을 사람이 눈으로 보는 것처럼 상세하게 묘사하세요:

```json
"description": "slim 250ml aluminum can, matte midnight black finish with subtle texture, large silver lightning bolt logo centered on front, thin neon blue stripe running around the middle, silver pull-tab on top"
```

작성 순서: **전체 형태 → 색상/재질 → 로고 위치 → 특별한 디테일**

---

### `camera` 필드 — 광고의 역동성 결정

| 카메라 움직임 | 효과 | 적합한 제품 |
|-------------|------|------------|
| `slow 360 orbit` | 제품 전체 공개, 고급감 | 향수, 시계, 명품 |
| `dramatic low angle push in` | 강력함, 위압감 | 에너지 드링크, 스포츠 브랜드 |
| `macro detail sweep` | 질감과 장인정신 강조 | 고급 식품, 화장품 |
| `pull back reveal` | 서프라이즈, 규모 공개 | 자동차, 전자제품 |
| `floating overhead drone shot` | 자연스럽고 현대적 | 건강식품, 음료 |

---

### `elements` 필드 — 브랜드 세계관 구축

제품 카테고리별 추천 elements:

**에너지/스포츠 음료:**
```json
"elements": ["electric sparks", "lightning effects", "speed lines", "particle burst", "neon glow"]
```

**향수/뷰티:**
```json
"elements": ["silk fabric draped around bottle", "rose petals floating", "gold dust particles", "smoke wisps", "crystal reflections"]
```

**건강/자연 음료:**
```json
"elements": ["fresh water splashes", "citrus slices", "green leaves", "morning dew drops", "natural sunlight bokeh"]
```

**고급 주류:**
```json
"elements": ["amber liquid pour", "ice cubes", "condensation droplets", "oak barrel texture in background", "moody candlelight"]
```

---

## 어떤 제품에 사용할 수 있는가?

이 템플릿은 **모든 소비재 제품**에 적용 가능합니다:

| 제품 카테고리 | 예시 | 주요 수정 필드 |
|-------------|------|--------------|
| 음료 | 에너지 드링크, 물, 주스, 주류 | style, elements, motion |
| 뷰티/향수 | 향수, 립스틱, 크림, 세럼 | lighting, atmosphere, elements |
| 패션 | 신발, 가방, 시계, 선글라스 | location, style, camera |
| 식품 | 초콜릿, 커피, 건강식품 | elements, lighting, atmosphere |
| 전자제품 | 이어폰, 스마트워치, 스피커 | style, camera, elements |
| 자동차/차량 | 자동차, 바이크, 전기차 | location, camera, motion |

---

## 빠른 시작 체크리스트

템플릿을 작성하기 전에 다음을 먼저 정하세요:

- [ ] 제품의 주요 색상과 재질은 무엇인가?
- [ ] 이 광고를 보는 사람에게 어떤 감정을 주고 싶은가?
- [ ] 경쟁사의 광고와 어떻게 차별화할 것인가?
- [ ] 배경은 제품을 부각시킬 수 있는가?
- [ ] 8초 안에 핵심 메시지를 전달할 수 있는 움직임인가?
