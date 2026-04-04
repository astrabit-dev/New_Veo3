# 네거티브 프롬프팅 기법

> **무엇을 원하는지만큼, 무엇을 원하지 않는지를 명확히 하면 결과물이 달라집니다**

---

## 네거티브 프롬프팅이란

프롬프트는 보통 "원하는 것"을 서술합니다. 하지만 AI는 때때로 원치 않는 요소를 만들어냅니다.

- 영화 같은 장면을 원했는데 어색한 CG 느낌
- 성인 캐릭터를 요청했는데 만화적으로 과장된 표현
- 조용한 실내 장면인데 불필요한 카메라 흔들림
- 진지한 장면인데 엉뚱한 배경 오브젝트 등장

**네거티브 프롬프팅(Negative Prompting)**은 이처럼 원하지 않는 요소를 명시적으로 제거하는 기술입니다.

---

## Veo 3에서 네거티브 프롬프팅이 작동하는 방식

Veo 3는 전용 네거티브 프롬프트 입력 필드를 따로 제공하지 않습니다. 대신 두 가지 방법으로 처리합니다.

### 방법 1: 인라인 부정 표현

프롬프트 본문 안에 부정 표현을 자연어로 삽입합니다.

```
... no camera shake, avoid cartoonish style, without text overlay ...
```

### 방법 2: [Avoid] 블록 사용

프롬프트 마지막에 피해야 할 요소들을 묶어서 명시합니다.

```
[Avoid: camera shake, cartoonish proportions, text on screen, lens flare, jumpcuts]
```

두 방법 모두 작동하며, **복잡한 프롬프트에는 [Avoid] 블록 방식이 더 명확합니다.**

---

## 가장 많이 쓰이는 네거티브 키워드

### 화질 및 스타일

| 피해야 할 요소 | 사용 키워드 |
|-------------|-----------|
| 만화·애니 스타일 | `cartoonish, anime-style, illustrated` |
| 어색한 CG 느낌 | `CGI look, plastic texture, artificial lighting` |
| 과도한 포화도 | `oversaturated colors, neon overload` |
| 뭉개진 화질 | `blurry, low resolution, grainy` |
| 워터마크·텍스트 | `text overlay, watermark, subtitles, captions` |

### 카메라 및 움직임

| 피해야 할 요소 | 사용 키워드 |
|-------------|-----------|
| 카메라 흔들림 | `camera shake, shaky camera, handheld wobble` |
| 급격한 점프컷 | `jumpcuts, abrupt cuts` |
| 너무 빠른 줌 | `rapid zoom, whip zoom` |
| 불필요한 왜곡 | `fisheye distortion, lens distortion` |

### 인물 및 오브젝트

| 피해야 할 요소 | 사용 키워드 |
|-------------|-----------|
| 부자연스러운 미소 | `forced smile, uncanny expression` |
| 손·손가락 왜곡 | `distorted hands, extra fingers` |
| 불필요한 엑스트라 | `crowds, extra people in background` |
| 어색한 신체 비율 | `unrealistic proportions, exaggerated features` |

### 오디오

| 피해야 할 요소 | 사용 키워드 |
|-------------|-----------|
| 배경 잡음 | `background noise, static, hiss` |
| 대사 발음 오류 | `muffled dialogue, unclear speech` |
| 갑작스러운 음량 변화 | `audio pop, volume spike` |

---

## 실전 예시: 네거티브 프롬프팅 전후 비교

### 예시 1 — 기업 광고 영상

**네거티브 없는 프롬프트:**
```
A professional businessman in a sleek office presents a product
to a camera, confident and charismatic.
[Audio: upbeat corporate music]
```
**자주 발생하는 문제:** 만화처럼 과장된 표정, 배경에 뜬금없는 텍스트, 불필요한 렌즈 플레어

**네거티브 추가 후:**
```
A professional businessman in his 40s, sharp navy suit,
stands at a minimalist glass-and-steel conference room,
presents toward camera with composed confidence,
natural lighting from floor-to-ceiling windows,
medium shot, stable camera.
[Audio: clean upbeat corporate background music]
[Avoid: cartoonish expressions, text overlay, lens flare,
        camera shake, cluttered background]
```

