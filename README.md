# Sertrans 通用服务报文转换工具

## 快速开始

- `pom.xml`

  ```xml
  <dependencies>
     	<!-- Sertrans Spring Boot Starter -->
  		<dependency>
        	<groupId>com.iwhalecloud.sertrans</groupId>
        	<artifactId>sertrans-spring-boot-starter</artifactId>
        	<version>1.0.0-SNAPSHOT</version>
    	</dependency>
    			
      <!-- 确保你的项目中有Spring Web环境 -->
      <dependency>
        	<groupId>org.springframework.boot</groupId>
        	<artifactId>spring-boot-starter-web</artifactId>
      </dependency>
  </dependencies>
  ```

- `application.yml`

  ```yaml
  # dataSource
  spring:
    datasource:
      password: my-oracle
      url: jdbc:oracle:thin:@localhost:1522:XE
      username: sys as sysdba
      driver-class-name: oracle.jdbc.OracleDriver
  
  # sertrans
  sertrans:
    datasource:
      db-type: oracle
  ```

- 数据库初始化脚本

  ```lua
  ├── deploy
      ├── script -- 数据库初始化脚本
          ├── oracle -- oracle脚本
              ├── Table.sql -- 建表脚本
              ├── Sequence.sql -- 序列脚本
  ```

  
