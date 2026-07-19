# VATOS Design System

VATOS Design System은 VATOS의 문서, 발표자료, 보고서, 웹 콘텐츠, 데이터 표 및 시각화 자료에 공통으로 적용되는 디자인 기준이다.

이 저장소는 공통 디자인 기준, 문서 유형별 제작 가이드, 공식 브랜드 자산, 편집 가능한 템플릿, 참고자료 및 완성 예시를 함께 관리한다.

---

## Purpose

이 디자인 시스템의 목적은 다음과 같다.

- VATOS 산출물의 브랜드 일관성 유지
- 문서, PPT, 보고서 및 웹 콘텐츠의 디자인 품질 편차 감소
- AI 기반 문서 작성 시 참고할 수 있는 공통 기준 제공
- 컬러, 타이포그래피, 레이아웃, 컴포넌트 및 테마 사용 기준 관리
- 외부 제출용 문서의 전문성, 신뢰감 및 수정 가능성 확보
- 공식 로고와 브랜드 자산의 일관된 사용
- 파일명과 경로 변경에 따른 문서 수정 범위 최소화

---

## File Structure

```text
vatos-design-system/
├─ README.md
├─ DESIGN.md
├─ SKILL.md
│
├─ assets/
│  ├─ logos/
│  └─ themes/
│
├─ guides/
├─ templates/
├─ references/
└─ examples/
```

---

## Repository Areas

| Area | Role |
|---|---|
| `README.md` | 저장소의 목적, 구조, 사용 방법 및 운영 원칙을 설명하는 안내 문서 |
| `DESIGN.md` | 모든 산출물에 공통 적용되는 브랜드 및 디자인 기준 |
| `SKILL.md` | AI가 VATOS 디자인 시스템을 탐색하고 적용하는 실행 지침 |
| `assets/` | 공식 로고와 테마 이미지 등 승인된 브랜드 자산 |
| `guides/` | PPT, Word, HTML 등 문서 유형별 제작 기준과 공통 테마 적용 기준 |
| `templates/` | 복제하여 실제 산출물 작성에 사용하는 편집 가능한 원본 |
| `references/` | 레이아웃과 시각적 균형, 승인된 UI 컴포넌트의 형태·상태·상호작용을 확인하기 위한 참고자료 |
| `examples/` | 디자인 시스템이 적용된 실제 완성 산출물 |

---

## Resource Roles

문서 간 연결은 특정 파일명이나 경로보다 아래 역할명을 우선 사용한다.

| Resource Role | Meaning |
|---|---|
| `common-design-rules` | 모든 산출물에 공통 적용되는 브랜드, 컬러, 타이포그래피, 레이아웃 및 컴포넌트 기준 |
| `ppt-production-rules` | PPT 작성 시 적용하는 슬라이드 구성, 안전 영역, 중앙 배치, 밀도 및 출력 안정성 기준 |
| `word-production-rules` | Word 문서 작성 시 적용하는 페이지 흐름, 여백, 표 및 빈 페이지 방지 기준 |
| `html-production-rules` | HTML 작성 시 적용하는 구조, 컴포넌트, 상태, 상호작용, 접근성 및 반응형 기준 |
| `theme-usage-rules` | 산출물 목적과 정보량에 따른 테마 선택 및 조합 기준 |
| `layout-references` | 산출물 전반의 레이아웃, 위치, 정렬, 간격 및 시각적 균형을 확인하기 위한 공통 참고자료 |
| `ppt-layout-references` | PPT의 실제 레이아웃, 위치, 간격, 정렬감 및 콘텐츠 밀도를 확인하는 참고자료 |
| `brand-assets` | 공식 로고와 테마 이미지 등 승인된 브랜드 자산 |
| `document-templates` | 실제 문서 작성에 사용하는 편집 가능한 템플릿 |
| `document-examples` | 디자인 시스템이 적용된 실제 완성 결과물 |
| `component-references` | 승인된 UI 컴포넌트의 시각 형태, 상태 및 상호작용을 확인하기 위한 참고자료 |

역할명은 문서 간 참조와 AI 탐색을 위한 분류명이다. 실제 파일명이나 폴더명과 반드시 동일할 필요는 없다.

---

## Core Concept

VATOS Design System은 다음 방향성을 기준으로 한다.

```text
Refined, Urban, Professional, Technical, Trustworthy
```

VATOS 산출물은 화려한 장식보다 정보 구조, 가독성 및 명확한 메시지 전달을 우선한다.

