# 📝 개인 개발 블로그

Notion을 CMS로 활용하는 개인 기술 블로그입니다. Notion 데이터베이스에서 글을 작성하고 `발행됨` 상태로 변경하면 블로그에 자동으로 반영됩니다.

## ✨ 주요 기능

- Notion 데이터베이스 기반 블로그 글 목록
- 개별 글 상세 페이지
- 카테고리별 필터링
- 검색 기능
- 반응형 디자인

> 현재 개발 초기 단계입니다. 자세한 요구사항은 [PRD](./docs/PRD.md)를 참고하세요.

## 🛠️ 기술 스택

- **Framework**: Next.js 15 (App Router + Turbopack), React 19, TypeScript
- **CMS**: Notion API (`@notionhq/client`)
- **Styling**: Tailwind CSS v4, shadcn/ui
- **Icons**: Lucide React
- **Deployment**: Vercel

## 🚀 시작하기

### 1. 의존성 설치

```bash
npm install
```

### 2. 환경 변수 설정

프로젝트 루트에 `.env.local` 파일을 만들고 아래 값을 설정합니다.

```bash
NOTION_API_KEY=         # Notion Integration 시크릿 토큰
NOTION_DATABASE_ID=     # 블로그 글 데이터베이스 ID
```

### 3. 개발 서버 실행

```bash
npm run dev
```

[http://localhost:3000](http://localhost:3000)에서 확인할 수 있습니다.

## 🗄️ Notion 데이터베이스 구조

| 속성        | 타입           | 설명                |
| ----------- | -------------- | ------------------- |
| `Title`     | `title`        | 제목                |
| `Category`  | `select`       | 카테고리            |
| `Tags`      | `multi_select` | 태그                |
| `Published` | `date`         | 발행일              |
| `Status`    | `select`       | 상태 (초안/발행됨)  |
| `Content`   | page content   | 본문                |

## ⚡ 주요 명령어

```bash
npm run dev         # 개발 서버 실행 (Turbopack)
npm run build       # 프로덕션 빌드
npm run check-all   # 타입 검사 + 린트 + 포맷 검사
```

## 📚 문서

- [PRD](./docs/PRD.md)
- [프로젝트 구조](./docs/guides/project-structure.md)
- [스타일링 가이드](./docs/guides/styling-guide.md)
- [컴포넌트 패턴](./docs/guides/component-patterns.md)
- [Next.js 15 가이드](./docs/guides/nextjs-15.md)
- [폼 처리 가이드](./docs/guides/forms-react-hook-form.md)
