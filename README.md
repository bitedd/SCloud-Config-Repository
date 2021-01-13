# Overview


 * 각기 다른 환경을 위한 설정을 가질 수 있는 가장 쉬운 방법
 
 
 * {program명}-{profile}.yml 로 정의후 

 * 아래와 같은 URL로 접근하게 된다.

```http://localhost:{config-client}/{program명}/{profile}```

* 하지만, profile이 설정되지 않거나 매치되지 않는다면, {program명}.yml 을 설정파일로 사용하게 된다.

* application-{profile}.yml 파일이 존재하게 되면, 해당 파일을 기본 설정파일로 사용하게 된다.

* application이라는 이름이 일종의 default명칭인거 같기도 하다.

 * 실행 옵션에 profile을 지정하는 경우는 아래와 같이 지정하면 된다  
   * -Dspring.profiles.active={환경}


 * @RefreshScope
   * 이 annotation은 http://192.168.0.1:8080/refresh 이렇게 주소를 입력하면 변경된 설정파일을 로드할 수 있게 해준다.

# 설정에 대한 여러가지 access방법

 * application.properties에 접근하는 방법은 여러가지 있는데. 아래처럼 Environment를 이용해서 접근도 가능하다.
 ```
 @Autowired
 private Environment env;
 
 env.getProperty("application.properties에 설정한 프로퍼티명");
 ```



