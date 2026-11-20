# wiki/courses/COURSE_SLUG/ — {과목명}

| 파일·폴더 | 내용 | 근거 자료 | 템플릿 |
|---|---|---|---|
| `overview.md` | 과목 개요: 기본 정보, 기말 범위, 단원 목록, 바로가기 | A (+ 출제 비중 열만 B) | [course-overview](../../../templates/course-overview.md) |
| `exam-trends.md` | 출제 경향: 단원별 빈도, 문제 형식, 학기별 정리, 변화 | **B만** | [exam-trends](../../../templates/exam-trends.md) |
| [sources.md](sources.md) | 자료 등록부: 반영된 raw 파일 목록과 등급·학기 | — | — |
| [units/](units/) | 단원 페이지 | A만 | [unit](../../../templates/unit.md) |
| [practice/](practice/) | 연습문제 세트 | 출제 근거 B, 정답·해설 A | [practice-set](../../../templates/practice-set.md) |

`overview.md`와 `exam-trends.md`는 첫 Ingest 때 만들어진다.

## 공부 흐름 (추천)

1. `overview.md`에서 기말 범위와 단원 목록 확인
2. `exam-trends.md`에서 어느 단원이 자주 나왔는지 확인
3. 해당 `units/` 페이지와 링크된 개념 페이지로 공부
4. `practice/` 연습문제로 확인 (또는 Claude에게 새로 만들어 달라고 요청)
