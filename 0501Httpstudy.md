# 네트워크 이해 0501

#### git

* jar로 하면 자바콘솔용 war는 웹어플리케이션용 pom은 멀티프로젝트용
`양식으로 봐야 보임`
```
eclipse java ProjectExplorer

|--/src/main/java
|    |---/echo
|          |
|          |---/EchoServer.java
|          |
|          |---/EchoClient.java
|
|
|--/src/main/resources
|    |---/echo
|          |
|          |
|          |---/config
|          |      |
|          |      |---echo.xml
|          |
|          
|--/bin
     |
     |---/echo
           |
           |---/EchoServer.class
           |---/EchoClient.class
           |
           |---/config
           |       |
                   |
                   |---echo.xml
```
>.jar 파일로 만들면 bin 부분이 jar로 들어가는거임
  이걸 리눅스에서 실행하려면 java -cp hello.jar echo.EchoServer 이런식으로 실행 하면

* pom.xml
  * `<dependencies>` 이 프로젝트는 이 태그안에 들어있는 라이브러리에 의존성이 있다를 명시함.

* string scanner 들의 객체는 JRE System library안에 있고 저 안에 들어있는 객체들에 의존성이 다 있고
Maven Dependencies안에 있는 클래스들에 다 의존성이 있다.

* 개발은 eclipse 에서 하고 network가 maven클래스가 아니었는데 maven클래스로 바꿔준 이유는 리눅스에서 maven으로 빌드해주려고 바꿈. 로컬환경과 리눅스환경이 달라서 이클립스에서 되도 리눅스에서 안될수 도 있

* thread thread = new chatting

package - chat
chat client
chatclientthread ->소켓가지고 들어가서 서버에서 오는거 출력
chatserver
chatserverthread

package - chatclientwindow
chatclientapp
chatwindow

실행

network/target/classes > java chat.ChatClient

클라 -> 닉네임>> 마이콜
서버 -> 입장하였습니다. 즐거운 채팅 되세요
클라 -> 아무도 없냐?
서버 -> 마이콜:아무도 없냐?
(4)
둘리님이 입장하셨습니다.
(5)
둘리님이 퇴장 하였습니다.

------
클라2 -> 닉네임>> 둘리 (4)
서버 -> 입장하였습니다. 즐거운 채팅 되세요
클라2 -> quit(5)

-------

java chat.client.win.ChatClientApp
