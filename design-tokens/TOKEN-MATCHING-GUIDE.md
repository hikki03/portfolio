# 🎯 Token Matching Guide

**모든 디자인 작업에서 기존 토큰과 일치하는 값은 무조건 토큰으로 연결**

## 📋 우선순위 원칙

### 1. **Semantic 토큰 우선** ⭐
```css
/* ✅ 우선 사용 */
var(--semantic-color-primary-normal)
var(--semantic-sizing-padding-5)
var(--semantic-typography-title-2-font-size)

/* ❌ 가능하면 피하기 */
var(--foundation-color-yellow-60)
var(--foundation-number-7)
```

### 2. **정확한 매칭 > 근사값**
- 정확히 일치하는 토큰이 있으면 무조건 사용
- 없을 때만 가장 가까운 값으로 조정

## 🎨 Color 매칭 테이블

### **자주 사용하는 컬러 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 용도 |
|-------------|---------------|------|
| `#000000`, `#000` | `var(--semantic-color-text-primary)` | 메인 텍스트 |
| `#FFFFFF`, `#fff` | `var(--semantic-color-background-primary)` | 배경 |
| `#EFBC0F` | `var(--semantic-color-primary-normal)` | 브랜드 컬러 |
| `#F6D32D` | `var(--semantic-color-primary-light)` | 브랜드 라이트 |
| `#D3A70B` | `var(--semantic-color-primary-strong)` | 브랜드 강조 |
| `rgba(0, 0, 0, 0.1)` | `var(--semantic-color-border-light)` | 가벼운 테두리 |
| `rgba(0, 0, 0, 0.28)` | `var(--semantic-color-border-normal)` | 일반 테두리 |
| `rgba(0, 0, 0, 0.5)` | `var(--semantic-color-material-dimmer-normal)` | 오버레이 |

### **시스템 컬러**

| 하드코딩 값 | Semantic 토큰 | 용도 |
|-------------|---------------|------|
| `#22C55E` | `var(--semantic-color-system-success-normal)` | 성공 |
| `#E73A3A` | `var(--semantic-color-system-danger-normal)` | 위험 |
| `#EA580C` | `var(--semantic-color-system-warning-normal)` | 경고 |
| `#1966CC` | `var(--semantic-color-system-info-normal)` | 정보 |

## 📏 Sizing 매칭 테이블

### **Padding 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `2px` | `var(--semantic-sizing-padding-1)` | 최소 여백 |
| `4px` | `var(--semantic-sizing-padding-2)` | 작은 여백 |
| `8px` | `var(--semantic-sizing-padding-3)` | 일반 여백 |
| `10px` | `var(--semantic-sizing-padding-4)` | 입력 필드 |
| `12px` | `var(--semantic-sizing-padding-5)` | 버튼 세로 |
| `16px` | `var(--semantic-sizing-padding-6)` | 버튼 가로 |
| `20px` | `var(--semantic-sizing-padding-7)` | 컨테이너 |
| `24px` | `var(--semantic-sizing-padding-8)` | 페이지 여백 |
| `32px` | `var(--semantic-sizing-padding-9)` | 섹션 여백 |
| `40px` | `var(--semantic-sizing-padding-10)` | 큰 컨테이너 |

### **Gap 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `8px` | `var(--semantic-sizing-gap-3)` | 관련 요소 |
| `12px` | `var(--semantic-sizing-gap-4)` | 그룹 요소 |
| `16px` (1rem) | `var(--semantic-sizing-gap-5)` | 일반 간격 |
| `20px` | `var(--semantic-sizing-gap-6)` | 컴포넌트 간 |
| `24px` | `var(--semantic-sizing-gap-7)` | 섹션 내 |
| `32px` (2rem) | `var(--semantic-sizing-gap-8)` | 주요 블록 |
| `40px` | `var(--semantic-sizing-gap-9)` | 레이아웃 블록 |
| `48px` | `var(--semantic-sizing-gap-10)` | 페이지 섹션 |
| `64px` | `var(--semantic-sizing-gap-11)` | 메이저 섹션 |
| `80px` | `var(--semantic-sizing-gap-12)` | 페이지 간 |

### **Border Radius 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `2px` | `var(--semantic-sizing-radius-xxs)` | 미묘한 모서리 |
| `4px` | `var(--semantic-sizing-radius-xs)` | 버튼, 태그 |
| `6px` | `var(--semantic-sizing-radius-sm)` | 입력 필드 |
| `8px` | `var(--semantic-sizing-radius-md)` | 카드 (기본) |
| `12px` | `var(--semantic-sizing-radius-lg)` | 패널 |
| `16px` | `var(--semantic-sizing-radius-xl)` | 모달 |
| `50px`, `999px` | `var(--foundation-number-max)` | 완전 둥근 모서리 |

