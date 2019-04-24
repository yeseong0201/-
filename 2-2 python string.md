# Python 문자열 관련 함수

## count()
* 문자 개수 확인하기
* 구성 요소가 몇개나 들어있는지 알려준다.

``` python
a='sunrins'
a.count('s') # 2
```

## find()
* 문자 위치를 반환해준다.
* 해당 요소가 없으면 -1을 반환한다.
* 같은 요소가 중복으로 출력되면 앞에 있는 요소의 인덱스값 반환

``` python
a='python is the best choice'
a.find('t') # 2
```

## index()
* 문자 위치 반환하기
* find와 유사함
* 해당 요소가 없을 시, error가 난다.

``` python
a='sunrins'
a='python is the best choice'
a.index('d') # error
```

## upper()
* 소문자를 대문자로 바꾸기
* 이미 대문자가 적혀있으면 그 요소를 포함한 모든 요소 대문자로 출력함.

``` python
a='hi'
a.upper() # HI
```

## lower()
* 대문자를 소문자로 바꾸기

``` python
a='HI'
a.lower() # hi
```
## replace()
* 문자열 바꾸기

``` python
a='Legends never die'
a.replace('die','sleep') # Legends never sleep
```

## split()
* 문자열 나누기
* 공백마다 문자열을 나누어 리스트로 만들어준다.

``` python
a= 'sunrin interent highschool'
a.split() # ['sunrin', 'internet', 'highschool']
```

## join()
* 문자열 삽입하기

``` python
a='abcdef'
'-'.join(a) # a-b-c-d-e-f
```
## strip(), lstrip(), rstrip()
* strip : 양쪽 공백 지우기
* lstrip : 왼쪽 공백 지우기
* rstrip : 오른쪽 공백 지우기

``` python
a='   hi    '
a.strip() # 'hi'
a.lstrip() # 'hi    '
a.rstrip() # '    hi'
```

