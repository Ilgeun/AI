# templates/ — 페이지 템플릿

LLM이 새 위키 페이지를 만들 때 복사해서 쓰는 틀이다. CLAUDE.md와 함께 schema(규칙)의 일부다. **위키 페이지가 아니므로** index.md에 올리지 않고, Lint 대상도 아니다.

## 과목 공부

| 템플릿 | 만들어지는 페이지 | 위치 |
|---|---|---|
| [course-overview.md](course-overview.md) | 과목 개요 (기본 정보, 기말 범위, 단원 목록) | `wiki/courses/<과목>/overview.md` |
| [exam-trends.md](exam-trends.md) | 출제 경향 (후기 기반, 학기별) | `wiki/courses/<과목>/exam-trends.md` |
| [unit.md](unit.md) | 단원 (요약, 핵심 개념, 공식·예제) | `wiki/courses/<과목>/units/NN-<slug>.md` |
| [concept.md](concept.md) | 학문 개념 (과목 공통 정의, 과목별 쓰임) | `wiki/concepts/<slug>.md` |
| [practice-set.md](practice-set.md) | 연습문제 세트 (문제, 출제 근거, 정답·해설) | `wiki/courses/<과목>/practice/YYYY-MM-DD-<범위>.md` |

## 학사 정보

| 템플릿 | 만들어지는 페이지 | 위치 |
|---|---|---|
| [source.md](source.md) | 원본 요약 (원본 정보, 요약, 반영 문서, 미해결) | `wiki/sources/{source-id}.md` |
| [rule.md](rule.md) | 규정·제도 (적용 대상별 기준, 예외) | `wiki/rules/<slug>.md` |
| [procedure.md](procedure.md) | 절차 (대상, 기한, 제출처, 서류, 단계) | `wiki/procedures/<slug>.md` |
| [entity.md](entity.md) | 조직·시설·시스템·부서 | `wiki/entities/<slug>.md` |

## 공통

| 템플릿 | 만들어지는 페이지 | 위치 |
|---|---|---|
| [qa.md](qa.md) | 질문과 답변 (결론 → 근거 → 예외 → 확인 필요) | `wiki/qa/<slug>.md` |
| [analysis.md](analysis.md) | 비교·종합 분석, Lint 결과 | `wiki/analyses/<slug>.md` |
| [metadata.yaml](metadata.yaml) | 원본 정보 파일 (위키 페이지 아님) | `raw/sources/{source-id}/metadata.yaml` |

## 템플릿 읽는 법

- `<...>`, `{...}`, `…`, `NN`, `YYYY-MM-DD`는 채워 넣을 자리다.
- `<!-- ... -->` 주석은 쓰는 규칙이다.
- `^[...]`는 출처 표기 자리다. 모든 사실 문장 끝에 붙는다.
- 맨 위 `---` 사이는 frontmatter다. 공통 필드: `title, type, status, sources, updated, tags`. 규정·절차에는 `applies_to, valid_from, valid_until`이 더 있다.
- `status`: `draft`(작성 중) / `active`(현재 유효) / `stale`(대체됐거나 기간 지남).

## 템플릿을 바꾸려면

템플릿과 [CLAUDE.md](../CLAUDE.md)를 함께 고친다. 이미 만들어진 페이지는 Claude에게 "새 템플릿에 맞춰 기존 페이지 정리해 줘"라고 하면 맞춰진다.
