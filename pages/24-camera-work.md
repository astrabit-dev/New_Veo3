# 영화 같은 카메라 워크

> **프롬프트에 카메라를 넣는 순간, 영상이 달라집니다**

---

## 카메라 워크가 왜 중요한가

같은 장면을 찍어도 카메라 각도와 움직임에 따라 완전히 다른 감정이 전달됩니다.

영화에서:
- 악당이 등장할 때는 로우앵글 (강인하고 위협적으로)
- 공포 장면에서는 하이앵글 (취약하고 작게)
- 화해 장면에서는 아이레벨 (동등하고 친밀하게)

Veo 3는 이런 영화 언어를 이해합니다. 프롬프트에 카메라 지시어를 넣으면 해당 방식으로 카메라가 배치되고 움직입니다.

---

## Veo 3가 이해하는 카메라 키워드

### 카메라 앵글
```
eye level shot          - 아이레벨 (자연스럽고 중립적)
low angle shot          - 로우앵글 (강인함, 위압감)
high angle shot         - 하이앵글 (취약함, 내려다봄)
bird's eye view         - 버드아이 (완전 수직 내려다봄)
over the shoulder shot  - OTS (대화 장면, 친밀함)
Dutch angle             - 더치앵글 (불안정, 긴장감)
aerial shot             - 항공샷 (장대함, 전경)
```

### 샷 크기
```
extreme wide shot       - 익스트림 와이드 (광활한 환경)
wide shot               - 와이드샷 (전체 장면)
medium shot             - 미디엄샷 (인물 상반신)
close-up                - 클로즈업 (얼굴, 표정)
extreme close-up        - 익스트림 클로즈업 (눈, 손 등 세부)
```

### 카메라 움직임
```
pan left / pan right    - 좌우 패닝 (가로로 이동)
tilt up / tilt down     - 틸트 (상하 이동)
dolly in / dolly out    - 달리인/달리아웃 (피사체를 향해/멀리)
tracking shot           - 트래킹 (피사체를 따라 이동)
crane shot              - 크레인샷 (아래에서 위로 또는 반대)
handheld camera         - 핸드헬드 (흔들리는 현장감)
steadicam               - 스테디캠 (부드러운 이동)
orbit / circular        - 피사체 주위를 원을 그리며
zoom in / zoom out      - 줌 (화면 안으로/밖으로)
```

---

## 카메라 워크 실전 예시

### 예시 1: 영웅 등장 장면
```
A battle-worn warrior emerges from the smoke,
dramatic low angle shot looking up at the warrior,
slow dolly forward, backlit by a burning city,
epic cinematic style, triumphant mood.
```
로우앵글 + 달리 포워드로 영웅을 극적으로 강인하게 표현

### 예시 2: 공포 장면
```
A child sits alone in a dark hallway,
high angle shot looking down,
handheld camera, slight shake,
dim overhead light, shadows creeping from both sides.
```
하이앵글 + 핸드헬드로 취약함과 불안함 표현

### 예시 3: 자연 다큐
```
Vast savanna stretching to the horizon at golden hour,
slow aerial tracking shot from left to right,
herd of wildebeest migrating below,
cinematic wide shot, breathtaking scale.
```
에어리얼 트래킹샷으로 장대한 자연 표현

### 예시 4: 친밀한 대화 장면
```
Two old friends sharing coffee in a cozy café,
over the shoulder shot switching between them,
soft natural window light, warm bokeh background,
intimate and nostalgic mood.
```
OTS 샷으로 친밀감 표현

### 예시 5: 액션 추격 장면
```
A spy races through narrow alleyways,
fast-paced tracking shot following from behind,
handheld camera for urgency,
rain-slicked streets reflecting neon lights,
intense and breathless pace.
```
트래킹샷 + 핸드헬드로 긴박감 표현

---

## 카메라 움직임과 감정의 관계

| 카메라 움직임 | 감정 효과 |
|-------------|----------|
| 달리 인 (가까이) | 긴장감, 집중, 압박 |
| 달리 아웃 (멀어짐) | 외로움, 해방, 마무리 |
| 느린 패닝 | 고요함, 관조, 서사 |
| 핸드헬드 흔들림 | 현장감, 긴박함, 현실감 |
| 하이앵글 | 취약함, 고립감 |
| 로우앵글 | 강인함, 위압감, 영웅성 |
| 버드아이 | 신의 시점, 전략적, 장대함 |
| 스테디캠 | 우아함, 서정성 |
| 원형 궤도 (오빗) | 인물 강조, 순간의 중요성 |

---

## 프롬프트에 카메라 정보 넣는 위치

카메라 정보는 일반적으로 장면 설명 뒤, 분위기 묘사 앞에 넣는 것이 좋습니다.

**권장 순서:**
```
[주인공/장면 묘사] + [카메라 앵글/움직임] + [조명/분위기]
```

**예시:**
```
An elderly violinist performs on a rain-soaked cobblestone square,
[카메라: slow circular tracking shot around the musician,]
dramatic side lighting from a street lamp,
melancholic and beautiful atmosphere.
```

---

## 처음 배울 때 추천하는 카메라 키워드 5가지

1. `cinematic wide shot` — 전체 장면을 아름답게
2. `close-up` — 감정을 강조
3. `low angle shot` — 강인하고 드라마틱하게
4. `aerial shot` — 장대하고 웅장하게
5. `handheld camera` — 현장감 있고 생동감 있게

이 5가지만으로도 영상이 훨씬 전문적으로 변합니다. PART 9에서 카메라 기법을 더 심층적으로 다룹니다.