전문적이지만 낡지 않고, 현대적이지만 가볍지 않은 균형을 지향한다.

여기서 Urban은 도시 사진, 건축물, 도로, 야경 또는 스카이라인을 의미하지 않는다. 정돈된 비대칭 구성, 깊은 네이비 명암, 구조적인 기하 표현, 현대적인 여백과 타이포그래피를 의미한다.

---

## Design Rule Priority

VATOS 산출물을 작성하거나 수정할 때 다음 순서로 판단한다.

1. 사용자가 제공한 원문과 명시 요청
2. 해당 산출물 유형의 제작 가이드
3. 문서 테마 적용 기준
4. 공통 디자인 기준
5. 사용자가 제공한 이미지, 아이콘 및 자료
6. 공식 브랜드 자산
7. 승인된 컴포넌트 참고자료
8. 레이아웃 참고자료
9. 편집 가능한 문서 템플릿
10. 디자인 시스템이 적용된 완성 예시
11. 저장소 운영 안내

특정 파일명이나 경로가 변경되더라도, 작업 목적과 일치하는 역할의 자료를 찾아 적용한다.

AI 또는 작성자는 원문에 없는 내용을 임의로 추가하지 않는다. 디자인 판단이 필요한 경우에는 사용자가 확인할 수 있는 예시나 대안을 우선 제시한다.

---

## Document Type Guidance

| Output Type | Primary Role | Additional Resources | Main Rule |
|---|---|---|---|
| PPT / Presentation | `ppt-production-rules` | `common-design-rules`, `theme-usage-rules`, `ppt-layout-references`, `brand-assets` | 제목 영역과 본문 영역을 분리하고, 콘텐츠 그룹을 중앙 안전 영역 안에서 가로·세로 균형 있게 배치한다. |
| Word / General Document | `word-production-rules` | `common-design-rules`, `brand-assets`, `document-templates` | 기본 여백, 페이지 흐름, 표 안정성 및 불필요한 빈 페이지 방지를 우선한다. |
| Excel | `common-design-rules` | `brand-assets`, `document-templates` | 데이터 가독성, 표 정렬, 인쇄 안정성 및 수정 가능성을 우선한다. |
| HTML / Web Document | `html-production-rules` | `common-design-rules`, `component-references`, `theme-usage-rules`, `brand-assets`, `document-examples` | HTML 전용 구조, 컴포넌트, 상태, 상호작용 및 접근성 기준을 우선 적용하고, 승인된 컴포넌트 참고자료를 함께 확인한다. |
| PDF | 원본 산출물의 적용 기준 | `document-examples` | 최종 배포 형태로 사용하며, 수정이 필요한 경우 원본 편집 파일에서 작업한다. |

### PPT Reference Usage

`ppt-layout-references` 역할의 자료는 PPT 내용 작성용 템플릿이 아니다.

다음 항목을 확인하기 위한 시각 참고자료로 사용한다.

- 슬라이드 유형별 활용 가능한 레이아웃
- 제목과 본문 콘텐츠의 실제 배치 위치
- 콘텐츠 그룹의 가로·세로 중앙 정렬
- 카드, 표, 차트 및 다이어그램 간 간격
- 슬라이드 상단 쏠림과 과도한 하단 여백 방지
- 레이아웃별 적정 콘텐츠 밀도와 권장 문장 길이

명시적 제작 규칙과 참고자료가 충돌할 경우에는 해당 문서 유형의 가이드를 우선 적용한다.

### Component Reference Usage

`component-references` 역할의 자료는 HTML 또는 웹 화면에서 승인된 UI 컴포넌트의 형태와 동작을 확인하기 위한 시각 참고자료이다.

다음 항목을 확인할 때 사용한다.

- 컴포넌트의 기본 형태와 정보 구조
- 선택, 활성, 비활성, 오류 및 로딩 상태
- 접기·펼치기, 선택, 날짜 지정 등 상호작용
- 컴포넌트 간 간격, 정렬 및 시각적 일관성
- HTML 전용 가이드에 정의된 동작이 실제 화면에서 어떻게 표현되는지

참고자료는 시각적 형태와 동작을 이해하기 위한 기준이며, 실제 화면의 목적과 데이터에 맞게 조정한다.
명시적 제작 규칙과 컴포넌트 참고자료가 충돌할 경우에는 `html-production-rules`를 우선 적용한다.

### Example Usage

`document-examples` 역할의 자료는 실제 완성 결과물이다.

동일한 유형의 문서를 작성할 때 다음 항목을 참고할 수 있다.

