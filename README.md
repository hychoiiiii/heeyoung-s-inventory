# 200525 월 파이썬 함수
print(10+20)
def addFun(x,y):
    print(x,y)
     return x+y
     
add Fun(10, 20)

함수 정의
defnition 함수명addFun매개변수(x,y)콜론:
들여쓰기 실행부 
들여쓰기 반환

def myFun():
  print("hello pytion")
  return
  
myFun()
myFun()
myFun()
myFun()
myFun()

def myFun(str):
  print(str)
  return
  
myFun("Hello pytion")
myFun("Hello jave")
myFun("Hello C++")
myFun("Hello world")
myFun(123)


def myFun(str1, str2):
  print(str1 + str2)
  return

myFun("Hello", "pytion")

Hello pytion 5번 호출해보시오.
def printFun(str):
  print(str)
  return
  
for i in range(5):
  printFun("Hello pytion")

매개변수: 함수의 정의부와 호출부를 맺어 연결해주는 변수. 지역변수.
i am pytion developer 출력하기
def outputFun(str1, str2, str3, str4):
  print({0}{1}{2}{3}.format(str1, str2, str3, str4))
  return
  
outputFunt('i', ' am', ' python', ' developer')

10과 20 곱해서 200 출력하기
def calFun(x, y):
  result = x * y
  return result
  
calcurator = calFun(10, 20)
print(calcurator)

지역변수, 전역변수 구분

# 10강_객체지향 프로그램-1
객체: 속성과 기능을 포함한 프로그램 단위 ex 자전거 = 색상 속성 + 무게 속성 + 기어 기능 + 브레이크 기능 + 주행 기능 
객체지향 프로그래밍 OOP: object-oriented programming 프로그램의 구성요소를 객체화하는 것
클래스: 객체를 생성하기 위한 틀 ex 자전거 생산 공정 틀. 생산=생성
클래스 이름은 일반적으로 대문자로 시작한다
속성: __int__ 메서도에 정의한다.
기능: 함수와 동일하게 정의한다. 

# 11강_객체지향 프로그램-2
접두사 언더바2개: 중요한 거라서 외부에서 접근 불가능하게 막기(private). 접미사 언더바1개 해도되고 안해도 됨
객체 생성은 __name__()메서드가 담당
초기화는 __init__()메서드가 담당
클래스 메서드(객체 생성): doubleMajor = []

# 12강_객체지향 프로그램-3
상속: 뒤에 (부모클래스)써주면 됨. 다중 부모 상속 가능
오버라이딩: 부모 클래스 기능 재정의
추상클래스: 자식 클래스에서 반듯이 구현해야 되는 기능을 가진 부모클래스. 자식클래스에서 다시 안써주면 끌어다 못씀. 에러남
super: 부모클래스. 상위로 올라가는 것임

# 모듈과 패키지
cooking.py
module
def makeJjajang(): 모듈가져오기
        print('makeJjajang')
        
def makeJjajang():
        print('makeJjamppong')
def makeJjajang():
        print('makePasta')
def makeJjajang():
        print('makePizza')   

temp.py
module

import cooking
cooking.makeJjajang()
cooking.makeJjamppong()
cooking.makePasta()
cooking.makePizza()

13_1.py
from cooking import makeJjajng (from 폴더(디렉토리=패키지) import 파일(모듈)) 필요한 
from cooking import makeJjamppong

form cooking import * (* = 모든 것을 가져오는 것)

makeJjajng()
makeJjamppong()

디렉토리를 이용해서 모듈을 관리할 수 있는데, 이때 디렉토리를 패키지라고 한다.
__int__.py 파일이 꼭 있어야 패키지화 될 수 있음.

import sys 파이썬 시스템의 모듈의 전체적 경로를 관리
for path is sys.path:
    print(path)
    
동등한 디렉토리가 아니더라도 사이트 패키지에 패키지, 모듈을 저장하면 언제든지 사용가능하다.

# 예외처리
목차: 예외란?, try~except, eles&finally, Exception 클래스, 사용자 Exception 클래스 

예외: 프로그램 소스 실행 중 발생하는 오류로 시스템적인 엔러하고는 구분된다. 소스 실행 중 발생. 예측 가능. 
에러: 시스템 문제 ex 외부전력문제. 예측 어려움. 네트웤, 하드웨어 오류 등. 대부분 물리적 오류

