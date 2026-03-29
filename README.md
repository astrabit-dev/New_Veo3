# 처음 시작하는 Google Veo 3

이 책은 WikiDocs와 연동된 GitHub 리포지토리입니다.

## 사용 방법

1. `TOC.md` 파일에서 목차 구조를 정의하세요.
2. `pages/` 디렉토리에 마크다운 파일을 추가하세요.
3. 변경사항을 push하면 WikiDocs에 자동으로 반영됩니다.

## 페이지 정렬 규칙 (중요!)

WikiDocs는 페이지를 **제목 알파벳순**으로 자동 정렬합니다.
원하는 순서를 유지하려면 제목에 **번호를 붙이세요**:

```markdown
# TOC.md 예시
* [01. 시작하기](pages/01-getting-started.md)
  * [01-1. 설치](pages/01-1-install.md)
  * [01-2. 환경설정](pages/01-2-config.md)
* [02. 기본 문법](pages/02-basics.md)
* [03. 심화 학습](pages/03-advanced.md)
```

## 이미지 사용

이미지는 `assets/` 디렉토리에 저장하고 상대 경로로 참조하세요:

```markdown
![이미지 설명](./assets/example.png)
```
