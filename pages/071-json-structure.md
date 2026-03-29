# 60. JSON 구조 상세 해설

## JSON 프롬프트의 전체 구조

VEO 3 제품 광고용 JSON 프롬프트는 다음 키들로 구성됩니다. 모든 키를 다 쓸 필요는 없지만, 각각의 역할을 이해하면 필요에 따라 선택적으로 사용할 수 있습니다.

```json
{
  "product_name": "",
  "product_type": "",
  "description": "",
  "brand_style": "",
  "style": "",
  "camera": "",
  "lighting": "",
  "location": "",
  "time_of_day": "",
  "atmosphere": "",
  "elements": [],
  "motion": "",
  "cta_motion": "",
  "ending": "",
  "text": "",
  "keywords": []
}
```

---

## 각 키(Key) 상세 설명

### `product_name`
**역할**: 제품의 이름을 명시합니다.

VEO 3가 영상 전반에 걸쳐 이 제품을 주인공으로 인식하게 합니다.

```json
"product_name": "Blaze Energy"
```

---

### `product_type`
**역할**: 제품의 카테고리와 형태를 설명합니다.

이름만으로는 VEO 3가 형태를 알 수 없습니다. 캔인지, 병인지, 박스인지 명시하세요.

```json
"product_type": "slim aluminum energy drink can, 250ml"
```

---

### `description`
**역할**: 제품의 시각적 외형을 상세하게 묘사합니다.

색상, 로고 위치, 특별한 질감이나 마감 처리를 여기서 설명합니다.

```json
"description": "matte black can with electric blue lightning bolt logo on the front, metallic silver top, slight holographic sheen on the lower half"
```

---

### `brand_style`
**역할**: 브랜드의 전반적인 성격과 포지셔닝을 설명합니다.

이 필드가 영상 전체의 무드와 톤을 결정합니다. 명품인지, 대중적인지, 스포티한지, 미니멀한지를 정의하세요.

```json
"brand_style": "premium dark luxury, extreme sports crossover, targeting 18-30 male demographic"
```

---

### `style`
**역할**: 영상의 시각적 스타일과 레퍼런스를 지정합니다.

영화 레퍼런스, 장르, 시각적 미학을 지정할 수 있습니다.

```json
"style": "cinematic dark commercial, similar to Monster Energy or Rockstar's high-end ads, dark and powerful aesthetic"
```

---

### `camera`
**역할**: 카메라의 움직임과 앵글, 렌즈 특성을 지정합니다.

```json
"camera": "slow 360-degree orbit around the can, starts from ground level tracking up, ends with close-up on logo, shallow depth of field"
```

카메라 키워드 예시:
- `slow orbit` — 느린 주위 회전
- `dramatic low angle` — 제품을 아래에서 올려보는 각도
- `extreme close-up macro` — 표면 질감까지 보이는 클로즈업
- `pull back reveal` — 줌아웃으로 전체 모습 공개

---

### `lighting`
**역할**: 조명의 방향, 강도, 색상, 특수 효과를 지정합니다.

제품 광고에서 조명은 가장 중요한 요소입니다.

```json
"lighting": "primary light from below creating dramatic uplighting, electric blue rim light on right side, deep shadows on left, occasional lightning flash from background"
```

조명 키워드 예시:
- `rim lighting` — 제품 테두리를 강조하는 역광
- `dramatic uplighting` — 아래에서 위로 비추는 극적 조명
- `soft diffused light` — 부드럽게 퍼지는 빛 (명품 제품에 적합)
- `single spotlight` — 하나의 강한 스포트라이트

---

### `location`
**역할**: 제품이 놓인 환경과 배경을 설명합니다.

```json
"location": "floating in dark void, with subtle abstract electrical storm in the background"
```

자주 쓰이는 배경:
- `dark void` — 어두운 무한 배경 (집중도 높음)
- `marble surface` — 대리석 표면 (명품 느낌)
- `natural environment` — 자연 배경 (친환경 브랜드)
- `floating in mid-air` — 공중에 떠있는 효과

---

### `time_of_day`
**역할**: 시간대와 이에 따른 자연광 조건을 설정합니다.

```json
"time_of_day": "night, with artificial light sources only"
```

---

### `atmosphere`
**역할**: 영상이 전달해야 할 감정과 분위기를 정의합니다.

```json
"atmosphere": "powerful, intense, electrifying, like the moment before a race starts"
```

---

### `elements`
**역할**: 화면에 포함될 추가적인 시각 요소들을 목록으로 나열합니다.

```json
"elements": [
  "electric sparks",
  "floating ice crystals",
  "neon light reflections",
  "particle effects orbiting the can"
]
```

---

### `motion`
**역할**: 제품과 주변 요소들의 움직임을 설명합니다.

```json
"motion": "can slowly rotates on its vertical axis, sparks orbit around it, occasional burst of particles from the top"
```

---

### `cta_motion`
**역할**: CTA(Call to Action) 단계의 움직임입니다. 광고 후반부에 제품을 강조하는 동작.

```json
"cta_motion": "can moves to center frame, camera pushes in slowly to logo close-up, energy particles converge on the can"
```

---

### `ending`
**역할**: 영상이 어떻게 끝나는지를 지정합니다.

```json
"ending": "freeze frame on close-up of logo with electric glow, fade to black"
```

---

### `text`
**역할**: 화면에 표시될 텍스트가 있다면 여기 지정합니다. (VEO 3의 텍스트 렌더링은 아직 실험적입니다)

```json
"text": "IGNITE YOUR LIMITS"
```

---

### `keywords`
**역할**: 전체 영상의 품질과 스타일을 강화하는 추가 키워드 목록입니다.

```json
"keywords": [
  "8K quality",
  "photorealistic",
  "cinematic color grade",
  "professional commercial production",
  "no humans"
]
```

---

## 핵심 원칙

**필드를 많이 쓸수록 좋다**: 각 필드는 VEO 3에게 추가적인 컨텍스트를 제공합니다. 빈 필드는 VEO 3가 임의로 채웁니다.

**구체적으로 쓸수록 좋다**: "good lighting"보다 "single overhead softbox creating warm golden shadows on the bottle"이 훨씬 낫습니다.

**모순을 피하라**: `style: "minimalist"`와 `elements: ["explosions", "lightning", "particles"]`는 충돌합니다.
