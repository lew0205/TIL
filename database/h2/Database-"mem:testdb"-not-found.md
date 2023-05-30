# Database "mem:testdb" not found
<img src="https://github.com/lew0205/TIL/assets/80537533/c6381528-f426-4f2f-a54b-09d1f99386b7">

application.yml
```yaml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
```
설정으로 해결했다.