try~except: 예외를 처리하기 위한 가잔 간단한 방법

userData = int(input())
result = int(10 / userData)
print('result : {0}'.format(result))


try:
        userData = int(input())
        result = int(10 / userData)
except:
        print('sorry~')
        
eles: 예외가 발생하지 않으면 else문 실행
finally: 예외 발생 여부와 상관없이 항상 finally문 실행

try:
        userData = int(input())
        result = int(10 / userData)
except:
        print('sorry~')
else:
        print('예외가 발생하지 않았어요.')
finally:
        print('항상 실행 합니다')

출력

정상 실행: 
예외가 발생하지 않았어요. 
항상 실행 합니다.

예외 발생: 
sorry~ 
항상 실행 합니다.

Exception 클래스: 모든 예외는 Exception 클래스의 자식 클래스이다.

try:
        userData = int(input())
        result = int(10 / userData)
except ZeroDivisionError as e: 이제는 e로 간단하게 부르겠다.
        print('ZeroDivisionError 예외 발생 : {0}'.format(e))

0입력시 출력
0
ZeroDivisionError 예외 발생 : divisoin by zero

a입력시 출력
프로그램 멈춤

try:
        userData = int(input())
        result = int(10 / userData)
except ZeroDivisionError as e: 
        print('ZeroDivisionError 예외 발생 : {0}'.format(e))
except Exception as e: 
        print('Exceprion 예외 발생 : {0}'.format(e))

a입력시 출력
Exceprion 예외 발생 : invalid literal for int() with base 10: 'a'


try:
        userData = int(input())
        result = int(10 / userData)
except Exception as e: 순서가 바뀌어서 이게 먼저 오면 뒤에 것이 소용없게 됨. 
        print('Exceprion 예외 발생 : {0}'.format(e))except ZeroDivisionError as e: 
        print('ZeroDivisionError 예외 발생 : {0}'.format(e))

사용자 Exception 클래스: 사용자가 Exception 클래스를 상속받아 예외 클래스를 만들 수 있다.
class MyException(Exceioption): 상속받아서 사용자 클래스 만듦
    def__int__(self, e):
           super().__int__('(0)으로 나눌 수 없습니다'.format(e))
           
def division(x, y):
    if y != 0: 만족하지 못하면
        return x /y
    else:
        raise MyExceiotion(y) 얘를 던져라
        
try:
    numX = int(input())
    numY = int(input())
    result = divion(numX, numY)
    print('result : {0}'.format(result))
    
except MyException as e:
    print(예외 발생 : {0}'.format(e))
else:
    print('정상 실행')
finally:
    print('자원 해제')

# 데이터 입출력
1. 파일 읽기 & 쓰기 함수
파이썬은 파일을 읽고 쓰기 위한 함수로 opne(), write(), read(), close() 함수를 제공한다.

파이썬 바로가기 아이콘 오른쪽 마우스 클릭 > 관리자 권한으로 실행
열기: 파일 객체 = open(파일 이름,파일 열기 모드)
읽기 or 쓰기: 파일 객체. write() or 파일 객체.read()
닫기: 파일 객체.close()

f = open('파일주소/textFile.txt', 'w') 쓰기목적으로 엶 
f.write('hello pytion')
f.close()

f = open('파일주소', 'r') 읽기목적으로 엶 
print('f.read() : {0}'.format(f.read()))
f.close()

2. 파일 모드
r 읽기 전용
w 쓰기 전용(이미 존재하면 덮어씌움) 초기화 되니깐 주의
a 쓰기 전용(이미 존재하면 덧붙임)
x 이미 존재하면 예외(IOError) 발생

f = open('파일주소', 'w') 쓰기목적으로 엶 
f.write('hello pytion')
f.close()

f = open('파일주소', 'w') 쓰기목적으로 엶 
f.write('HELLO PYTHON')
f.close()

소문자에서 대문자로 덮어씌어짐 바뀜

f = open('파일주소', 'w') 쓰기목적으로 엶 
f.write('HELLO PYTHON')
f.close()

f = open('파일주소', 'a') 쓰기목적으로 엶 
f.write('hello pytion\n') 화면 밖으로 나가면 자동줄바꿈
f.close()

출력:
HELLO PYTHONhello pytion

3. 텍스트 읽기 & 쓰기
파이썬은 읽고, 쓰기 위한 편리한 함수를 제공한다.
닫을 필요가 없음 with ~ as
리스트 문자열 쓰기 f.witelines()
모든 문자열 읽기 f.readlines()
행단위로 문자열 읽기 f.readline()

with f = open('파일주소', 'r') as f:
    print('f.read() : {0}'.format(f.read()))
    
출력화면
f.read(): HELLO PYTHONhello pytion

ts = ['hello pytion', 'hello c++\n', 'hello java\n']

with open('파일주소/txtLine.txt','w') as f: 위드 사용했기 때문에 닫을 필요 없음
    for tl in ts:
        f.write(tl)

출력화면
hello pytion
ello c++
hello java

기존 파일 삭제 후
ts = ['hello pytion', 'hello c++\n', 'hello java\n']

with open('파일주소/txtLine.txt','w') as f:
    f.writelines(ts) 바로 쓰기가 가능함

출력화면
hello pytion
ello c++
hello java

with open('파일주소','r') as f:
   ls = f.readlines()
    print('type(ls) : {0}'.type(ls)))

    l = ''
    for l in ls:
        print(l, end='') 엔드는 개행문자 끝까지를 한 행으로 봄
        
