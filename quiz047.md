**QUIZ 047** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

47. Use the database bitcoin_exchange.db: and create a program that check the hash signature stored for every transaction and prints:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
import sqlite3
from my_lib import DatabaseWorker
from passlib.hash import sha256_crypt

hasher = sha256_crypt.using(rounds=30000)

def checkPass(hashedSign, userSign):
    return hasher.verify(userSign, hashedSign)

m = DatabaseWorker("bitcoin_exchange.db")
query = """SELECT * from ledger"""
text = m.search_query(query,multiple=True)
m.close()

for r in text:
    id, sender_id, receiver_id, amount, signature = r[0], r[1], r[2], r[3], r[4]
    hashString=f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"
    true=checkPass(hashedSign = signature, userSign = hashString)
    if true is True:
        print(f"Tx {id}, Signature Matches")
    else:
        print(f"Tx {id}, Error Signature")


```

#proof of work　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-17%20at%2014.37.58.png)

