**QUIZ 039** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

39. Write a program that creates the GUI below


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
from kivymd.app import MDApp


class MyQuizzApp39(MDApp):
    def build(self):
        return
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0
    def add_counter(self):
        self.count += 1
        self.root.ids.label_counter.text = f"count {self.count}"
        if self.count == 20:

            self.count=0
    def reduce_counter(self):
        self.count -= 1
        self.root.ids.label_counter.text = f"count {self.count}"



text = MyQuizzApp39()
text.run()
```

**kivy code**


```.py
Screen:
    size:500,500
    md_bg_color:"white"
    MDBoxLayout:
        id:box_main
        orientation: "horizontal"
        size_hint: 0.7,0.3
        pos_hint: {"center_x":0.5,"center_y":0.5}


        MDLabel:
            id:label_counter
            halign:"center"
            valign:"center"
            text:"Count 0"
            font_size:34
            size_hint:0.3,1
            md_bg_color:"pink"



        MDRaisedButton:
            id:add_button
            text: "Add +1"
            pos_hint: {"center_x":0.5}
            size_hint:0.3,1
            font_size: 34
            on_release:
                app.add_counter()

        MDRaisedButton:
            id:reduce_button
            text:"Reduce -1"
            pos_hint: {"center_x":0.5}
            size_hint:0.3,1
            font_size: 34
            on_release:
                app.reduce_counter()

        MDRaisedButton:


```
#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/39-ezgif.com-video-to-gif-converter.gif)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-01%20at%2000.41.35.png)
