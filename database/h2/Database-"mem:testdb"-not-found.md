# Database "mem:testdb" not found
![스크린샷 2023-05-31 오전 8.43.20.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F9v%2F3vlx4v6n4jg_zn5gf3pf44vw0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_l23kMp%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-05-31%20%EC%98%A4%EC%A0%84%208.43.20.png)

application.yml
```yaml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
```
설정으로 해결했다.