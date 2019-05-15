# mysql 0503

#### mysql command line

* 데이터타입으로 varchar(20)은 3크기의 데이터가 들어오면 3으로 줄여준다.
   char은 그런거 상관없이 그 크기대로 넣는데
    varchar은 안에 알고리즘이 구현되어있어서 자동으로 줄여주는데 아무래도 로직이 조금 돌다보니 char보다는 좀 느리지만 디스크를 효율적으로 쓸 수 있다.

* DDL은 롤백이안되는 쿼리.
  롤백이 되는 쿼리는 DML - Insert,update,delete가 롤백이됨.

* xtp4로 webmaster 아래에 .txt 파일을 넣어놓고 load data local infile '/home/webmaster/pet.txt' into table pet;
  이렇게 해놓으면 테이블에 알아서 들어감 데이터간에 식별자는 기본이 탭이고 설정시 다르게 구현가능하다.

* mysql -p < employees.sql ->employees.sql가 있는 폴더에 들어가서 이렇게 풀어줌.

* /etc/sysconfig/iptable 에서 방화벽설정해주고 telnet ip 방화벽 으로 방화벽확인해준다.

* 3.hr 계정생성
  3-1 로컬접근 hr 계정 생성
      create user 'hr'@'localhost' identified by 'hr';

      권한부여
      grant all privileges on employees.* to 'hr'@'localhost';

      권한 부여 하고나선 flush privileges 해주는게조음
  3-2 192.168.1.\* 에서 접근하는 hr계정
      create user 'hr'@'192.168.1.%' identified by 'hr';
      집에서는  192.168.\* 에서 접근하는 hr계정
      create user 'hr'@'192.168.%' identified by 'hr';

      권한부여
      grant all privileges on employees.* to 'hr'@'192.168.1.%';


#### SQL

* DML
  - select(99%)    
  - insert
  - update
  - delete

  기본, 집계, JOIN, subQuery
* DDL(Data Modeling) -> 논리(ERD)  -> 물리(Table)

* DBApplication

* in ( a, b) -> a이거나 b일때

* DB에서 자바로 넘겨서 가공하는게 아니라 DB에서 가공을 끝낸후 자바에서 처리할것. DB가 훨씬 속도가 빠르기떄문.
