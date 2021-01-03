## Git Flow

![](https://images.velog.io/images/finelinefe/post/17d0ef23-eba6-40ef-9d47-d4021ef8596a/git%20flow.png)

> 일반적으로 Master, Develop, Feature, Release, Hotfix 5가지 브랜치를 사용해 개발 전반에 대한 운영을 하는 것을 의미한다.

<br />

## 각 브랜치

- **Master**  : 배포 브랜치, 기준이 되는 브랜치 중 하나.

- **Develop** : 개발 브랜치, 각 개발자들이 개발한 Feature 브랜치들이 Merge 된 최종 브랜치.

- **Feature** : 작업 단위 개발 브랜치, 각 개발자들이 담당하는 기능을 개발하는 별도의 브랜치이며 완료시 Dev 브랜치에 Merge 된 후 삭제된다.(다른 기능 추가 시에는 별개의 Feature 브랜치 생성-삭제)

- **Release** : Develop 브랜치에서 Master 브랜치로 최종 배포 직전 QA 테스트를 위해 생성하는 브랜치. / 출시(Master 배포) 버전 이후로 차후 버전 배포를 위해 생성하는 브랜치

- **Hotfix**  : 제품 사용 중에 발견된 버그(Bug)의 수정(Fix)이나 취약점 보완, 또는 성능 향상을 위해 긴급히 배포되는 응급 패치 프로그램. Master 브랜치로 배포 후 버그 발생 시 간단한 수정을 위해 존재하는 브랜치.

<br />

## Fork

![](https://images.velog.io/images/finelinefe/post/a9dcf36c-f83b-4e60-b630-cab296b80f27/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-01-02%2023.23.20.png)

> 메인 Repo에 있는 소스코드를 개인 Github에 복사하는 것. Fork를 실행하게 되면 **Github ID / Fork 주소** 로 개인 레파지토리 목록에 추가된다. 쉽게 말해 프로젝트 전체를 복제한다고 생각하면 된다.

일반 branch와 다른 것은 branch는 Merge라는 작업으로 통합되지만 Fork의 경우엔 Pull request를 통해 Merge 된다.


<br />
