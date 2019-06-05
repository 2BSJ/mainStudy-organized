# Mysite 3

* 멀티프로젝트를 할때에 부모 프로젝트는 메이븐생성할때 pom으로 만들어줌(jar,war,pon)중에
  그러고나서 src폴더를 지우고 공통되는 pom을 작성
  예를들면 스프링코어,스프링웹,스프링mvc나 빌드에서 컴파일러 플러그인등
  조심해야할건 war플러그인은 멀티프로젝트에 jar형식이 있을수도 있으니 공통되지 않기떄문에
  빼주는게 좋음

* 부모 프로젝트를 생성했으면 그다음엔 자식 프로젝트를 생성해야한다.
  maven-module 프로젝트로 생성하면 알아서 부모프로젝트 아래로 들어감
  그러고나서 개별적으로 가져야하는 라이브러리는 따로 pom에 놔두고
  중복되는 라이브러리는 부모에게 상속받아서 내려받음
  자식프로젝트가 라이브러리가 중복이되도 부모가 줄때 덮기때문에 상관안해도됨


* javaconfig로 설정하기. (spring-servlet.xml) 에있는 내용들을 다 config파일로 생성함.
  applicationContext.xml -> AppConfig.class로 설정.

  @EnableAspectAutoProxy -> autoproxy 설정
