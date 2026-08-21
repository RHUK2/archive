# 아카이브

2023년부터 쌓아온 기술 문서 아카이브다. 태그가 곧 디렉터리이고, 폴더를 열면 문서가 바로 렌더링된다.

| 주제 | 문서 | 주제 | 문서 |
| --- | --- | --- | --- |
| [javascript](javascript) | 11 | [network](network) | 4 |
| [security](security) | 8 | [dom](dom) | 3 |
| [browser](browser) | 6 | [aws](aws) | 2 |
| [linux](linux) | 6 | [cs](cs) | 2 |
| [react](react) | 6 | [nodejs](nodejs) | 2 |
| [style](style) | 5 | [typescript](typescript) | 1 |
| [db](db) | 1 | [git](git) | 1 |
| [design](design) | 1 | [i18n](i18n) | 1 |
| [issue](issue) | 1 | [math](math) | 1 |
| [nextjs](nextjs) | 1 | [regexp](regexp) | 1 |

그 외에 [algorithm](algorithm)은 TypeScript 구현 모음이고, [career](career)는 경력 정리다.

## 왜 앱이 없는가

이 저장소는 2023년 9월부터 2026년 7월까지 Next.js로 만든 개인 블로그였다. 2026년 8월에 앱을 걷어내고 마크다운만 남겼다.

이유는 앱이 하던 일의 대부분이 GitHub 렌더러의 재구현이었기 때문이다. mermaid, KaTeX, 코드 구문 강조, 상대 경로 이미지, 목차 앵커까지 GitHub이 이미 전부 처리한다. 앱이 추가로 제공하던 것은 태그 탐색, 검색, 커스텀 도메인 셋뿐이었는데, 태그는 디렉터리 구조로 대체했고, 검색은 GitHub 검색과 로컬 `grep`으로 충분했으며, 도메인은 쓰지 않고 있었다. 독자가 나 혼자인 아카이브를 위해 Next.js, FSD, steiger, shadcn, React Query를 유지할 이유가 없었다.

앱 코드는 삭제된 것이 아니라 히스토리에 남아 있다. `blog-final` 태그를 체크아웃하면 마지막 상태 전체를 복원할 수 있다.

```bash
git checkout blog-final
```

이관 시점의 원본 자산 백업은 `~/personal/blog-assets-backup-20260820/`에 있다.
