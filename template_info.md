# 源码自动生成模板 spring-boot

### 概述

* 模板: spring-boot
* 模板使用时间: 2019-08-09 15:37:55

### Docker
* Image: registry.cn-beijing.aliyuncs.com/code-template/spring-boot
* Tag: 20190731
* SHA256: b2d9b97c2b1a6f9b7571d9aad3aab64ce069a8b6a4b226bda0e84bc80c948aca

### 用户输入参数
* repoUrl: "git@code.aliyun.com:myzhy/123123.git" 
* needDockerfile: "Y" 
* appName: "application" 
* from: "newPipeline" 
* codeRepo: "code.aliyun.com/myzhy/123123" 
* operator: "aliyun_845503" 

### 上下文参数
* appName: application
* operator: aliyun_845503
* gitUrl: git@code.aliyun.com:myzhy/123123.git
* branch: master


### 命令行
	sudo docker run --rm -v `pwd`:/workspace -e repoUrl="git@code.aliyun.com:myzhy/123123.git" -e needDockerfile="Y" -e appName="application" -e from="newPipeline" -e codeRepo="code.aliyun.com/myzhy/123123" -e operator="aliyun_845503"  registry.cn-beijing.aliyuncs.com/code-template/spring-boot:20190731

