# StringTokenizer

StringTokenizer을 사용하기 위해 java.util 패키지의 StringTokenizer 클래스를 `import`로 가져와야 한다.   

```java
import java.util.StringTokenizer;
```

## 생성자

**StringTokenizer(String s)**  
- 디폴트 구획문자로 공백문자(\t, \n, \r, \f)를 가진다.  

**StringTokenizer(String s, String delim)**  
- 구획문자(delimiter)를 인자로 받는 생성자.   
- 구획문자는 2자리 이상도 설정할 수 있다.   
- 구획문자를 $%라고 설정하면 $, %를 기준으로 끊어주고, %%라고 설정하면 %를 기준으로 끊어준다.
- 즉, 구획문자는 길이가1로 고정이고 길이가 2이상인 구획문자를 받으면 구획문자가 여러개가 된다.  

**StringTokenizer(String s, String delim, boolean returnDelims)**  

- 구획문자(delimiter)를 인자로 받는 생성자.  
- returnDelims가 true이면 구획문자도 토큰으로 간주한다.   
- 각 구획문자는 길이가 1인 String이 된다.   
- returnDeilms가 false면 구획문자를 token으로 사용하지 않는다.   

## 메서드

메서드|설명
|:---:|:--:
|int countTokens()| 남아있는 토큰의 개수를 반환. 전체 토큰의 개수가 아닌 현재 남아있는 토큰의 개수.
|String nextToken(), Object nextElement()| 토큰을 하나씩 반환. 두 메서드는 같은 객체를 반환하지만 반환형은 다르다. nextElement는 Object를, nextToken은 String을 반환.
|boolean hasMoreTokens(), hasMoreElements()| 남아 있는 토큰이 있는지 여부를 반환. 다음 토큰이 있으면 true, 없으면 false를 리턴.
