# Execution failed for task ':test'.

> 테스트 메서드를 실행하던 중 이런 에러가 발생헀다.

#### 원인: 테스트 메서드 명이 한글일 경우 이렇게 에러가 난다고한다.
#### 해결법: Prefrences - Build, Execution, Deployment - Build Tools - Gradle 에서 Run tests using 을 Gradle 에서 IntelliJ IDEA로 변경해주면 된다.