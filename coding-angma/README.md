## Learn Next.js with Coding Angma

### [#1]

1. `npx create-next-app nextjs`
2. `npm run dev`

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
>
> 2. Server Side Rendering (SSR, Dynamic Rendering) : 매 요청마다 html을 생성
>
> - 항상 최선 상태 유지
> - getServerSideProps

<br>

- next/link 사용 이유: a태그나 location을 사용하여 이동시 페이지가 새로고침됨
