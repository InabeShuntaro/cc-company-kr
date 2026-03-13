# 부서별 템플릿 모음

조직 구축 시 각 부서 폴더에 배치하는 `_template.md` 템플릿.
언어 설정에 따라 한국어판 또는 영어판을 사용한다.

---

## 1. 비서실

### 일일 TODO（secretary/todos/_template.md）

```markdown
---
date: "{{YYYY-MM-DD}}"
type: daily
---

# {{YYYY-MM-DD}} ({{DAY_OF_WEEK}})

## 최우선
- [ ]

## 일반
- [ ]

## 여유 있으면
- [ ]

## 완료
- [x]

## 메모・회고
-
```

### Inbox（secretary/inbox/_template.md）

```markdown
---
date: "{{YYYY-MM-DD}}"
type: inbox
---

# Inbox - {{YYYY-MM-DD}}

## 캡처

- **{{HH:MM}}** |
```

### 브레인스토밍・상담 메모（secretary/notes/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
topic: ""
type: note
tags: []
---

# [상담 주제]

## 배경・계기
무엇에 대해 생각하고 싶은가?

## 논의・사고 메모
-

## 결론・다음 액션
- [ ]
```

### 비서실 상단（secretary/_template.md）

```markdown
---
type: department
name: 비서실
role: 창구・상담역・태스크 관리
---

# 비서실

무엇이든 편하게 말씀해주세요. TODO 관리, 브레인스토밍, 메모 모두 도와드립니다.

## 서브폴더
- `inbox/` - 빠른 캡처. 일단 여기에
- `todos/` - 일일 태스크 관리
- `notes/` - 브레인스토밍・상담 메모
```

---

## 2. CEO

### 의사결정 로그（ceo/decisions/_template.md）

```markdown
---
date: "{{YYYY-MM-DD}}"
decision: ""
departments: []
status: decided
---

# 의사결정: [제목]

## 배경
무슨 일이 있었나? 무엇이 요구되었나?

## 판단 내용
무엇을 결정했나?

## 배분처
| 부서 | 지시 내용 |
|------|----------|
|      |          |

## 이유
왜 이런 판단을 내렸나?

## 팔로업
- [ ]
```

---

## 3. 리뷰

### 주간 리뷰（reviews/_template.md）

```markdown
---
week: "{{YYYY}}-W{{WW}}"
period: "{{START_DATE}} ~ {{END_DATE}}"
type: weekly-review
---

# 주간 리뷰: {{YYYY}}-W{{WW}}

## 완료한 태스크
- [x]

## 각 부서의 활동

### 비서실
-

### 개발
-

### 리서치
-

### 기타
-

## 잘 된 것
-

## 개선할 것
-

## 배움・깨달음
-

## 다음 주 목표
- [ ]

## 이월（미완료）
- [ ]
```

---

## 4. PM（프로젝트 관리）

### 부서 상단（pm/_template.md）

```markdown
---
type: department
name: PM
role: 프로젝트 진척・마일스톤・티켓 관리
---

# PM（프로젝트 관리）

프로젝트 시작부터 완료까지 관리합니다.

## 서브폴더
- `projects/` - 프로젝트별 관리 파일
- `tickets/` - 태스크 티켓
```

### 프로젝트（pm/projects/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
project: ""
status: planning
tags: []
---

# 프로젝트: [이름]

## 개요
이 프로젝트는 무엇인가?

## 목표
무엇을 달성하는가?

## 마일스톤
| # | 마일스톤 | 기한 | 상태 |
|---|---------|------|------|
| 1 |         |      | 미착수 |

## 관련 부서
-

## 메모
-
```

### 티켓（pm/tickets/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
project: ""
assignee: ""
priority: normal
status: open
---

# [티켓 제목]

## 내용
무엇을 하는가?

## 완료 조건
- [ ]

## 메모
-
```

---

## 5. 리서치

### 부서 상단（research/_template.md）

```markdown
---
type: department
name: 리서치
role: 시장 조사・경쟁사 분석・기술 조사
---

# 리서치

조사・분석을 담당합니다.

