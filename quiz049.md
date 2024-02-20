**QUIZ 049** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

49.

　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py

from my_lib import DatabaseWorker
m = DatabaseWorker("bitcoin_exchange.db")

create = """ CREATE TABLE IF NOT EXISTS users(
    id integer PRIMARY KEY
    name text NOT NULL
    email text NOT NULL)"""

insert = """ INSERT INTO users (id, name, email) VALUES (920,'bob','bob@gmail.com'),
(560, 'bob1', 'bob1@xyz.com'), 
(488,'bob2', 'bob2@xyz.com'), 
(254, 'bob3','bob3@yzc.com'), 

""";
select = """SELECT * from users"""
query = """SELECT * from ledger where receiver_id = 920"""
m.run_query(query)
m.search(query, True)
print(x.search(query, True))

```

#proof of work　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-17%20at%2014.37.58.png)

