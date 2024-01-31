**QUIZ 036** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 


36. A class named Converter. The class initializes with a dictionary with key decimal numbers and values the letters of the Roman numeral system. No inputs in the initializer.




　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

*code*
```.py
class Convert:
    def __init__(self):
        self.symbols = {100: 'C', 90: 'XC', 50: 'L', 40: 'XL',
                              10: 'X', 9: 'IX', 5: 'V', 4: 'IV', 1: 'I'
                              }

    def roman_convert(self, decimal: int) -> str:
        output = ''
        if 0 < decimal < 101:
            for k, v in self.symbols.items():
                q = decimal // k
                output += q * v
                decimal = decimal % k
        else:
            output = 'invalid input'

        return output

text = Convert()
print(text.roman_convert(decimal=71))
```



#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-01-31%20at%2023.11.23.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-01%20at%2000.21.21.png)

