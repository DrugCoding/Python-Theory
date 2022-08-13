# Python Theory

- [문자열(string) ](#문자열string)

- [리스트(list) ](#리스트list)
- [딕셔너리(dictionary)](#딕셔너리dictionary)

- [반복문(while) ](반복문while)
- [반복문(for) ](반복문for)



















# 문자열(string)

> 문자열은 ``str()``로 표현한다.
>
> 문자열과 문자열은 더할 수 있다 #'He' + 'llo' = Hello
>
> 

- python 에서 문자열의 문자를 바꾸는 방법

  - 슬라이싱

  ```python
  word = 'ABCDE'
  word[start:end:step] # python 기본 문법과 동일 end는 포함하지 않는다
  print(word[1, 4, 1]) # index 1부터 4까지(즉 index 3까지) 1씩 증가하며 출력한다 # BCD
  ```

  - 문자열.replace() 함수

  ```python
  # replace 함수는 원본을 바꾸지 않는다
  word = 'ABCDE'
  word = word.replace('a', 'b') # word 에 'A'를 'B'로 바꾼다
  print(word) # BBCDE
  
  .replace('문자1', '문자2', 1) # '문자1'을 '문자2'로 제일 처음 한 번만 바꾼다
  ```


# 리스트(list)

> ㅇ
>
> 

- 리스트를 정렬하는 방법

  - 오름차순 정렬 - 리스트.sort() / sorted(리스트)

  ```python
  num = [3, 1, 5, 0, 4, 2]
  # 1번
  num.sort() 
  print(num) # [0, 1, 2, 3, 4, 5]
  # 2번
  sorted(num) 
  print(num) # [3, 1, 5, 0, 4, 2]
  # 3번
  num_ = sorted(num)
  print(num_) # [0, 1, 2, 3, 4, 5]
  
  # sort(),sorted() 차이점 : sort는 원래 리스트를 바꾼다 sorted는 원래 리스트를 보존한다
  ```

  - 내림차순 정렬(거꾸로) - 리스트.reverse() / list(reversed(리스트)) / 리스트[::-1] / 리스트.sort(reverse=True)

  ```python
  num = [3, 1, 5, 0, 4, 2]
  # 1번
  num.sort()
  num.reverse() # num = [5, 4, 3, 2, 1, 0]
  print(num) # [5, 4, 3, 2, 1, 0]
  # 2번
  num.sort()
  print(list(reversed(num))) # [5, 4, 3, 2, 1, 0]
  # 3번
  num.sort()
  print(a[::-1]) # [5, 4, 3, 2, 1, 0]
  
  # 내림차순은 리스트를 오름차순 정렬 후 뒤집어 준다
  ```


- 이중 리스트 해제 방법
  - 변수 =  sum(리스트, [])

# 딕셔너리(dictionary)

- 반복문으로 딕셔너리 만들기 - key 값 출력 - value 값 출력

  ```python
  list = ['a', 'a', 'b', 'c', 'd', 'e', 'a', 'b'] # list 값
  dict = {} # 딕셔너리를 저장 할 빈 변수
  for i in list: # list를 반복
      if i in dict: # 만약 list의 각 자리가 dict 안에 있다면
          dict[i] += 1 # dict 안에 key값 'i'(a,b,c,d,e)의 value값에 + 1  
      else: # 그게 아니라면
          dict[i] = 1 # dict 안에 key값 'i' = 1 을 입력한다
  print(dict) # {'a': 3, 'b': 2, 'c': 1, 'd': 1, 'e': 1}
  
  # key 하나를 지정해서 value 가져오기
  print(dict.get('a')) # 3
  
  # 조건을 걸어서 key 또는 value 값 출력하기 (key 또는 value 값으로 반대의 값 출력)
  for key, value in dict.items(): # dict안에 key, value 순회
      if key == 'a': # 만약 key값이 'a'라면 
          print(value) # 3
  
  # 일반코드 key, value 값 전부를 리스트에 받기 (value 는 key값에 value만 넣기)
  key_ = [] # key값을 저장할 변수
  for key, value in dict.items(): # dict을 순회해서 key, value 값을 동시에 가져온다
  	key_.append(key) # key_ 변수에 key 값 추가
  print(key_) # ['a', 'b', 'c', 'd', 'e']
  
  # 한줄코드 (value 값 key에 value 넣기)
  key_ = [key for key, value in dict.items()]
  print(key_) # ['a', 'b', 'c', 'd', 'e']
  
  # key, value 값 뒤집기 (단 중복된 value 값이 존재 할 경우 가장 뒤에 하나만 가져옴)
  dict_re = {value:key for key, value in dict.items()}
  print(dict_re) # {3: 'a', 2: 'b', 1: 'e'}
  ```

  

# 반복문(while)





# 반복문(for)

