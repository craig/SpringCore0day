UPDATE: Praetorian Labs claims they've verified the bug.
"Spring Core on JDK9+ is vulnerable to remote code execution due to a bypass for CVE-2010-1622."

https://twitter.com/praetorianlabs/status/1509207085485113356

https://twitter.com/praetorianlabs/status/1509207144675086343

Confirmation from GitHub security researcher:

https://twitter.com/pwntester/status/1509235919106236416


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