- 전체적인 디자인 완성도와 브랜드 인상
- 정보 위계와 섹션 구성
- 컬러, 타이포그래피 및 컴포넌트 조합
- 문서 유형에 적합한 콘텐츠 표현 방식

예시 파일의 내용이나 구조를 그대로 복제하지 않고, 작성 목적과 원문에 맞게 재구성한다.

승인된 예시는 고정 템플릿이 아니라 컬러 균형, 깊이감, 여백, 타이포그래피 위계 및 마감 수준을 판단하는 품질 기준으로 사용한다.

예시의 제목 위치, 도형 비율, 사선 위치, 면 분할 및 하단 구조를 그대로 반복 복제하지 않는다.

---

## Theme Reference Usage

`theme-usage-rules` 역할의 가이드는 표지, 섹션 구분, 내지 및 Closing의 기본 테마 적용 기준을 정의한다.

- 별도 디자인 요청이 없는 경우 Urban Navy 표지와 밝은 내지 조합을 기본으로 적용한다.
- 승인된 테마 예시는 고정 템플릿이 아니라 시각적 품질 기준으로 활용한다.
- 예시에서 컬러 면적 비율, 네이비 깊이감, Cyan 사용량, 여백, 타이포그래피 위계와 전문성을 우선 확인한다.
- 표지의 제목 위치, 사선 위치, 도형 개수, 면 분할 및 하단 구조를 그대로 반복하지 않는다.
- 사선 레이어는 선택 가능한 조형 방식 중 하나이며 필수 요소가 아니다.
- 표지에는 사선 레이어, 세로 밴드, 오프셋 프레임, 면 분할, 라인 그리드, 타이포그래피 중심 구성 등에서 하나의 주요 조형 방식을 선택할 수 있다.
- Cover, Section Divider, Closing은 같은 시각 언어를 공유하되 동일한 구도를 반복하지 않는다.
- Dark Theme와 Light Theme를 단순한 색상 견본 카드처럼 표현하지 않는다.
- 네이비 직사각형 하나만 배치하여 표지를 완성하지 않는다.
- 본문 전체를 단순 카드 나열형으로만 구성하지 않는다.

---

## How to Use

### For AI Document Creation

AI에게 VATOS 산출물 작성을 요청할 때는 특정 파일명을 나열하기보다 산출물 유형과 필요한 자료 역할을 명확히 전달한다.

권장 요청 형식:

```text
VATOS Design System을 적용하여 아래 산출물을 작성해줘.

문서 목적:
대상 독자:
산출물 형식:
반영할 원문:
적용할 테마:
사용할 로고:
강조할 내용:
제외할 내용:
수정 가능한 형태 필요 여부:
```

HTML 요청 시에는 적용 기준에 `html-production-rules`를 지정하고, 필요한 경우 `component-references`를 함께 확인하도록 요청한다.

PPT 요청 예시:

```text
VATOS Design System을 적용하여 고객 제출용 제안서 PPT를 작성해줘.

문서 목적: 신규 고객사 제안
대상 독자: 고객사 임원 및 실무 담당자
산출물 형식: PPT
적용 기준: PPT 제작 규칙, 문서 테마 적용 기준, 공통 디자인 기준
참고자료: PPT 레이아웃 참고자료와 승인된 테마 예시
적용 테마: Urban Navy Theme + Light Theme
사용 로고: 어두운 배경용 시그니처 로고
강조 내용: 기술 전문성, 안정성, 도입 효과
제외 내용: 내부 비용, 담당자 개인정보
수정 가능한 형태: 필요
```

---

## Brand Assets

VATOS 공식 브랜드 자산은 `assets/`에서 관리한다.

### Logo Assets

| Asset | Usage |
|---|---|
| `vatos-logo-signature-slogan-on-light.png` | 밝은 배경용 공식 시그니처와 슬로건 |
| `vatos-logo-signature-slogan-on-dark.png` | 어두운 배경용 공식 시그니처와 슬로건 |
| `vatos-logo-symbol-wordmark-stacked.png` | 심볼과 워드마크의 세로 조합 |
| `vatos-logo-symbol-only.png` | 아이콘, 워터마크, 썸네일 등 작은 브랜드 영역 |
| `vatos-logo-wordmark-only.png` | 좁은 영역, 푸터 및 보조 브랜드 표기 |

### Theme Assets

| Asset | Usage |
|---|---|
| `vatos-theme-default-urban-navy.png` | VATOS 기본 Urban Navy 테마의 색상과 분위기 참고 |

