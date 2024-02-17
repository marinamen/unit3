**QUIZ 048** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

48. Use the database bitcoin_exchange.db: and create a program that calculates the total amount of bitcoins transferred for only those transactions that are valid:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
import sqlite3
from passlib.hash import sha256_crypt
hasher = sha256_crypt.using(rounds=3000)


def encrypt(user_passowrd):
    return hasher.encrypt(user_passowrd)


def check(hashed_password, user_password):
    return hasher.verify(user_password, hashed_password)


class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


m = database_worker("bitcoin_exchange.db")
query = "SELECT * from ledger"
result = m.search(query)

m.close()
bitcoin_amount=0
for row in result:
    id= row[0]
    sender_id=row[1]
    receiver_id=row[2]
    amount=row[3]
    hash=row[4]
    string_hash=f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"
    equal=check(hashed_password = hash, user_password = string_hash)
    if equal is False:
        print(f"{id} Error signature")
    else:
        print(f"{id} Signature correct")
        bitcoin_amount+=amount
print(f"total amount of bt is {bitcoin_amount} BTC")


```
#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-17%20at%2014.20.57.png)

