# StringBuilder / StringBuffer

>Java에서 String 객체는 한번 값이 할당되면 그 공간은 변하지 않지만, Stringbuilder나 StringBuffer 객체는 한번 값이 할당되더라도 다른 값이 할당되면 할당된 공간이 변하는 특성을 갖고 있다.

## 두 클래스의 공통점과 차이점
공통점 - 가변(mutable)  
차이점 - 동기화(Synchronization)  

StringBuilder - 동기화를 지원하지 않는다.  
StringBuffer - 동기화를 지원. 멀티 스레드 환경에서도 안전하게 동작할 수 있다.   

-> StringBuffer는 메서드에서 `synchronized` 키워드를 사용한다.  
`synchronized`는 여러개의 스레드가 한 개의 자원에 접근할려고 할 때, 현재 데이터를 사용하고 있는 스레드를 제외하고 나머지 스레드들이 데이터에 접근할 수 없도록 막는 역할을 한다.


## StringBuilder를 사용 해야 할 때

StringBuilder는 동기화를 지원하지 않지만 속도는 StringBuffer보다 좋다.  

-> 단일 스레드 환경과 문자열의 추가, 수정, 삭제 등이 자주 발생하는 경우, StringBuilder를 사용하는 것이 유리하다.  
-> 스레드가 안전한 프로그램 개발시 사용.  	

## StringBuffer를 사용해야 할 때

StringBuffer는 동기화를 지원하여 멀티 스레드 환경에서도 안전하게 동작할 수 있다.  

-> 멀티 스레드 환경과 문자열의 추가, 수정, 삭제 등이 자주 발생하는 경우, StringBuffer를 사용하는 것이 유리하다.  
-> 연산이 많을 경우 유리.  

# Method

|메서드|설명
|:--:|:--:
|append()|인수로 전달된 값을 문자열로 변환한 후, 해당 문자열의 마지막에 추가. String 클래스의 concat() 메서드와 같은 결과를 반환하지만, 처리 속도가 훨씬 빠르다.
|capacity()|StringBuffer 인스턴스의 현재 버퍼 크기를 반환. 만약 길이가 4인 문자열이라면, 기본적으로 생성되는 여유 버퍼 크기 16에 문자의 길이인 4를 더한 총 20개의 문자를 저장할 수 있는 버퍼가 생성된다.
|delete(index1,index2)|전달된 인덱스에 해당하는 부분 문자열을 해당 문자열에서 제거. index1부터 index2 바로 앞의 문자까지를 삭제. deleteCharAt() 메소드를 사용하면 특정 위치의 문자 한 개만을 제거할 수 있다.
|insert()|인수로 전달된 값을 문자열로 변환한 후, 해당 문자열의 지정된 인덱스 위치에 추가. 이때 전달된 인덱스가 해당 문자열의 길이와 같으면, append() 메서드와 같은 결과를 반환.


[StringBuffer 클래스의 API 문서](https://docs.oracle.com/javase/7/docs/api/java/lang/StringBuffer.html){:target="_blank"}
