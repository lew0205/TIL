# 코딩
```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class HelloWorld : MonoBehaviour
{
    void Start()
    {
        Debug.Log("Hello World!!!");
    }

    void Update() 
    {

    }
}
```
### using문
---
```cs
using UnityEngine;
```
UnityEngine 네임스페이스에서 정의된 형(변수, 메서드) 등을 사용한다는 의미이다.

### Class
---
```cs
public class HelloWorld : MonoBehaviour
{
}
```
MonoBehaviour의 상속을 받는 HelloWorld.cs의 메인 클래스.<br>
스크립트 이름과 클래스 이름은 같아야 한다.

### Start 문
---
```cs
    void Start()
    {
        Debug.Log("Hello World!!!");
    }
```
Update의 첫 프레임이다.

### 입출력
---
```cs
Debug.Log("Hello World!!!");
```
Hello World!!!를 출력한다.

### Update 문
---
```cs
    void Update() 
    {

    }
```
매 프레임마다 실행되는 명령이다.

# 변수
### 데이터 형식
---
데이터가 어떤 종류의 데이터인지 정의해 주는 것. ex) 숫자 문자 기호
* 값 형식<br>
  해당 데이터가 직접 포함된다.<br>
  데이터의 사본이 들어있기 때문에 값이 바뀌어도 영향을 별로 미치지 않는다(ref, out 매개변수는 예외).
* 참조 형식<br>
  데이터에 대한 참조가 저장된다.<br>
  두 가지 이상의 변수가 같은 객체를 참조할 때에는 한 변수의 작업이 다른 변수에 영향을 미칠 수 있다.

### 메모리 영역
---
* 스택(Stack)
  값 형식 데이터가 저장된다.<br>
  차례대로 데이터를 저장하였다가, 사용이 끝나면 데이터를 모두 제거한다.
* 힙(Heap)
  참조 형식 데이터가 저장된다.<br>
  Garbage Collector를 사용하여 데이터를 제거한다.<br>
  Garbage Collector는 개발자가 별도로 신경을 쓰지 않아도 된다는 편안함을 제공하지만, 가끔 실행 시 프로그램이 느려지는 문제점이 있다.

  ### C# 데이터 형식
  ---
  |종류||내용|||
  |---|---|---|---|---|
  |값 형식|단순 형식|부호 있는 정수|sbyte|-128,127|
  ||||short|-32768, 32767|
  ||||int|-2147483648, 2147483647|
  ||||long|9223372036854770000|
  |||부호 없는 정수|byte|0,255|
  ||||unhort|0,65535|
  ||||uint|0, 4294967295|
  ||||ulong|18446744073709500000|
  |||유니코드 문자|char|'a','b'
  |||IEEE 이진 부동 소수점|float|0, 12, 3.45|
  ||||double|0, 12, 3.45|
  |||고정밀 10진수 부동 소수점|decimal|0, 12, 3.45|
  |||부울|bool|true, false|
  ||열거형 형식||enum E {...} 양식의 사용자 정의 형식||