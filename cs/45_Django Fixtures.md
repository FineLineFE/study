## Fixtures

> Fixtures = 실제 DB의 데이터를 Json 형식, Yaml, Xml 형식으로 Django에 insert 할 때 사용

일반적으로 장고에서 지원하는 Mock Data 등을 통한 단위(유닛) 테스트는 실제 DB 에 영향을 미치지 않게 SetUP, TearDown 등으로 그 기능을 제공했다. 장고는 실제 DB의 접근에 대해서는 상당히 폐쇄적이기 때문이다.

그러나 경우에 따라서 실제 DB 상에 들어있는 데이터를 가지고 테스트를 해야 할 필요가 있을 경우 이와 같은 기능을 제공하는 것이 있다. Fixture 란 것이다.

## Fixtures Dumpdata

> ** python manage.py dumpdata 앱이름.모델이름 > 파일명.json**


1) 실행하고자 하는 APP 안에 Fixtures 폴더 생성(mkdir fixtures)
하지만 
2) python manage.py 상으로 이동

**3) python manage.py dumpdata _앱이름.모델이름(❗️❗️❗️단수) > 파일이름.json**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(이러한 json 파일로 fixtures 라는 폴더에 저장하겠다는 뜻)

4) vscode 혹은 vim 에서 fixtures 폴더 내에 json 파일 생성됐는지 확인


## (+) Dumpdata 정렬

> **python manage.py dumpdata 앱이름.모델이름 --indent N > 파일명.json

> **python manage.py dumpdata 앱이름.모델이름 --indent N > /사용자경로/파일명.json => ❗️해당 fixtures 폴더 안에 json 파일 그대로 저장

위의 방식으로 data를 dump 할 경우 정렬이 되지 않은 말 그대로 한줄짜리로 데이터가 들어와 가독성이 떨어진다. 조금 더 예쁘게 data를 json 형식으로 dump 하고 싶다면 **indent N(line number)** 옵션을 명령어 중간에 추가해주면 된다.


## 경고는 경고일 뿐

> order.Order.order_extra: (fields.W340) null has no effect on ManyToManyField.

data를 dump 하다보면 터미널 하단에 이러한 경고 문구가 뜨나 오류는 아니니 걱정할 필요 없다. Django의 fixture 기능은 다대다 관계 테이블에 관해서도 이러한 기능을 똑같이 효율적으로 제공한다


<br />
