# Overview

{program명}-{profile}.yml 로 정의후 

아래와 같은 URL로 접근하게 된다.

```http://localhost:{config-client}/{program명}/{profile}```

하지만, profile이 설정되지 않거나 매치되지 않는다면, 

{program명}.yml 을 설정파일로 사용하게 된다.

application-{profile}.yml 파일이 존재하게 되면, 해당 파일을 기본 설정파일로 사용하게 된다.
