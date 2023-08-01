## translate()
문자열 내에서 문자를 다른 문자로 바꾸는 방법을 떠올리면 보통 replace()를 떠올릴 것이다.<br>
하지만 replace()는 하나만 치환할 수 있다는 한계점에서 아래와 같은 문제가 발생한다.<br>
우선 replace()를 이용해 문자열 '1 l0v2 y0u'를 'i love you'로 바꿔보자.<br><br>
<br>



```python
str = "1 l0v2 y0u"
str = str.replace('1', 'i').replace('0', 'o').replace('2', 'e')
```
replace()의 한계점으로 인해 replace()를 연달아 쓰며 지저분한 코드가 완성됐다.<br>
이때 활용하기 좋은 함수가 바로 translate()이다.<br>
바로 코드에 적용해보자.
<br><br>
<br>

```python
str = "1 l0v2 y0u"
a = str.maketrans('102','ioe')  # a = str.maketrans('바꿀 문자','새로운 문자')
b = "1 l0v2 y0u".translate(a)  # b = "원래 문자열".translate(a)
```
translate()를 사용할 땐 우선적으로 maketrans()를 통해 어떤 문자를 어떻게 바꾸겠다는 틀을 잡아두어야 한다.<br>
a = str.maketrans('102','ioe')는 '1'->'i', '0'->'o', '2'->'e'로 각각 바꾸겠다는 것이다. <em>(maketrans 함수 속 두 인자의 길이는 똑같아야 한다!)</em><br>
b = "1 l0v2 y0u".translate(a)는 원래 문자열인 "1 l0v2 y0u"에 최종적으로 translate()를 적용해 문자를 바꾼 것이다.<br><br>
