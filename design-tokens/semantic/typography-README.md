# Semantic Typography Tokens

Pretendard 폰트를 기반으로 구축된 체계적인 타이포그래피 토큰 시스템입니다.

## 📝 타이포그래피 스케일

### 1. **Display (디스플레이)**
가장 큰 텍스트 - 히어로 섹션, 랜딩 페이지 등:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `display-1` | 56px | 72px | 700 (Bold) | -0.0319em | 메인 히어로 헤드라인 |
| `display-2` | 40px | 52px | 700 (Bold) | -0.0282em | 서브 히어로 헤드라인 |

### 2. **Title (타이틀)**
페이지 및 섹션 제목:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `title-1` | 36px | 48px | 700 (Bold) | -0.027em | 페이지 제목 |
| `title-2` | 28px | 38px | 700 (Bold) | -0.0236em | 섹션 제목 |
| `title-3` | 24px | 32px | 700 (Bold) | -0.023em | 서브섹션 제목 |

### 3. **Heading (헤딩)**
컴포넌트 제목:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `heading-1` | 22px | 30px | 500 (Medium) | -0.0194em | 카드 제목 |
| `heading-2` | 20px | 28px | 500 (Medium) | -0.012em | 컴포넌트 제목 |

### 4. **Headline (헤드라인)**
리스트 및 항목 제목:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `headline-1` | 18px | 26px | 500 (Medium) | -0.002em | 리스트 제목 |
| `headline-2` | 17px | 24px | 500 (Medium) | 0em | 항목 제목 |

### 5. **Body (본문)**
일반 텍스트 내용:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `body-1-normal` | 16px | 24px | 400 (Regular) | 0.0057em | 기본 본문 |
| `body-1-reading` | 16px | 26px | 400 (Regular) | 0.0057em | 읽기용 본문 (더 넓은 행간) |
| `body-2-normal` | 15px | 22px | 400 (Regular) | 0.0096em | 작은 본문 |
| `body-2-reading` | 15px | 24px | 400 (Regular) | 0.0096em | 작은 읽기용 본문 |

### 6. **Label (라벨)**
버튼, 폼 라벨 등:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `label-1-normal` | 14px | 20px | 500 (Medium) | 0.0145em | 버튼, 네비게이션 |
| `label-1-reading` | 14px | 22px | 400 (Regular) | 0.0145em | 읽기용 라벨 |
| `label-2` | 13px | 18px | 500 (Medium) | 0.0194em | 작은 라벨 |

### 7. **Caption (캡션)**
부가 정보, 메타데이터:

| Token | Size | Line Height | Weight | Letter Spacing | 사용처 |
|-------|------|-------------|---------|----------------|--------|
| `caption-1` | 12px | 16px | 400 (Regular) | 0.0252em | 기본 캡션 |
| `caption-2` | 11px | 14px | 400 (Regular) | 0.0311em | 작은 캡션 |

## 🎨 폰트 시스템

### Font Family
```css
--semantic-font-family-primary: Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, 'Helvetica Neue', 'Segoe UI', 'Apple SD Gothic Neo', 'Noto Sans KR', 'Malgun Gothic', sans-serif;
```

### Font Weights
- **Regular**: 400 ⭐ (기본 본문, 캡션)
- **Medium**: 500 ⭐ (헤딩, 헤드라인, 라벨)
- **Bold**: 700 ⭐ (디스플레이, 타이틀)

## 📋 사용법

### CSS Classes
```css
/* 히어로 타이틀 */
.hero-title {
  font-size: var(--semantic-typography-display-1-font-size);
  line-height: var(--semantic-typography-display-1-line-height);
  font-weight: var(--semantic-typography-display-1-font-weight);
  letter-spacing: var(--semantic-typography-display-1-letter-spacing);
}

/* 섹션 제목 */
.section-title {
  font-size: var(--semantic-typography-title-2-font-size);
  line-height: var(--semantic-typography-title-2-line-height);
  font-weight: var(--semantic-typography-title-2-font-weight);
  letter-spacing: var(--semantic-typography-title-2-letter-spacing);
}

/* 본문 텍스트 */
.body-text {
  font-size: var(--semantic-typography-body-1-reading-font-size);
  line-height: var(--semantic-typography-body-1-reading-line-height);
  font-weight: var(--semantic-typography-body-1-reading-font-weight);
  letter-spacing: var(--semantic-typography-body-1-reading-letter-spacing);
}
```

### Utility Classes (권장)
```scss
// SCSS 믹신으로 타이포그래피 유틸리티 생성
@mixin typography($style) {
  font-size: var(--semantic-typography-#{$style}-font-size);
  line-height: var(--semantic-typography-#{$style}-line-height);
  font-weight: var(--semantic-typography-#{$style}-font-weight);
  letter-spacing: var(--semantic-typography-#{$style}-letter-spacing);
}

.text-display-1 { @include typography('display-1'); }
.text-title-2 { @include typography('title-2'); }
.text-body-1-reading { @include typography('body-1-reading'); }
```

### Component 적용
```jsx
// React 컴포넌트 예시
<Typography variant="display-1">메인 헤드라인</Typography>
<Typography variant="title-2">섹션 제목</Typography>
<Typography variant="body-1-reading">본문 내용</Typography>
```

## 📐 사용 가이드라인

### 1. **계층적 구조**
- **Display**: 페이지 최상위 헤드라인
- **Title**: 페이지/섹션 구분
- **Heading**: 컴포넌트 제목
- **Headline**: 리스트/항목 제목
- **Body**: 일반 내용
- **Label**: UI 라벨
- **Caption**: 부가 정보

### 2. **반응형 적용**
```css
/* 모바일에서 더 작은 크기 사용 */
h1 {
  font-size: clamp(
    var(--semantic-typography-title-1-font-size), 
    5vw, 
    var(--semantic-typography-display-1-font-size)
  );
}
```

### 3. **읽기 최적화**
- **Normal**: 일반 UI 텍스트
- **Reading**: 긴 텍스트 읽기용 (더 넓은 행간)

### 4. **접근성 고려사항**
- **최소 폰트 크기**: 12px 이상 권장
- **충분한 대비**: 텍스트와 배경 간 4.5:1 이상
- **적절한 행간**: 1.4 이상 권장

## ⚠️ 주의사항

1. **일관성 유지**: 동일한 계층의 텍스트는 동일한 토큰 사용
2. **의미적 사용**: 크기가 아닌 용도에 따라 토큰 선택
3. **Pretendard 우선**: 폰트 스택의 첫 번째는 항상 Pretendard
4. **Letter Spacing**: 네거티브 값은 큰 텍스트, 포지티브 값은 작은 텍스트에 사용

## 🔗 관련 파일

- `typography.json` - 토큰 정의
- `../foundation/numbers.json` - 기본 숫자 시스템
- `design-tokens.css` - CSS Variables
- `styles.css` - 실제 적용
