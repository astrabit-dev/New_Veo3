# 클립 연장(Extend) & 연결 심화 기법

> **8초를 넘어서 — 자연스럽게 이어지는 더 긴 장면 만들기**

---

## 클립 연장이 필요한 순간

단순한 풍경 클립이나 짧은 장면은 8초로 충분합니다. 하지만 다음 상황에서는 더 긴 연속 장면이 필요합니다.

- 인물이 걷는 장면이 끊기지 않고 이어져야 할 때
- 카메라가 멈추지 않고 계속 움직여야 할 때
- 긴 대사나 모놀로그 장면
- 분위기 전환이 없는 동일 씬의 지속

이 챕터에서는 Google Flow에서 제공하는 연장 기능과, 여러 클립을 자연스럽게 이어 붙이는 심화 전략을 다룹니다.

---

## 세 가지 클립 연장 방법 비교

| 방법 | 작동 방식 | 적합한 상황 |
|------|---------|-----------|
| **Add to Scene** | 마지막 프레임 기반으로 새 클립 생성 (새 프롬프트 필요) | 다른 행동이나 앵글로 전환할 때 |
| **Extend (직접 연장)** | 기존 클립의 흐름을 그대로 이어서 생성 | 동일 장면을 더 길게 유지할 때 |
| **편집 연결** | 여러 클립을 CapCut에서 자연스럽게 이어 붙임 | 모든 경우 — 최종 마무리 단계 |

---

## 방법 1: Add to Scene (복습 + 심화)

22장에서 소개한 Add to Scene의 심화 활용법입니다.

### 기본 원리

이전 클립의 마지막 프레임을 참조해 다음 클립을 생성합니다. **같은 장면을 계속 이어가면서 행동이나 관점만 바꾸는 데 강합니다.**

### 연속성을 높이는 Add to Scene 작성법

단순히 새 프롬프트를 쓰는 것보다, 이전 클립과의 연결성을 명시하면 더 자연스러운 결과가 나옵니다.

```
[이전 클립]
A woman in a red coat walks down a rainy alley toward the camera,
cobblestone street, night, overhead lamp.

[Add to Scene — 같은 장면 계속]
프롬프트: "Continuing — same woman in red coat now closer to camera,
she stops and looks up at a lit window above,
rain still falling, same alley setting,
medium close-up from same camera position"

핵심: "Continuing — same [주요 요소]" 로 시작하면
AI가 이전 클립과의 연결성을 더 잘 인식합니다.
```

---

## 방법 2: Extend 기능

Google Flow는 생성된 클립에 대해 **Extend** 옵션을 제공합니다. 기존 클립의 끝 부분에서 동일한 움직임과 분위기를 유지하며 추가 8초를 생성합니다.

### Extend 사용 방법

```
1. 생성 완료된 클립 선택
2. 클립 하단 옵션 메뉴에서 "Extend" 선택
   (또는 클립 우측 ... 메뉴 → Extend)
3. 추가 프롬프트 없이 진행 (자동 연장) 또는
   간단한 방향 지시 프롬프트 추가
4. 생성 완료 후 원본 + 연장 클립을 함께 사용
```

> **인터페이스 주의:** Extend 기능의 표기와 위치는 Google Flow UI 업데이트에 따라 변경될 수 있습니다. "Continue", "Extend clip", "Generate more" 등으로 표시될 수 있습니다.

### Extend가 잘 작동하는 클립 유형

```
잘 작동:
- 일정한 속도로 움직이는 카메라 (Dolly, Pan, Tilt)
- 지속적인 자연 현상 (비, 바람, 물, 구름)
- 걷거나 달리는 캐릭터
- 안정적인 분위기의 정적인 씬

작동이 불안정한 경우:
- 복잡한 액션 장면 (방향이 급격히 변하는)
- 클립 끝이 자연스럽지 않게 잘린 경우
- 너무 짧거나 급격히 변화하는 씬
```

### Extend 활용 예시

```
[원본 클립 — 8초]
A misty mountain valley at dawn, camera slowly panning right
revealing layered mountain ridges in morning fog.

[Extend 후 — 추가 8초]
같은 카메라 패닝이 계속되며 더 넓은 산맥이 드러남.
안개가 조금 더 걷히며 아래 계곡이 보이기 시작.
```

