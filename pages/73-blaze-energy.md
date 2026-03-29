# 62. 실전 예시 1 — Blaze Energy 에너지 드링크

## Blaze Energy 브랜드 컨셉

Blaze Energy는 **극한 스포츠와 게이밍**을 타깃으로 하는 가상의 에너지 드링크 브랜드입니다. 이 광고의 목표:

- 타깃: 18-30세 남성, 스포츠/게이밍 관심층
- 무드: 어둡고 강력한, 전기적 에너지
- 메시지: "한계를 불태워라 (Ignite Your Limits)"
- 플랫폼: YouTube 프리롤 광고, Instagram Reels

---

## 완전한 JSON 프롬프트

```json
{
  "product_name": "Blaze Energy",
  "product_type": "slim aluminum energy drink can, 250ml",
  "description": "matte black aluminum can with deep texture finish, large electric blue lightning bolt logo centered on the front face, thin neon blue LED-style stripe running horizontally around the middle of the can, metallic silver pull-tab and rim at top, 'BLAZE ENERGY' text in bold condensed font below the lightning bolt, slightly reflective chrome at the very bottom",
  "brand_style": "dark luxury extreme sports, targeting 18-30 male demographic, Monster Energy meets high-end Apple aesthetic",
  "style": "cinematic dark commercial, dramatic and powerful, similar to high-production energy drink advertisements",
  "camera": "starts with extreme close-up of the lightning bolt logo filling the entire frame, then slowly pulls back in a low angle arc to reveal the full can floating in space, followed by a slow 360-degree orbit, ending with a push-in back to the logo",
  "lighting": "primary dramatic uplighting from directly below the can creating intense shadows upward, electric blue rim light on the right edge, deep black void behind, occasional burst of blue-white lightning illuminating the entire frame for a split second, subtle reflection on the can's chrome base",
  "location": "floating in a dark void, absolute black background, with abstract dark storm clouds barely visible deep in the background",
  "time_of_day": "timeless — no natural light, artificial and electric only",
  "atmosphere": "intense, electrifying, powerful, like the moment of ignition before a rocket launch or the moment before an athlete breaks a world record",
  "elements": [
    "electric blue lightning arcs shooting outward from the can",
    "small metallic particles orbiting the can like electrons around an atom",
    "occasional full-frame lightning flash",
    "subtle smoke wisps at the base of the can",
    "neon blue reflective surface below the floating can"
  ],
  "motion": "can rotates very slowly on its vertical axis — one full rotation over 8 seconds — while lightning arcs pulse rhythmically in sync with an unheard bass beat, particles orbit in elliptical paths",
  "cta_motion": "rotation slows to a stop with the logo perfectly centered toward camera, all lightning converges inward to the logo in one final burst, the logo glows intensely blue for 2 seconds",
  "ending": "hard cut to black with the afterimage of the blue lightning bolt burned into the darkness for a brief moment, then fade",
  "text": "IGNITE YOUR LIMITS",
  "keywords": [
    "no humans",
    "product hero shot",
    "photorealistic 8K",
    "professional commercial quality",
    "cinematic color grade — deep blacks and electric blues",
    "dramatic lighting",
    "no music described but electric tension in the visuals"
  ]
}
```

---

## 각 필드 선택 이유

### `description` — 구체적인 외형 묘사
단순히 "검은 캔"이 아니라 재질(matte black), 질감(deep texture finish), 로고 특성(electric blue lightning bolt), 폰트 스타일(bold condensed font)까지 구체적으로 명시했습니다. 이렇게 하면 VEO 3가 캔의 외형을 영상 전반에 걸쳐 일관되게 유지합니다.

### `brand_style` — 레퍼런스 브랜드 제시
"Monster Energy meets high-end Apple aesthetic"처럼 잘 알려진 브랜드를 레퍼런스로 제시하면 VEO 3가 원하는 시각적 톤을 더 잘 이해합니다.

### `camera` — 3단계 움직임 서사
단순한 회전이 아니라 **시작(클로즈업)→ 중간(풀 리빌) → 마무리(로고 클로즈업)**의 3단계 서사를 카메라 움직임으로 구성했습니다. 8초 안에 제품을 소개하고 강조하는 완전한 광고 구조입니다.

### `lighting` — 복수의 조명 소스
"electric blue rim light" + "dramatic uplighting" + "occasional lightning flash"의 조합은 평범한 제품 촬영과 차별화된 역동적인 조명을 만듭니다. 에너지 드링크의 "전기적" 이미지를 조명으로 시각화했습니다.

### `elements` — 브랜드 세계관 구축
번개, 입자, 연기의 조합은 에너지, 파워, 신비로움을 동시에 표현합니다. "electrons around an atom" 비유는 과학적/기술적 이미지도 더합니다.

---

## 예상 결과 묘사

이 프롬프트로 생성되는 영상은 다음과 같은 장면을 포함합니다:

**0-2초**: 번개 볼트 로고의 극단적 클로즈업. 금속 질감의 디테일이 보임. 아래에서 올라오는 파란 빛이 로고를 강조.

**2-4초**: 카메라가 낮은 각도로 뒤로 물러나면서 캔의 전체 모습이 어둠 속에서 등장. 첫 번째 번개 플래시.

**4-7초**: 천천히 360도 회전하는 캔 주위를 카메라가 돌면서 모든 면을 보여줌. 입자들이 궤도를 돌고, 연기가 아래에서 피어오름.

**7-8초**: 로고가 정면을 향해 멈추고 모든 번개가 로고로 집중되는 클라이맥스. "IGNITE YOUR LIMITS" 텍스트 등장. 암전.

---

## 변형 버전 아이디어

| 버전 | 변경 필드 | 효과 |
|------|-----------|------|
| 붉은 버전 | color를 red로 변경 | 더 공격적, 스포츠 느낌 |
| 겨울 버전 | elements에 ice crystals 추가 | "아이스 블레이즈" 시즌 에디션 |
| 자연 버전 | location을 forest night으로 | 야외 활동 타깃 |
| 단순 버전 | elements 제거 | 미니멀 프리미엄 느낌 |
