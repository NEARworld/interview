<details>
  <summary>1 클라이언트 컴포넌트와 서버 컴포넌트 중 기본 컴포넌트</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  서버 컴포넌트
  이유: 기본이기 때문에 서버 컴포넌트에 빠르게 익숙해질 수 있다.
  성능 최적화
  ```
</details>

<details>
  <summary>2 앱 라우터와 페이지 라우터 방식 혼용 여부</summary>

  ### 코드
  ```js
  project/
    app/
    pages/
  ```
  ### 정답
  ```js
  혼용 가능
  이유: 페이지 라우터로 개발된 프로젝트에서 앱 라우터로 점진적으로 전환 가능
  notice: 앱 라우터와 페이지 라우터의 url이 같은 경우
  빌드 타임에서 에러 발생
  ```
</details>

<details>
  <summary>3 앱 라우터</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  넥스트 13 버전부터 지원되는 라우팅 방식
  ```
</details>

<details>
  <summary>4 router 세그먼트</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  도메인 뒤에 붙는 하위 경로
  프로젝트 디렉토리에서 app 폴더의 하위 폴더
  갯수에 제한이 없음
  ```
</details>

<details>
  <summary>5 catch-all segment</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  domain/[...slug]
  domain/a/b/c/d/e/...
  ```
</details>

<details>
  <summary>6 다이나믹 라우팅</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  app/
    main/
      [slug]/
        page.tsx
  ```
</details>

<details>
  <summary>7 서버 액션</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  form 액션에 등록되는 함수
  'use server' 명령문 사용
  클라이언트 컴포넌트에서는 사용 불가능 (import 해야함)
  async function
  ```
</details>

<details>
  <summary>8 useSession</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>9 Image 컴포넌트</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>10 getServerSession</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary></summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary></summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>
