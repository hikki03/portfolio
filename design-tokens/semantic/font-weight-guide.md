# Font Weight System

단순하고 일관된 **3단계 굵기 시스템**입니다.

## 🎯 굵기 체계

### **Regular (400)**
```css
font-weight: var(--semantic-font-weight-regular); /* 400 */
```
**사용처:**
- 본문 텍스트 (Body 1/2 Normal, Reading)
- 캡션 (Caption 1/2)
- Label 1 Reading

**특징:** 가독성이 좋은 기본 굵기

---

### **Medium (500)**
```css
font-weight: var(--semantic-font-weight-medium); /* 500 */
```
**사용처:**
- 헤딩 (Heading 1/2)
- 헤드라인 (Headline 1/2)
- 라벨 (Label 1 Normal, Label 2)

**특징:** 적당한 강조, UI 요소에 적합

---

### **Bold (700)**
```css
font-weight: var(--semantic-font-weight-bold); /* 700 */
```
**사용처:**
- 디스플레이 (Display 1/2)
- 타이틀 (Title 1/2/3)

**특징:** 강한 강조, 제목과 헤드라인에 사용

## 📋 사용 규칙

### 1. **계층적 적용**
```
Bold (700)    → 페이지/섹션 제목 (Display, Title)
Medium (500)  → 컴포넌트 제목 (Heading, Headline, Label)
Regular (400) → 본문 내용 (Body, Caption)
```

### 2. **의미적 사용**
- **Bold**: 페이지 구조를 나타내는 주요 제목
- **Medium**: UI 요소와 컴포넌트 라벨
- **Regular**: 읽기 위한 텍스트 내용

### 3. **일관성 유지**
- 동일한 계층의 텍스트는 동일한 굵기 사용
- 임의의 굵기 변경 금지
- 토큰을 통해서만 굵기 적용

## 🎨 실제 적용 예시

### HTML + CSS
```html
<h1 class="hero-title">메인 헤드라인</h1>          <!-- Bold -->
<h2 class="section-title">섹션 제목</h2>           <!-- Bold -->
<h3 class="card-title">카드 제목</h3>              <!-- Medium -->
<p class="body-text">본문 내용입니다.</p>           <!-- Regular -->
<span class="label">버튼 라벨</span>                <!-- Medium -->
<small class="caption">부가 정보</small>            <!-- Regular -->
```

### CSS Variables
```css
.hero-title {
  font-weight: var(--semantic-font-weight-bold);    /* 700 */
}
.card-title {
  font-weight: var(--semantic-font-weight-medium);  /* 500 */
}
.body-text {
  font-weight: var(--semantic-font-weight-regular); /* 400 */
}
```

## ⚠️ 주의사항

1. **직접 숫자 사용 금지**
   ```css
   /* ❌ 잘못된 사용 */
   font-weight: 600;
   font-weight: 800;
   
   /* ✅ 올바른 사용 */
   font-weight: var(--semantic-font-weight-bold);
   ```

2. **중간 굵기 금지**
   - 400, 500, 700 외의 굵기는 사용하지 않음
   - 디자인 일관성을 위해 3단계만 유지

3. **Pretendard 지원 확인**
   - Regular (400) ✅
   - Medium (500) ✅  
   - Bold (700) ✅

## 🔄 Migration Guide

기존 굵기에서 새 시스템으로 변경:

```css
/* Before → After */
font-weight: 300; /* Light → Regular (400) */
font-weight: 600; /* Semi Bold → Bold (700) */
font-weight: 800; /* Extra Bold → Bold (700) */
```
