springboot程序打jar包与运行：

1、springboot程序打包，在pom.xml文件加入如下springboot 的maven插件
<plugin>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-maven-plugin</artifactId>
    <!--打jar包，使用该版本，其它版本目前测试有问题-->
    <version>1.4.2.RELEASE</version>
</plugin>

2、在项目中使用Maven install 在本地maven仓库安装成一个jar

3、使用java -jar 运行第2步生成的jar包，从而可以启动spring boot 程序

4、访问第3步运行起来的spring boot 程序

当访问jsp页面时弹出下载页面，解决办法：

1、先看pom.xml中是否有对jsp的解析包，要确保有对jsp的解析包

2、在第一步确定的情况下，还不能解决问题，可以给项目访问路径加上项目工程名


springboot 部署及打包小结：
 
springboot程序启动运行方式：

1、在idea中直接运行springboot程序的main方法(开发阶段)

2、用maven将springboot安装为一个jar包，使用java命令运行:java -jar springboot-xxx.jar
   可以将该命令封装到一个linux的一个shell脚本中(上线部署) 
   
3、使用springboot 的maven插件将springboot程序打成war包，单独部署在tomcat中运行(上线部署)   