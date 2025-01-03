### 객체 널 체크: `Objects.isNull()` vs `==`
---
- 완전히 똑같은 기능을 수행
- `Objects.isNull()` 이 따로 메서드로 존재하는 이유는 Predicate 인터페이스로 사용하기 위함

***=> 단순 널 체커로는 `==` 을 사용하는 것이 타당***

<br>

### `Optional` 의 `orElse()` vs `orElseGet()`
---
```java
public T orElse(T other) {
    return value != null ? value : other;
}

public T orElseGet(Supplier<? extends T> other) {
    return value != null ? value : other.get();
}
```
- 두 메서드 모두 `value` 가 `null` 일 경우 `other` 를 return 하는 패턴
- 하지만 메서드를 인자로 가지게 될 경우 `orElse()` 는 value 의 null 여부와 상관없이 other 를 실행

***=> 이미 있는 기본 개체나 단순히 null 을 반환할 경우에는 `orElse()` 를 사용해도 상관없지만, 그 외에는 `orElseGet()` 을 사용하는 것이 맞음***
  
