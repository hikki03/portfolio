# 디자인 토큰

이 폴더는 포트폴리오 사이트의 디자인 토큰을 관리합니다.

## 폴더 구조

```
design-tokens/
├── foundation/         # 기본 토큰 (Foundation)
│   ├── colors.json    # Foundation 컬러 시스템
│   ├── numbers.json   # 숫자 시스템 (Spacing, Sizing)
│   └── README.md      # Foundation 가이드
├── semantic/          # 의미적 토큰 (Semantic)
├── theme/            # 테마별 토큰
├── components/       # 컴포넌트별 토큰
├── colors/           # 원본 Figma 파일들
│   └── General.json  # Figma 원본
└── README.md         # 이 파일
```

## Foundation 토큰

### Colors
- **Base Colors**: 순수 흰색(0), 검정(100)
- **Gray Scale**: 0-100까지 21단계
- **Brand Colors**: Yellow, Red, Orange, Green 등
- **Extended Palette**: Blue, Indigo, Purple, Teal 등
- **Alpha Colors**: 투명도가 적용된 검정/흰색

### Numbers
- **Spacing**: 0, 1, 2, 4, 6, 8, 10, 12, 16, 20, 24, 28, 32, 36, 40, 44, 48, 56, 64, 72, 80, 96
- **Max Value**: 1000

## 사용법

Foundation 토큰은 직접 사용하지 말고, Semantic 토큰을 통해 사용하세요.

```css
/* ❌ 직접 사용 금지 */
color: var(--foundation-color-red-60);

/* ✅ Semantic 토큰 사용 */
color: var(--semantic-color-danger-normal);
```

## 토큰 네이밍 컨벤션

- **Foundation**: `foundation.{category}.{name}.{value}`
- **Semantic**: `semantic.{purpose}.{variant}`
- **Theme**: `theme.{themeName}.{semanticToken}`
