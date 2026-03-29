# 73. Fast Mode vs High Quality 선택 기준

## 두 모드의 기본 특성

VEO 3는 두 가지 생성 모드를 제공합니다:

**Fast Mode (빠른 모드)**
- 생성 시간: 30초-2분
- 크레딧 소요: 약 10-20크레딧
- 품질: 괜찮지만 디테일이 부족함
- 용도: 아이디어 검증, 방향성 확인

**High Quality (고품질 모드)**
- 생성 시간: 2-8분
- 크레딧 소요: 약 100크레딧
- 품질: 최고 수준, 영화적 디테일
- 용도: 최종 납품, 포트폴리오, 게시

---

## 상세 비교표

| 비교 항목 | Fast Mode | High Quality |
|---------|-----------|-------------|
| 크레딧 비용 | ~10-20 | ~100 |
| 생성 속도 | 빠름 | 느림 |
| 프롬프트 반영도 | 70-80% | 90-95% |
| 세부 디테일 | 보통 | 매우 높음 |
| 조명 정밀도 | 기본 | 세밀함 |
| 얼굴 표현 | 단순 | 정교함 |
| 텍스처 품질 | 보통 | 고품질 |
| 움직임 유동성 | 보통 | 매끄러움 |
| 카메라 움직임 | 단순 | 영화적 |
| 음향 품질 | 기본 | 풍부함 |

---

## 언제 어떤 모드를 쓸지: 결정 트리

```
새 프롬프트를 작성했다
         ↓
처음 써보는 프롬프트인가?
   YES → Fast Mode로 먼저 테스트
   NO → 이미 검증된 프롬프트인가?
           YES → High Quality 바로 사용
           NO → Fast Mode로 확인 후 결정
         ↓
Fast Mode 결과 확인
         ↓
방향성이 맞는가?
   YES → High Quality로 최종 생성
   NO → 프롬프트 수정 후 다시 Fast Mode 테스트
         ↓
(반복)
         ↓
방향성 확정 → High Quality 최종 생성
```

---

## 비용 대비 효과 분석

### 시나리오: 새 콘텐츠 아이디어 테스트

**Fast Mode 없이 High Quality만 사용하는 경우:**
- 첫 시도: 100크레딧 (만족스럽지 않음)
- 수정 후: 100크레딧 (방향은 맞지만 세부 수정 필요)
- 재수정: 100크레딧 (완성)
- **총 300크레딧 소비**

**Fast Mode 먼저 사용하는 경우:**
- 첫 테스트: 15크레딧 (방향성 확인)
- 프롬프트 수정 후 테스트: 15크레딧 (개선 확인)
- 방향 확정 후 High Quality: 100크레딧 (최종)
- **총 130크레딧 소비 (57% 절약)**

---

## Fast Mode를 쓰면 안 되는 경우

Fast Mode도 훌륭하지만, 절대로 써서는 안 되는 상황이 있습니다:

1. **클라이언트 최종 납품물**: 차이가 눈에 띄게 납니다
2. **포트폴리오용 쇼케이스**: 당신의 실력을 보여주는 영상
3. **대형 플랫폼 업로드**: YouTube, Instagram에서 고품질이 노출에 유리
4. **감정 표현이 핵심인 장면**: 배우의 미세한 표정이 중요한 경우

---

## 모드별 프롬프트 차이

Fast Mode에서는 긴 프롬프트의 모든 디테일이 반영되지 않을 수 있습니다. 따라서:

**Fast Mode용 프롬프트**: 핵심 요소만 간략하게
```
"A wizard casting lightning in a dark cave, dramatic lighting, cinematic"
```

**High Quality용 프롬프트**: 모든 디테일을 포함한 완전한 묘사
```
"An elderly male wizard with long silver beard and deep navy robes stands at the center of a vast underground cavern. His outstretched hands crackle with blue-white lightning that arcs upward to the stalactites above. The lightning illuminates his weathered face with intense shadows. The camera slowly orbits around him at medium distance. Audio: thunderous crackling, distant echo, dramatic orchestral score building. Cinematic, 8K, dramatic chiaroscuro lighting."
```

---

## 실용 규칙 요약

1. **첫 테스트는 항상 Fast Mode**
2. **프롬프트 수정 반복도 Fast Mode**
3. **방향성이 확정된 후에만 High Quality**
4. **클라이언트 작업은 항상 High Quality로 납품**
5. **개인 실험과 학습은 Fast Mode로 크레딧 절약**