---

### 예시 2 — 공포 영상

**네거티브 없는 프롬프트:**
```
An empty hospital corridor at night, flickering lights, eerie atmosphere.
```
**자주 발생하는 문제:** 지나치게 밝은 색상, 배경에 사람 등장, 카메라가 어색하게 패닝

**네거티브 추가 후:**
```
An abandoned hospital corridor at 3am,
single flickering fluorescent tube overhead,
paint peeling from walls, old wheelchair at the far end,
static wide shot down the corridor, deep shadows on both sides,
horror film aesthetic, oppressive silence.
[Audio: electrical buzzing, distant dripping water]
[Avoid: people or figures in background, bright colors,
        camera movement, cheerful music, cartoon style]
```

---

### 예시 3 — 자연 다큐멘터리

**네거티브 없는 프롬프트:**
```
A lone wolf walks through a snowy forest at dawn.
```
**자주 발생하는 문제:** 비현실적으로 과장된 털 질감, CG 배경, 인공적 조명

**네거티브 추가 후:**
```
A lone grey wolf moves silently through a snow-covered boreal forest
at dawn, breath visible in cold air, paw prints in fresh snow,
low tracking shot following at eye level,
overcast sky filtering soft diffused light through bare birch trees,
BBC Earth documentary aesthetic, photorealistic.
[Audio: soft wind, snow crunching underfoot, distant crow call]
[Avoid: CGI look, artificial lighting, saturated colors,
        dramatic music, any human presence]
```

---

## 장르별 핵심 네거티브 키워드 모음

### 실사·드라마

```
[Avoid: cartoon style, anime aesthetic, unrealistic proportions,
        plastic skin texture, overexposed highlights, camera shake]
```

### 공포·스릴러

```
[Avoid: bright warm colors, background people moving, comedic elements,
        upbeat music, lens flare, fast camera movement]
```

### 광고·제품

```
[Avoid: text overlay, watermark, cluttered background, camera shake,
        lens distortion, cartoonish proportions, amateur lighting]
```

### 자연·다큐멘터리

```
[Avoid: CGI look, artificial lighting, color grading overuse,
        dramatic music score, human presence, unnatural animal behavior]
```

### SF·판타지

```
[Avoid: low-budget visual effects, plastic textures, obvious green screen,
        anachronistic elements, modern urban backgrounds]
```

---

## 네거티브 프롬프팅의 한계

네거티브 프롬프팅은 강력하지만 만능은 아닙니다.

**효과가 있는 것:**
- 전반적인 스타일 방향 조정
- 자주 발생하는 공통 오류 억제
- 특정 불필요한 요소 제거

**효과가 제한적인 것:**
- 매우 구체적인 오브젝트 제거 ("배경의 저 의자를 없애줘")
- 생성 후 수정 요청 (사후 편집은 불가)
- 모든 클립에서 100% 일관된 적용

> **핵심 원칙:** 네거티브 프롬프팅은 "원하는 것을 더 명확히 하는 보조 도구"입니다. 포지티브 프롬프트가 탄탄해야 효과가 극대화됩니다.

---

## 프롬프트 작성 순서 권장안

1. **포지티브 묘사 먼저** — 캐릭터, 배경, 카메라, 조명, 오디오를 충분히 서술
2. **테스트 생성** — Fast Mode로 한 번 확인
3. **문제 식별** — 결과물에서 원치 않는 요소를 구체적으로 파악
4. **[Avoid] 블록 추가** — 확인된 문제 요소를 키워드로 변환
5. **재생성 비교** — 변경 전후 결과물을 비교해 효과 확인

---

## 요약

| 개념 | 내용 |
|------|------|
| 네거티브 프롬프팅이란 | 원치 않는 요소를 명시적으로 제거하는 기술 |
| Veo 3 적용 방법 | 인라인 부정 표현 또는 `[Avoid: ...]` 블록 |
| 가장 유용한 상황 | 스타일 불일치, 반복되는 오류 요소, 품질 저하 억제 |
| 한계 | 사후 수정 불가, 100% 적용 보장 없음 |
| 권장 순서 | 포지티브 프롬프트 → 테스트 → 문제 확인 → [Avoid] 추가 |
