## Learn Next.js with Coding Angma

### [#1]

```
npx create-next-app nextjs
npm run dev
```

> create-next-app 설치 시
>
> - 컴파일과 번들링이 자동으로 된다 (webpack과 babel)
> - 자동 리프레쉬 기능으로 수정하면 화면에 바로 반영된다
> - 서버 사이드 렌더링이 지원된다
> - 스태틱 파일을 지원한다

<br>

[_app.js]

- 페이지 전환시 레이아웃 유지 가능
- 페이지 전환시 상태값 유지 가능
- componentDidCatch를 이용하여 커스텀 에러 핸들링 가능
- 추가적인 데이터를 페이지로 주입 가능
- 글로벌 CSS 선언

<br>

[_document.js]

- 서버에서만 렌더링됨
- Html, Head, body를 수정해야 할 때 사용

<br>
<br>

### [#2]

- js 파일에 module.css 적용
  - /src/component/ItemList.js
  - /src/component/ItemList.module.css
- Dynamic Routes 적용
  - /pages/view/[id].js
- next/link 적용
  - /src/component/ItemList.js

<br>
<br>

### [#3]

- Next.js는 모든 페이지를 사전 렌더링함 (Pre-rendering)
  - 더 좋은 퍼포먼스
  - 검색엔진최적화 (SEO)

> [Pre-rendering 형태]
> 차이점: 언제 html 파일을 생성하는가
>
> 1. 정적 생성
>
> - 프로젝트가 빌드하는 시점에 html 파일들이 생성
> - 모든 요청에 재사용
> - 퍼포먼스 이유로, Next.js는 정적 생성을 권고
> - 정적 생성된 페이지들은 CDN에 캐시
> - getStaticProps / getStaticPaths
> - 마케팅 페이지, 블로그 게시물, 제품 목록, 도움말/문서
>
> 2. Server Side Rendering (SSR, Dynamic Rendering) : 매 요청마다 html을 생성
>
> - 항상 최신 상태 유지
> - getServerSideProps
> - 관리자 페이지, 분석 차트

<br>

- next/link를 사용하는 이유 : a태그나 location을 사용하여 이동시 페이지가 새로고침됨

<br>
<br>

### [#4]

[_error.js]

- client와 server의 에러를 한번에 관리 가능
- 404 에러는 static으로 관리하는 것을 권장

<br>

[.env]

- node. js 환경에서는 `process.env.변수명`
- browswer 환경에서는 `process.env.NEXT_PUBLIC_변수명`

<br>
<br>

### [#5]

> Pre-rendering (사전 렌더링)
>
> - 사전에 기본적으로 모든 페이지 Html 파일을 만든다는 의미
> - 퍼포먼스 향상, SEO

- Pre-rendering을 하지 않으면
  처음에 빈 화면이 로드되고 JS 로드가 끝나면 해당 페이지의 요소들을 채움

- Pre-rendering을 하면
  사전에 만들어진 Html 요소들이 처음부터 나타남 (meta data 포함)
  JS 로드가 끝나면 Link와 같은 컴포넌트들이 작동을 시작함
  → Hydration: 정적인 요소에 활기를 불어넣는 작업

<br>
<br>

### [#6]

- next/router의 useRouter, isFallback을 이용해서 빈 화면에 로딩 아이콘을 보여줌
- API 리스트 결과를 기반으로 static paths를 넘겨줌

<br>
<br>

### [#7]

- API Routes 설정 후 로그인 구현 (쿠키 사용)

<br>
<br>
<br>
<br>
<br>

[코딩앙마 유튜브 채널](https://www.youtube.com/watch?v=Ujjdn2wMIew&list=PLZKTXPmaJk8Lx3TqPlcEAzTL8zcpBz7NP&index=1)
[코딩앙마 깃허브](https://github.com/coding-angma/nextjs-tutorial)
