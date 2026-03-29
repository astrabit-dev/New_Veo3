# 71. 장면 전환 기법

## 장면 전환의 역할

장면 전환은 단순히 클립A에서 클립B로 넘어가는 것이 아닙니다. 좋은 전환은 **시간, 공간, 감정의 변화**를 시청자에게 자연스럽게 전달합니다. 영화감독들이 수십 년 동안 연구해온 편집 기법들을 VEO 3 프롬프트 계획에 적용해봅시다.

---

## 부드러운 전환을 위한 프롬프트 기법

### 기법 1: 매칭 컷 (Match Cut)

두 클립의 구도, 움직임, 형태가 비슷하면 자연스럽게 연결됩니다.

**구도 매칭 예시:**
```
클립 A: "A coffee cup is lifted from a table, close-up, moving upward toward lips, morning light"
클립 B: "A telescope is lifted toward the eye, close-up, same upward movement, night sky background"
```
두 클립 모두 "물체가 위로 들어올려지는" 구도를 공유합니다.

**형태 매칭 예시:**
```
클립 A: "A round clock face, close-up, hands at 12 o'clock — the full moon fills the frame"
클립 B: "The full moon in the night sky, same size and position as the clock face in previous shot"
```
둥근 시계와 둥근 달이 시각적으로 연결됩니다.

---

### 기법 2: 방향성 연결

캐릭터나 움직임의 방향을 이용해 연결감을 만드는 방법입니다.

**180도 규칙:**
두 클립에서 캐릭터가 항상 같은 방향을 향하도록 유지하세요:
```
클립 A: 캐릭터가 오른쪽으로 이동 (왼쪽에서 오른쪽으로)
클립 B: 같은 캐릭터가 계속 오른쪽으로 이동 (같은 방향 유지)
```

```
// 방향성 연결 프롬프트 예시
클립 A: "The warrior runs from left to right across a stone bridge..."
클립 B: "Continuing from the right, the warrior enters a castle gate, still moving right..."
```

---

## 시작 프레임과 끝 프레임 매칭

각 클립의 시작과 끝 프레임을 계획해서 연결이 자연스럽도록 만드는 방법입니다:

### 전환 계획 표 예시

| 클립 | 시작 프레임 | 끝 프레임 | 다음 클립과의 연결 |
|------|-----------|---------|-----------------|
| 1 | 와이드샷, 숲 전경 | 미디엄샷, 캐릭터 얼굴 | 클로즈업으로 연결 |
| 2 | 클로즈업, 손이 문을 밂 | 문이 열리는 순간 | 열린 문 너머로 연결 |
| 3 | 문 뒤 공간 시작 | 공간 내부로 이동 | 공간 탐색으로 연결 |

프롬프트에서 이를 표현하는 방법:

```
클립 2 프롬프트 끝에 추가:
"...ends with the door fully open, the interior space revealed beyond the threshold"

클립 3 프롬프트 시작에 추가:
"Starting from just inside the doorway, looking back at the open door and then turning to face the interior..."
```

---

## 컷 전환 vs 페이드

### 컷(Cut)
한 클립에서 다른 클립으로 즉각 전환. 가장 흔한 전환 방식.

**효과적인 사용:**
- 같은 시간대, 같은 공간 내 전환
- 액션의 연속성 (달리기, 전투 등)
- 빠른 리듬이 필요한 장면

프롬프트 계획: 시작/끝 프레임의 구도와 조명을 맞춥니다.

### 페이드(Fade)
화면이 검어지거나 흰 화면으로 사라졌다가 다시 등장.

**효과적인 사용:**
- 시간이 크게 건너뛸 때 (오전 → 다음 날 아침)
- 공간이 완전히 바뀔 때
- 감정적 전환 (슬픔 → 희망)

프롬프트에서 지시:
```
클립 A 끝에: "...camera slowly fades to black"
클립 B 시작에: "Fades in from black to reveal..."
```

### 크로스 디졸브(Cross Dissolve)
한 클립이 서서히 사라지며 다른 클립이 겹쳐 나타남. 편집 툴에서 처리.

---

## 색상과 조명으로 연결감 만들기

색상과 조명의 연속성은 개별 클립들을 하나의 세계처럼 보이게 합니다.

### 색상 팔레트 통일

프롬프트에 색상 팔레트를 명시하고 모든 클립에 적용합니다:

```
[영상 전체 공통 색상 가이드]
"warm earthy tones — terracotta, burnt orange, deep brown, dusty gold — consistent across all clips"
```

### 조명의 연속성

- 낮 장면들: `"soft overcast daylight"` 유지
- 밤 장면들: `"warm torchlight and moonlight"` 유지
- 실내 장면들: `"practical indoor lighting, warm incandescent"` 유지

### 감정적 색상 변화

의도적으로 색상을 바꿔 감정 전환을 표현할 수도 있습니다:

```
슬픔/우울한 장면: "cold blue-grey, desaturated, flat light"
희망/행복한 장면: "warm golden, high saturation, soft glow"
위험/긴장 장면: "deep red tones, harsh shadows, low key lighting"
```

---

## 장면 전환 체크리스트

다음 클립으로 넘어가기 전에 확인하세요:

- [ ] 이전 클립의 끝 조명과 다음 클립의 시작 조명이 호환되는가?
- [ ] 캐릭터의 움직임 방향이 클립 간에 일관되는가?
- [ ] 시간대가 논리적으로 진행되는가?
- [ ] 색상 팔레트가 영상 전체에서 유지되는가?
- [ ] 급격한 전환이라면 의도적인가? (페이드, 색상 변화 등)
