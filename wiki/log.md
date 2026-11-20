# 작업 기록 (log)

추가만 한다. 기존 항목은 고치지 않는다.
각 항목은 `## [YYYY-MM-DD] <ingest|query|lint|schema|init> | <제목>`으로 시작한다.
최근 5개 보기: `grep "^## \[" wiki/log.md | tail -5`

---

## [2026-11-20] init | 저장소 생성

- raw/, wiki/, templates/ 폴더 구조를 만들었다.
- CLAUDE.md(스키마), wiki/index.md, wiki/log.md, wiki/courses/COURSE_SLUG/sources.md를 만들었다.
- 템플릿 5종: course-overview, exam-trends, unit, concept, practice-set.
- 교과과정·졸업요건·공지는 빈 폴더로 자리만 잡았다.
- 과목 이름은 아직 정하지 않았다 (`COURSE_SLUG`).

## [2026-11-20] schema | 폴더별 README 추가

- 루트와 모든 raw/, wiki/, templates/ 폴더에 사람용 README.md를 추가했다.
- CLAUDE.md에 README 취급 규칙(위키 페이지·자료 아님, 규칙 변경 시 함께 갱신)과 Lint 항목을 추가했다.

## [2026-11-20] schema | llm-main 구조와 통합
- Source: 없음 (참고: llm-main 저장소의 AGENTS.md, README, 폴더 구조)
- Summary: 학사 정보용 구조(원본 요약, 규정, 절차, 조직, 분석, QA, 유효 기간, status)를 가져와 과목 공부 구조와 합쳤다. 학사 규정은 rules/로, 학문 개념은 concepts/로 나눴다. 로그 형식을 Source/Summary/Changed/Open questions로 바꿨다 (이전 항목은 그대로 둠).
- Changed: CLAUDE.md, README.md, .gitignore, templates/ (기존 5종 frontmatter 통일, source·rule·procedure·entity·qa·analysis·metadata.yaml 추가), wiki/index.md, wiki/overview.md (신규), wiki/{sources,rules,procedures,entities,analyses,qa,assets}/ (신규), raw/sources/ (신규), raw/·wiki/의 curriculum·graduation·notices 자리 폴더 삭제, 폴더별 README
- Open questions: 과목 이름 미정 (`COURSE_SLUG`). 첫 Ingest 대상 결정 필요.
