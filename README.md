# Overview

{program명}-{profile}.yml 로 정의후 

아래와 같은 URL로 접근하게 된다.

```http://localhost:{config-client}/{program명}/{profile}```

하지만, profile이 설정되지 않거나 매치되지 않는다면, 

{program명}.yml 을 설정파일로 사용하게 된다.

application-{profile}.yml 파일이 존재하게 되면, 해당 파일을 기본 설정파일로 사용하게 된다.


 * 실행 옵션에 profile을 지정하는 경우는 아래와 같이 지정하면 된다  
   * -Dspring.profiles.active={환경}


 * @RefreshScope
   * 이 annotation은 http://192.168.0.1:8080/refresh 이렇게 주소를 입력하면 변경된 설정파일을 로드할 수 있게 해준다.
