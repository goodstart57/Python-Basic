02

# Jump to Python



### 04-3 파일 읽고 쓰기

```
f = open("새파일.txt", 'w')
f.close()
```

#### 'w' : 쓰기모드, 기존의 내용이 없어진다.

```
f= open("C:/Pworkspace/새파일.txt", 'w')
for i in range(1, 11):
    data = "%d번째 줄입니다.\n" %i
    f.write(data)
f.close()
```



readlines로 파일 읽는 법

```
f = open("C:/Pworkspace/새파일.txt", 'r')
lines = f.readlines()
for line in lines:
    print(line)
f.close()
```



'a' : 기존의 파일 내용 유지하면서 추가하기

```
f = open("C:/Pworkspace/새파일.txt", 'a')
for i in range(11, 20):
    data = "%d번째 줄입니다.\n" %i
    f.write(data)
f.close()
```



with : 자동으로 파일 객체가 close된다

```
with open("C:/Pworkspace/foo.txt", "w") as f:
    f.write("Life is too short, you need python")
```



