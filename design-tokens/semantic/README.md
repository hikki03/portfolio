# Semantic Tokens

Semantic Token은 Foundation Token을 의미적 용도에 따라 분류한 토큰입니다.

## 📁 파일 구조

```
semantic/
├── colors.json        # Semantic 컬러 토큰
├── figma-mapping.json # Figma ↔ Semantic 매핑
└── README.md          # 이 파일
```

## 🎨 컬러 토큰 체계

### 1. **Primary (브랜드 컬러)**
브랜드의 메인 컬러 시스템으로 Yellow 기반:
```json
semantic.color.primary.light    // 연한 강조 (호버, 배경)
semantic.color.primary.normal   // 기본 강조 (CTA, 액션)
semantic.color.primary.strong   // 강한 강조 (중요한 요소)
semantic.color.primary.heavy    // 최대 강조 (최우선 요소)
```

### 2. **Text (텍스트)**
텍스트 계층별 컬러 시스템:
```json
semantic.color.text.primary     // 제목, 가장 중요한 텍스트
semantic.color.text.secondary   // 일반 본문 텍스트
semantic.color.text.tertiary    // 보조 정보 텍스트
semantic.color.text.quaternary  // 메타 정보 텍스트
semantic.color.text.assistive   // 가이드, 힌트 텍스트
semantic.color.text.disabled    // 비활성 텍스트
semantic.color.text.inverse     // 반전 텍스트 (어두운 배경)
```

### 3. **Background (배경)**
배경 컬러 시스템:
```json
semantic.color.background.primary    // 기본 배경 (흰색)
semantic.color.background.secondary  // 보조 배경 (섹션 구분)
semantic.color.background.tertiary   // 3차 배경 (카드, 패널)
semantic.color.background.accent     // 강조 배경 (특별한 영역)
semantic.color.background.overlay    // 오버레이 (모달, 딤드)
```

### 4. **Border (테두리)**
테두리 강도별 컬러:
```json
semantic.color.border.light    // 미묘한 구분선
semantic.color.border.normal   // 일반적인 테두리
semantic.color.border.medium   // 명확한 구분선
semantic.color.border.strong   // 강조된 테두리
```

### 5. **Surface (표면)**
입력 필드, 카드 등의 표면 컬러:
```json
semantic.color.surface.background  // 카드 내부 배경
semantic.color.surface.normal      // 입력 필드 기본 상태
semantic.color.surface.strong      // 입력 필드 활성 상태
```

### 6. **Interaction (상호작용)**
사용자 상호작용 상태별 컬러:
```json
semantic.color.interaction.hover     // 호버 상태
semantic.color.interaction.active    // 클릭/활성 상태
semantic.color.interaction.selected  // 선택된 상태
semantic.color.interaction.disabled  // 비활성 상태
semantic.color.interaction.focus     // 포커스 상태
```

### 7. **System (시스템 피드백)**
시스템 상태별 피드백 컬러:

#### Success (성공)
```json
semantic.color.system.success.light   // 성공 배경
semantic.color.system.success.normal  // 성공 기본
semantic.color.system.success.strong  // 성공 강조
semantic.color.system.success.heavy   // 성공 최대 강조
```

#### Warning (경고)
```json
semantic.color.system.warning.light   // 경고 배경
semantic.color.system.warning.normal  // 경고 기본
semantic.color.system.warning.strong  // 경고 강조
semantic.color.system.warning.heavy   // 경고 최대 강조
```

#### Danger (위험)
```json
semantic.color.system.danger.light    // 위험 배경
semantic.color.system.danger.normal   // 위험 기본
semantic.color.system.danger.strong   // 위험 강조
semantic.color.system.danger.heavy    // 위험 최대 강조
```

#### Info (정보)
```json
semantic.color.system.info.light      // 정보 배경
semantic.color.system.info.normal     // 정보 기본
semantic.color.system.info.strong     // 정보 강조
semantic.color.system.info.heavy      // 정보 최대 강조
```

### 8. **Material (머티리얼 효과)**
오버레이, 백드롭 등의 효과:
```json
semantic.color.material.dimmer.light    // 연한 딤드
semantic.color.material.dimmer.normal   // 기본 딤드 (모달)
semantic.color.material.dimmer.strong   // 강한 딤드
semantic.color.material.backdrop.light  // 연한 백드롭
semantic.color.material.backdrop.normal // 기본 백드롭
semantic.color.material.backdrop.strong // 강한 백드롭
```

### 9. **Static (정적 컬러)**
테마에 관계없이 고정된 컬러:
```json
semantic.color.static.white  // 순수 흰색
semantic.color.static.black  // 순수 검정
```

## 🔗 Figma 매핑

Figma의 `Sementic.json` 토큰이 다음과 같이 매핑됩니다:

### Primary 컬러
- `Primary/Light` → `semantic.color.primary.light`
- `Primary/Normal` → `semantic.color.primary.normal`
- `Primary/Strong` → `semantic.color.primary.strong`
- `Primary/Heavy` → `semantic.color.primary.heavy`

### Label (텍스트) 컬러
- `Label/Strong` → `semantic.color.text.primary`
- `Label/Normal` → `semantic.color.text.secondary`
- `Label/Neutral` → `semantic.color.text.tertiary`

### System 컬러
- `System/Danger/*` → `semantic.color.system.danger.*`
- `System/Warning/*` → `semantic.color.system.warning.*`
- `System/Success/*` → `semantic.color.system.info.*` (Figma에서 blue 사용)

## 📋 사용법

### CSS Variables
```css
.btn-primary {
  background-color: var(--semantic-color-primary-normal);
  color: var(--semantic-color-text-inverse);
}

.alert-success {
  background-color: var(--semantic-color-system-success-light);
  border: 1px solid var(--semantic-color-system-success-normal);
  color: var(--semantic-color-system-success-heavy);
}

.text-muted {
  color: var(--semantic-color-text-tertiary);
}
```

### Design System 활용
```jsx
// React 컴포넌트 예시
<Button variant="primary">Primary Action</Button>
<Alert type="success">성공 메시지</Alert>
<Text color="secondary">보조 텍스트</Text>
```

## ⚠️ 사용 규칙

1. **Foundation 토큰 직접 사용 금지**
   ```css
   /* ❌ */
   color: var(--foundation-color-yellow-60);
   
   /* ✅ */
   color: var(--semantic-color-primary-normal);
   ```

2. **의미적 네이밍 우선**
   - 용도에 맞는 토큰 사용
   - 색상명보다 의미 중심

3. **일관성 유지**
   - 동일한 용도는 동일한 토큰 사용
   - 예외 상황 최소화

## 🎯 다음 단계

1. **Theme Token 생성**: Light/Dark 테마별 매핑
2. **Component Token**: 컴포넌트별 특화 토큰
3. **CSS Variables 생성**: 실제 사용 가능한 CSS 파일
4. **Design System 적용**: 현재 포트폴리오에 적용
