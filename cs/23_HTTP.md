## HTTP
> HTTP(HyperText Transfer Protocol). 컴퓨터들 간 HTML 파일을 주고받을 수 있도록 하는 사전의 정의된 소통 방식.

- HyperText : html 문서간 연결 할 수 있는 링크로 구성된 것을 말한다.
- Transfer : 내 컴퓨터 뿐만 아니라 다른 컴퓨터들 간 사이에서도
- Protocol : 사전에 협의된 통신 규약을 말한다.

<br />

## 특징
- 요청과 응답(Request / Response)
- 상태없음(Stateless) -> 연속된 요청과 응답의 경우 매번 보내는것이 아닌 쿠키, 세션, 로컬 스토리지를 이용하여 해결

<br />

## 요청(request)구조
### Start Line
- HTTP Method
- Request Target
- HTTP Version
### Headers
-Key : Value(자바스크립트 : 객체 / 파이썬 : 딕셔너리)
```
Headers: {
	Host :
    User-Agent :
    Content-Type:
    Content-Length:
    Authorization:
}
```
<br />

### Body
- Post 메소드를 주로 사용
```
Body:{
	"id" : ,
    "name" : ,
    .
    .
    .
}
```
<br />

## 응답(response)구조
### Start Line
- HTTP Version
- Status Code
- Status Text

```
HTTP/1.1 404 Not Found
```

### Headers
- 요청 부분의 헤더와 동일
### Body
- 요청 부분의 바디와 동일. JSON 형식의 데이터 타입을 사용

```
Body:{
"message" : "Login_Success"
}
```

<br />

## HTTP Request Methods
- GET : 서버에서 데이터를 받아올 때. 가장 간단.
- POST : 데이터를 생성, 수정할 때. 대부분의 내용이 Body에 포함되어 보내진다.
- DELETE : 서버에서 특정 데이터를 삭제할 때.
## HTTP Response Methods
- 200 : 요청 성공
- 201 : 생성 성공
- 400 : 잘못된 요청
- 401 : 회원가입, 로그인 등 사전 작업이 필요할 때(권한없음)
- 403 : 해당요청 권한 없음(Forbidden)
- 404 : 요청된 URL 존재하지 않음
- 500 : 서버에러

