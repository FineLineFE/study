## Mongo DB의 샤딩?
> 딘일 서버에서의 큰 취약점은 과부하, 데이터 처리량 증가에 따른 효율성 저하가 있다. 샤딩은 여러 시스템에 데이터를 분산적으로 배포하면서 이러한 문제점을 해결한다. 시스템 확장의 일종이다. MongoDB는 샤딩을 통해서 수평 확장을 지원한다.

<br />

## 수직적 확장
- 강력한 CPU 사용
- RAM 추가, 스토리지(저장용량) 추가
- 단일 서버 내에서의 용량 증가

<br />

## 수평적 확장
시스템의 데이터 세트를 분화. 여러 서버에 로드. 필요시 용량 증대를 위해 서버를 추가한다.
