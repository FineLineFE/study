## 작업순서
> 1) _mysql -u root -p 로컬DB이름_ **로컬 DB <- 변경사항.sql 파일 dump**
2) _로컬DB -> 운영DB_ **변경된 로컬 DB를 실 운영DB에 그대로 적용**
2-1) _2)번의 작업을 MYSQL WORKBENCH로 수행_ **collate 0900_ai_ci 문제수정, 주석처리, 원래 collate 양식으로 수정 후 적용**

<br />

## Local -> AWS dump

> _mysql-h **(AWS DB이름)** -u root -p **(운영서버 DB이름)** **<** **(local에서 추출한 sql 파일이름).sql** => 패스워드 입력 => 입력 완료 시 dump_

<br />
