# 프롬프트 트러블슈팅 가이드

> **원하는 영상이 안 나올 때, 막히지 않고 해결하는 체계적인 방법**

---

## 왜 트러블슈팅이 필요한가

프롬프트를 아무리 잘 써도 처음부터 완벽한 결과가 나오는 경우는 드뭅니다. 중요한 것은 실패했을 때 **무작정 다시 쓰는 것이 아니라 원인을 찾고 정확히 수정하는 능력**입니다.

이 챕터는 가장 자주 발생하는 9가지 문제 유형과 각각의 해결법을 다룹니다.

---

## 문제 진단 체크리스트

결과물이 마음에 들지 않을 때, 먼저 아래 질문에 답해보세요.

```
1. 의도한 캐릭터/배경이 나왔는가?      → NO: 문제 유형 A
2. 카메라 구도가 원했던 것인가?         → NO: 문제 유형 B
3. 조명이나 색감이 맞는가?              → NO: 문제 유형 C
4. 오디오가 제대로 포함되었는가?        → NO: 문제 유형 D
5. 캐릭터 외모가 이전 클립과 일치하는가? → NO: 문제 유형 E
6. 원치 않는 요소가 포함되어 있는가?    → YES: 문제 유형 F
7. 움직임이나 모션이 어색한가?          → YES: 문제 유형 G
8. 텍스트나 자막이 영상에 표시되는가?   → YES: 문제 유형 H
9. 생성 자체가 실패하거나 거부당했는가? → YES: 문제 유형 I
```

---

## 문제 유형 A — 의도한 장면이 나오지 않음

**증상:** 완전히 다른 배경, 엉뚱한 캐릭터, 요청과 무관한 장면이 생성됨

**원인:**
- 프롬프트에 핵심 요소가 빠져 있음
- 너무 짧거나 모호한 묘사
- 여러 상충하는 요소가 동시에 포함됨

**해결법:**

```
수정 전:
"A detective in a mysterious place at night"

수정 후:
"A middle-aged male detective in a worn grey overcoat
stands alone on a fog-covered stone bridge
over a dark river at 2am, city lights blurred in the mist below,
film noir style."
```

**원칙:** 장소, 인물, 시간, 분위기를 각각 명확하게 분리해서 서술하세요.

---

## 문제 유형 B — 카메라 구도가 의도와 다름

**증상:** 원했던 앵글이나 샷 타입이 반영되지 않음. AI가 임의로 구도를 선택함

**원인:**
- 카메라 관련 키워드가 빠짐
- 지나치게 일반적인 카메라 지시 ("good shot")

**해결법:**

카메라 지시는 세 가지를 함께 명시합니다.

```
[샷 타입] + [카메라 위치/각도] + [카메라 움직임]

예시:
"Extreme close-up of her eyes, camera at eye level,
 slow push-in toward face"

"Wide establishing shot from high angle (bird's eye view),
 camera slowly descends toward the subject"
```

**빠른 참조:**

| 원하는 구도 | 사용할 키워드 |
|-----------|------------|
| 전신 인물 | `full body shot, wide shot` |
| 얼굴 집중 | `close-up, extreme close-up` |
| 아래에서 위로 | `low angle, worm's eye view` |
| 위에서 아래로 | `high angle, bird's eye view` |
| 카메라 이동 없음 | `static shot, locked camera` |
| 천천히 다가감 | `slow dolly in, slow push-in` |

---

## 문제 유형 C — 조명과 색감이 맞지 않음

**증상:** 원했던 분위기와 전혀 다른 색조나 밝기로 생성됨

**원인:**
- 조명 키워드 미포함
- 색온도나 분위기 미지정

**해결법:**

조명은 두 가지로 나눠 서술합니다: **광원**과 **색온도/분위기**.

```
[광원] + [색온도/분위기]

따뜻한 느낌:
"warm golden hour backlight, amber and orange tones"

차갑고 긴장된 느낌:
"cold blue fluorescent overhead lighting, desaturated palette"

신비로운 느낌:
"single practical lamp casting long shadows,
 low-key lighting, deep contrast"
```

**장르별 조명 키워드:**

| 장르 | 조명 키워드 |
|------|-----------|
| 로맨스 | `golden hour, warm candlelight, soft diffused light` |
| 공포 | `harsh shadows, single overhead light, cold blue tones` |
| 액션 | `dramatic side lighting, high contrast, dynamic` |
| 다큐멘터리 | `natural light, overcast sky, soft even lighting` |
| SF | `neon accents, cool blue-green tones, artificial light sources` |

---

## 문제 유형 D — 오디오가 없거나 어색함

**증상:** 무음 영상 생성, 의도와 다른 음향, 대사가 뭉개짐

**원인 및 해결법:**

**케이스 1 — 오디오 자체가 없음:**
- Fast Mode(Veo 2)로 생성한 경우 → Veo 3.1 Lite 이상으로 전환
- `[Audio: ...]` 블록을 프롬프트에 추가하지 않은 경우 → 명시적으로 추가

```
[Audio: 구체적인 음향 묘사]

예시:
[Audio: heavy rain on windows, distant thunder, jazz piano softly playing]
```

**케이스 2 — 음향이 장면과 안 맞음:**
- 음향 묘사가 너무 짧거나 모호함 → 구체적인 음향 3가지 이상 나열

```
수정 전:
[Audio: music]

수정 후:
[Audio: slow melancholic piano melody, quiet ambient café noise,
        rain on window, occasional coffee cup clink]
```

