## 암호화란?
![](https://images.velog.io/images/finelinefe/post/06a06e27-1b47-498b-bcfe-889495f4394e/image.png)

> 인증 인가에 앞서 개인정보 보호 등을 위해 필수적으로 해야하는 요소.

암호화의 세부 과정은 다음과 같다.
<br />
![](https://images.velog.io/images/finelinefe/post/14cf09d3-77cc-4b23-b43a-339366bff62c/%E1%84%8B%E1%85%A1%E1%86%B7%E1%84%92%E1%85%A9%E1%84%92%E1%85%AA.jpeg)bcrypt에서 지원하는 암호화는 바이트 형식의 데이터를 말한다. 
그러므로 일반적으로 입력된 스트링 형식의 데이터를 바이트 형식으로 바꿔줄 필요가 있다.
이것을 **인코딩** 한다고 하며 **string -> byte** 형식으로 바꾼다.
그 반대의 경우에는 **디코딩** 이라고 하며 **byte - string** 형식이 된다.

```python
password = '1234'
hashed_password = bcrypt.hashpw(password.encode('utf-8'), bcrypt.gensalt())
print(hashed_password)
b'$2b$12$YFs9rh.1LgJwZuf9ibyjpuLvBoCaGX0MzedFWF2Jo0zU3lMZurZ4a'
```
마찬가지로 예제를 보면 인코드/디코드 시에는 알아볼 수 있는 유니코드 문자 규격인 **UTF-8** 을 사용한다. 
```python
type(hashed_password)
<class 'bytes'>
```
그리고 암호화 된 문자를 얻을 수 있다 **(형식은 byte)**. 
이 경우의 암호화 방식은 단방향 암호화 이므로 복호화가 불가능하다.

> bcrypt.checkpw(입력받은 문자, 암호화 하여 저장된 문자) **// 반드시 둘다 byte여야 함**

그렇기 때문에 원래 문자를 확인하는 방법으로 **bcrypt.checkpw()** 메소드를 사용하며 기본 형태는 위와 같다.


<br />

## 단방향(One-Way Hash Function)이란?

한번 암호화 시 복호화 불가능. 쉽게 말해 삶은 감자를 가지고 **해쉬포테이토**를 만드는 것을 생각하면 쉽다. 해쉬포테이토를 만들면 으깬 것으로 원형의 감자 모양으로 되돌릴 수 없는 것처럼 생각하면 된다. 그리고 암호화 된 결과물을 **digest** 라고 한다.

<Br />

## Bcrypt(SHA-256 암호화 알고리즘)
* salting, key stretching을 쉽게 하기 위해 사용되는 대표적인 라이브러리
* 다양한 언어를 지원하며 간편하다
* 해쉬 결과값 = salting+hash 값 같이 보관 -> DB 설계의 복잡화 최소화


<br />

## Salting, Key Stretching

단방향 해쉬 함수의 취약점은 레인보우 테이블(해쉬값을 계산 해 놓은 별도의 테이블) 공격에 취약하기 때문이다. 뿐만 아니라 해쉬 함수 특성상 검색 성능 향상을 목적으로 고안되었기 때문에 해킹 시 빠른 속도로 대조할 수 있다는 점에서 보안 우려가 있다.

* salting : 위와 같은 문제점을 해결하기 위해 추가적인 데이터를 넣어 해시값을 계산한다
* key stretching : 반복적으로 해싱함으로써 유추하기 어렵게 한다.



<br />
<br />
