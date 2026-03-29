# 63. 실전 예시 2 — Noir Bloom 향수 광고

## Noir Bloom 브랜드 컨셉

Noir Bloom은 **어둠과 꽃의 대조**를 테마로 하는 가상의 고급 향수 브랜드입니다. 이 광고의 목표:

- 타깃: 25-40세 여성, 프리미엄 뷰티 소비자
- 무드: 신비롭고 관능적, 어두운 우아함
- 메시지: "어둠 속에서 피어나다 (Bloom in the Dark)"
- 플랫폼: Instagram, 잡지 디지털 광고, YouTube

에너지 드링크 광고가 전기적이고 강력한 느낌이었다면, 향수 광고는 완전히 반대로 **부드럽고 신비로우며 관능적**이어야 합니다. 같은 JSON 구조를 사용하지만 각 필드의 내용이 얼마나 달라지는지 비교해보세요.

---

## 완전한 JSON 프롬프트

```json
{
  "product_name": "Noir Bloom",
  "product_type": "luxury perfume bottle, 50ml",
  "description": "elegant dark glass perfume bottle with a slightly irregular organic shape — not perfectly symmetric, as if sculpted by hand — deep midnight black glass that becomes slightly translucent purple when backlit, gold-leaf 'NOIR BLOOM' text etched delicately on the front, a faceted crystal stopper that catches light into rainbow refractions, a single dried black rose petal sealed inside the glass visible through the base, thin gold metal collar around the neck",
  "brand_style": "haute parfumerie, dark florals, premium French luxury house aesthetic, targeting sophisticated women 25-40, Maison Margiela or Black Opium energy",
  "style": "editorial dark luxury, reminiscent of high-end fragrance films — mysterious, sensual, artistic. Think Yves Saint Laurent Black Opium or Dior Poison aesthetic",
  "camera": "begins with a slow overhead shot looking straight down at the bottle surrounded by black rose petals, then gracefully arcs down to eye level in a slow curving motion, settles into a slightly low angle looking up at the bottle backlit, final close-up on the crystal stopper refracting light into colors",
  "lighting": "primary backlight from directly behind the bottle creating a dramatic silhouette with a purple-black halo, secondary soft diffused light from one side to reveal the bottle's form, no harsh highlights, all light is soft and wrapped, occasional candle flicker from off-screen adding organic warmth, gold rim light catching the bottle's edges",
  "location": "resting on a surface of black velvet draped loosely, natural black rose petals scattered around the base, a small pool of dark water partially reflecting the bottle, very subtle wisps of perfume vapor rising from the stopper",
  "time_of_day": "late night ambiance, no daylight, only intimate artificial light sources — candles and soft studio lights",
  "atmosphere": "mysterious, deeply sensual, like a secret garden at midnight, intoxicating and slightly dangerous in its beauty, the feeling of something rare and forbidden",
  "elements": [
    "black rose petals — some fresh, some dried — scattered organically",
    "very subtle wisps of translucent smoke or perfume vapor rising from the stopper",
    "tiny gold dust particles floating in the air around the bottle",
    "the bottle's reflection in the dark water surface below it",
    "barely visible moonlight through mist in the extreme background",
    "crystal stopper casting rainbow light patterns on the velvet"
  ],
  "motion": "the bottle remains perfectly still — all motion comes from the environment: petals sway almost imperceptibly, vapor wisps drift upward slowly, gold particles float in gentle Brownian motion, the water reflection shimmers slightly, candlelight flickers softly",
  "cta_motion": "camera very slowly pushes in from mid-shot to close-up of the bottle as the gold particles all drift toward the bottle and the purple backlight intensifies subtly, suggesting the bottle draws everything toward it",
  "ending": "slow fade to black, keeping only the faint silhouette of the bottle visible for a moment, then complete darkness with the memory of the visual",
  "text": "NOIR BLOOM — Bloom in the Dark",
  "keywords": [
    "no humans",
    "luxury product film",
    "photorealistic",
    "cinematic 4K",
    "dark editorial photography aesthetic",
    "no fast movements",
    "everything is slow and intentional",
    "color grade: deep blacks, purple-black shadows, warm gold accents"
  ]
}
```

---

## 각 필드 선택 이유

### `description` — 불완전한 아름다움
"slightly irregular organic shape — not perfectly symmetric, as if sculpted by hand" — 완벽한 대칭이 아닌 수공예 느낌의 형태를 지정했습니다. 이는 브랜드의 아르티장(artisan) 정체성을 전달하고, 대량 생산 제품과 차별화합니다.

"a single dried black rose petal sealed inside the glass" — 병 안에 장미 꽃잎이 보존되어 있다는 스토리텔링 디테일은 향수에 깊이와 미스터리를 더합니다.

### `style` — 구체적인 레퍼런스 브랜드
"Yves Saint Laurent Black Opium or Dior Poison aesthetic"처럼 실제 향수 브랜드의 광고 스타일을 레퍼런스로 사용하면 VEO 3가 업계의 시각적 언어를 참조할 수 있습니다.

### `lighting` — 드라마 없는 드라마
에너지 드링크에서는 "lightning flashes"로 극적 조명을 썼지만, 향수에서는 "no harsh highlights, all light is soft and wrapped"로 완전히 반대 접근을 합니다. 같은 '극적임'이지만 방법이 다릅니다.

"occasional candle flicker from off-screen" — 실제 촬영처럼 화면 밖 요소가 화면 안에 영향을 미치는 디테일은 영상에 생동감을 줍니다.

### `motion` — 제품은 정지, 환경이 움직임
"the bottle remains perfectly still — all motion comes from the environment" — 이것이 고급 향수 광고의 핵심 기법입니다. 제품 자체는 움직이지 않고, 꽃잎, 연기, 파티클만 조용히 움직입니다. 안정감과 고급감을 동시에 전달합니다.

---

## 예상 결과 묘사

**0-2초**: 위에서 내려다보는 오버헤드 샷. 검은 벨벳 위 장미 꽃잎들과 중앙의 향수 병이 미스터리한 구성을 이룸. 보라빛 역광.

**2-5초**: 카메라가 우아하게 아치를 그리며 아이레벨로 내려옴. 병의 실루엣이 역광 속에서 드라마틱하게 등장. 파티클이 주변에 부유.

**5-7초**: 낮은 각도에서 병을 올려다보는 샷. 크리스탈 마개에서 무지개 빛이 퍼짐. 증기가 천천히 위로 올라감.

**7-8초**: 크리스탈 마개의 클로즈업. 빛이 분산되어 색이 가득. "NOIR BLOOM" 텍스트. 천천히 암전.

---

## Blaze Energy vs Noir Bloom 비교

| 항목 | Blaze Energy | Noir Bloom |
|------|-------------|------------|
| 배경 | 완전한 검은 허공 | 검은 벨벳 + 물 반영 |
| 조명 | 강렬한 전기 파란빛 | 부드러운 보라+황금빛 |
| 움직임 | 회전하는 캔 + 번개 | 정지한 병 + 주변 환경 |
| 파티클 | 전기 입자, 번개 | 금색 먼지, 연기, 꽃잎 |
| 카메라 | 낮은 각도에서 위 | 위에서 아래로 호 |
| 분위기 | 전기적, 강렬 | 신비롭고 관능적 |

두 광고 모두 같은 JSON 구조를 사용하지만 타깃과 브랜드 성격에 따라 완전히 다른 영상이 나옵니다.
