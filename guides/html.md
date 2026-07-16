---
title: VATOS HTML Design Guide
version: alpha
status: approved
document_type: html
document_role: html-production-rules
category: document-type-guide
last_updated: 2026-07-16
reference_scope:
  - common-design-rules
  - component-references
  - theme-usage-rules
  - brand-assets
  - document-examples
  - ai-execution-rules
---

# VATOS HTML Design Guide

이 문서는 VATOS 웹 화면과 정적 HTML 산출물을 작성하거나 수정할 때 적용하는 HTML 전용 제작 기준이다.

공통 컬러, 타이포그래피, 레이아웃, 컴포넌트의 기본 형태는 `common-design-rules`를 따른다.  
이 문서에서는 HTML에서 추가로 필요한 상호작용, 상태 표현, 접근성, 반응형 동작을 정의한다.

시각적 형태를 확인할 때는 `component-references`와 `document-examples`를 참고한다.  
참고 자료는 구성과 완성도를 판단하기 위한 자료이며 그대로 복제하지 않는다.

---

## 1. Resource Roles

작업 시 실제 파일명이나 경로에 의존하지 않고 아래 역할에 해당하는 자료를 탐색하여 사용한다.

| Resource Role | Purpose |
|---|---|
| `common-design-rules` | 컬러, 타이포그래피, spacing, radius, border, shadow 및 공통 컴포넌트 기준 |
| `component-references` | 승인된 HTML 컴포넌트의 시각 형태와 상호작용 확인 |
| `brand-assets` | 공식 로고와 브랜드 자산 |
| `theme-usage-rules` | HTML 화면의 테마 선택과 Dark / Light 조합 기준 |
| `document-examples` | 디자인 시스템이 적용된 HTML 완성 예시 |
                                           
| `ai-execution-rules` | AI가 자료를 탐색하고 산출물을 생성하는 실행 기준 |

### Resource Usage Notes

- 공통 디자인 토큰과 기본 컴포넌트는 `common-design-rules`를 따른다.
- HTML 전용 상태와 상호작용은 이 문서를 따른다.
- 화면의 테마 선택과 Dark / Light 조합은 `theme-usage-rules`를 확인한다.
- 실제 시각 형태는 `component-references`를 확인한다.
- 예시는 완성도와 조합 방식을 참고하되 그대로 복제하지 않는다.
- 공식 로고와 브랜드 이미지는 `brand-assets`에 포함된 승인 자산만 사용한다.
- 특정 파일명이나 경로에만 의존하지 않는다.

---

## 2. Priority

HTML 산출물을 생성하거나 수정할 때 판단 우선순위는 다음과 같다.

1. 사용자가 제공한 원문과 명시 요청
2. `html-production-rules`
3. `common-design-rules`
4. `component-references`
5. `theme-usage-rules`
6. `brand-assets`
7. `document-examples`
8. 화면 목적과 사용자 흐름
9. 기술적 제약과 접근성 요구사항

해당 상황에 대한 세부 규칙이 없거나 내용이 부족한 경우에는 사용자 요청, 공통 디자인 기준, 컴포넌트 참고자료 및 실제 화면 목적을 조합하여 판단한다.

---

## 3. Core Principles

VATOS HTML은 다음 인상을 유지한다.

```text
Refined, Urban, Professional, Technical, Trustworthy
```

- 정보 구조와 가독성을 장식보다 우선한다.
- 전문적이지만 낡지 않고, 현대적이지만 가볍지 않은 균형을 유지한다.
- AI 또는 노션 특유의 단순 카드 나열형 화면을 기본값으로 사용하지 않는다.
- 불필요한 검색창, 필터, 카드, 아이콘 및 버튼을 자동으로 추가하지 않는다.
- 과도한 네온, 유리 효과, 3D 오브젝트, 이모지 장식을 사용하지 않는다.
- 상호작용은 짧고 예측 가능하게 설계한다.
- 동일 역할의 컴포넌트는 동일한 상태 표현을 사용한다.

---

## 4. HTML Output Rules

