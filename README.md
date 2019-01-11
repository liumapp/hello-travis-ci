# hello-travis-ci  

dd tt ff sdf
面向Java Web项目的Travis CI 教程. A tutorial of Travis CI for Java projects. 

## 1. 如何使用

### 1.1 注册Travis-CI

在GitHub的marketplace中搜索Travis CI，然后下载，并关联自己的GitHub账号

ps: Travis CI只支持在GitHub使用

![register.png](https://github.com/liumapp/hello-travis-ci/blob/master/data/pic/register.png?raw=true)

### 1.2 配置Travis-CI

老版本的Travis CI需要登陆它的官网：https://travis-ci.com 选中项目来开启，但是通过GitHub的marketplace关联后，是默认支持所有项目，所以不再需要走这一步

直接在项目中创建一个".travis.yml"文件

添加以下内容:

````yml
language: java
install: true
script: gradle build
jdk: oraclejdk8
````

在Java项目中，我们常用的依赖管理工具就是Maven和Gradle，Travis CI默认是Maven3进行编译，所以当我们的项目使用Gradle的时候，需要配置它的script去使用Gradle

ps: gradlew是Gradle在Linux环境下的可执行脚本文件

### 1.3 查看Travis-CI编译效果

走到这一步后，我们每一次提交代码，都会触发Travis CI去检验代码的事件

登陆Travis CI的官网，找到我们的hello-travis-ci项目，就能够直观的查看每一次编译结果：

![list.png](https://github.com/liumapp/hello-travis-ci/blob/master/data/pic/list.png?raw=true)

如果编译失败的话，点击进去也可以查看具体问题出现在哪儿（travis ci自己会提供编译环境）

![detail.png](https://github.com/liumapp/hello-travis-ci/blob/master/data/pic/detail.png?raw=true)













 
