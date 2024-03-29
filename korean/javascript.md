# 스코프

<details>
  <summary>1 렉시컬 스코프</summary>

  ### 정답
  ```
  정적 스코프라고도 불린다
  선언된 위치에서 스코프 체인이 정해지는 것을 의미
  ```
  
</details>

<details>
  <summary>2 this</summary>

  ### 정답
  ```js
  const obj = {
    foo: () => {
      console.log(this);
    },
    zoo: function() {
      console.log(this);
    },
    bar() {
      console.log(this);
    },
    cat() {
      const arr = [1, 2, 3];
      arr.map(item => {
        console.log(this);
      })
    }
  }
  ```
</details>

<details>
  <summary>3 TDZ</summary>

  ### 정답
  ```
  식별자를 통해 값에 접근할 수 없는 영역
  let 변수나 const 상수는 호이스팅때 값이 할당되어 있지 않으므로
  선언문 위에서 변수에 접근하면 reference error가 발생
  ```
</details>

<details>
  <summary>4 함수 선언문 내부의 this값</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>5 var 변수의 스코프</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

# 클래스

<details>
  <summary>1 static 메서드</summary>

  ### 코드
  ```js
  class Person {
    constructor(name) {
      this.name = name;
    }
  }
  ```
  ### 정답
  ```js
  class Person {
    constructor(name) {
      this.name = name;
    }

    static run() {
      console.log('run!');
    }
  }
  ```
</details>

# 함수

<details>
  <summary>1 함수 선언식과 함수 표현식의 차이</summary>

  ### 정답
  ```js
  foo();
  bar();

  function foo() {
    console.log('hello foo');
  }
  const bar = function () {
    console.log('hello bar');
  };
  ```
</details>

<details>
  <summary>2 클로저</summary>

  ### 정답
  ```
  실행 컨텍스트의 렉시컬 환경 객체를 참조하는 격리된 환경
  함수 실행이 종료되어 콜 스택에서 제거되어도 렉시컬 환경이 다른 함수 내의 변수에 의해 참조되어 메모리에 존재
  다른 변수가 렉시컬 환경을 참조하는 것 불가능하여 외부에서 접근이 불가능
  함수 종료 뒤에도 렉시컬 환경이 메모리에 남아있는 이유는 참조되고 있으므로 가비지 컬렉터가 삭제하지 않기 때문
  ```
</details>

<details>
  <summary>3 고차 함수</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>28 return 문이 없는 async 함수 호출 결과</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

# 프로토타입

<details>
  <summary>1 프로토타입 체인의 작동 방식을 이용하여 메서드 생성</summary>

  ### 코드
  ```js
  class Person {
    constructor(name) {
      this.name = name;
    }
  }
  ```
  ### 정답
  ```js
  Person.prototype.run = () => {
    console.log(this.name, 'is running!')
  }
  const p = new Person('kim');
  person.run();
  ```
</details>

# 비동기 처리

<details>
  <summary>1 await의 작동 방식</summary>

  ### 코드
  ```js
  async function getUser() {
    console.log('this is getUSer');
    
    const res = await fetch('http://localhost:3000');
    const user = await res.json();
    console.log(user);
  }
  ```
  ### 정답
  ```js
  await 전에는 동기적으로 처리
  await 부터는 비동기로 처리되어 마이크로 태스트 큐에서 대기
  ```
</details>

<details>
  <summary>2 Promise</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  비동기 코드를 작성할 때 콜백 지옥을 피하기 위해서 사용하는 객체
  then, catch 메서드를 사용하여 비동기 코드를 절차적으로 변경하여 콜백 지옥 문제 해결
  비동기 작업이 성공적으로 끝나면 fulfilled 상태: resolve 함수 호출로 발생
  문제가 생기면 rejected 상태: resolve 함수 호출로 발생
  ```
</details>

<details>
  <summary>3 이벤트 루프 작동원리</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>4 Promise 결과 2가지</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>6 Promise.all</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>7 Promise.race</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>


# 실행 컨텍스트

<details>
  <summary>1 아래 코드의 실행을 실행컨텍스트를 통해 설명</summary>

  ### 정답
  ```js
  var a = 1;
  const b = 10;

  function foo() {
    return 100;
  }
  const bar = () => {
    return 1000;
  };

  class Animal {
    constructor() {
      this.dna = string;
    }
  }

  const obj = {
    zoo: () => {
      return 2;
    }
  };
  ```
</details>

<details>
  <summary>2 호이스팅</summary>

  ### 정답
  ```
  코드 실행 전에 식별자가 먼저 메모리에 등록이 되기 때문에
  마치 코드 최상단으로 변수들이 끌어올려진 것 처럼 보이는 현상
  함수나 클래스 선언문은 값도 평가 단계에서 메모리에 등록
  var 변수는 undefined 값이 할당됨
  let 변수와 상수는 값이 없는 상태로 식별자만 메모리에 등록
  ```
</details>

# 배열

<details>
  <summary>1 unshift</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>2 shift</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>3 pop</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>4 push</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>5 filter</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>6 some</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>7 every</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>8 find</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>


# 기타

<details>
  <summary>1 이벤트 버블링과 캡처링</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  버블링: 이벤트 핸들러가 등록된 태그에서 이벤트가 발생한 경우 돔 트리 상위 레벨로
  이벤트가 전파되는 것
  캡처링: 
  ```
</details>

<details>
  <summary>13 currentTarget과 target 차이점</summary>

  ### 코드
  ```jsx
  function handler(e) {
    console.log(e.currentTarget);
    console.log(e.target);
  }

  <div onClick={handler}>
    <div></div>
  </div>
  ```
  ### 정답
  ```js
  currentTarget: 현재 이벤트 핸들러가 등록되어있는 태그를 참조
  target: 이벤트가 발생한 태그를 참조
  ```
</details>

<details>
  <summary>16 전개연산자를 사용하면 어떤 복사가 발생하나</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>18 가비지 컬렉터</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>20 ECMAScript와 자바스크립트 차이점</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>21 JSON.stringify</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>22 JSON.parse</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>23 for of</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>24 for in</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>25 얕은복사 깊은복사</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>26 statement 문</summary>
 
  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>


<details>
  <summary>29 전개연산자</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>30 유사 객체 배열</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>33 generator</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>34 자바스크립트 데이터 타입</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>


<details>
  <summary>46 iterable</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>47 iterator</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>48 setTimeout</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>49 setInterval</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>

<details>
  <summary>50 </summary>

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
<details>
  <summary></summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  ```
</details>
