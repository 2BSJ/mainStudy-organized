# Jenkins

* Jenkins 접근 비밀번호 확인법

#### Jenkins 설치 방법

* jenkins홈페이지에서 .war파일 링크주소 복사후 리눅스 홈에서 wget 경로 해서  jenkins 받는다.
  그다음에 mv jenkis.war /usr/local/cafe24/tomcat/webapps/에 붙여넣기하면
  webapps에선 알아서 war파일이 압축이 풀린다.
  192.168.1.92:8080/jenkins 를 들어가면 들어가짐



* 오류 났을때는
  /root 에서 rm -rf .jenkins/ 제거 한뒤에 다시 처음부터받음

* local에서 빌드하는건 이클립스기반이고
  server에서 빌드하는건 프로파일링을 설정해줘야

* 젠킨스에서 빌드하는법!
  * -Pproduction을 젠킨스에서 적어주면 이클립스에 pom.xml에 있는 profile이 적용이된다.`clean package tomcat:redeploy -Pproduction -Dmaven.test.skip=true`



Username h3tmdwns
password
confirm password
full name 양승준
email address yyg0825@naver.com

save and continue

save and finish

start using jenkins
