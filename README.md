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

  - .replace() 함수

  ```python
  # replace 함수는 원본을 바꾸지 않는다
  word = 'ABCDE'
  word = word.replace('a', 'b') # word 에 'A'를 'B'로 바꾼다
  print(word) # BBCDE
  
  .replace('문자1', '문자2', 1) # '문자1'을 '문자2'로 제일 처음 한 번만 바꾼다
  ```


# 리스트(list)





# 딕셔너리(dictionary)



# 반복문(while)





# 반복문(for)

