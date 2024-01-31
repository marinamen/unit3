**QUIZ 041** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

41. Write a program that creates the GUI below, Tic Tac Toe


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
from kivymd.app import MDApp
from kivymd.uix.button import MDFlatButton


class MyButton(MDFlatButton):
    pass


class Quiz41(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        pass

    def change_turn(self, m):
        if self.root.ids.whose_turn.text == "It's Cross's Turn":
            self.root.ids.whose_turn.text = "It's Nought's Turn "
            m.text_color = "white"
            m.text = "X"
            m.font_size = 40
            m.disabled = "True"

        else:
            self.root.ids.whose_turn.text = "It's Cross's Turn"
            m.font_size = 40
            m.text = "O"
            m.text_color = "white"
            m.disabled = "True"


text = Quiz41()
text.run()

```

**kivy code**


```.py
Screen:
    size: 500, 500
    MDBoxLayout:
        id: main_box
        md_bg_color: "#f7cbe0"
        orientation: "vertical"
        size_hint: 1, .95
        pos_hint: {"center_x": .5, "center_y": .5}

        MDLabel:
            size_hint: 1, None  # Make the height automatic
            text: "Tic Tac Toe by Marina"
            halign: "center"
            valign: "top"
            font_size: 45
            text_size: self.width, None

        MDLabel:
            id: whose_turn
            size_hint: 1, None  # Make the height automatic
            text: "It's Cross's turn"
            halign: "center"
            valign: "bottom"
            font_size: 45
            text_size: self.width, None
            md_bg_color: "#b3bef2"

    MDBoxLayout:
        id: box_one
        orientation: "horizontal"
        pos_hint: {"center_x": 0.5, "center_y": 0.3}
        size_hint: 0.6, .25
        md_bg_color: "white"
        MyButton:
        MyButton:
        MyButton:

    MDBoxLayout:
        id: box_one
        orientation: "horizontal"
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        size_hint: 0.6, .25
        md_bg_color: "white"
        MyButton:
        MyButton:
        MyButton:

    MDBoxLayout:
        id: box_one
        orientation: "horizontal"
        pos_hint: {"center_x": 0.5, "center_y": 0.75}
        size_hint: 0.6, .25
        md_bg_color: "white"
        MyButton:
        MyButton:
        MyButton:

<MyButton>:
    id: button3
    size_hint: 0.3, 1
    md_bg_color: "#DDFFBB"
    on_release: app.change_turn(self)


```
#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/Screenshot%202023-11-18%20at%2014.14.57.png)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/CS2023/blob/main/unit%202/quizzes/pictures/quiz017.jpg)
