# 파이썬의 list
* [] = list 기호
* 선언 방법 name = []
* list를 만들 때는 ([])로 감싸주고 안에 들어가는 원소는 쉼표를 통해 구분
* 요소(element)들은 어떠한 type도 가능함.
* 심지어 list도 element가 될 수 있음.
* Empty list : element를 하나도 갖지 않는 list
* 변수는 사용되기 전에 반드시 할당되어야 한다.

## list의 index
* list의 각 원소들은 list 변수 내에서 index를 통해 개별적으로 다루어 짐
* list 는 집합과 유사하지만, index를 통해 접근할 수 있다는 점에서 차이가 남.
* list와 string의 공통점 : 서로 index를 가진다.
* 항상 0번째 요소부터 순서가 매겨 짐.
* list의 index를 활용하여 index에 해당하는 값을 반환 가능 

## index 응용 : element에 접근하기
* index도 연산이 가능(나눗셈 연산자 제외) => 결과값은 정수가 되어야 함

``` python
num=[1,2,3,4,5,6,7,8,9]
temp =3
num[temp+1] # 5
```

## list의 membership : 'in' & 'not in'
* string에서 사용했던 방식과 같이 왼쪽의 element가 오른쪽 list에 포함되어 있는지 판단.
* in : list의 element 인가를 결정하는 연산자
* not in : list의 element가 아닌 element를 결정하는 연산자

``` python
num=[1,2,3,4,5,6,7,8,9]
3 in num # true
100 in num # false
```

## list 길이 len()
* len() 함수는 list의 element 개수를 int type으로 반환함.

``` python
num=[1,2,3,4,5,6,7,8,9]
len(num) # 9
```

* list가 다른 list를 담고 있어도, 하나의 element로 간주

``` python
num=[1,2,3,['a','b','c','d'],5,6]
len(num) # 6
len(num[3]) # 4
```

## list의 연산
* list1 + list2 : 여러개의 list를 하나의 list로 병합 (각 요소와 요소가 합쳐짐) 

``` python
list1 = [1,2,3]
list2 = [4,5,6]
list1+list2 # 1,2,3,4,5,6
```

## list slice
* list도 slice 기법을 사용하여 자를 수 있음
``` python
a=[1,2,3,4,5,6]
a[2:5] # 3 4 5
a[:] # 1~6
```
## list형 원소 변경 
* string과 달리 list는 할당문을 활용하여 element를 교체할 수 있음.

```python
a=[1,2,3,4,5,6]
a[3]= 44 # 4대신 44가 들어감
a # 1,2,3,44,5,6
```
## list의 element 대체
``` python
a=[1,2,3,4,5,6]
a[2:4]=[4,3] # 1,2,4,3,5,6
a
```
## list delete
* del : 요소 삭제하기

``` python
a=[1,2,3,4,5]
del a[2]
a
```

## list append
* append : 리스트의 맨 마지막 요소에 추가하기
``` python
a=[1,2,3,4,5,6,6,7,8,]
a.append([5,6])
print (a)
```

## list sort
* sort : 리스트 정렬하기

``` python 
a=[10,9,8,7,6,5,4,3,2,1]
a.sort() # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
a
```


## list reverse
* reverse : 리스트 순서 뒤집기

``` python 
a=['d','b','c','a','e']
a.reverse() # e a c b d
a.sort() # a b c d e
a
```

## list index
* index : 요소 위치 반환하기
``` python
#index(x) x의 위치값을 리턴
a=[1,2,3]
print(a.index(3))
print(a.index(1))
```

## list insert
* insert : 특정 인덱스에 요소 삽입하기

``` python
#insert(a,b) = list의 a번재 위치에 b를 삽입함
a=[1,2,3]
a.insert(0,4)
a
```

## list remove
* remove : 특정 요소 삭제하기

```python
# 값을 삭제하고 싶을 때 사용
a=[1,1,2,2,2,3,3,3,3,4,4]
a.remove(2)
a.remove(4)
a
```

## list pop
* pop : 특정 인덱스 요소 꺼내기
``` python
# return pop 은 맨 마지막 요소를 돌려주고 그 요소는 삭제한다.
a=[1,2,3]
b=a.pop(1)#incdex of object
print(a)
print(b)
```
## list count 
* count : 요소 개수 확인하기

```python
#count(x)는 리스트 내에 x가 몇 개나 있는지 알려줌
a=[1,2,2,2,2,3,1]
a.count(2)
```
## list extend : 리스트 확장하기 (더하기)
* extend : 리스트 확장

```python
#연결시켜줌 a+= [4,5] == a.extend([4,5])
a=[1,2,3]
b=[6,7]
a.extend([4,5])
a.extend(b)
print(a)
```

## list join
* join : 요소 마다 공백이 들어가는 부분에 사용자 설정 기호 표시해줌
```python
",".join([1,2,3,4])
```

## list copy
copy : from copy import copy

```python
from copy import copy
a=[1,2,3]
b=a.copy()
print(id(a))
print(id(b))
b
```

## 요약
* list형을 활용하면 같은 목적의 원소들을 각각의 변수로 선언하는 것보다 효율적임.
* list형은 string형의 구조와 같은 index 구조이며 index를 이용하여 원소에 쉽게 접근 가능
* 연산자를 이용하여 list형 활용 가능
* slice 연산을 이용하여 list형을 활용할 수 있다.















