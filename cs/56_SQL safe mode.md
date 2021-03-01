> Error Code: 1175. You are using safe mode and you tried to update a table without a WHERE that uses a KEY column To disable safe mode.

SQL 문을 UPDATE 또는 DELETE 구를 사용해 변경하고자 할 때 간혹 보는 에러 현상이다. 
이는 일시적으로 테이블과 외래키 관계에 있는 다른 테이블까지 `임시적 연결해제` 하는 명령어와 동일하다.

### How to Solve

 `SET SQL_SAFE_UPDATES = 0; ` 를 사용한다.
 
 <br />
