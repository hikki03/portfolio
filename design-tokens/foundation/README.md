# Foundation Tokens

Foundation 토큰은 디자인 시스템의 가장 기본이 되는 원자적 토큰들입니다.

## 📁 파일 구조

```
foundation/
├── colors.json     # Foundation 컬러 시스템
├── numbers.json    # 숫자 시스템 (Spacing, Sizing)
└── README.md       # 이 파일
```

## 🎨 Colors

### Base Colors
```json
foundation.color.base.white   // #FFFFFF
foundation.color.base.black   // #000000
```

### Gray Scale (21단계)
```json
foundation.color.gray.{0-100}
```
- `0`: 완전한 흰색
- `50`: 중간 회색
- `100`: 완전한 검정

### Brand Color Palettes
각 컬러는 0-100까지 21단계로 구성:

#### Primary Colors
- **Yellow**: 브랜드 메인 컬러
- **Red**: 에러, 위험 상황
- **Orange**: 경고 상황
- **Green**: 성공 상황

#### Secondary Colors
- **Blue**: 정보 전달
- **Indigo**: 강조 색상
- **Purple**: 프리미엄 느낌
- **Teal**: 차분한 강조
- **Cyan**: 시원한 느낌
- **Lime**: 활기찬 느낌
- **Magenta**: 화려한 강조

### Alpha Colors
투명도가 적용된 검정/흰색:
```json
foundation.color.alpha.black.{0,10,25,50,75,100}
foundation.color.alpha.white.{0,10,25,50,75,100}
```

## 🔢 Numbers

순수한 숫자 시스템 (픽셀 값):
```json
foundation.number.{0-21,max}
```

### 숫자 스케일
- **0**: 0px (없음)
- **1**: 1px (최소 단위)
- **2**: 2px (미세한 간격)
- **3**: 4px (작은 간격)
- **4**: 6px
- **5**: 8px (기본 단위)
- **6**: 10px
- **7**: 12px (표준 간격)
- **8**: 16px (중간 간격)
- **9**: 20px
- **10**: 24px (큰 간격)
- **11**: 28px
- **12**: 32px (주요 간격)
- **13**: 36px
- **14**: 40px (터치 타겟)
- **15**: 44px
- **16**: 48px (헤더 높이)
- **17**: 56px
- **18**: 64px (큰 요소)
- **19**: 72px
- **20**: 80px (네비게이션)
- **21**: 96px (대형 간격)
- **max**: 1000px (최대값)

## ⚠️ 사용 규칙

1. **Foundation 토큰은 직접 사용 금지**
   - Semantic 토큰을 통해서만 사용
   
2. **컬러 범위**
   - 0-20: 매우 밝음 (배경용)
   - 30-70: 중간 톤 (UI 요소용)
   - 80-100: 매우 어두움 (텍스트용)

3. **Spacing 사용**
   - 일관된 간격을 위해 지정된 값만 사용
   - 커스텀 값 사용 시 Foundation에 추가 고려

## 🎯 다음 단계

Foundation 토큰을 기반으로 다음을 생성하세요:

1. **Semantic Tokens**: 의미적 용도별 토큰 ✅
   - **Colors**: Primary, Text, Background, System 등
   - **Sizing**: Radius, Padding, Gap, Height 등
2. **Theme Tokens**: 라이트/다크 테마 매핑
3. **Component Tokens**: 컴포넌트별 특화 토큰

## 📁 관련 파일

- `../semantic/colors.json` - 컬러 의미적 토큰
- `../semantic/sizing.json` - 사이징 의미적 토큰
- `../semantic/figma-mapping.json` - Figma 매핑 테이블
