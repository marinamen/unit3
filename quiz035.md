**QUIZ 023** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

 
35. Write the function mystery and pass the tests contained in the file test_quiz_33.py 




　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

*code*
```.py
def mystery(list1: list, list2: list) -> list:
    output = []
    for el1 in list1:
        for el2 in list2:
            if el1 == el2:
                output.append(el1)
                break

    return output
```



#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)


        output = ""
        if 0 < decimal < 400:
            for key, value in self.roman_symbols.items():
                q = decimal // key
                output += value * q
                decimal %= key
        return output
