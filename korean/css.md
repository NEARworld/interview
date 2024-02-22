<details>
  <summary>1 CSS 파싱 과정</summary>  
  
  ### 정답
  ```
  바이트 스트림 디코딩 -> 토큰화 -> 노드 생성 -> CSSOM 생성
  ```
</details>

<details>
  <summary>2 CSS는 무슨 언어라 불리나?</summary>

  ### 정답
  ```
  Style Sheet Language
  ```
</details>

<details>
  <summary> 3 CSS 명령문에 대한 설명 </summary>

  ### 정답
  ```css
  at rules 라고 불립니다.
  예시로는 @media, @layer, @keyframes 등이 있다.
  ```
</details>

<details>
  <summary> 4 POSTCSS에 대해 설명해주세요 </summary>

  ### 정답

  - CSS 모듈
    ```
    index.module.css 형식의 CSS 파일을 사용하여 CSS를 모듈화 가능
    그냥 css 파일을 만들어 다른 파일에서 클래스명을 같이 써주면 클래스가 겹치게 되는데
    모듈화를 하면 클래스명에 랜덤키 값이 붙은 클래스명 자동 생성
    ```
  - Auto-prefix
    ```  
    CSS 사용시 브라우저 호환성을 맞추기 위해 -moz-, -webkit- 등의 prefix 자동 삽입
    ```
  - CSS 플러그인
    ```
    stylelint, tailwindcss 등의 플러그인을 사용 가능
    ```
</details>

<details>
  <summary>5 tailwindcss에서 @apply에 대한 설명</summary>

  ### 정답
  ```
  tailwind의 커스텀 CSS 명령문(at rules)이며  
  CSS 파일에서 유틸리티 클래스를 사용할 수 있게 한다
  ```
</details>

<details>
  <summary>6 POSTCSS로 tailwind를 사용하는 방법</summary>

  ### 정답
  postcss.config.js 파일의 plugins 프로퍼티에 tailwindcss 등록
  ```js
  module.exports = {
    plugins: {
      tailwindcss: {},
      autoprefixer: {},
    },
  };
  ```
</details>

<details>
  <summary>7 min-width와 max-width의 차이점</summary>

  ### 정답
  
</details>

<details>
  <summary>8 rem</summary>

  ### 정답
  브라우저 기본 폰트 크기가 16px인데 기본 폰트를 10px로 맞추기 위해  
  `10 / 16 = 0.625 사용`
  ```css
  html {
    font-size: 62.5%;
  }

  p {
    font-size: 10rem;
  }
  ```
</details>

<details>
  <summary> </summary>

  ### 정답
  
</details>
