**QUIZ 040** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

40. Write a program that creates the GUI below:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
from kivymd.app import MDApp


class Quiz40(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
    def build(self):
        return
    def dark_mode(self):
        self.root.ids.main_screen.md_bg_color = "black"
        self.root.ids.label.color = "white"
        self.root.ids.change.color = "white"


text = Quiz40()
text.run()
```

**kivy code**


```.py
Screen:
    size:500,500
    MDBoxLayout:
        id:main_screen
        md_bg_color:"white"
        orientation: "vertical"
        size_hint: 1,0.95
        pos_hint: {"center_x":0.5,"center_y":0.5}

        MDLabel:
            id:label
            text:"Your Name"
            valign:"center"
            halign:"center"
            color:"black"
            font_size:60
            size_hint:1,0.3

        MDRaisedButton:
            id:change
            text:"Dark Mode"
            size_hint: 0.15,0.05
            pos_hint_x:0.1
            color:"blue"
            on_release:
                app.dark_mode()


```
#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/quiz017.jpg)