### **Height 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `24px` | `var(--semantic-sizing-height-4)` | 작은 버튼 |
| `32px` | `var(--semantic-sizing-height-5)` | 입력 필드 |
| `40px` | `var(--semantic-sizing-height-6)` | 일반 버튼 |
| `48px` | `var(--semantic-sizing-height-7)` | 큰 버튼 |
| `56px` | `var(--semantic-sizing-height-8)` | 헤더 |
| `64px` | `var(--semantic-sizing-height-9)` | 히어로 요소 |
| `80px` | `var(--semantic-sizing-height-11)` | 네비게이션 |

## ✍️ Typography 매칭 테이블

### **Font Size 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `56px` | `var(--semantic-typography-display-1-font-size)` | 메인 히어로 |
| `40px` | `var(--semantic-typography-display-2-font-size)` | 서브 히어로 |
| `36px` | `var(--semantic-typography-title-1-font-size)` | 페이지 제목 |
| `28px` | `var(--semantic-typography-title-2-font-size)` | 섹션 제목 |
| `24px` | `var(--semantic-typography-title-3-font-size)` | 서브섹션 |
| `22px` | `var(--semantic-typography-heading-1-font-size)` | 카드 제목 |
| `20px` | `var(--semantic-typography-heading-2-font-size)` | 컴포넌트 제목 |
| `18px` | `var(--semantic-typography-headline-1-font-size)` | 리스트 제목 |
| `16px` | `var(--semantic-typography-body-1-normal-font-size)` | 기본 본문 |
| `15px` | `var(--semantic-typography-body-2-normal-font-size)` | 작은 본문 |
| `14px` | `var(--semantic-typography-label-1-normal-font-size)` | 라벨 |
| `12px` | `var(--semantic-typography-caption-1-font-size)` | 캡션 |

### **Font Weight 값 → Semantic 토큰**

| 하드코딩 값 | Semantic 토큰 | 설명 |
|-------------|---------------|------|
| `400` | `var(--semantic-font-weight-regular)` | 기본 본문 |
| `500` | `var(--semantic-font-weight-medium)` | UI 라벨 |
| `700` | `var(--semantic-font-weight-bold)` | 제목 |

## 🔄 실제 적용 예시

### **Before (하드코딩)**
```css
.card {
  padding: 24px;
  gap: 16px;
  border-radius: 12px;
  background: #ffffff;
  border: 1px solid rgba(0, 0, 0, 0.1);
}

.title {
  font-size: 28px;
  font-weight: 700;
  color: #000000;
  margin-bottom: 16px;
}
```

### **After (토큰 사용)**
```css
.card {
  padding: var(--semantic-sizing-padding-8);
  gap: var(--semantic-sizing-gap-5);
  border-radius: var(--semantic-sizing-radius-lg);
  background: var(--semantic-color-background-primary);
  border: 1px solid var(--semantic-color-border-light);
}

.title {
  font-size: var(--semantic-typography-title-2-font-size);
  font-weight: var(--semantic-font-weight-bold);
  color: var(--semantic-color-text-primary);
  margin-bottom: var(--semantic-sizing-gap-5);
}
```

## ⚠️ 매칭 규칙

### 1. **정확한 매칭 우선**
```css
/* ✅ 정확한 매칭 */
padding: 16px; → var(--semantic-sizing-padding-6)

/* ❌ 부정확한 매칭 */
padding: 15px; → var(--semantic-sizing-padding-6) /* 16px로 조정 */
```

### 2. **의미적 사용**
```css
/* ✅ 의미에 맞는 사용 */
button { padding: var(--semantic-sizing-padding-4); }
text { color: var(--semantic-color-text-primary); }

/* ❌ 의미에 안 맞는 사용 */
button { color: var(--semantic-color-system-danger-normal); } /* 위험하지 않은데 danger 색상 */
```

### 3. **없는 값 처리**
```css
/* 토큰에 없는 값일 때 */
/* 1. 가장 가까운 토큰 사용 */
width: 25px; → var(--semantic-sizing-height-4); /* 24px */

/* 2. Foundation 토큰 고려 */
margin: 3px; → var(--foundation-number-2); /* 2px 또는 4px로 조정 */

/* 3. 새 토큰 제안 (필요시) */
/* 자주 사용되는 값이면 토큰 시스템에 추가 고려 */
```

## 🎯 작업 플로우

### **새 디자인 작업 시**
1. **컬러 확인**: Figma/디자인에서 사용한 컬러가 semantic 토큰에 있는지 확인
2. **사이즈 매칭**: padding, margin, gap 등이 매칭 테이블에 있는지 확인  
3. **타이포그래피 적용**: 폰트 크기, 굵기가 typography 토큰과 매칭되는지 확인
4. **토큰 우선 사용**: 하드코딩 대신 항상 토큰부터 찾아서 사용

### **기존 코드 수정 시**
1. **하드코딩 값 스캔**: 숫자 값들 확인
2. **토큰 매칭**: 이 가이드를 참고해서 대응하는 토큰 찾기
3. **일괄 교체**: 동일한 값들은 모두 토큰으로 교체
4. **테스트**: 시각적 변화 없이 토큰으로 잘 교체되었는지 확인

이제 **모든 새로운 디자인 작업은 이 가이드를 따라 토큰 우선으로 진행**됩니다! 🎨✨
