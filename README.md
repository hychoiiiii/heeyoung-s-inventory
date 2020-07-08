# heeyoung-s-inventory
# hi

# 200525 월 파이썬 함수
print(10+20)
def addFun(x,y):
    print(x,y)
     return x+y
     
add Fun(10, 20)

# 함수 정의
# defnition 함수명addFun매개변수(x,y)콜론:
# 들여쓰기 실행부 
# 들여쓰기 반환

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

# Hello pytion 5번 호출해보시오.
def printFun(str):
  print(str)
  return
  
for i in range(5):
  printFun("Hello pytion")

# 매개변수: 함수의 정의부와 호출부를 맺어 연결해주는 변수. 지역변수.
# i am pytion developer 출력하기
def outputFun(str1, str2, str3, str4):
  print({0}{1}{2}{3}.format(str1, str2, str3, str4))
  return
  
outputFunt('i', ' am', ' python', ' developer')

# 10과 20 곱해서 200 출력하기
def calFun(x, y):
  result = x * y
  return result
  
calcurator = calFun(10, 20)
print(calcurator)

# 지역변수, 전역변수 구분

# 10강_객체지향 프로그램-1
# 객체: 속성과 기능을 포함한 프로그램 단위 ex 자전거 = 색상 속성 + 무게 속성 + 기어 기능 + 브레이크 기능 + 주행 기능 
# 객체지향 프로그래밍 OOP: object-oriented programming 프로그램의 구성요소를 객체화하는 것
# 클래스: 객체를 생성하기 위한 틀 ex 자전거 생산 공정 틀. 생산=생성
# 클래스 이름은 일반적으로 대문자로 시작한다
# 속성: __int__ 메서도에 정의한다.
# 기능: 함수와 동일하게 정의한다. 

# 11강_객체지향 프로그램-2
# 접두사 언더바2개: 중요한 거라서 외부에서 접근 불가능하게 막기(private). 접미사 언더바1개 해도되고 안해도 됨
# 객체 생성은 __name__()메서드가 담당
# 초기화는 __init__()메서드가 담당
# 클래스 메서드(객체 생성): doubleMajor = []

# 12강_객체지향 프로그램-3
# 상속: 뒤에 (부모클래스)써주면 됨. 다중 부모 상속 가능
# 오버라이딩: 부모 클래스 기능 재정의
# 추상클래스: 자식 클래스에서 반듯이 구현해야 되는 기능을 가진 부모클래스. 자식클래스에서 다시 안써주면 끌어다 못씀. 에러남
# super: 부모클래스. 상위로 올라가는 것임

# 모듈과 패키지
cooking.py
module
def makeJjajang():
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
from cooking import makeJjajng
from cooking import makeJjamppong

form cooking import * = 모든 것을 가져오는 것

makeJjajng()
makeJjamppong()
