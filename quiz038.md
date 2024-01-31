**QUIZ 038** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

 38. Create a program that creates the SalemanMap using your OOP code




　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

*code*
```.py
import matplotlib.pyplot as plt
import random
class Saleman_Map:
    def __init__(self):
        self.x = []
        self.y = []
        self.name = []

    def generate_data(self, name):
        self.name = name
        for i in range(len(name)):
            self.x.append(random.randint(0, 100))
            self.y.append(random.randint(0, 100))

    def generate_map(self):
        plt.scatter(self.x, self.y)
        for i, city in enumerate(self.name):
            plt.text(self.x[i], self.y[i], city, fontsize=8)

        plt.title('Japan Map')
        plt.xlabel('Distance (Km)')
        plt.ylabel('Distance (Km)')
        plt.show()

text=Saleman_Map()
text.generate_data(['Tokyo', 'Osaka', 'Kyoto', 'Nagoya', 'Yokohama', 'Hiroshima', 'Sapporo', 'Kobe', 'Kyoto', 'Osaka', 'Tokyo'])
print(text.generate_map())
```

#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/quiz017.jpg)

