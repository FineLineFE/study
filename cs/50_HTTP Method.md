## HTTP Method

> HTTP 메소드(HTTP Method)를 이용해 클라이언트가 서버에 데이터를 전송하고, 반대로 서버에서 클라이언트로 데이터를 회신할 수 있다. 클라이언트가 서버에 데이터를 요청할 때는 GET 메소드를 사용하고, 클라이언트에서 서버로 회신할 때는 POST 메소드를 사용한다.


### GET
> GET [request-uri]?query_string HTTP/1.1 Host:[Hostname] or [IP]

요청받은 URL의 정보를 찾아 응답(READ)

<br />

### POST
> POST [request-uri] HTTP/1.1 Host:[Hostname] or [IP] Content-Lenght:[Length in Bytes] Content-Type:[Content Type]

요청 자원을 생성(CREATE)

<br />

### PUT
> PUT [request-uri] HTTP/1.1 Host:[Hostname] or [IP] Content-Lenght:[Length in Bytes] Content-Type:[Content Type]

요청 자원을 수정(UPDATE)

<br />

### PATCH
> PATCH [request-uri] HTTP/1.1 Host:[Hostname] or [IP] Content-Lenght:[Length in Bytes] Content-Type:[Content Type]

요청 자원을 일부 수정. PUT은 전체 수정(UPDATE)인 반면 PATCH는 일부 수정

<br />

### DELETE
> DELETE [request-uri] HTTP/1.1 Host:[Hostname] or [IP]

요청 자원을 삭제(DELETE)

<br />