- 단일 HTML 파일로 작성한다.
- 외부 CDN, 외부 CSS, 외부 JavaScript에 의존하지 않는다.
- CSS는 문서 내부에 포함한다.
- JavaScript는 실제 상호작용에 필요한 경우에만 사용한다.
- React, Vue, Tailwind CDN, external font import 및 iframe을 사용하지 않는다.
- 이미지와 로고는 승인된 자산을 상대 경로로 참조한다.
- 모바일 대응은 단순하고 안정적인 media query를 사용한다.
- HTML 요소는 의미에 맞는 semantic tag를 사용한다.
- 키보드 조작과 ARIA 상태를 기본으로 포함한다.
- 복잡한 애니메이션, 과도한 hover 효과 및 장식 목적의 3D 효과를 사용하지 않는다. 승인된 Loading State의 `card-stack-cycling` 동작은 예외로 한다.
- 화면에 필요하지 않은 장식 요소를 추가하지 않는다.

---

## 5. Common Components Reference

다음 컴포넌트의 기본 시각 규칙은 `common-design-rules`를 따른다.

| Component | Reference Scope |
|---|---|
| Cards | Summary, Metric, Status, Feature, Comparison |
| Buttons | Primary, Secondary, Dark |
| Tables | Header, Body, Border, Alignment |
| Badges / Tags | Brand, Success, Danger, Warning, Info, Neutral |
| Notice Boxes | 안내, 참고, 주의 정보 |
| Metric Blocks | Label, Value, Unit, Context, Status |
| Navigation | 현재 위치와 선택 상태 |
| Input Fields | Label, Placeholder, Help, Error |

### 5.1 Button Rule

Button은 아래 세 유형만 사용한다.

```yaml
buttons:
  variants:
    - primary
    - secondary
    - dark
```

- `Primary`: 주요 실행, 저장, 적용, 확인
- `Secondary`: 취소, 이전, 보조 실행
- `Dark`: 강한 브랜드 강조 또는 핵심 실행
- `Text Button`은 별도 버튼 유형으로 정의하지 않는다.
- 문맥형 텍스트 액션은 Navigation 또는 링크 규칙을 적용한다.

### 5.2 Table Alignment

```yaml
table-alignment:
  header: center
  name-and-label: left
  long-description: left
  status: center
  number-and-unit: right
```

---

## 6. HTML-specific Components

### 6.1 Dropdown

선택 가능한 옵션 목록을 표시하고 하나의 값을 선택한다.

```yaml
dropdown:
  variants:
    field-trigger:
      show-selected-value: true
      show-chevron: true

    icon-trigger:
      trigger: icon-button
      show-selected-value: false
      panel:
        placement: bottom-start
        align: trigger-start
        width: content-fit
        min-width: 140px
        max-width: 220px
        offset: 8px

  shared:
    panel:
      background: surface-white
      border: 1px border-subtle
      radius: radius-lg
      shadow: shadow-none

    selected-option:
      color: accent-cyan
      font-weight: Bold

    behavior:
      single-selection: true
      close-after-select: true
      close-on:
        - outside-click
        - Escape
```

### 6.2 Tabs

같은 화면 안에서 범주, 섹션 또는 콘텐츠를 전환한다.

```yaml
tabs:
  variants:
    pill:
      active:
        background: dark-navy
        text-color: surface-white

    underline:
      active:
        text-color: dark-navy
        border-bottom: 2px accent-cyan

    folder-index:
      inactive:
        background: border-subtle
        text-color: semantic-neutral

      active:
        background: surface-white
        text-color: dark-navy
        font-weight: Bold

      content:
        border: 1px border-subtle
        rule: "활성 탭 아래 경계만 가리고 나머지 상단 보더는 콘텐츠 영역과 연결한다."

  behavior:
    single-active-tab: true
```

### 6.3 Compact Selection List

좁은 영역에서 데이터 항목을 하나 선택할 때 사용한다.

