# CLAUDE.md

이 저장소는 애플리케이션이 아니라 마크다운 문서 아카이브다. 빌드 도구, 패키지 매니저, 실행할 명령어가 없다. `pnpm`, `npm`, 빌드, 린트, 테스트를 시도하지 말 것.

렌더링은 GitHub이 담당한다. mermaid, KaTeX(`$`), 코드 구문 강조, 상대 경로 이미지, 제목 앵커, `.excalidraw` 미리보기가 모두 네이티브로 동작한다. 렌더링을 위한 코드를 추가할 이유가 없다.

## 디렉터리 규약

태그가 곧 디렉터리다. 문서 하나는 폴더 하나이며, 본문 파일명은 반드시 `README.md`다. GitHub은 폴더를 열 때 `README.md`만 자동 렌더링하고 `index.md`는 렌더링하지 않는다.

```text
javascript/README.md              태그에 문서가 하나뿐이거나 태그 자체를 다루는 문서
javascript/prototype/README.md    태그 아래 개별 주제 문서
javascript/prototype/images/      해당 문서의 이미지, 상대 경로로 참조
```

- 폴더명은 snake_case를 사용한다. 상위 태그명을 폴더명에 반복하지 않는다 (`javascript/prototype`이며 `javascript/js_prototype`이 아니다).
- 이미지는 문서와 같은 폴더의 `images/`에 두고 `images/파일명.webp`로 참조한다. 저장소 절대 경로를 쓰면 GitHub과 로컬 뷰어 양쪽에서 깨진다.
- 프론트매터를 쓰지 않는다. `title`, `tag`, `isPublished`, `folderName`은 각각 h1 제목, 디렉터리 경로, 본문 내 초안 표기로 대체됐다.
- 메타데이터 인덱스(`list.json`) 같은 생성 산출물이 없다. 문서를 추가한 뒤 실행할 후속 작업은 루트 `README.md`의 문서 수를 갱신하는 것뿐이다.

## 문서 작성

문서를 작성하거나 수정할 때는 `markdown-writer-local` 스킬을 사용한다. 문서 구조, 말투, 포맷, 금지 사항 등 글쓰기 규칙 전체가 해당 스킬에 정의되어 있다. 위의 디렉터리 규약이 스킬의 파일 위치·프론트매터 항목보다 우선한다.

초안 상태의 문서는 h1 바로 아래에 작성 중이라는 사실을 한 줄로 적는다.

## 히스토리

2023년 9월부터 2026년 7월까지 이 저장소는 Next.js 블로그였다. 앱 전체는 `blog-final` 태그에서 복원할 수 있고, 이관 배경은 루트 `README.md`에 적혀 있다. 앱 시절의 구조(FSD, shadcn, steiger)를 되살리거나 참고하지 말 것.