---

## 방법 3: 편집 연결 — 컷 포인트 기법

Extend와 Add to Scene만으로 해결하기 어려운 경우, CapCut에서 여러 클립을 자연스럽게 이어 붙이는 기법입니다.

### 매칭 컷 (Match Cut)

유사한 구도나 움직임에서 클립을 전환해 끊기지 않는 느낌을 만듭니다.

```
클립 A: 인물이 문을 밀며 앞으로 걸어 들어가는 장면 (카메라 뒤에서)
클립 B: 같은 인물이 반대편 공간에서 걸어 나오는 장면 (카메라 앞에서)

두 클립을 컷 없이 바로 이어 붙이면 한 공간에서 다른 공간으로
자연스럽게 이동하는 것처럼 보입니다.
```

### J-컷 / L-컷 (오디오 오버랩)

CapCut에서 오디오를 앞뒤로 조금 겹쳐서 편집하면 클립 전환이 더 부드럽게 느껴집니다.

```
J-컷: 다음 클립의 오디오가 먼저 시작된 후 영상이 전환됨
L-컷: 이전 클립의 오디오가 끝나지 않고 다음 영상으로 넘어감

적용 방법 (CapCut):
1. 클립 사이에서 오디오 레이어를 분리
2. 오디오를 0.5~1초 앞당기거나 뒤로 밀기
3. 볼륨을 부드럽게 페이드 처리
```

---

## 자연스러운 연결을 위한 프롬프트 전략

동일 장면에서 연결될 클립들을 생성할 때는 **환경 요소를 고정**하는 것이 핵심입니다.

### 고정 요소 블록 만들기

```
[씬 고정 블록 — 모든 클립 프롬프트에 동일하게 포함]
환경: "rain-soaked Seoul alleyway at night, neon signs overhead,
       wet cobblestones, single overhead lamp, foggy atmosphere"
인물: "30-year-old Korean woman, black trench coat, short hair"
카메라 기준: "cinematic film style, shallow depth of field"

씬 1 프롬프트:
[씬 고정 블록] + "she walks toward the lamp, back to camera, medium shot"

씬 2 프롬프트:
[씬 고정 블록] + "she stops under the lamp, looks up slowly, close-up"

씬 3 프롬프트:
[씬 고정 블록] + "she turns to face camera, wet face, tense expression"
```

환경 묘사를 반복하면 클립 간 배경 일관성이 유지됩니다.

---

## Extend vs Add to Scene vs 편집 연결 — 선택 기준

```
동일 움직임을 단순히 더 길게?
→ Extend 사용

같은 환경에서 행동이나 앵글을 바꾸고 싶다?
→ Add to Scene 사용

여러 다른 씬들을 모아 완성 영상을 만들고 싶다?
→ 편집 연결 (CapCut)

자연스러운 느낌이 최우선이다?
→ 세 방법을 혼합: Extend로 1차 연장 → Add to Scene으로 씬 전환
   → CapCut에서 오디오 오버랩으로 마무리
```

---

## 실전 예시: 3분 단편 영화 클립 구성

```
장면 1 — 도입 (분위기 설정)
프롬프트: 안개 낀 항구 새벽 전경 (8초)
→ Extend: 같은 전경 계속 + 배가 서서히 들어옴 (+8초)
총 16초

장면 2 — 캐릭터 등장
Add to Scene: 부두에 낯선 인물이 가방을 들고 서 있음 (8초)

장면 3 — 접근
새 프롬프트: 같은 인물, 카메라가 천천히 클로즈업 (8초)
→ Extend: 인물의 표정에서 긴장감 지속 (+8초)
총 16초

장면 4 — 반전
새 프롬프트: 인물이 뒤를 돌아봄 (8초)

장면 5 — 엔딩
새 프롬프트: 항구 전체 와이드샷, 안개 속으로 사라지는 인물 (8초)
→ Extend: 빈 부두만 남음 (+8초)
총 16초

합계: 클립 7개 × 평균 11초 ≈ 약 77초
CapCut 편집 후: 전환 효과 포함 약 80~90초
```
