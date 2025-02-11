### **잘못된 Random 사용 사례**

- `Random.nextInt()` 대신, **범위를 지정할 수 있는 `Random.nextInt(int bound)`를 사용하라.**
    - `Random.nextInt()`는 모든 `int` 값 중에서 무작위로 선택하므로, 일반적인 용도(특정 범위의 난수 생성)에 적합하지 않다.
- 자바 7부터는 `ThreadLocalRandom`을 사용하는 것이 성능 면에서 유리하다.
    - 멀티스레드 환경에서 **`Random`은 동기화 이슈로 인해 병목**이 발생할 수 있다.
    - `ThreadLocalRandom`은 각 스레드에 독립된 난수 생성기를 제공해 성능이 더 뛰어나다.

---

### **직접 구현 대신 라이브러리를 써야 하는 이유**

- 대부분의 경우, **라이브러리가 이미 제공하는 기능을 직접 구현할 필요가 없다.**
    - 시간과 비용을 절약할 수 있다.
- **문제가 발생했을 때** 라이브러리 커뮤니티나 문서를 통해 도움을 받을 수 있다.
- **자바 메이저 릴리스마다 추가된 표준 라이브러리를 확인하라.**
    - 예를 들어, 자바 8에 도입된 `Stream` API, 자바 11의 `HttpClient` 등.

---

### **왜 직접 구현할까?**

1. **라이브러리 존재를 몰라서**
    - 많은 개발자가 기존 라이브러리 대신 직접 구현하는 이유는 **라이브러리를 찾지 않아서**이다.
    - 그러니까 자바 메이저 릴리스마다 새롭게 추가된 기능을 확인하라.
2. **직접 구현한 코드의 문제점**
    - 라이브러리를 직접 구현하면 더 많은 시간이 소요될 뿐만 아니라, 라이브러리 수준의 성능과 안정성을 보장할 수 없다.

---

### **결론**

1. **전문가가 설계한 표준 라이브러리를 활용하라.**
    - 이를 통해 규모의 경제를 누리고, 애플리케이션 개발에 집중할 수 있다.
2. **표준 라이브러리를 사용하면 유지보수성이 좋아지고, 코드의 품질이 향상된다.**
3. **직접 구현하지 말고 항상 기존 라이브러리를 먼저 찾아라.**
    - 자바 메이저 릴리스마다 추가된 새로운 라이브러리를 확인하라.