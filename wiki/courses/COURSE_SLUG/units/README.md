# units/ — 단원 페이지

강의 단원마다 페이지 하나다.

- 파일 이름: `NN-<slug>.md` — NN은 강의 순서 (예: `03-process-scheduling.md`). `raw/.../lectures/`의 파일 번호와 맞춘다.
- 형식: [templates/unit.md](../../../../templates/unit.md) — 요약, 핵심 개념(개념 페이지 링크), 공식·알고리즘, 강의자료 속 예제, 출제 경향 링크, 관련 단원.
- 근거: **공식 자료(A)만**. 후기 내용은 여기 쓰지 않고 `exam-trends.md`로 링크만 한다.
- 개념의 자세한 설명은 `wiki/concepts/`에 두고, 여기서는 이 과목에서의 맥락만 짧게 쓴다.
- frontmatter `final_scope:`로 기말 범위인지 표시한다.
