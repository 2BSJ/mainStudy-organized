방화벽 vi/etc/sysconfig/iptables 에서 
1yy로 복사한다음 p해서 한줄붙여넣기해서 포트를 9090으로 만들어줌(9090은 8080이랑 구별용으로)

/etc/init.d/iptables restart iptables 설정 리스타트로 적용해주고

/cafe24/tomcat-jenkins/bin/shutdown.sh
/cafe24/tomcat-jenkins/bin/startup.sh 해서 톰캣 구동시켜주고

젠킨스 열어보기

chkconfig --add tomcat-cafe24 이런식으로 켰을때 활성화

JkMountFile
