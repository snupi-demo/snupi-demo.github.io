# Design

## Source of truth
- Status: Active
- Last refreshed: 2026-09-09
- Primary product surfaces: GitHub Pages 개인 홈페이지
- Evidence reviewed: `index.html`, `README.md`, `/Users/jeonghunpark/Downloads/DESIGN-lovable.md`

## Brand
- Personality: 따뜻하고 절제된, 연구자다운 차분함
- Trust signals: 명확한 소속, 읽기 쉬운 정보 구조, 직접적인 GitHub 연결
- Avoid: 순백 배경, 강한 그림자, 과도하게 채도가 높은 색, 장식적 요소 과다 사용

## Product goals
- Goals: 박정훈의 소속·소개·관심사·연락 방법을 한 화면 흐름에서 전달한다.
- Non-goals: 블로그, 회원 기능, 서버 기반 상호작용
- Success signals: 작은 화면에서도 메뉴와 핵심 정보, GitHub 링크를 쉽게 찾을 수 있다.

## Personas and jobs
- Primary personas: 연구 동료, 채용 담당자, 개인 홈페이지 방문자
- User jobs: 정훈의 배경과 관심사를 빠르게 파악하고 GitHub 프로필로 이동한다.
- Key contexts of use: 데스크톱 브라우저, 휴대폰 브라우저, GitHub Pages

## Information architecture
- Primary navigation: 소개, 관심사, 연락처
- Core routes/screens: 단일 스크롤 페이지
- Content hierarchy: 이름과 소속 → 소개 → 관심사 → GitHub 연락처

## Design principles
- Principle 1: 크림색 기반의 넉넉한 여백으로 편안하고 편집적인 리듬을 만든다.
- Principle 2: 카드 그림자 대신 온화한 테두리로 정보의 경계를 표현한다.
- Tradeoffs: 제공된 글꼴 파일이 없으므로 시스템 한글 글꼴을 사용한다.

## Visual language
- Color: 배경 `#f7f4ed`, 본문 `#1c1c1c`, 보조 글자 `#5f5f5d`, 테두리 `#eceae4`
- Typography: 시스템 산세리프, 큰 제목은 600 굵기와 촘촘한 자간
- Spacing/layout rhythm: 8px 기반, 섹션 간 64–96px 이상
- Shape/radius/elevation: 카드 12–16px, 버튼 6px, 진한 버튼에만 얕은 inset shadow
- Motion: 짧은 hover 전환만 사용
- Imagery/iconography: 이미지 없이 부드러운 다색 그라데이션으로 히어로 분위기를 만든다.

## Components
- Existing components to reuse: 없음 (단일 HTML)
- New/changed components: 고정 상단 메뉴, 히어로, 관심사 그리드, 연락처 카드
- Variants and states: 진한 CTA 버튼, 테두리 보조 버튼, hover/focus 상태
- Token/component ownership: CSS 사용자 정의 속성은 `index.html` 상단에서 관리

## Accessibility
- Target standard: 시맨틱 랜드마크와 키보드 포커스를 갖춘 기본 접근성
- Keyboard/focus behavior: 모든 링크에 명확한 focus shadow 제공
- Contrast/readability: 차콜-크림 조합과 16px 이상 본문 글자 유지
- Screen-reader semantics: 메뉴 레이블과 섹션 제목 연결
- Reduced motion and sensory considerations: 필수 애니메이션 없음

## Responsive behavior
- Supported breakpoints/devices: 700px 이하 휴대폰, 그 이상 태블릿·데스크톱
- Layout adaptations: 2열 소개 영역·관심사 카드가 한 열로 전환되고, 일반 메뉴 링크는 숨긴다.
- Touch/hover differences: 주요 CTA는 최소 40px 높이를 유지한다.

## Interaction states
- Loading: 해당 없음
- Empty: 해당 없음
- Error: 해당 없음
- Success: 해당 없음
- Disabled: 해당 없음
- Offline/slow network, if applicable: 외부 리소스 없이 본문은 즉시 표시된다.

## Content voice
- Tone: 짧고 담백하며 친근한 연구자 소개
- Terminology: 어려운 전문 용어보다 방문자가 이해하기 쉬운 표현 사용
- Microcopy rules: 행동을 나타내는 짧은 버튼 텍스트 사용

## Implementation constraints
- Framework/styling system: 외부 의존성 없는 정적 HTML/CSS
- Design-token constraints: 정의된 크림·차콜·테두리 색상만 사용
- Performance constraints: 서버, 빌드, 유료 서비스, 외부 글꼴 불필요
- Compatibility constraints: 현대적인 모바일·데스크톱 브라우저와 GitHub Pages
- Test/screenshot expectations: 데스크톱과 모바일 너비에서 제목, 메뉴, GitHub 링크 확인

## Open questions
- [ ] 실제 연구 주제 또는 프로젝트가 정해지면 관심사와 소개 문구를 구체화한다. / 박정훈 / 낮음