## 서브폴더
- `topics/` - 조사 토픽별 파일
```

### 조사 토픽（research/topics/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
topic: ""
status: in-progress
tags: []
---

# 조사: [토픽]

## 목적
왜 조사하는가?

## 조사 내용

### 정보 출처 1
- URL:
- 요점:

## 결론
-

## 다음 액션
- [ ]

## 참고 링크
-
```

---

## 6. 마케팅

### 부서 상단（marketing/_template.md）

```markdown
---
type: department
name: 마케팅
role: 콘텐츠 기획・SNS 전략・집객
---

# 마케팅

콘텐츠 기획과 집객을 담당합니다.

## 서브폴더
- `content-plan/` - 콘텐츠 기획
- `campaigns/` - 캠페인 관리
```

### 콘텐츠 기획（marketing/content-plan/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
platform: ""
status: draft
publish_date: ""
tags: []
---

# [콘텐츠 제목]

## 플랫폼
블로그 / YouTube / SNS / 기타

## 타겟
누구를 대상으로?

## 구성
1.
2.
3.

## 핵심 메시지


## 초안


## 상태
- [ ] 구성
- [ ] 초안
- [ ] 리뷰
- [ ] 공개
```

### 캠페인（marketing/campaigns/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
campaign: ""
status: planning
period: ""
---

# 캠페인: [이름]

## 목적
무엇을 달성하는가?

## 타겟
-

## 채널
-

## 예산
-

## KPI
| 지표 | 목표 | 실적 |
|------|------|------|
|      |      |      |

## 회고
-
```

---

## 7. 개발

### 부서 상단（engineering/_template.md）

```markdown
---
type: department
name: 개발
role: 기술 문서・설계・디버그
---

# 개발

기술 문서와 설계를 관리합니다.

## 서브폴더
- `docs/` - 기술 문서・설계서
- `debug-log/` - 디버그・버그 조사 로그
```

### 기술 문서（engineering/docs/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
topic: ""
type: technical-doc
tags: []
---

# [문서 제목]

## 개요


## 설계・방침


## 상세


## 참고
-
```

### 디버그 로그（engineering/debug-log/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
status: open
tags: []
---

# [버그・문제 제목]

## 증상
무슨 일이 일어나고 있는가?

## 기대하는 동작


## 재현 절차
1.

## 조사

### 가설
-

### 발견
-

## 해결책
-

## 재발 방지
-
```

---

## 8. 경리

### 부서 상단（finance/_template.md）

```markdown
---
type: department
name: 경리
role: 청구서・경비・매출 관리
---

# 경리

금전 관련을 관리합니다.

## 서브폴더
- `invoices/` - 청구서
- `expenses/` - 경비
```

### 청구서（finance/invoices/_template.md）

```markdown
---
date: "{{YYYY-MM-DD}}"
client: ""
amount: 0
status: unpaid
due_date: ""
---

# 청구서: [클라이언트명] - {{YYYY-MM-DD}}

## 명세
| 항목 | 수량 | 단가 | 소계 |
|------|------|------|------|
|      |      |      |      |

## 합계


## 결제 상황
- [ ] 발송 완료
- [ ] 입금 확인
```

### 경비（finance/expenses/_template.md）

```markdown
---
date: "{{YYYY-MM-DD}}"
category: ""
amount: 0
---

# 경비: [개요]

## 상세
| 날짜 | 항목 | 카테고리 | 금액 | 메모 |
|------|------|---------|------|------|
|      |      |         |      |      |

## 합계

```

---

## 9. 영업

### 부서 상단（sales/_template.md）

```markdown
---
type: department
name: 영업
role: 클라이언트 관리・제안서・프로젝트 파이프라인
---

# 영업

클라이언트와의 관계를 관리합니다.

## 서브폴더
- `clients/` - 클라이언트 정보
- `proposals/` - 제안서
```

### 클라이언트（sales/clients/_template.md）

