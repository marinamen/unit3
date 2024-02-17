**QUIZ 045** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

45. A company requires a program that calculates the average word length from a database of words. Complete the following code:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
**python code**

```.py
import sqlite3

haiku = ("""Code flows like a stream
         Algorithms guide its way
         In silence, it solves""")

connection = sqlite3.connect("quiz45.db")
cursor = connection.cursor()

query = f"""Create Table if not exists Words(
id INTEGER PRIMARY KEY,
word_text NOT NULL,
word_length int 
)
"""
cursor.execute(query)
connection.commit()

for word in haiku.split():
    querytwo=f"""
    INSERT into Words(word_text,word_length) VALUES('{word}',{len(word)});
    """
    cursor.execute(querytwo)
    connection.commit()

querythree=""" SELECT avg(word_length) FROM Words
;"""
cursor.execute(querythree)

print(f"The average word length {cursor.fetchone()}")

connection.close()
```
**proof of work**　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-16%20at%2016.38.54.png)
