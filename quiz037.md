**QUIZ 037** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

 
37.




　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

*code*
```.py
class CompoundInterest:
    def __init__(self, principal, rate, years):
         self.principal = principal
         self.rate = rate
         self.years = years
    def calculate(self):
         return self.principal * ( 1 +self.rate/12) ** (self.years*12)

class Accounting(CompoundInterest):

     def __init__(self,customer_name,customer_email,principal,rate,years):
         self.cname=customer_name
         self.cemail=customer_email
         super(Accounting,self).__init__(principal,rate,years)
     def print_message(self):
         return f"Hello {self.cname},after {self.years} years you will have {self.calculate():.2f} if you have a compound interest of {self.rate}."


marina=Accounting("Marina","marina@example.com",100,0.1,10)
print(marina.print_message())

```


#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/quiz017.jpg)
