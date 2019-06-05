# Junit 0527

com.cafe24.springcontainer.User
com.cafe24.springcontainer.soundsystem
com.cafe24.springcontainer.videosystem
    |-DigitalVideoDisc
    |-Avengers
    |-DVDPlayer
    |-BlankDisc
    |-DVDPack

    --- src/main/java

    config.user
    	|---- UserConfig.class
    config.soundsystem
    	|---- CDPlayerConfig.java (자동
    config.videosystem
    	|---- DVDPlayerConfig.java (명시적설정)

    ===src/main/resources

    config.user
    	|---- UserConfig.xml
    config.sundsystem
    	|---- CDPlayerConfig.xml(자동)
    config.videosystem
    	|---- DVDPlayerConfig.xml(명시적설정)

    ===src/test/java
    	|-----com.cafe24.springcontainer.soundsystem
    		|----CDPlayerJavaConfigTest.java
    		|----CDPlayerXmlConfigTest.java
    	|-----com.cafe24.springcontainer.videosystem
    		|----DVDPlayerJavaConfigTest.java
    		|----DVDPlayerXmlConfigTest.java
    		|----DVDPlayerMixingConfigTest01.java
    		|----DVDPlayerMixingConfigTest02.java
    		|----DVDPlayerMixingConfigTest03.java

* annotation의 종류
  * @Component ---Spring지원
    @Named ---java표준(디펜더시 추가해야됨)

    @Autowired ---Spring지원
    @iNJECT ---JAVA표준(디펜더시 추가)
