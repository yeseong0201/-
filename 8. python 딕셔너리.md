# Python 딕셔너리(dictionary)
* 사전과 비슷한 형식의 자료형

## 1. 딕셔너리 선언
* 딕셔너리명 ={요소1, 요소2, 요소3...} 순서가 없다.
* 딕셔너리를 만들 때는 위에서 보는 것과 같이 {} 중괄호로 감싸고 각 요소를 , 쉼표로 구분한다.
* 요소는 한 쌍의 Key: Value 형태 {Key1:Value1, Key2:Value2, Key3:Value3, ...}  
* key와 value값이 중복이 되면 안되고 수정할 수 없는 자료형으로 만들어야 함.
* key 에는 변경할 수 없는 자료형을 사용하고, value에는 모든 자료형을 사용해야 한다.
* Key를 통해 value를 얻는다.

``` python
dict = {'name' : 'leeyeseong', 'age' : 18, 'school': 'sunrin internet highschool'}
dict['name'] # leeyeseong
dict['age'] # 18
dict['school'] # sunrin internet highschool
```

### list를 key 값으로 사용하기
```python
price = {1:['a','b'],2:['c','d']}
print(price[1],price[2]) # ['a', 'b'] ['c', 'd']
```

### tuple을 key 값으로 사용한 경우

``` python
price={('떡볶이','김밥'):'3000원',('라면','만두'):'4000원'}
print(price) # {('떡볶이', '김밥'): '3000원', ('라면', '만두'): '4000원'}
```


## 2. 딕셔너리 사용 방법
* key를 통해 value를 얻음
* 어떤 key의 value를 얻기 위해서는 딕셔너리명[key]를 사용

```python
grade={'pey':10,'jullet':99}
print(grade['pey']) # 10
print(grade['jullet']) # 99
```
* key는 고유한 값이므로 중복되는 key값을 설정해 놓으면 하나를 제외한 나머지 것들이 모두 무시된다.
* 동일한 key가 존재하면 어떤 key에 해당하는 vaule를 불러야 할지 알 수 없다.
* 어떤 key값이 무시될 지 예측할 수 없다.

### 딕셔너리 요소 추가하기

```python
#mutuable 한 자료형
a={1:'a'}
a[2]='b'
a['name']='pey'
a[3]=[1,2,3,]
print(a) # {1: 'a', 2: 'b', 'name': 'pey', 3: [1, 2, 3]}
```

### 딕셔너리 요소 삭제하기

```python
a={1:'happy',2:'sad',3:'angry'}
del(a[1]
print(a) # {2: 'sad', 3: 'angry'}
```

## 3. 딕셔너리 관련 함수들
* keys: key 리스트 만들기

```python
res = {1:'apple',2:'orange', 3:'grape', 4:'melon'}
res.keys() # dice_keys([1,2,3,4])
```

* 딕셔너리의 key만 모아서 dict_keys라는 객체를 리턴함.
* 리스트를 사용하는 것과 차이가 없지만, 리스트 고유의 함수인 append,insert,pop, remove, sort등의 함수 사용불가.

### key를 리스트로 만들기
```python
list(res.keys()) # [1,2,3,4]
```

### values를 리스트로 만들기
```python
list(res.values()) # ['apple', 'orange', 'grape', 'melon']
```

### items(Key, Value)를 리스트로 만들기
```python
list(res.items()) #[(1, 'apple'), (2, 'orange'), (3, 'grape'), (4, 'melon')]
```

### clear : 요소 모두 지우기
```python
res.clear() 
print(res) # {}
```

### get : key로 value얻기
```python
res.get(1) # apple
```

### in : key가 딕셔너리 안에 있는지 조사하기
```python
print(1 in res) # True
```


