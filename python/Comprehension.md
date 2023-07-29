## 컴프리헨션 (Comprehension)
컴프리헨션은 파이썬의 자료구조(list, dictionary, set)에 데이터를 더욱 간결하게 담기 위한 문법이다.<br>
반복문과 조건문을 결합해 '하나의 구문'으로 만들어 넣는 것을 의미한다.<br>
실제로 코딩을 하며 가장 자주 사용하는 리스트 컴프리헨션으로 간단히 예시를 정리한다.<br><br>
<br>



```python
lst = []
for i in range(1, 11) :
    if i%2 == 0 :
        lst.append(i)
```
위 코드를 컴프리헨션 문법으로 한 줄에 담아보자.<br>
<br>

```python
lst = [i for i in range(1,11) if i%2 == 0]
# 1~10 중 짝수로만 이루어진 리스트 lst
```
for문 뒤에 if문을 붙여 간단히 한 줄로 만들었다. <em>(단, 같은 변수명을 사용해야 한다!)</em><br>
여기에 if문을 또 이어 붙이는 것도 가능하다.<br><br>

```python
lst = [i for i in range(1,10) if i%2 == 0 if i<8]
# 1~10 중 8 미만의 짝수로만 이루어진 리스트 lst
```