```yaml
compact-selection-list:
  selection-mode: single
  background: surface-white

  selected:
    background: surface-bg
    text-color: dark-navy
    font-weight: Bold
    border: 1px border-subtle

  type-filter:
    optional: true
    trigger: icon-trigger-dropdown
```

### 6.4 Catalog Selection List

분류별 항목을 탐색하고 선택할 때 사용한다.  
필요한 경우 동일한 구조를 사이드 내비게이션으로 활용한다.

```yaml
catalog-selection-list:
  usage:
    - data-selection
    - sidebar-navigation

  container:
    background: surface-white
    border: 1px border-subtle
    radius: radius-md
    internal-scroll: true

  section:
    group-name: required
    sticky-header: true
    collapsible: optional
    default-state: expanded

    toggle:
      expanded-icon: chevron-up
      collapsed-icon: chevron-down
      trigger-area: full-section-header

  item:
    count: optional

    selected:
      background: surface-bg
      text-color: accent-cyan
      font-weight: Bold

    hover:
      background: surface-bg
      text-color: dark-navy

  navigation-usage:
    active-state: current-location
    link-behavior: supported
    nested-group: supported
```

#### Catalog Selection List Rules

- 분류명 전체 영역을 클릭하면 접고 펼칠 수 있다.
- 우측 Chevron은 현재 펼침 상태를 표시한다.
- 항목 클릭 시 선택 또는 현재 위치를 `accent-cyan`으로 강조한다.
- 사이드 메뉴로 사용할 때 별도 Sidebar 컴포넌트를 새로 정의하지 않는다.
- 항목 수 또는 관련 건수는 우측 Count로 표시할 수 있다.
- 접기·펼치기를 사용하지 않는 경우 기존 Catalog Selection List처럼 내부 스크롤과 Sticky Header를 유지한다.

### 6.5 Checkbox

```yaml
checkbox:
  states:
    unchecked:
      background: surface-white
      border: 1px accent-cyan

    checked:
      background: accent-cyan
      border: 1px accent-cyan
      mark-color: surface-white

    indeterminate:
      background: accent-cyan
      border: 1px accent-cyan
      mark: horizontal-line
      behavior: "하위 선택 결과에 따라 결정"

    disabled:
      background: surface-bg
      border-color: border-subtle
      text-color: semantic-neutral
```

### 6.6 Radio

```yaml
radio:
  selected:
    background: accent-cyan
    border-color: accent-cyan
    inner-dot: surface-white

  unselected:
    background: surface-white
    border-color: semantic-neutral

  group:
    selection-mode: single
```

### 6.7 Toast

작업 결과를 짧게 알리는 텍스트 피드백이다.

```yaml
toast:
  style: text-only
  background: none
  border: none
  icon: none
  shadow: none

  text:
    color: dark-navy
    font-weight: Bold

  behavior:
    auto-dismiss: true
    aria-live: polite
```

### 6.8 Pagination

```yaml
pagination:
  item:
    background: surface-white
    border: 1px border-subtle
    radius: radius-sm

  current:
    background: dark-navy
    border-color: dark-navy
    text-color: surface-white
    font-weight: Bold

  disabled:
    text-color: border-subtle
    cursor: not-allowed

  controls:
    - previous
    - page-number
    - next
```

### 6.9 Tooltip

```yaml
tooltip:
  panel:
    background: surface-white
    border: 1px border-subtle
    radius: radius-sm
    shadow: shadow-none

  text:
    color: semantic-neutral
    font-size: 12px
    font-weight: Medium

  behavior:
    show-on:
      - hover
      - focus
    hide-on:
      - mouse-leave
      - blur
      - Escape
    click-to-pin: false
    interactive-content: false

  accessibility:
    role: tooltip
    relation: aria-describedby
```

### 6.10 Calendar / Date Picker

하나의 달력에서 선택한 날짜 수에 따라 단일 조회 또는 기간 조회를 자동 결정한다.

