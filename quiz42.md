**QUIZ 042** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

42. Write a program that creates the GUI described by the UML diagram for classes below:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
from kivymd.app import MDApp
from kivy.core.window import Window
from kivymd.uix.screen import MDScreen


class MysteryScreenA(MDScreen):
    pass


class MysteryScreenB(MDScreen):
    pass


class Quiz42Screen(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        return


text = Quiz42Screen()
text.run()

```

**kivy code**


```.py

ScreenManager:
    MysteryScreenA:
        name:"MysteryA"
    MysteryScreenB:
        name:"MysteryB"




<MysteryScreenA>:
    MDCard:
        md_bg_color:"#AADD99"
        size_hint:.7,.7
        pos_hint:{"center_x":.5,"center_y":.5}
        orientation:"vertical"
        MDLabel:
            text:"welcome to mystery page A"
            size_hint:1,.1
            halign:"center"
            valign:"center"
        MDBoxLayout:
            MDLabel:
                size_hint:.2,.1
            MDRaisedButton:
                size_hint:.2,.1
                text:"go to mystery page"
                md_bg_color:"purple"
                on_release:
                    root.parent.current="MysteryB"
            MDLabel:
                size_hint:.2,.1

<MysteryScreenB>:
    MDCard:
        md_bg_color:"pink"
        style:"elevated"
        size_hint:.7,.7
        pos_hint:{"center_x":.5,"center_y":.5}

        orientation:"vertical"
        MDLabel:
            text:"welcome to mystery page B"
            size_hint:1,.01
            halign:"center"
            valign:"center"
        MDBoxLayout:
            MDLabel:
                size_hint:.2,.1
            MDRaisedButton:
                size_hint:.2,.1
                pos_hint_x:"center"
                text:"Go to page A"
                md_bg_color:"purple"
                on_release:
                    root.parent.current="MysteryA"
            MDLabel:
                size_hint:.2,.1



```
#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/quiz017.jpg)
