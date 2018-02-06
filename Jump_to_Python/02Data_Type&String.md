#### 02

# Jump to Python

### 02-1 숫자형

#### 정수형(Integer)

```
a = 123
a = 0
```

#### 실수형(Floating-point)

```
a = 1.2
a = -3.45
```

#### 8진수(Octal)

```
a = Oo0177
```

8진수를 만들기 위해서 0o or 0O(숫자0 + 알파벳 소문자 o or 대문자 O)로 시작

#### 16진수(Hexadecimal)

```
a = 0x8ff
a = 0xABC
```

16진수를 만들기 위해서 0x로 시작하면 된다.

#### 복소수

```
a = 1+2j
b = 3-4J
b.real
b.imag
abs(b)
```

```
3.0
-4.0
5
```

abs(복소수) : 복소수의 절대값을 리턴



#### 사칙연산

x^y

```
x**y
```

나머지 반환

```
7%3
```

```
1
```

나눗셈 후 소숫점 아랫자리를 버리는 연산

```
7//4
```

```
1
```





### 02-2 문자열 자료형

#### 문자열 만드는 방법

```
"Hello World"
'Hello World'
"""Hello World"""
'''Hello World'''
```

따옴표 안에 다른 따옴표를 넣을때 사용

```
"Python's favorite food is perl."
'Python\'s favorite food is perl.'
```



#### 여러줄인 문자열 대입

```
"Life is too short\nYou need python"
'''
	Life is too short
	You need python
	'''
```



### 문자열 연산하기

#### 문자열끼리 더하기

```
head = "Python"
tail = " is fun"
head + tail
```

```
'Python is fun'
```



#### 문자열끼리 곱하기

```
a = "python"
a * 2
```

```
'pythonpython'
```



#### 문자열 인덱싱

```
a = "Life is too short, You need Python"
a[3]
a[-1]
```

```
'e'
'n'
```



#### 문자열 슬라이싱

| Code   | Output                               |
| ------ | ------------------------------------ |
| a[0:4] | 'Life'                               |
| a[:]   | 'Life is too short, You need Python' |
| a[:8]  | 'Life is '                           |
| a[8:]  | 'too short, You need Python'         |



#### 문자열 포매팅

```
>>> "I eat %d apples." %3
'I eat 3 apples.'

>>> "I eat %s apples." % "five"
'I eat five apples.'

>>> number = 3.5
>>> "I eat %f apples." %number
'I eat 3.5 apples.'

>>> day = "three"
>>> "I ate %d apples. so I was sick for %s days." %(number, day)
"I ate 3 apples. so I was sick for three days."

>>> "Error is %d%%." % 98
'Error is 98%.'
```



#### 포맷 코드

| 코드   | 설명                         |
| ---- | -------------------------- |
| %s   | 문자열(다른 변수타입을 대입해도 문자열로 변환) |
| %c   | 문자 1개                      |
| %d   | 정수                         |
| %f   | 부동 소수                      |
| %o   | 8진수                        |
| %x   | 16진수                       |
| %%   | Literal %(%문자 자체)          |



####포맷 코드와 숫자 함께 사용하기

1. 정렬과 공백

```
>>> "%10s" % "hi"
'        hi'
```

10칸짜리 문자열에서 오른쪽 정렬

```
>>> "%-10sJane" % 'hi'
'hi        Jane'
```

10칸짜리 문자열에서 왼쪽 정렬



2. 소수점 표현하기

```
>>> "%0.4f" % 3.42134234
'3.4213'
```

소수점 4째 자리까지 표현

```
>>> "%10.4f" % 987654321.42134234
'    3.4213'
```

소수점 4째 자리까지 표현하고 10칸짜리 문자열에서 오른쪽 정렬



### 문자열 관련 함수들

문자 개수 세기(count)

```
>>> a = "hobby"
>>> a.count('b')
2
```



위치 알려주기1(find)

```
>>> a = "Python is best choice"
>>> a.find('b')
10
>>> a.find('k')
-1 
```

문자열에서 제일 처음 나오는 b의 위치를 찾아준다.

-1이 반환되면 존재하지 않는 문자이다.



