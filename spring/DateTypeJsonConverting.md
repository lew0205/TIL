# DateType Json Converting

<br>

> 개발을 하다보면 자주 사용하게 되는 LocalDateTime, LocalDate 타입은 요청을 받거나 응답을 할 때, 직렬화를 해주어야한다.<br>
> Spring에서는 이 직렬화를 지원해주는데, 이에 대해 알아보겠다.

직렬화를 지원해주는 어노테이션은 @DateTimeFormat과 @JsonFormat이 있다.

## 1. @DateTimeFormat

 - Spring에서 지원하는 Annotation이다.
 - LocalDate / LocalDateTime 과 같은 날짜 관련 타입의 직렬화를 지원한다.

<br>

- GET 요청 시 RequestBody, RequestParam에서 사용한다.
- POST 요청시 RequestBody에서 사용한다.