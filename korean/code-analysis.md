# Javascript
<details>
  <summary>1 this & use strict</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  'use strict';

  function foo() {
    console.log(this);
  }
  ```

  ```js
  function foo() {
    console.log(this);
  }
  ```
</details>

<details>
  <summary>2 lexical scope </summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  function init() {
    let x = 10;
  
    button.addEventListener(() => {
      console.log(x);
      console.log(this);
    });

    x = 20;
  }
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
