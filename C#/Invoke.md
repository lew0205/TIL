# Invoke

### 기본 형태
Invoke("호출할 함수", 초);<br>
설정한 시간 후 함수를 호출한다

### 반복 호출
InvokeRepeating("호출할 함수", 초1, 초2);<br>
초1 시간 후 함수를 호출하고 초2 시간마다 함수를 호출한다.

### 멈춤
CancleInvoke("호출할 함수");<br>
매개변수에 있는 함수의 Invoke를 멈추고 매개변수에 아무것도 없으면 모든 Invoke를 멈춘다.
 
### 상태 확인
IsInvoking("호출할 함수");<br>
매개변수에 있는 함수의 Invoke가 실행중인지 확인하고 아무것도 없으면 모든 함수의 Invoke를 확인한다.

### 주의점
#### 멈추지 않는다?<br>
Invoke는 게임 오브젝트가 비활성화되어도 멈추지 않는다.<br>
그러므로 게임 오브젝트를 파괴하거나 CancleInvoke를 해주어야한다.
#### Invoke보단 Coroutine!
Invoke의 기능은 Coroutine에서도 구현이 가능하다.<br>
Invoke처럼 함수를 문자열으로 찾는건 C#의 리플렉션이라는 기능을 사용하는데,<br>
직접 호출하는것보다 수천배나 느리니 최적화를 위해선 Coroutine 사용이 권장된다고 한다.<br>