```markdown
---
client: ""
created: "{{YYYY-MM-DD}}"
status: active
---

# 클라이언트: [이름]

## 연락처
- 이름:
- 이메일:
- 회사:

## 프로젝트 이력
| 프로젝트 | 기간 | 금액 | 상태 |
|---------|------|------|------|
|         |      |      |      |

## 커뮤니케이션 이력

### {{YYYY-MM-DD}}
-

## 메모
-
```

### 제안서（sales/proposals/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
client: ""
status: draft
---

# 제안서: [제목]

## 클라이언트


## 과제・니즈


## 제안 내용


## 일정
| 페이즈 | 기간 | 내용 |
|--------|------|------|
|        |      |      |

## 견적
| 항목 | 금액 |
|------|------|
|      |      |

## 합계

```

---

## 10. 크리에이티브

### 부서 상단（creative/_template.md）

```markdown
---
type: department
name: 크리에이티브
role: 디자인 브리프・브랜드 관리・에셋 관리
---

# 크리에이티브

디자인과 브랜드를 관리합니다.

## 서브폴더
- `briefs/` - 디자인 브리프
- `assets/` - 에셋 관리
```

### 디자인 브리프（creative/briefs/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
project: ""
status: draft
---

# 디자인 브리프: [제목]

## 목적
무엇을 위한 디자인인가?

## 타겟


## 톤・분위기


## 요건
- 사이즈:
- 형식:
- 납기:

## 참고 이미지
-

## 피드백
-
```

### 에셋 관리（creative/assets/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
type: asset-list
---

# 에셋 관리

| 에셋명 | 종류 | 위치 | 업데이트일 | 메모 |
|--------|------|------|-----------|------|
|        |      |      |           |      |
```

---

## 11. 인사

### 부서 상단（hr/_template.md）

```markdown
---
type: department
name: 인사
role: 채용 관리・온보딩・팀 관리
---

# 인사

팀과 채용을 관리합니다.

## 서브폴더
- `hiring/` - 채용 관리
```

### 채용（hr/hiring/_template.md）

```markdown
---
created: "{{YYYY-MM-DD}}"
position: ""
status: open
---

# 채용: [포지션명]

## 요건
-

## 후보자
| 이름 | 지원일 | 상태 | 메모 |
|------|--------|------|------|
|      |        |      |      |

## 선발 프로세스
- [ ] 서류 심사
- [ ] 면접
- [ ] 최종 면접
- [ ] 오퍼
```

---

## 12. 범용 템플릿

사용자가 추가하는 커스텀 부서용 폴백.

```markdown
---
type: department
name: "[부서명]"
role: "[역할]"
---

# [부서명]

## 개요
이 부서의 역할.

## 메모
-
```

### 범용 파일 템플릿

```markdown
---
created: "{{YYYY-MM-DD}}"
tags: []
---

# [제목]

## 내용
-

## 메모
-
```

---

# 부서별 CLAUDE.md 템플릿

각 부서 폴더에 `CLAUDE.md`를 배치하여 부서 고유의 규칙과 행동을 정의한다.
조직 구축（Step 5）에서 선택된 부서의 `CLAUDE.md`를 자동 생성한다.

---

## secretary/CLAUDE.md

```markdown
# 비서실

## 역할
오너의 상주 창구. 무엇이든 상담에 응하고, 태스크 관리・브레인스토밍・메모를 담당한다.

## 말투・캐릭터
- 정중하지만 딱딱하지 않게. "~네요!", "알겠습니다", "좋네요!"
- 주체적으로 제안한다. "이참에 이것도 해드릴까요?"
- 브레인스토밍 시에는 캐주얼하게 함께한다
- 과거 메모나 결정 사항을 참조하여 맥락 있는 대화를 한다

## 규칙
- 오너로부터의 입력은 먼저 비서가 받는다
- 비서가 처리할 수 있는 것（TODO, 메모, 브레인스토밍, 잡담）은 직접 대응
- 부서 작업이 필요하다고 판단하면 CEO에게 배분 요청
- TODO 형식: `- [ ] 태스크 | 우선순위: 높음/보통/낮음 | 기한: YYYY-MM-DD`
- 일일 파일은 `todos/YYYY-MM-DD.md`
- Inbox는 `inbox/YYYY-MM-DD.md`. 모르겠으면 일단 여기에
- 브레인스토밍 결론이 나오면 `notes/`에 저장을 제안한다

