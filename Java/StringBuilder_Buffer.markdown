두 클래스의 기능은 동일하지만 한 가지 차이점이 존재합니다. 바로 동기화(Synchronization)에서의 차이점인데요.

StringBuilder는 동기화를 지원하지 않는 반면, StringBuffer는 동기화를 지원하여 멀티 스레드 환경에서도 안전하게 동작할 수 있습니다.

그 이유는 StringBuffer는 메서드에서 synchronized 키워드를 사용하기 때문인데요.

java에서 synchronized 키워드는 여러개의 스레드가 한 개의 자원에 접근할려고 할 때, 현재 데이터를 사용하고 있는 스레드를 제외하고 나머지 스레드들이 데이터에 접근할 수 없도록 막는 역할을 수행합니다.

예를 들어 멀티스레드 환경에서 A 스레드와 B스레드 모두 같은 StringBuffer 클래스 객체 sb의 append() 메서드를 사용하려고 하면, 다음과 같은 절차를 수행하게 된다.

A 스레드 : sb의 append() 동기화 블록에 접근 및 실행
B 스레드 : A 스레드 sb 의 append() 동기화 블록에 들어가지 못하고 block 상태가 됨.
A 스레드 : sb의 append() 동기화 블록에서 탈출
B 스레드 : block 에서 running 상태가 되며 sb 의 append() 동기화 블록에 접근 및 실행.
StringBuilder 클래스 주석에서 동기화가 필요할 경우 StringBuffer을 추천한다는 문구를 확인할 수 있다.

StringBuilder 를 사용 해야 할 때
StringBuilder는 동기화를 지원하지 않는 반면, 속도면에선 StringBuffer 보다 성능이 좋습니다.

그렇기 때문에 우리는 단일 스레드 환경 과 문자열의 추가, 수정, 삭제 등이 빈번히 발생하는 경우 StringBuilder를 사용하는 것이 성능면에서 유리할 것입니다.

5. StringBuffer 를 사용해야 할 때
StringBuffer는 동기화를 지원하여 멀티 스레드 환경에서도 안전하게 동작할 수 있습니다.

그렇기 때문에 우리는 멀티 스레드 환경 과 문자열의 추가, 수정, 삭제 등이 빈번히 발생하는 경우 StringBuffer를 사용하는 것이 성능면에서 유리할 것입니다.
