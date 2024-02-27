# Javascript
<details>
  <summary>1 this & use strict</summary>

  ### 코드
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
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>2 lexical scope </summary>

  ### 코드
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
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>3 Closure</summary>

  ### 코드
  ```js
  function foo() {
    let x = 10;
    return function () {
      console.log(x);
    }
  }

  const bar = foo();
  bar();
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>4 currying</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>
