# .company/CLAUDE.md 생성 템플릿

조직 구축（Step 5）시에 아래 템플릿을 사용하여 `.company/CLAUDE.md`를 생성한다.
`{{...}}`의 변수는 온보딩 데이터로 치환한다.

---

```markdown
# Company

## 조직 개요

- **오너**: {{OWNER_NAME}}
- **사업・활동**: {{BUSINESS_TYPE}}
- **미션・목표**: {{MISSION}}
- **언어**: {{LANGUAGE}}
- **생성일**: {{CREATED_DATE}}

## 조직 구조

```
당신（오너）
    │
  CEO（배분・의사결정）
    │
  ┌─┴─────────────────┐
  │                   │
비서실（상시）    [선택된 부서들]
```

## 상시 설치 부서

- **비서실** (`secretary/`) - 창구・태스크 관리・브레인스토밍
- **CEO** (`ceo/`) - 의사결정・배분 로직
- **리뷰** (`reviews/`) - 주간・월간 회고

## 선택된 부서

{{SELECTED_DEPARTMENTS}}

## 운영 규칙

### 기본 원칙
- 비서가 항상 엔트리 포인트
- 사용자에게 부서를 의식시키지 않는다
- 운영 모드 시작 시에는 이 파일을 먼저 읽는다

{{SELECTED_OPERATION_RULES}}

## 연락처・맥락

### 현재 포커스
{{CURRENT_FOCUS}}

### 주의사항
{{NOTES}}
```

---

## 변수 목록

| 변수 | 내용 | 예시 |
|------|------|------|
| `{{OWNER_NAME}}` | 오너 이름 | 홍길동 |
| `{{BUSINESS_TYPE}}` | 사업・활동 종류 | 개인 앱 개발, 프리랜서 |
| `{{MISSION}}` | 미션・목표 | SaaS로 월 100만원 수익 달성 |
| `{{LANGUAGE}}` | 공용어 | 한국어 |
| `{{CREATED_DATE}}` | 생성일 | 2026-03-13 |
| `{{SELECTED_DEPARTMENTS}}` | 선택된 부서 목록 | - 개발 (`engineering/`)\n- 리서치 (`research/`) |
| `{{SELECTED_OPERATION_RULES}}` | 선택된 운영 규칙 (Step 2e에서 선택) | `references/operation-rules.md`의 해당 규칙 내용을 삽입 |
| `{{CURRENT_FOCUS}}` | 현재 집중 사항 | MVP 개발 중 |
| `{{NOTES}}` | 특별 주의사항 | 없음 |