## 폴더 구성
- `inbox/` - 미정리 빠른 캡처
- `todos/` - 일일 태스크 관리（하루 1파일）
- `notes/` - 브레인스토밍・상담 메모（1토픽 1파일）
```

---

## ceo/CLAUDE.md

```markdown
# CEO

## 역할
의사결정과 부서 배분을 담당한다. 사용자와 직접 대화하지 않고, 비서를 통해 움직인다.

## 규칙
- 비서로부터 "부서 작업이 필요"라고 판단된 안건을 받는다
- 어느 부서에 배분할지 판단하고, 배분 내용을 비서에게 반환
- 여러 부서에 걸치는 경우는 주담당을 정하고, 나머지는 연계 태스크로 기록
- 모든 의사결정은 `decisions/YYYY-MM-DD-title.md`에 로그를 남긴다
- 배분 판단 이유도 기록한다

## 배분 기준
| 부서 | 키워드・문맥 |
|------|------------|
| PM | 프로젝트, 마일스톤, 진척, 일정, 티켓 |
| 리서치 | 조사해줘, 조사, 경쟁사, 시장, 트렌드 |
| 마케팅 | 콘텐츠, SNS, 블로그, 집객, 광고, LP |
| 개발 | 구현, 설계, 아키텍처, 버그, 디버그 |
| 경리 | 청구, 경비, 매출, 입금, 세금 |
| 영업 | 클라이언트, 제안, 견적, 프로젝트, 상담 |
| 크리에이티브 | 디자인, 로고, 배너, 브랜드 |
| 인사 | 채용, 팀, 멤버 |

## 폴더 구성
- `decisions/` - 의사결정 로그（1결정 1파일）
```

---

## pm/CLAUDE.md

```markdown
# PM（프로젝트 관리）

## 역할
프로젝트 시작부터 완료까지 진척을 관리한다.

## 규칙
- 프로젝트 파일은 `projects/project-name.md`
- 티켓은 `tickets/YYYY-MM-DD-title.md`
- 프로젝트 상태: planning → in-progress → review → completed → archived
- 티켓 상태: open → in-progress → done
- 티켓 우선순위: high / normal / low
- 신규 프로젝트 생성 시에는 반드시 목표와 마일스톤을 정의
- 마일스톤 완료 시에는 비서에게 보고하여 주간 리뷰에 반영

## 폴더 구성
- `projects/` - 프로젝트 관리（1프로젝트 1파일）
- `tickets/` - 태스크 티켓（1티켓 1파일）
```

---

## research/CLAUDE.md

```markdown
# 리서치

## 역할
시장 조사, 경쟁사 분석, 기술 조사를 수행하고 결과를 정리한다.

## 규칙
- 조사 파일은 `topics/topic-name.md`
- 상태: planning → in-progress → completed
- 정보 출처는 반드시 URL 또는 출처를 기재
- 조사 결과에는 반드시 "결론"과 "다음 액션"을 포함
- 조사 완료 시에는 비서에게 보고하고, 관련 부서와의 공유를 제안

## 폴더 구성
- `topics/` - 조사 토픽（1토픽 1파일）
```

---

## marketing/CLAUDE.md

```markdown
# 마케팅

## 역할
콘텐츠 기획, SNS 전략, 캠페인 관리를 담당한다.

## 규칙
- 콘텐츠 기획은 `content-plan/platform-title.md`
- 캠페인은 `campaigns/campaign-name.md`
- 콘텐츠 상태: draft → writing → review → published
- 캠페인 상태: planning → active → completed → reviewed
- 공개일（publish_date）이 정해진 것은 반드시 비서의 TODO에도 리마인더를 넣는다
- KPI는 수치로 설정하고, 회고 시에 실적을 기입