**케이스 3 — 대사가 불명확함:**
- 대사를 직접 인용 부호로 명시

```
[Audio: Character says clearly: "We need to leave. Now."
        tense whisper, urgency in voice]
```

---

## 문제 유형 E — 클립 간 캐릭터 외모가 달라짐

**증상:** 같은 캐릭터를 여러 클립에서 생성했는데 매번 외모가 다름

**원인:** Veo 3는 클립 간 캐릭터 정보를 자동으로 기억하지 않음

**해결법:**

모든 클립에 **동일한 캐릭터 묘사 블록**을 복사해서 붙여넣습니다.

```
[캐릭터 블록 — 모든 장면에 동일하게 반복]
A 35-year-old Korean woman, short straight black hair with blunt bangs,
sharp jawline, slim athletic build, wearing a dark navy trench coat,
white shirt visible at collar, small silver earrings.
```

**참조 이미지 병행 사용:**

Google Flow에서 참조 이미지(Reference Image)를 업로드하면 외모 일관성이 크게 향상됩니다. (자세한 내용은 16장 참조)

---

## 문제 유형 F — 원치 않는 요소가 포함됨

**증상:** 배경에 불필요한 사람, 텍스트, 어색한 오브젝트가 등장

**해결법:**

`[Avoid: ...]` 블록으로 명시적 제거. (자세한 내용은 31장 네거티브 프롬프팅 참조)

```
[Avoid: text on screen, extra people in background,
        cluttered objects, cartoonish elements]
```

---

## 문제 유형 G — 움직임이 어색하거나 과함

**증상:** 캐릭터 동작이 부자연스럽거나, 카메라가 과도하게 움직임

**해결법:**

움직임의 **속도와 방식**을 구체적으로 지정합니다.

```
너무 빠른 움직임:
"slow deliberate movement, unhurried pace"
"smooth controlled motion, no sudden jerks"

너무 과한 카메라 무빙:
"static camera, tripod-mounted, no camera movement"
"gentle slow dolly, imperceptible movement"

부자연스러운 신체 동작:
"natural realistic human movement, subtle gestures only"
"minimal movement, slight weight shift and breathing visible"
```

---

## 문제 유형 H — 영상에 텍스트/자막이 생성됨

**증상:** 화면에 원치 않는 문자, 자막, 타이틀이 표시됨

**원인:**
- 프롬프트에 "title", "text", "caption" 등의 단어가 포함됨
- 뉴스·광고 스타일 장면에서 자동 생성되는 경우

**해결법:**

```
[Avoid: text overlay, subtitles, captions, title cards,
        on-screen text of any kind, watermarks]
```

또는 인라인으로:

```
... no text on screen, no subtitles, no captions, clean video only ...
```

---

## 문제 유형 I — 생성 거부 또는 오류

**증상:** 영상이 생성되지 않거나, "콘텐츠 정책" 관련 메시지가 뜸

**원인 확인:**
- 프롬프트에 실제 인물(유명인) 이름이 포함된 경우
- 폭력·선정적 표현이 포함된 경우
- 너무 긴 프롬프트(600자 이상)로 인한 처리 오류

**해결법:**

```
실제 인물 언급 대신:
"a famous actor" → "a charismatic middle-aged man with strong features"

폭력적 표현 완화:
"brutal fight" → "intense combat scene, action movie style"

너무 긴 프롬프트:
핵심 요소만 남기고 200~300자 내외로 줄이기
```

---

## 반복 실패 시 대응 전략

같은 프롬프트를 3회 이상 수정해도 원하는 결과가 나오지 않을 때:

### 전략 1: 분리 생성 후 편집 합성

복잡한 장면을 한 프롬프트에 담으려 하지 말고, 요소를 나눠 생성합니다.

```
원래 목표: "캐릭터 A와 B가 눈 덮인 산 정상에서 대화하는 장면"

분리 전략:
- 프롬프트 1: 눈 덮인 산 정상 배경만 생성
- 프롬프트 2: 캐릭터 A 단독 생성
- CapCut에서 합성
```

### 전략 2: 레퍼런스 이미지 활용

원하는 색감, 구도, 스타일의 이미지를 직접 업로드해 방향을 시각적으로 제시합니다.

### 전략 3: 단계별 간소화

완성 프롬프트를 50% 줄인 간소화 버전으로 먼저 테스트한 뒤, 점진적으로 요소를 추가합니다.

```
간소화 버전 (테스트):
"A woman in red dress walks through Tokyo market at night,
film style, medium shot."

요소 추가 (확인 후):
+ neon lights reflecting on wet pavement
+ [Audio: market noise, rain]
+ slow tracking shot
```

---

## 빠른 참조 — 증상별 해결 키워드

| 증상 | 추가할 키워드 |
|------|------------|
| 장면이 의도와 다름 | 장소·인물·시간을 각각 구체화 |
| 구도가 안 맞음 | 샷 타입 + 앵글 + 움직임 명시 |
| 색감이 안 맞음 | 광원 + 색온도 키워드 추가 |
| 오디오 없음 | 모델 Veo 3.1 이상 선택 + `[Audio: ...]` |
| 캐릭터 불일치 | 동일 캐릭터 묘사 블록 복붙 |
| 불필요한 요소 | `[Avoid: ...]` 블록 추가 |
| 움직임 어색 | 속도·방식 구체화 |
| 텍스트 표시 | `[Avoid: text overlay, subtitles]` |
| 생성 거부 | 실제 인물 제거, 표현 순화, 길이 단축 |