### Brand Asset Rules

- 승인된 공식 자산만 사용한다.
- 로고의 색상, 비율 및 형태를 임의로 변경하지 않는다.
- 로고에 그림자, 테두리, 그라데이션 또는 장식 효과를 추가하지 않는다.
- 밝은 배경과 어두운 배경에 맞는 로고를 구분하여 사용한다.
- 로고를 장식 패턴처럼 반복 사용하지 않는다.
- AI가 VATOS 로고나 유사 로고를 새로 생성하지 않는다.
- 외부 이미지나 아이콘은 사용 가능 여부가 명확한 경우에만 사용한다.

---

## Design Usage Principles

### Colors

- Urban Navy는 VATOS의 주요 브랜드 다크 배경으로 사용한다.
- Premium Dark는 검은색 메인 컬러가 아니라 깊이감 보조 다크 톤으로 사용한다.
- Vatos Cyan은 브랜드 포인트 컬러로 제한적으로 사용한다.
- Vatos Cyan을 성공, 개선 또는 완료 의미로 사용하지 않는다.

- 상태 의미는 Semantic Color를 사용한다.

### Typography

- 기본 서체는 Pretendard를 사용한다.
- 하나의 산출물 안에서 여러 서체를 섞지 않는다.
- 제목은 단순 라벨이 아니라 핵심 메시지가 드러나도록 작성한다.
- 본문은 긴 문단보다 짧은 문단과 간결한 목록을 우선한다.

### Layout

- 한 페이지 또는 슬라이드에는 하나의 핵심 메시지를 중심으로 구성한다.
- 정보량이 많으면 페이지, 슬라이드 또는 섹션을 분리한다.
- 여백은 빈 공간이 아니라 정보 구조를 만드는 요소로 사용한다.
- 표, 카드, 차트 및 긴 본문을 한 화면에 과도하게 혼합하지 않는다.

### Components

- 컴포넌트는 장식이 아니라 정보 구조를 명확하게 하기 위해 사용한다.
- 카드 하나에는 하나의 주제만 담는다.
- 표에는 헤더, 단위, 기준 및 정렬 규칙을 명확히 적용한다.
- Badge와 Tag는 색상만으로 의미를 전달하지 않고 텍스트 라벨을 함께 사용한다.

### Theme

- 모든 산출물을 Dark Theme로 만들지 않는다.
- 정보량이 많은 본문은 Light Theme를 우선 사용한다.
- 표지, 섹션 구분 및 Closing에는 Dark Theme 또는 Urban Navy Theme를 사용할 수 있다.
- 회사소개서, 제안서 및 영업용 소개 자료에는 Urban Navy Theme를 우선 적용한다.
- VATOS 테마는 특정 표지 레이아웃 하나를 반복하는 고정 템플릿이 아니다.
- 브랜드 컬러 역할과 시각적 품질은 유지하되 문서 목적에 따라 구도와 조형 방식을 다양하게 구성할 수 있다.
- 승인된 예시는 컬러 균형, 깊이감, 여백, 타이포그래피 위계와 전문성을 판단하는 품질 기준으로 사용한다.
- 예시의 제목 위치, 사선 위치, 도형 비율 및 면 분할을 그대로 복제하지 않는다.
- 사선 레이어는 선택 가능한 조형 방식 중 하나이며 필수 요소가 아니다.
- Cover, Section Divider, Closing은 같은 시각 언어를 공유하되 동일한 구도를 반복하지 않는다.
- 본문 전체를 단순 카드 나열형으로만 구성하지 않는다.

---

## AI Writing Rules

AI는 VATOS 문서 작성 시 다음 기준을 따른다.

- 제공된 원문에 없는 내용을 임의로 추가하지 않는다.
- 고객사명, 프로젝트명, 수치, 일정, 금액 및 계약명은 원문 기준으로 유지한다.
- 자료에 없는 내용은 `추가 확인 필요` 또는 `자료 미제공`으로 표시한다.
- 성능 개선율, 비용 절감률 및 매출 효과는 근거 없이 과장하지 않는다.
- 고객사 자료, 계약 정보, 개인정보, 계정 정보 및 내부 대외비 자료는 업로드 가능 여부를 확인한다.
- 외부 배포용 문서는 사람이 최종 검수한다.

---

## Editable Output Principle

PPT, Word, Excel 및 HTML 등 수정 가능한 산출물에서는 로고와 원본 이미지 자산을 제외한 요소를 가능한 한 편집 가능한 형태로 작성한다.