```yaml
calendar-date-picker:
  selection:
    mode: automatic
    max-dates: 2

    first-click:
      result: single-date

    second-click:
      result: date-range
      sort-dates-ascending: true
      highlight-between-dates: true

    click-selected-date-again:
      behavior: deselect-clicked-date

    click-third-date:
      behavior: reset-and-start-new-selection

  summary:
    empty-text: 날짜를 선택하세요
    single-format: YYYY.MM.DD
    range-format: YYYY.MM.DD ~ YYYY.MM.DD

  day:
    today:
      border: 1px accent-cyan

    selected:
      background: dark-navy
      text-color: surface-white
      font-weight: Bold

    in-range:
      background: surface-bg
      text-color: dark-navy
```

---

## 7. System States

Empty, Error, Loading State는 같은 시각 언어를 사용한다.

### 7.1 Shared Structure

```yaml
system-state:
  layout:
    type: visual-plus-text
    alignment: center

  visual:
    type: stacked-placeholder-cards
    layers: 3
    border: 1px border-subtle
    background: surface-white
    shadow: shadow-none

  text:
    title:
      font-weight: Bold

    description:
      color: semantic-neutral
      font-weight: Regular
```

세 상태의 카드 크기, 카드 간 간격, 제목과 설명 간격은 동일하게 유지한다.

### 7.2 Empty State

```yaml
empty-state:
  reference: system-state

  visual:
    animation: none

  title:
    color:
      allowed:
        - dark-navy
        - accent-cyan
      selection-rule: "화면 디자인에 따라 선택"

  accessibility:
    role: status
    aria-live: polite
```

기본 문구:

```text
조회된 데이터가 없습니다.
조회 조건을 변경한 후 다시 시도하세요.
```

### 7.3 Error State

```yaml
error-state:
  reference: system-state

  visual:
    error-mark:
      shape: circle
      symbol: exclamation
      border-color: semantic-danger
      text-color: semantic-danger
      placement: front-card-right

  title:
    color: semantic-danger

  accessibility:
    role: alert
```

기본 문구:

```text
데이터를 불러오지 못했습니다.
잠시 후 다시 시도하세요.
```

### 7.4 Loading State

```yaml
loading-state:
  reference: system-state

  visual:
    animation:
      name: card-stack-cycling
      behavior:
        - "앞 카드가 위로 살짝 들리며 사라진다."
        - "뒤 카드가 순차적으로 앞으로 이동한다."
        - "사라진 카드는 맨 뒤로 돌아가 반복된다."
      duration: 3.6s
      infinite: true

  title:
    color: accent-cyan

  accessibility:
    role: status
    aria-live: polite
    reduced-motion:
      behavior: static-stacked-cards
```

기본 문구:

```text
데이터를 불러오고 있습니다.
잠시만 기다려 주세요.
```

---

## 8. Context-dependent Patterns

### 8.1 Form Field Group

Form Field Group은 독립 컴포넌트가 아니라 화면 목적에 따라 조합하는 패턴이다.

```yaml
form-field-group:
  type: composition-pattern
  fixed-layout: false

  compose-from:
    - label
    - input
    - dropdown
    - calendar-date-picker
    - textarea
    - help-text
    - error-message

  layout: context-dependent
```

### 8.2 Textarea

Textarea는 Input Field 규칙을 따르되 높이와 Resize는 화면과 콘텐츠 목적에 따라 정한다.

```yaml
textarea:
  reference: input-field-rules
  height: content-dependent
  resize: context-dependent
  readonly: supported
  disabled: supported
  error: supported
```

---

## 9. Interaction and Accessibility

```yaml
accessibility:
  focus:
    visible: true
    color: accent-cyan
    shadow: shadow-none

  aria:
    selected: aria-selected
    expanded: aria-expanded
    described-by: aria-describedby
    live-status: aria-live
```

