
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
