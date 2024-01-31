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
<img src="https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-01-31%20at%2023.15.41.png" width=90% height=90%>

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-01%20at%2000.16.07.png)
