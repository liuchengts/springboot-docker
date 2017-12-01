# 将springboot程序做成docker镜像运行
# 前提条件：
* 有docker、java及maven环境
# 执行操作
* cd到当前项目目录 执行 mvn package docker:build
* 执行启动 docker run -p 8080:8080 -t springio/springboot-docker 
# 验证结果
* 执行 docker images 查看打包的镜像
* 执行 docker ps -a 查看当前运行中的容器
* 访问 http://localhost:8080  出现"How are you" (低版本的docker可能是192.168.99.100，即http://192.168.99.100:8080)

相关链接 https://spring.io/guides/gs/spring-boot-docker/
参考书《spring cloud与docker微服务架构实战》