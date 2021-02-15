## 1. 헷갈리지 말 것 ❗️❗️

### 1) 로컬 -> 외부로 DB sql 파일 생성(그대로 본 뜨는 것이기 때문에 명령어가 mysqldump=)
>  _mysqldump -u root -p `로컬DB name > 파일명.sql**`

<br />


![](https://images.velog.io/images/finelinefe/post/1314ed49-c8b5-4d18-a229-8ce11e04377d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-15%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2011.32.30.png)

### 1-2) 로컬 -> 외부로 Table sql 파일 생성(그대로 본 뜨는 것이기 때문에 명령어가 mysqldump=)
>  _mysqldump -u root -p `로컬DB name 테이블name > 파일명.sql`_

Mysqlworkbench에서 임의의 data를 .sql 확장자로 export할 경우 `TRUNCATE`를 별도로 지정, `SELECT * FROM TABLENAME 부분을 수정`해야하는 등 세 네번의 작업이 추가로 소용되므로, `터미널의 CLI 상에서 SQL 파일을 생성하는게 간편하다.`

<br />

### 2) 외부 -> 로컬로 DB sql 파일 dump(외부 파일을 적용하는 것이므로 명령어가 mysql)
>  _mysql -u root -p `로컬DB name < 파일명.sql`_



<br />

## 2. SQL file Dump(외부 sql -> 로컬 DB 적용)
![](https://images.velog.io/images/finelinefe/post/6889885c-e354-4a73-97de-1ad53471dc13/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-12%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%208.14.27.png)
> mysql -u root -p **project name** < (로컬 DB에 덤프하고자 하는)**해당파일name**.sql

1) 터미널에서 mysql 진입하는 명령라인에 **(mysql 진입 후 (x))**
**프로젝트 이름(앱 폴더이름 아님) < sql 파일 이름**을 적는다.

_ex) mysql -uroot -p nike_refactor < account.sql_


참고로 < 표시는 안으로 들어와 dump 하는 것이고, 
일반적으로 git ignore 목록으로 취급되어 외부로 빼는 requirement.txt 같은 파일의 경우 방향은 반대(>)이다.

> _1-1) < -> 로컬, 안쪽으로 파일을 dump_
_1-2) > -> 로컬, 안쪽에서 파일을 새로 생성(빼냄)_

또한 일부 테이블만 dump 할수도 있다.(sql 파일 자체를 일부만 가져오면 됨)

<br />



## 3. requirement

> pip install -r requirement.txt

어떤 프로젝트를 구성하는데 필수적으로 필요한 라이브러리 설치 등을 집약적으로 기술한 명세서.(txt 파일)

requirement 목록에 해당하는 수많은 라이브러리 등을 일일이 터미널에서 설치하는 것보다 한번의 cli 명령어로 설치할 수 있다. **(새 프로젝트의 requirement 목록을 한번에 일괄설치 할 수 있다.)**

<br />
