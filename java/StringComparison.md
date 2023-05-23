# Java String 문자열 비교

## == 비교연산자

비교하는 문자열의 주소를 비교한다.<br>
Call by Refrence라고 볼 수 있다.(java에선 Call by Refrence는 존재하지 않고 Call by Value만 존재하지만, 편의를 위해 Call by Refrence라고 표현하겠다.)<br>

```java
public static void main(String[]args){
    String a="java";
    String b="java";
    String c=new String("java");
    String d="python";
    String e=a;

    System.out.println(a==b);
    System.out.println(a==c);
    System.out.println(a==d);
    System.out.println(a==e);
}
```

위 코드를 실행시키면 아래와 같은 결과가 나온다

```
true (java는 value가 같은 문자열이 있으면 선언시 그 값을 참조하므로 주소가 같다.)
false (위와 달리 c는 새로운 String객체를 생성했으므로 주소가 다르다.)
false (주소가 다르다. 물론 값도 다르다.)
true (a를 참조하고있으니 주소가 같다.)
```

## .eqauls() 메서드

비교하는 문자열의 값을 비교한다.<br>
Call by Value라고 볼 수 있다.<br>

```java
public static void main(String[]args){
    String a="java";
    String b="java";
    String c=new String("java");
    String d="python";
    String e=a;

    System.out.println(a.equals(b));
    System.out.println(a.equals(c));
    System.out.println(a.equals(d));
    System.out.println(a.equals(e));
}
```

위 코드를 실행시키면 아래와 같은 결과가 나온다

```
true (값이 같다.)
true (==의 경우와 달리 값이 같으므로 true가 나온다.)
false (물론 값도 다르다.)
true (a를 참조하고있으니 값이 같다.)
```

==가 객체의 주소를 비교한다는 사실을 모르고 곤혹을 치른적이 있다.<br>
다음에 같은 실수를 하지 않도록 정리해보았다.