출력화면
type(ls) : <class 'list'>
hello pytion
ello c++
hello java


with open('파일주소','r') as f:
   l = f.readlines()
   print('type(l) : {0}'.type(l)))

    while l != '': 더이상 문제가 없을 때 까지 반복
        print(l, end='')
        l = f.readlines()

출력화면
type(l) : <class 'str'>
hello pytion
ello c++
hello java

with open('파일주소','r') as f:
   l = f.readlines()
   print('type(l) : {0}'.type(l)))

    c = 1

    while l != '': 더이상 문제가 없을 때 까지 반복
        print(l, end='')
        l = f.readlines()
        c += 1
        
    print('c-1 : {0}'.format(c-1))

출력화면
type(l) : <class 'str'>
hello pytion
ello c++
hello java
c-1 : 3

# 네트워크
1. 네트워크 통신이란?
네트워크 통신을 하기 위해서는 통신장치(socket. 전화기라고 생각하기)가 필요하다.
pc를 연결하는거.

[통신 조건]
- 당연히 네트워크 연결 유지
- 주소 필요(IP) ex 각 전화기의 전화번호
- 통신 장치 필요(socket) ex 전화기

[통신 방식] 참고
- TCP: 송/수신 확인함 ex "친구야 놀자"라는 말이 도달했는지 확인가능
- UDP: 송/수신 확인하지 않음 ex 방송국에서 방송하듯이 너네가 들었는지 관심없다. 속도 빠름

[클라이언트-서버]
소킷(client)-패킷-패킷-패킷-리스너소킷(server)

2. 메시지 송/수신
Notepad++ 사용방법: https://toquee.blog.me/221162894277

예제: messageTranfer

[client]

import socket
서버 IP & port
ip = '192.168.0.10' --> 실행창에서 cmd 명령 프롬프트 들어가서 ipconfig 치면 ip 알 수 있음. 
prot = 9999 --> port: 항구. 서버 중에서 어떤 포트만 부분적으로 이용 가능

클라이언트 소켓 준비
client=socket.socket()

서버 접속
client.connect((ip,port))
print('----Server is connected----')

메시지 송신
client.send(b'Hello~~i\'m client') --> 역 슬레시 사용하면 작은 따옴표 삽입 가능
print('----Message send----')

메시지 수신
msg=client.recv(!024)
print('----Message received----')
print(msg)

client.close()

패킷

[server]

서버소켓준비
server = socket.socket()
server.bind(('192.168.0.10',9999))
server.listen(1) --> 1명만 접속 가능
print('server is ready----')

클라이언트 접속 수락
client, addr = server.accept() --> client 입장 허락
print('----Client is connected----')

메시지 수신
msg = clinet.recv(1024)
print('----Message received----')
print(msg)

메시지 송신
client.sendall(b'Hi Hi\'m server. your message is \" + msg + b'\")
print('----message send----')

해제
client.close()
server.close()

3. 파일 송/수신




28분




























