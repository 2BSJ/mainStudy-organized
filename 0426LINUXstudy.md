#LINUX 0426 STUDY

####고정IP

* 192.168.1.46
  * IP : 192.168.1.46
  * NETMASK = 255.255.255.0
    >NETMASK랑 IP랑 AND연산을 하면 192.168.1.0 이나오고 다 같은 네트워크에 있게됨
    NETMASK의 제일 뒷자리가 0이면 255개 아이피를 쓰는거고 10이면 10개 20이면 20개 이런식이다
  * GETEWAY = 192.168.1.1
    >192.168.1.1 -> 공유기 (게이트웨이를 통해서 나감)
  * DNS1 = 168.126.63.1
  * 설정하는 루트
    >/etc/sysconfig/network-script/ifcfg-eth0
* 재부팅 shutdown -h no

* 포트번호 22 sftp

#### NETWORK PROGRAMMING

* ProjectExplorer = 논리적으로
* Navigator = 물리적으로
 >
* InetSocketAddress 는 InetAddress + Port를 가지고있음
* IP Address 는 InetAddress
* http : 웹서버 만드는 패키지
* test : ip랑 등등 테스트 하는 패키지
* util : 오늘 nslookup 할 과제할 패키지

* Stream
  * System.in 이 InputStream을 통해 byte단위로 들어오면 (주스트림) InputStreamReader(부스트림) 이 읽고 캐릭터로 변환시킨다.
  * 부스트림에 또 꽂아서 이어지는 Stream으로 BufferdReader 스트림을 만든다 이 BufferdReader은 내부적으로 버퍼를 가지고있다.
  그래서 이 스트림이 있으면 키보드로부터 입력을 받아서 버퍼에 채우고 이게 다 차거나 사용자가 fflush메서드를 이용하면 io가 발생해서 입력이됨
  불필요한 io를 줄일수 있어서 좋다
* Try catch 는 가독성이 떨어지고 상투적인 코드임 없으면 안되고 넣자니 쓸모없어서 Spring에서는 다 없어짐

* 데코레이션 패턴
  >Runtime시 객체를 받아와서
카스테라에 바닐라 붙히고 데코레이션 하는 개념
(상속과는 약간 다른데 비슷)

####2강 TCP 소켓 프로그래밍1

  * TCP 소켓 프로그래밍 절차
    >소켓 객체를 생성하고 -> 주소를 바인딩을 한다 ->
  * 서버를 만드는 이유는 http 프로토콜 이해하려고
