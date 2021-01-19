## Deque란

![](https://images.velog.io/images/finelinefe/post/1f8a549a-be16-410c-b2a2-dcaa83079ce7/D967_i2.jpg)

> 리스트의 양쪽 끝에서 삽입삭제가 가능한 자료구조. 스택+큐를 합친 구조이다. 스택의 각 bottom 영역을 이어붙여 top 부분이 좌우로 향한 구조라고 생각하면 된다.(양쪽에서 삽입삭제 연산 수행)


<br />


## 특징

![](https://images.velog.io/images/finelinefe/post/26355e01-3cc3-4d5e-8d6f-82d5199da1f1/D967_i1.jpg)

- 두개의 포인터를 사용한다. 각 양쪽에서 삽입삭제 연산을 실행
- 한쪽의 입력을 제한하는 입력제한데크(Scroll), 한쪽의 출력을 제한하는 출력제한데크(Shelf)가 있다
- 큐와 스택을 선형리스트 구조에 결합시킨 구조
- 스택의 bottom 부분이 연결된 것과 같다


<br />
