# RDBMS의 이해 0501

#### 데이터베이스의 기본개념

* RDBMS를 처음 접했을때 속도보다는 데이터모델링을 정확하게 하고 SQL문도 잘 작성하여서
  신뢰성을 확보해야 한다.

da data arcitect -> 비즈니스 분석해서 query만들고 erd 설계하고 스키마 만들고
Database Admin -> 테스팅 할때 sql날라가는거 모니터링해서 메모리 많이잡는것들 같은거 잡아냄.
->dbms 별로 admin 특화되어있음 oracle admin,mysql admin 등등 이렇게
Database Developer ->

* chown -R mysql:mysql /usr/local/cafe24/mariadb -> mariadb의 -R(모든 디렉토리에 권한) 을 줌
  cp -R /usr/local/cafe24/mariadb/etc/my.cnf.d/ /etc 에 옮겨놔야댐
  (우리 잘못은아니고 스크립트환경에서 .d를 확인을 못해서 수동으로 옮겨)

* mysql -u -D -p

* cp /usr/local/cafe24/mariadb/support-files/mysql.server /etc/init.d/mariadb
  데몬에 추가

* chkcnfig로 확인후 chkconfig mariadb on 으로 데몬을 올려줌

* /etc/profile 로 가서 PATH설정을 해주면 아무대서나 mysql을 치면 알아서 들어가짐~!
