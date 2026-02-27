# React Base Template

React 19 + Vite 7 기반의 풀스택형 SPA 보일러플레이트입니다.  
라우팅, 데이터 페칭, UI 컴포넌트가 미리 구성되어 있어 새 프로젝트를 빠르게 시작할 수 있습니다.

## 기술 스택

| 구분 | 기술 |
|------|------|
| **프레임워크** | React 19 |
| **빌드** | Vite 7 |
| **라우팅** | TanStack Router (파일 기반, 타입 세이프) |
| **데이터 페칭** | TanStack React Query |
| **UI** | Mantine (Emotion 기반) |
| **컴파일러** | React Compiler (babel-plugin-react-compiler) |
| **언어** | TypeScript |

## 요구 사항

- **Node.js** 18+
- **pnpm** (패키지 매니저)

## 시작하기

### 설치

```bash
pnpm install
```

### 개발 서버

```bash
pnpm dev
```

개발 서버가 실행되면 브라우저에서 [http://localhost:5173](http://localhost:5173) 으로 접속할 수 있습니다.

### 빌드

```bash
pnpm build
```

### 미리보기 (프로덕션 빌드)

```bash
pnpm preview
```

### 린트

```bash
pnpm lint
```

## 프로젝트 구조

```
src/
├── app/           # 앱 전역 설정·타입
│   └── type/      # 타입 정의 (예: emotion.d.ts)
├── routes/        # TanStack Router 파일 기반 라우트
│   ├── __root.tsx # 루트 레이아웃 (QueryClient 컨텍스트)
│   └── index.tsx  # / 경로
├── main.tsx       # 엔트리 (Router, Mantine, React Query 설정)
└── routeTree.gen.ts  # 자동 생성된 라우트 트리 (수정하지 않음)
```

- **경로 별칭**: `@/` → `src/` (import 시 `@/routes/...` 등 사용 가능)
- **라우팅**: `src/routes/` 아래에 파일을 추가하면 자동으로 라우트가 등록됩니다.

## 주요 기능

- **타입 세이프 라우팅**: TanStack Router로 경로·파라미터 타입 추론
- **코드 스플리팅**: 라우트 단위 자동 코드 스플리팅 (`autoCodeSplitting`)
- **React Query**: 라우트 컨텍스트에 `queryClient` 주입, 데이터 캐싱·동기화
- **Mantine + Emotion**: 테마·컴포넌트와 Emotion 스타일 통합
- **React Compiler**: 별도 `useMemo`/`useCallback` 없이 렌더 최적화

## 라이선스

Private
