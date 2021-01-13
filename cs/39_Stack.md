### Stack 구조

> 데이터를 후입선출 구조로 유지하는 추상 데이터형. 아래부터 쌓은 구조를 생각하면 이해하기 쉽다. 가장 먼저 들어온 것이 아래에 쌓이기 때문에 맨 마지막에 들어온 것이 가장 먼저 나간다.(LIFO)

선형 자료구조의 하나이다. Last In First Out. 일반적으로 콘 아이스크림을 쌓다보면 맨 처음에 쌓은 맛은 가장 마지막에 먹을 수 있게 된다. 스택은 가장 먼저 들어온 데이터가 가장 나중에 나가게 되고 반대로 가장 나중에 들어온 데이터가 먼저 나가는 구조를 취한다.

<br />

![](https://images.velog.io/images/finelinefe/post/21224fab-0b8a-4975-aefa-cf53c1308d1d/S1809_i1.jpg)
스택의 윗부분을 top, 윗 부분에 데이터를 집어넣는 것을 push, 꺼내는 것을 pop 이라 한다. push, pop의 연산 과정은 top 에서 +-1씩 가감하면서 진행된다.



![](https://images.velog.io/images/finelinefe/post/0ff66040-f544-4754-bd07-931c0cecf37d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA,%202020-09-09%2014-13-01.png)

#### 예시

- 인터넷 브라우저의 이용 history
- pwd 명령어
- 함수 실행시 콜 스택 등

<br />