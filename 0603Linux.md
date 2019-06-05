# 0603(월) Spring and Linux

 ```java
  <build>
    <finalName>${artifactId}</finalName>
    <plugins>
      <plugin>
        <artifactId>maven-war-plugin</artifactId> <!-- war로 만들거니까 -->
        <configuration>
        <warSourceDirectory>src/main/webapp</warSourceDirectory><!-- war가   webapp으로
            만들어지므로 절대경로 설정 -->
        </configuration>
      </plugin>

      <plugin>
        <groupId>org.codehaus.mojo</groupId>
        <artifactId>tomcat-maven-plugin</artifactId>
        <configuration>
          <url>http://127.0.0.1:8080/manager/text</url> <!-- 로컬에서 로컬이기  때문에 이 주소가 가능 -->
          <path>/mysite2</path>
          <username>admin</username>
          <password>admin</password>
        </configuration>
      </plugin>
    </plugins>
  </build>
  ```

* mysite - (pom)
    * mysite2 -       web.xml ( xml)
    * mysite3 -      web.xml (javaconfig)
    * mysite4 -        x     (intialier, java config)
    * springboot-mysite x    (java config, application.properties)
wh
* jblog(Maven Project, pom) (부모메이븐)
    * jblog2(web.xml, xml 설정)
    * jblog3(web.xml, javaconfig)
    * jblog4(application initializer, javaconfig)
    * jblog5(Spring boot,application.properties, java config)
