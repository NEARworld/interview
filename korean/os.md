<details>
  <summary>1 32비트 시스템에서 가상 메모리 주소의 길이와 갯수</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  32비트, 2^32개 (비트가 모두 0인 주소 -> 비트가 모두 1인 주소 카운트)
  ```
</details>

<details>
  <summary>2 32비트 시스템에서 가상 메모리 주소 공간의 크기</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  4GB

  1KB = 2^10 bytes = 1024 bytes
  1MB = 2^10 KB = 1024 KB
  1GB = 2^10 MB = 1024 MB
  4GB = 2^10 bytes * 2^10 bytes * 2^10 bytes * 2^2
  ```
</details>

<details>
  <summary>3 가상 메모리를 구현할때 필요한 하드웨어</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  MMU (Memory Management Unit)
  가상 메모리 주소를 물리 메모리 주소로 변환
  ```
</details>

<details>
  <summary>4 가상 메모리 주소의 구성</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  20비트는 가상 페이지 번호
  12비트는 페이지 오프셋

  예시: 0x00105102
  가상 페이지 번호: 0x00105
  페이지 오프셋: 0x102
  ```
</details>

<details>
  <summary>5 32비트 가상 메모리 주소를 16진수로 나타내기</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  0x00000000 (8자리)
  16진수로 나타낸경우 한자리당 4 bit
  4 bit * 8자리 = 32 bit
  ```
</details>

<details>
  <summary>6 32비트 시스템에서 가상 메모리 작동 원리</summary>

  ### 코드
  ```js
  ```
  ### 정답
  ```js
  가상 메모리 주소의 20비트를 페이지 번호로 사용하고 이 가상 페이지 번호를 페이지 테이블(TLB)에서 찾는다.
  가상 페이지 번호에 매핑된 물리 페이지 번호와 페이지 오프셋(가상 메모리 주소 12비트)을 합친다. 
  ```
  참고: https://blogs.vmware.com/vsphere/2020/03/how-is-virtual-memory-translated-to-physical-memory.html
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