위치 알려주기2(join)

```
>>> a = ","
>>> a.join('abcd')
'a,b,c,d'
```

문자열 사이에 변수 a값인 ","를 넣어준다.



소문자를 대문자로 바꾸기(upper)

대문자를 소문자로 바꾸기(lower)

```
>>> a = "hi"
>>> a.upper()
'HI'

>>> a = "HI"
>>> a.lower()
'hi'
```



왼쪽 공백 지우기(lstrip)

오른쪽 공백 지우기(rstrip)

양쪽 공백 지우기(strip)

```
>>> a = " hi "
>>> a.lstrip()
'hi '

>>> a.rstrip()
' hi'

>>> a.strip()
'hi'
```



문자열 바꾸기: replace(바뀌게될 문자열, 바꿀 문자열)

```
>>> a = "Life is too long"
>>> a.replace("Life", "Your leg")
'Your leg is too long'
```



문자열 나누기 : split(기준 문자열)

```
>>> a = "Life is too short"
>>> a.split()
['Life', 'is', 'too', 'short']

>>> a = "a:b:c:d"
>>> a.split(":")
['a', 'b', 'c', 'd']
```



format 함수를 이용한 고급 문자열 포매팅

```
>>> number = 10
>>> day = "three"
>>> "I ate {0} apples. so I was sick for {1} days.".format(number, day)
'I ate 10 apples. so I was sick for three days.'
```



이름으로 넣기

```
>>> "I ate {0} apples. so I was sick for {day} days.".format(10, day=3)
'I ate 10 apples. so I was sick for 3 days.'
```



소수점 표현하기

```
>>> y = 3.42134234
>>> "{0:0.4f}.format(y)"
'3.4213'
```



### 02-3 리스트 자료형

```
리스트명 = [요소1, 요소2, 요소3, ...]
```



리스트 인덱싱

```
>>> a = [1,2,3, ['a','b','c']]
>>> a[0]
1

>>> a[-1]
['a','b','c']

>>> a[-1][0]
'a'
```



리스트 슬라이싱

```
>>> a = [1,2,3,4,5]
>>> b = a[:2];b
[1, 2]
>>> c = a[2:];c
[3,4,5]
```



#### 리스트 연산자

리스트 더하기(+)

```
>>> a = [1,2,3]
>>> b = [4,5,6]
>>> a + b
[1,2,3,4,5,6]
```



리스트 반복하기(*)

```
>>> a = [1,2,3]
>>> a*3
[1,2,3,1,2,3,1,2,3]
```



#### 리스트 수정, 변경 그리고 삭제

리스트에서 연속된 범위의 값 수정

```
>>> a = [1, 2, 3]
>>> a[1] = ['a', 'b', 'c']; a
[1, ['a', 'b', 'c'], 3]

>>> a = [1, 2, 3]
>>> a[1:2] = ['a', 'b', 'c'];a
[1, 'a', 'b', 'c', 3]
```

a[1:2]에 대입하는것과 a[1]에 대입하는건 다르다.



[] 사용해 리스트 요소 삭제하기

```
a[1:3] = []
a
[1, 'c', 4]
```



del 함수를 이용해 리스트 요소 삭제하기

```
>>> del a[1]
>>> a
[1, 4]
```



리스트 요소 추가 : append

```
>>> a = [1, 2, 3]
>>> a.ppend(4)
>>> a
[1,2,3,4]

>>> a.append([5,6])
>>> a
[1,2,3,4,[5,6]]
```



리스트 정렬 : sort, reverse

```
>>> a = [1,4,3,2]
>>> a.sort(); a
[1, 2, 3, 4]

>>> a = ['a','c','b']
>>> a.reverse(); a
['b', 'c', 'a']
```



위치 반환 : index

```
>>> a = [1,2,3]
>>> a.index(3)
2
```



리스트에 요소 삽입 : insert(위치, 요소)

```
>>> a = [1,2,3]
>>> a.insert(0,4)
[4,1,2,3]
```



리스트 요소 제거 : remove

```
>>> a = [1,2,3,1,2,3]
>>> a.remove(3)
[1,2,1,2,3]
```
