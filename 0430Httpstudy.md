# 네트워크 이해 0430

#### RequestHandler

* ```java
  try{
    FileInputStream fs = new FileInputStream(DOCUMENT_ROOT)
  }catch(FileNotFoundException e){

  }
  //------------------------------
  File file = new File(DOCUMENT_ROOT + url);
  if(file.exists()==false) {

  }
  ```
  위와 아래의 코드는 똑같이 없는걸 검사하는 코드지만 위의 코드처럼 if문을 쓸수 있는데도
  오류문으로 catch로 잡아내는거는 바보같은 짓이다. 우선 객체도 생성할 뿐만아니라
  메모리 부분에서도 문제가있음. if로 검사가 가능한경우엔 무조건 if로 할것


* 개행할떄 `\r\n` 하는 이유![Uploading 캡처1.PNG… (kx87itdwq)]()는 옛날방식이 \r이 캐리지리턴 \n은 뉴라인해서 두개를 같이썻다
  리눅스에선 \r\n하고 윈도우는 \n에 \r\n이 합쳐져있다.

* 브라우저가 이 html을 파싱하면서 css가 있어서 한번 요청하고 이미지파일이 있어서 이미지를 또 요청하고 이런식으로 진행한다.
----------------------

##### UDP Echo 서버/클라이언트
* udp time 서버 java callender

-----------------------------
##### TCP 소켓 프로그래밍
![tcp header](https://i.imgur.com/KUt8M0y.png)

* TCP는 데이터를 전송하고나서 ACK가 안오면 여러번 시도하고 여러번 시도에 안될때 소켓에러를 발생시킨다.

----------------

##### JAVA 채팅

* JAVA base64로 인코딩 디코딩을 해서 보내면
채팅 문제가 없어짐
* 사용자 contents를 변경해서 db에 저장하면 안됨.**원칙!!**
