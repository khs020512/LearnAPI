# Learn C++ STL
### STL 공부 순서
1. STL에 대한 구조 공부
2. STL 구성요소 공부
3. STL를 이용한 예시 코드 작성


## STACK STL 공부
### 1. 스택이란?
* 스택은 컴퓨터에서 가장 많이 사용되는 자료 구조이다.
* LIFO : (Last-In-First-Out) 후입선출의 구조를 가진다.
![stack-gif](https://github.com/khs020512/LearnAPI/assets/97209803/bdb1f7bd-2cc3-4c5f-9230-bd4b6a7d661b)
### 2. 스택의 구성 요소
* **스택의 생성(선언) (Stack)**
  * 스택을 생성하는 연산
  * **stack<데이터 타입> 스택이름;** 의 형태로 생성한다
  ```
  stack<int> myStack;
  ```
* **스택 공백확인 연산 (empty)**

  * 스택이 비었는지 아닌지 확인하는 연산
  * Bool타입의 함수로 true 또는 false 로 return값이 생성된다.
  * **스택이름.empty()** 의 형태로 사용한다.
  ```
  if(!myStack.empty()){
    ...
  }
  ```
  
* **스택 크기 확인 연산 (size)**
  * 스택속의 데이터가 얼마나 들어있는지 확인하는 연산
  * int타입의 함수로 비었을 때에는 -1을 반환하고 비어있지 않을 때에는 크기 값을 반환한다
  * **스택이름.size()** 의 형태로 사용한다
  ```
  size = myStack.size();
  ```
* **스택 최상단값 확인 연산 (top)**
  * 스택의 최상단값을 확인하는 연산
  * 스택의 데이터 타입에 따라 반환하는 값이 다름
  * **스택이름.top()** 의 형태로 사용한다
  ```
  top = myStack.top();
  ```
* **스택 삽입 연산 (push)**
  * 스택속에 데이터를 삽입하는 연산
  * 스택의 최상단에 데이터를 저장함
  * **스택이름.push(데이터 값)** 의 형태로 사용한다
  ```
  myStack.push(10)
  ```
* **스택 삭제 연산 (pop)**
  * 스택속의 데이터를 삭제하는 연산
  * 스택의 최상단의 데이터를 삭제한다.
  *  **스택이름.pop()** 의 형태로 사용한다.
  ```
  data = myStack.pop();
  ```
* **스택 삽입 연산_2 (emplace)**
  * 스택의 push와 비슷한 연산
  * 특정 클래스의 스택일 경우 해당 args를 그 클래스의 생성자로넘겨 해당 클래스의 객체를 생성해 push한다.
  * **스택이름.emplace(args)** 의 형태로 사용한다.
  ```
  myStack.emplace("First sentence");
  ```
* **스택 바꾸기 연산 (swap)**
  * 두개의 스택을 바꾸는 연산
  * 서로 다른 스택이 있을 때 각 스택의 구성요소 전부를 서로 바꾼다.
  * **스택이름.swap(바꿀스택의 이름)** 의 형태로 사용한다.
  ```
  stack<int> foo.bar;
  ...
  foo.swap(bar);
  ...
  ```
  
## QUEUE STL 공부
### 1. 큐 란?
* 큐는 먼저들어온 데이터가 먼저나가는 **선입선출(First-In-First-Out)** 의 구조를 가진다.
* front와 rear의 인덱스값을 한방향으로 움직이면서 데이터를 저장 또는 출력한다.
![queue-gif](https://github.com/khs020512/STL_STACK/assets/97209803/df3ef1da-1af9-4cae-a8b6-9ba8097a724d)

### 2. 큐의 구성요소
* **큐의 생성 연산**
  * 스택의 생성연산
  * **queue<데이터 타입> 큐의이름**,의 형태로 생성한다.
  ```
  queue<int> myQueue;
  ```
* **큐의 공간 확인 연산(empty)**
  * 큐의 빈공간을 확인하는 연산이다.
  * bool타입의 함수로 리턴값은 true 또는 false 이다.
  * **변수이름.empty()** 로 사용한다.
  ```
  if(!myQueue.empty()){
    ...
  }
  ```
* **큐의 크기 확인연산(size)**
  * 큐에 들어있는 데이터의 개수를 확인하는 연산이다.
  * * **변수이름.size()** 로 사용한다
  ```
  size = myQueue.size;
  ```
* **큐의 최선두값 접근연산(front)**
  *큐의 맨 앞에있는 데이터에 접근하는 연산이다.
  * **변수이름.front()** 로 사용한다
   ```
   myQueue.push(55);
   myQueue.push(66); // 큐의 데이터 삽입 순서 55 -> 66
   x = myQueue.front; // 큐의 front값에 접근 -> 55에 접근
   cout << x; // 55 출력
   ```
* **큐의 최후방값 접근연산(back)**
  * 큐의 맨 마지막에 있는 데이터에 접근하는 연산이다.
  * **변수이름.back()** 로 사용한다
    ```
    myQueue.push(55);
    myQueue.push(66); // 큐의 데이터 삽입 순서 55 -> 66
    x = myQueue.back; // 큐의 back값에 접근 -> 66에 접근
    cout << x; //66 출력
    ```
* **큐의 데이터 삽입연산(push)**
  * 큐의 맨 뒤에 데이터를 삽입하는 연산이다.
  *  **변수이름.push(데이터 값)** 로 사용한다.
    ```
    myQueue.push(55);
    ```
* **큐의 데이터 삭제연산(pop)**
  * 큐의 맨 앞에 데이터를 삭제하는 연산이다.
  *  **변수이름.pop()** 로 사용한다.
    ```
    x = myQueue.pop();
    ```
* **큐의 클래스형 데이터 삽입연산(emplace)**
  * 큐의 맨 뒤에 클래스형 데이터를 삭제하는 연산이다.
  *  **변수이름.emplace(클래스형 테이터)** 로 사용한다.
    ```
    queue<string> myQueue;
    myQueue.emplace("First Sentence");
    myQueue.emplace("Second Sentence");
    ```
* **큐의 교환 연산(swap)**
  * 서로 다른 큐를 교환하는 연산이다.
  *  **변수이름.swap(바꿀 변수의 이름)** 로 사용한다.
    ```
    queue<int> foo,bar;
    foo.push(10),foo.push(20);
    bar.push(111);
    foo.swap(bar);
    cout << foo.size << endl;
    cout << bar.size << endl;
    ```

## DEQUEUE STL 공부
### 덱이란?
* 
## LIST STL 공부