- 텍스트는 편집 가능한 텍스트로 작성한다.
- 표는 편집 가능한 표로 작성한다.
- 카드, 다이어그램 및 프로세스 구조는 도형과 텍스트로 구성한다.
- 차트는 가능한 한 편집 가능한 차트로 작성한다.
- 슬라이드 전체, 표, 카드 또는 텍스트 묶음을 통이미지로 삽입하지 않는다.
- 로고, 사진, 스크린샷 및 승인된 원본 이미지는 이미지로 사용할 수 있다.

---

## Naming Rules

### General Rules

- 일반 파일명과 폴더명은 영문 소문자와 하이픈을 사용한다.
- 공백, 언더스코어 및 대소문자 혼합을 사용하지 않는다.
- 문서 유형은 `ppt`, `word`, `excel`, `html`, `pdf`처럼 짧고 익숙한 이름을 사용한다.
- 역할명은 `template`, `reference`, `library`, `example`처럼 전체 단어를 사용한다.
- `ref`, `tpl`, `ex`, `temp` 같은 축약어는 사용하지 않는다.
- 루트 핵심 문서는 `README.md`, `DESIGN.md`, `SKILL.md` 표기를 유지한다.

### File Name Patterns

```text
Guide
[document-type].md

Template
vatos-[document-type]-template.[extension]

Reference
vatos-[document-type]-[subject]-reference.[extension]

Layout Library
vatos-[document-type]-layout-library.[extension]

Theme
vatos-theme-[status]-[theme-name].[extension]

Logo
vatos-logo-[combination]-[usage].[extension]

Completed Example
vatos-[content-or-purpose].[extension]
```

완성 예시는 파일 형식이 아니라 실제 산출물의 주제와 목적이 드러나도록 명명한다.

---

## Maintenance Rules

- 파일 또는 폴더를 추가할 때 기존 분류와 명명 규칙을 우선 적용한다.
- 문서 간 연결은 가능한 한 역할명으로 작성한다.
- 특정 파일명이나 경로를 직접 참조해야 할 때는 변경 시 함께 수정해야 하는 문서를 확인한다.
- 동일한 파일을 여러 폴더에 복사하여 관리하지 않는다.
- 완성 예시는 `examples/`, 레이아웃 및 컴포넌트 참고자료는 `references/`, 복제하여 사용하는 원본은 `templates/`에서 관리한다.
- 파일 구조가 변경되면 하위 가이드부터 검토한 뒤 `DESIGN.md`, `README.md`, `SKILL.md` 순서로 반영한다.
- 변경 후 저장소 전체에서 이전 파일명과 경로가 남아 있는지 검색한다.

---

## Final Review Checklist

- [ ] 원문 내용이 누락 없이 반영되었는가?
- [ ] 원문에 없는 내용을 임의로 추가하지 않았는가?
- [ ] 해당 산출물 유형의 가이드를 적용했는가?
- [ ] 공통 디자인 기준을 따랐는가?
- [ ] 문서 테마 적용 기준을 확인했는가?
- [ ] 승인된 테마 예시를 고정 템플릿처럼 복제하지 않았는가?
- [ ] Urban을 도시 사진, 건축물, 야경 또는 스카이라인으로 해석하지 않았는가?
- [ ] Cover, Section Divider, Closing이 같은 시각 언어를 공유하되 동일한 구도를 반복하지 않았는가?
- [ ] 필요한 레이아웃 참고자료, 컴포넌트 참고자료 및 완성 예시를 올바른 역할로 활용했는가?
- [ ] 공식 브랜드 자산만 사용했는가?
- [ ] 로고의 색상, 비율 및 형태를 변경하지 않았는가?

- [ ] 정보량이 많은 영역에 충분한 여백과 밝은 배경을 사용했는가?
- [ ] 본문 전체가 단순 카드 나열형으로만 구성되지 않았는가?
- [ ] 표 정렬 기준과 수치 단위를 명확히 표시했는가?

- [ ] 색상만으로 의미를 전달하지 않았는가?
- [ ] 과도한 그림자, 라운드 및 장식 효과를 사용하지 않았는가?
- [ ] 결과물이 가능한 한 수정 가능한 형태로 작성되었는가?
- [ ] 이전 파일명과 경로가 문서 안에 남아 있지 않은가?

---

## Version

| Item | Value |
|---|---|
| Version | alpha |
| Status | Draft |
| Last Updated | 2026-07-16 |
