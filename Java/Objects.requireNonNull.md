### 널 체크를 위한 `<T> T Objects.requireNonNull(T obj)`
---
- 파라미터로 들어온 값이 null 이면 NPE 를 발생, 그렇지 않다면 `obj` 를 그대로 반환
- 해당 객체가 null 이면 안되는 것을 명시적으로 표현함과 동시에 디버깅에 용이함

***=> 명시적으로 null 체크를 함으로써 코드의 예측가능한 동작을 보장하기 위해 사용***
