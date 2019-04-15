# python string
* string형은 따옴표인 quote를 이용하여 나타낸다.
* 파이썬에서는 string형을 나타낼 때 4가지 형식의 Qutoe가 모두 허용된다.

## string 형에서의 quote

기호 | 설명 
:-----: | :-----: 
 'a' | string 내에 ""를 포함해야 하는 경우 
 "a" | string 내에 ''를 포함해야 하는 경우 
 '''a''' | 여러 문장을 사용하고, string 내에 ""를 포함해야 하는 경우 
 """a""" | 여러 문장을 사용하고, string 내에 ''를 포함해야 하는 경우 
 
 ## 문자열 병합(string Concatenation)
 
 * '+'연산자를 두 문자(열) 사이에 사용하여 둘을 합칠 수 있다.
  
 ``` python
 a = '==='
 b = 'python'
 c = '==='
 print(a+b+c) # ===python===
 ```
 
 ## 문자열 반복(string iteration)
 
 * '*'연산자를 사용해서 같은 문자열을 반복적으로 출력 할 수 있다.
 ``` python
 start = '='*10
 title = 'python program'
 finish = '='*10
 print(start+title+finish) #출력 결과 : ==========Python Program========== 
 ```

 
 ## string의 길이 보여주기 함수 : len()
 
 * python 에서는 공백도 문자로 취급한다.
 * 길이 측정 시 공백 또한 문자열의 길이에 속함.
 
 ex) a = 'I am a boy' len(a) 는 10이 출력됨 
 
 ## string의 indexing
 * string의 index는 string 내의 문자들에 대해 순번을 부여하는 것과 같음.
 * string 변수명[index_num] 일때
 
 index_num에 해당하는 문자를 반환 (index는 항상 0부터 시작함) 
 
 단, index_num으로 음수를 입력하면 string의 끝부터 문자 반환
 
 ## string은 immutable
 * string은 한 번 지정하면 더 이상 바꿀 수 없음
 * 할당문(=)을 지원하지 않음
 * index를 이용한 변경을 허용하지 않음. 즉 index를 이용한 할당은 에러가 됨.
 
 str='hello' str[1]='a' => 불가
 
 ## string의 slice
 
 * slice를 활용하면 string의 일부를 취할 수 있다.
 
 ```python
 str='hello python'
 print(str[6:10]) # pyth가 출력됨
 ```
 
 * slice의 범위를 지정하는 n과 m은 string의 index범위 내의 양의 정수로 정해져야 함.
 * 지정하지 않은 slice 범위에 대해서는 기본값이 적용된다.
 * string의 처음과 끝에 해당하는 index로 자동 지정됨.
 
 기호 | 설명
 :----: | :----:
 [:n] | 처음부터 n을 포함하지 않는 범위까지 slice
 [m:] | m부터 끝까지 slice
 [m:문자열보다 큰 값] | m부터 끝까지 출력
 
 
 
 
 
 
 
 
 
 
 
 
 
