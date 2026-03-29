# 64. 나만의 JSON 템플릿 만들기

## ChatGPT/Claude로 JSON 만들기

JSON 프롬프트를 처음 만드는 것이 어렵게 느껴진다면, AI 어시스턴트를 활용해보세요. ChatGPT나 Claude에게 다음과 같이 요청하면 됩니다:

### AI에게 요청하는 프롬프트 예시

```
당신은 VEO 3 AI 영상 생성 전문가입니다.
다음 제품에 대한 VEO 3용 JSON 프롬프트를 작성해주세요:

제품명: [이름]
제품 유형: [음료/향수/시계 등]
타깃 고객: [나이, 성별, 관심사]
브랜드 무드: [강력한/우아한/신선한/신비로운 등]
원하는 배경: [어두운 스튜디오/자연/도시 등]
특별히 포함할 요소: [번개/꽃잎/물 등]

JSON 형식으로 출력해주세요. 각 필드에 구체적이고 시각적인 묘사를 넣어주세요.
```

### 더 구체적인 요청 예시

```
다음 정보를 바탕으로 VEO 3 제품 광고 JSON을 작성해주세요:

- 제품: 프리미엄 그린티 음료 "JADE CALM"
- 외형: 투명 유리병, 연한 초록빛 액체, 흰색 미니멀 라벨, 대나무 뚜껑
- 타깃: 20-35세 여성, 웰니스/미니멀리즘 관심층
- 경쟁 브랜드 레퍼런스: Cha Tiger Tea의 미니멀한 광고 스타일
- 배경: 일본식 선(禅) 정원 또는 미니멀 흰 스튜디오
- 분위기: 조용하고 평화롭고 자연적인
- 특별 요소: 대나무, 떨어지는 벚꽃 잎, 아침 안개

이 JSON은 VEO 3에 직접 붙여넣을 수 있도록 완성된 형태로 작성해주세요.
```

---

## 단계별 커스터마이징 방법

### Step 1: 제품 시각화

먼저 제품의 외형을 최대한 상세하게 묘사합니다. 이것이 `description` 필드의 기초가 됩니다.

아래 질문에 답해보세요:
- 이 제품의 형태는? (캔, 병, 박스, 튜브...)
- 주요 색상은? 재질의 느낌은? (유리, 금속, 플라스틱, 무광, 유광...)
- 로고/텍스트는 어디에 어떤 폰트로?
- 특별한 시각적 특징은? (패턴, 투명도, 반사율...)

### Step 2: 브랜드 무드 정의

`brand_style`과 `atmosphere` 필드를 위해 3가지 형용사로 브랜드를 설명해보세요.

| 브랜드 유형 | 형용사 3개 | 스타일 참조 |
|------------|-----------|------------|
| 에너지/스포츠 | 강렬, 전기적, 대담한 | Monster, Red Bull |
| 명품/향수 | 신비로운, 관능적, 희귀한 | Chanel, Dior |
| 건강/자연 | 신선한, 순수한, 활력 있는 | Innocent, Vita Coco |
| 럭셔리 주류 | 깊은, 따뜻한, 시간을 초월한 | Macallan, Hennessy |
| 테크/혁신 | 미래적, 깔끔한, 정밀한 | Apple, Tesla |

### Step 3: 배경과 조명 결정

배경과 조명은 같은 제품을 완전히 다르게 만듭니다:

```
같은 제품, 다른 배경/조명의 결과 차이:

dark void + electric lighting = 파워풀하고 현대적
marble surface + soft natural light = 고급스럽고 클래식
forest + golden hour = 자연적이고 친환경적
studio white + minimal lighting = 미니멀하고 세련됨
```

### Step 4: 움직임 설계

8초 안에 제품을 소개하는 움직임 서사를 설계합니다:

**3막 구조 활용:**
- 1막 (0-2초): 강렬한 시작 / 티저 / 클로즈업
- 2막 (2-6초): 전체 공개 / 제품 특징 탐색
- 3막 (6-8초): 클라이맥스 / CTA / 브랜드 각인

---

## 흔한 실수와 수정법

### 실수 1: 너무 짧고 추상적인 description
```json
// 나쁜 예
"description": "black energy drink can"

// 좋은 예
"description": "matte black aluminum can, 250ml slim format, electric blue lightning bolt logo centered on front, neon blue horizontal stripe at the midpoint, bold condensed font, metallic silver top"
```

### 실수 2: 모순된 스타일 요소
```json
// 나쁜 예 (미니멀 + 과도한 요소 충돌)
"style": "minimal, clean, zen",
"elements": ["explosions", "lightning bolts", "neon signs", "fire effects", "particle storm"]

// 좋은 예 (스타일과 요소가 일치)
"style": "minimal, clean, zen",
"elements": ["single water droplet", "morning mist", "soft light refraction"]
```

### 실수 3: 모든 것을 움직이려는 욕심
```json
// 나쁜 예 (혼란스러운 움직임)
"motion": "can rotates fast while spinning and jumping and bouncing and sparks fly everywhere and camera also spins around"

// 좋은 예 (단순하고 명확한 움직임)
"motion": "can rotates slowly on its axis — one revolution over 8 seconds, particles orbit gently, camera holds steady"
```

### 실수 4: 인물 포함 시 부자연스러움
제품 광고에서 인물을 포함하고 싶다면 `keywords`에 "no close-ups of faces, focus on hands only"를 추가하거나, 완전히 실루엣으로만 인물을 처리하는 것이 안전합니다.

---

## 나만의 템플릿 저장 시스템

자주 사용하는 브랜드 스타일별로 JSON 템플릿을 저장해두면 나중에 재활용할 수 있습니다:

- `template-dark-luxury.json` — 어두운 고급 브랜드 기본 템플릿
- `template-natural-wellness.json` — 자연/건강 브랜드 기본 템플릿
- `template-sports-energy.json` — 스포츠/에너지 브랜드 기본 템플릿
- `template-minimal-tech.json` — 미니멀/테크 브랜드 기본 템플릿

각 템플릿에서 `product_name`, `description`, `text`만 바꾸면 새 광고가 완성됩니다.
