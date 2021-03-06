## JWT
> JWT(Jason Web Token). json 기반 표준에 의존하여, 쉽게 말해 토큰 기반 인증 방식이다.

토큰 또한 쿠키나 세션과 같은 인증 방식 중 하나이지만 토큰의 장점은 아래와 같다.

- 쿠키, 세션과 다르게 별도 관리가 필요하지 않음
- 저장소를 따로 필요로 하지 않기 때문에 유지보수에 용이
- 그러나 별도 관리가 없기 때문에 토큰 탈취시 토큰의 수명에 따라 그 시간만큼 얼마든지 정보를 사용할 수 있다.
- 저장소가 없기 때문에 세션과 쿠키에 비해서 길이가 긴 편. 다인증 시 서버에 과부하를 불러올 수 있다

<br />

## Access Token
로그인 수행 시 필요한 보안 정보가 들어있는 객체의 일종. 로그인 할 때 만들어지며 사용자, 사용자 그룹 및 특권을 식별하여 시스템에서 보안 객체의 접근과 시스템 운용 제한을 위해 사용된다.

<br />

## Refresh Token
갱신된 기존의 access token을 다시 얻는데 사용되는 토큰이다. 새 새로고침 토큰을 발급함에 따라 Auth0에 대한 각 요청이 있을 시에 기존 발급된 선행 토큰을 무효화 함으로써 보안을 강화할 수 있다.

<br />

## 토큰 발행 과정
![](https://images.velog.io/images/finelinefe/post/13943ed3-f47a-4338-a795-71a361f29365/Screenshot%202020-12-15%20at%2017.07.46.png)

리프레시 토큰은 새 엑세스 토큰을 획득하는데 사용되는 자격 증명과 같다.

- 리프레시 토큰 수명 > 액세스 토큰 수명
- 리프레시 토큰 또한 만료될 수 있지만 오래 지속
- 현재의 액세스 토큰 만료 또는 유효하지 않게 되면 권한 부여 서버에서는 리프레시 토큰을 얻기 위해 클라이언트에 리프레시 토큰을 제공

<br />

### 1단계
클라이언트는 권한 부여를 제공하여 서버에 인증한다

### 2단계
권한 부여 서버에서는 클라이언트의 인증을 실시한다. 유효한 경우 액세스 토큰과 리프레시 토큰을 클라이언트에게 발급

### 3단계
클라이언트는 서버에서 부여받은 액세스 토큰을 제공하여 리소스에 대한 권한을 리소스 서버에 요청한다

### 4단계
리소스 서버는 클라이언트의 액세스 토큰을 확인 후 제공

### 5단계
클라이언트는 앞 단계와 마찬가지로 액세스 토큰이 만료되기 전까지 리소스 서버에 대해 권한을 요청하고 리소스 요청을 반복

### 6단계
액세스 토큰 만료시 클라이언트는 권한 부여 서버로 인증 후 리프레시 토큰을 제공하여 새 엑세스 토큰을 요청. 액세스 토큰이 잘못된 경우 리소스 서버에서는 잘못된 토큰 오류 응답을 클라이언트에 보내야한다

### 7단계
클라이언트는 리프레시 토큰을 부여하여 권한 부여 서버로 인증

### 8단계
인증 서버는 클라이언트를 인증한 뒤 리프레시 토큰의 유효성을 검사한다. 유요한 경우 새 액세스 토큰을 발급

<br />

