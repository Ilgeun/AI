# raw/sources/ — 학사 원본 (A 공식)

교과과정, 졸업요건, 학사 규정, 학사일정, 학부 공지, 신청 안내 같은 **학부·대학 공식 자료**를 원본마다 폴더 하나씩 둔다. (과목 자료는 여기가 아니라 `raw/courses/`에 둔다.)

## 구조

```
raw/sources/
└── undergraduate-curriculum-2026/     ← source-id
    ├── curriculum.pdf                 ← 원본 파일 (원래 파일명 그대로 가능)
    └── metadata.yaml                  ← 원본 정보
```

- **source-id**: 영문 소문자 kebab-case + 연도. 예: `undergraduate-curriculum-2026`, `academic-calendar-2026`, `graduation-regulation-2024`, `notice-2026-11-15-double-major`.
- 한 원본에 파일이 여러 개(본문 + 별표 등)면 같은 폴더에 둔다.
- 같은 규정의 새 버전은 **새 source-id**로 넣는다 (옛 버전을 지우거나 덮어쓰지 않는다). 연도마다 적용 대상이 다르기 때문이다.

## metadata.yaml

원본을 넣을 때 같이 만들면 좋다. 없으면 Ingest 때 Claude가 만든다. 형식은 [templates/metadata.yaml](../../templates/metadata.yaml).

| 필드 | 뜻 |
|---|---|
| `issuer` | 발행 기관·부서 |
| `url` | 원문 주소 |
| `published`, `collected` | 게시일, 수집일 |
| `applies_to` | 적용 대상 (예: 2024학번 이후) |
| `valid_from`, `valid_until` | 유효 기간 |
| `supersedes` | 이 원본이 대체하는 이전 source-id |

## 위키에서는

원본마다 `wiki/sources/{source-id}.md` 요약 페이지가 생기고, 내용은 `wiki/rules/`, `wiki/procedures/`, `wiki/entities/`로 퍼진다.