- 마우스 Hover 상태만 제공하지 않고 Keyboard Focus 상태를 함께 제공한다.
- 접기·펼치기 상태는 `aria-expanded`로 표시한다.
- 선택 상태는 `aria-selected` 또는 native form 상태를 사용한다.
- Loading과 Empty State는 `role="status"`와 `aria-live="polite"`를 사용한다.
- Error State는 `role="alert"`를 사용한다.
- `prefers-reduced-motion` 환경에서는 Loading 애니메이션을 정적인 카드 스택으로 대체한다.
- 포커스는 `accent-cyan` outline 또는 border를 사용한다.
- 임의의 glow, halo 또는 강한 shadow를 사용하지 않는다.

---

## 10. Output Workflow

사용자가 VATOS HTML 산출물을 요청하면 다음 순서로 수행한다.

1. 화면 목적과 대상 사용자를 파악한다.
2. 원문 내용과 필수 기능을 확인한다.
3. `common-design-rules`를 확인한다.
4. `theme-usage-rules`를 확인한다.
5. 필요한 컴포넌트를 `component-references`에서 탐색한다.
6. 화면 구조와 사용자 흐름을 먼저 정리한다.
7. 필요한 컴포넌트만 선택한다.
8. HTML 구조를 semantic tag로 작성한다.
9. 공통 디자인 토큰과 HTML 전용 상태 규칙을 적용한다.
10. 키보드 조작과 ARIA 상태를 적용한다.
11. 모바일과 좁은 화면에서 잘리지 않는지 확인한다.
12. 최종 산출 전 기능, 접근성, 브랜드 기준 및 외부 의존성을 검토한다.

---

## 11. Do Not

- 특정 파일명이나 경로에만 의존하지 않는다.
- 외부 CDN, 외부 CSS, 외부 JavaScript를 사용하지 않는다.
- React, Vue, Tailwind CDN, iframe을 사용하지 않는다.
- 승인되지 않은 임의 색상과 그림자를 추가하지 않는다.
- 선택 상태를 색상만으로 표현하지 않는다.
- 모든 목록에 검색창과 필터를 기본으로 넣지 않는다.
- Catalog Selection List와 Sidebar를 중복 컴포넌트로 정의하지 않는다.
- Loading State에 Spinner와 카드 순환 애니메이션을 동시에 사용하지 않는다.
- Empty, Error, Loading State의 카드 크기와 간격을 서로 다르게 만들지 않는다.
- Dropdown, Tooltip, Calendar 패널을 화면 경계 밖으로 배치하지 않는다.
- 화면에 필요하지 않은 버튼, 카드, 아이콘을 장식 목적으로 추가하지 않는다.
- Text Button을 별도 버튼 유형으로 추가하지 않는다.
- 과도한 애니메이션, 장식 목적의 3D 효과 및 hover 효과를 사용하지 않는다. 승인된 Loading State의 `card-stack-cycling` 동작은 예외로 한다.

---

## 12. Final Review Checklist

- [ ] 사용자 원문과 명시 요청을 정확히 반영했는가?
- [ ] `html-production-rules`를 적용했는가?
- [ ] `common-design-rules`를 적용했는가?
- [ ] `theme-usage-rules`를 확인했는가?
- [ ] 필요한 `component-references`를 확인했는가?
- [ ] 특정 파일명이나 경로에 의존하지 않았는가?
- [ ] Button은 Primary, Secondary, Dark만 사용했는가?
- [ ] 표의 텍스트와 수치 정렬 기준이 올바른가?
- [ ] 선택, Hover, Focus, Disabled 상태가 구분되는가?
- [ ] Catalog Selection List가 내부 스크롤과 접기·펼치기를 올바르게 지원하는가?
- [ ] Empty, Error, Loading State의 카드 크기와 간격이 동일한가?
- [ ] Loading 애니메이션에 Reduced Motion 대체 상태가 있는가?
- [ ] Dropdown과 Tooltip이 화면 밖으로 넘치지 않는가?
- [ ] 키보드 조작과 ARIA 상태가 적용되었는가?
- [ ] 모바일 또는 좁은 화면에서 컴포넌트가 잘리지 않는가?
- [ ] 외부 CDN과 외부 라이브러리에 의존하지 않는가?
- [ ] 불필요한 카드, 아이콘, 검색창, 그림자를 추가하지 않았는가?
