# String Method 


|메서드|설명
|:---:|:---:
|char charAt(int index)	|해당 문자열의 특정 인덱스에 해당하는 문자를 반환
|int compareTo(String str)	|해당 문자열을 인수로 전달된 문자열과 사전 편찬 순으로 비교
|int compareToIgnoreCase(String str)	|해당 문자열을 인수로 전달된 문자열과 대소문자를 구분하지 않고 사전 편찬 순으로 비교
|String concat(String str)	|해당 문자열의 뒤에 인수로 전달된 문자열을 추가한 새로운 문자열을 반환
|int indexOf(int ch)int indexOf(String str)	|해당 문자열에서 특정 문자나 문자열이 처음으로 등장하는 위치의 인덱스를 반환
|int indexOf(int ch, int fromIndex)int indexOf(String str, int fromIndex)	|해당 문자열에서 특정 문자나 문자열이 전달된 인덱스 이후에 처음으로 등장하는 위치의 인덱스를 반환
|int lastIndexOf(int ch)	|해당 문자열에서 특정 문자가 마지막으로 등장하는 위치의 인덱스를 반환
|int lastIndexOf(int ch, int fromIndex)	|해당 문자열에서 특정 문자가 전달된 인덱스 이후에 마지막으로 등장하는 위치의 인덱스를 반환
|String[] split(String regex)	|해당 문자열을 전달된 정규 표현식(regular expression)에 따라 나눠서 반환
|String substring(int beginIndex)	|해당 문자열의 전달된 인덱스부터 끝까지를 새로운 문자열로 반환
|String substring(int begin, int end)	|해당 문자열을 전달된 정규 표현식(regular expression)에 따라 나눠서 반환
|String toLowerCase()	|해당 문자열의 모든 문자를 소문자로 변환
|String toUpperCase()	|해당 문자열의 모든 문자를 대문자로 변환
|String trim()	|해당 문자열의 맨 앞과 맨 뒤에 포함된 모든 공백 문자를 제거
|length()	|해당 문자열의 길이를 반환
|isEmpty()	|해당 문자열의 길이가 0이면 true를 반환하고, 아니면 false를 반환
|equals() |해당 문자열 끼리 동일한 값인지 비교
