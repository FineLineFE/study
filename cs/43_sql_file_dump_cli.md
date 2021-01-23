## SQL file Dump
> mysql -u root -p (project app) < 해당파일.sql



1) 터미널에서 mysql 진입하는 명령라인에 **프로젝트 폴더 이름 < sql 파일 이름**을 적는다.
참고로 < 안으로 들어와 dump 하는 것이고, 일반적으로 git ignore 목록으로 취급되어 외부로 빼는 requirement.txt 같은 파일의 경우 방향은 반대이다.
또한 일부 테이블만 dump 할수도 있다.(sql 파일 자체를 일부만 가져오면 됨)

<br />

## requirement

> pip install -r requirement.txt

어떤 프로젝트를 구성하는데 필수적으로 필요한 라이브러리 설치 등을 집약적으로 기술한 명세서.(txt 파일)
requirement 목록에 해당하는 수많은 라이브러리 등을 일일이 터미널에서 설치하는 것보다 한번의 cli 명령어로 설치할 수 있다.

<br />
