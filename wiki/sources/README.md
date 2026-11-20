# wiki/sources/ — 원본 요약

`raw/sources/{source-id}/`의 학사 원본마다 요약 페이지 하나를 둔다.

- 파일 이름: `{source-id}.md` (raw 폴더 이름과 같게)
- 형식: [templates/source.md](../../templates/source.md) — 원본 정보(발행 기관, 게시일, 적용 대상, 유효 기간), 요약, 핵심 내용, 이 원본을 반영한 문서, 미해결 사항.
- 새 버전 원본이 나오면 옛 요약 페이지는 지우지 않고 `status: stale`, `superseded_by:`로 표시한다.
- **과목 자료는 여기에 요약 페이지를 만들지 않는다.** 과목 자료는 `wiki/courses/<과목>/sources.md` 등록부에 올리고, 단원 페이지가 요약 역할을 한다.