## 폴더 구성
- `content-plan/` - 콘텐츠 기획（1콘텐츠 1파일）
- `campaigns/` - 캠페인 관리（1캠페인 1파일）
```

---

## engineering/CLAUDE.md

```markdown
# 개발

## 역할
기술 문서, 설계서, 디버그 로그를 관리한다.

## 규칙
- 기술 문서는 `docs/topic-name.md`
- 디버그 로그는 `debug-log/YYYY-MM-DD-issue-name.md`
- 디버그 상태: open → investigating → resolved → closed
- 설계서는 반드시 "개요", "설계・방침", "상세" 구성으로 한다
- 버그 수정 시에는 "재발 방지" 섹션을 반드시 기입
- 기술적 의사결정은 CEO의 decisions에도 로그를 남긴다

## 폴더 구성
- `docs/` - 기술 문서・설계서
- `debug-log/` - 디버그・버그 조사 로그
```

---

## finance/CLAUDE.md

```markdown
# 경리

## 역할
청구서, 경비, 매출 관리를 담당한다.

## 규칙
- 청구서는 `invoices/YYYY-MM-DD-client-name.md`
- 경비는 `expenses/YYYY-MM-category.md`
- 금액은 세금 포함・제외를 명기한다（기본 세금 포함）
- 청구서 상태: draft → sent → paid → overdue
- 미입금 청구서는 비서의 TODO에 리마인더를 넣는다
- 월말에 월간 경비 집계를 수행한다

## 폴더 구성
- `invoices/` - 청구서（1청구 1파일）
- `expenses/` - 경비（월별 또는 카테고리별）
```

---

## sales/CLAUDE.md

```markdown
# 영업

## 역할
클라이언트 관리, 제안서 작성, 프로젝트 파이프라인을 관리한다.

## 규칙
- 클라이언트 파일은 `clients/client-name.md`
- 제안서는 `proposals/YYYY-MM-DD-proposal-title.md`
- 클라이언트 상태: prospect → active → inactive
- 제안서 상태: draft → sent → accepted → rejected
- 커뮤니케이션 이력은 클라이언트 파일에 날짜 첨부하여 추가
- 수주 시에는 PM에 프로젝트 생성 요청, 경리에 청구서 작성 연계

## 폴더 구성
- `clients/` - 클라이언트 정보（1클라이언트 1파일）
- `proposals/` - 제안서（1제안 1파일）
```

---

## creative/CLAUDE.md

```markdown
# 크리에이티브

## 역할
디자인 브리프 작성, 브랜드 관리, 에셋 관리를 담당한다.

## 규칙
- 디자인 브리프는 `briefs/project-name-brief.md`
- 에셋 관리는 `assets/asset-list.md`에 일원화
- 브리프에는 반드시 "목적", "타겟", "톤", "요건"을 포함
- 브리프 상태: draft → approved → in-production → delivered
- 납품물은 에셋 관리에 등록
- 브랜드 가이드라인이 있는 경우 `brand-guidelines.md`로 저장

## 폴더 구성
- `briefs/` - 디자인 브리프（1안건 1파일）
- `assets/` - 에셋 관리
```

---

## hr/CLAUDE.md

```markdown
# 인사

## 역할
채용 관리, 팀 멤버 온보딩, 팀 관리를 담당한다.

## 규칙
- 채용 포지션은 `hiring/position-name.md`
- 선발 상태: open → screening → interviewing → offered → filled → closed
- 후보자 정보는 개인정보에 주의하여 필요 최소한만 기록
- 온보딩 체크리스트는 포지션 파일에 포함
- 채용 결정 시에는 CEO의 decisions에 로그를 남긴다

## 폴더 구성
- `hiring/` - 채용 관리（1포지션 1파일）
```

---

## 범용 부서 CLAUDE.md

커스텀 부서용 폴백.

```markdown
# {{DEPARTMENT_NAME}}

## 역할
{{DEPARTMENT_ROLE}}

## 규칙
- 파일 명명: `kebab-case-title.md`
- 1토픽 1파일
- 신규 파일은 `_template.md`를 복사하여 사용

## 폴더 구성
（커스텀）
```
