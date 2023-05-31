# Mustache 한글 깨짐

발생 원인: Spring boot 2.7버전 이상에선 Mustache 한글이 깨진다고 한다.
<br>
해결법: 
1. build.gradle에서 spring boot 버전을 내려준다.

2. application.yml(properties)에 설정한다.
<br>

application.yml
```yaml
server:
  servlet:
    encoding:
      force-response: true
```
application.properties
```properties
server.servlet.encoding.force-response=true
```