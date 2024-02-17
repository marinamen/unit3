**QUIZ 046** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

46. Use the Handout for Quiz 047, and the starting files quiz047.py quiz047.kv, payments.db: to create the application below:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py
import sqlite3
from passlib.hash import sha256_crypt
from my_lib import DatabaseWorker
hasher = sha256_crypt.using(rounds=30000)


def encrypt(user_passowrd):
    return hasher.encrypt(user_passowrd)


def check(hashed_password, user_password):
    return hasher.verify(user_password, hashed_password)


from kivymd.app import MDApp



class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect("payments.db")
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


class quiz046(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.components = {"basic": 0}

    def build(self):
        return

    def save(self):
        pass

    def update(self):
        base = self.root.ids.base.text
        hash = ""
        ids = ["inhabitant", "income_tax", "pension", "health"]
        if base != "":
            total = int(base)
            hash += f"base{total}"
            for id in ids:
                value = self.root.ids[id].text
                if value != "":
                    new_value = f"{int(value) * int(base) // 100} JPY"
                    total -= int(value) * int(base) // 100
                    hash += f"{id}{value}"
                else:
                    new_value = "JPY"
                    hash += f"text"
                self.root.ids[id + "_label"].text = new_value
            hash += f"total{total}"
            self.root.ids.salary_label.text = f"{total} JPY"
            encrypted_hash = encrypt(hash)


    def save(self):
        base = self.root.ids.base.text
        hash = ""
        ids = ["inhabitant", "income_tax", "pension", "health"]

        if base != "":
            total = int(base)
            hash += f"base{total}"
            for column in ids:
                value = self.root.ids[column].text
                if value != "":
                    new_value = f"{int(value) * int(base) // 100} JPY"
                    total -= int(value) * int(base) / 100
                    hash += f"id_of_textField{value}"
                else:
                    new_value = " JPY"
                    hash += f"id_of_textField{0}"
                self.root.ids[f"{column}_label"].text = new_value
            hash += f"total{total}"
            self.root.ids.salary_label.text = f"{total} JPY"
            encrypted_hash = encrypt(hash)
            self.root.ids.hash.text = encrypted_hash[:50]

        inhabitant = int(self.root.ids.inhabitant_label.text.split(" JPY")[0])
        income_tax = int(self.root.ids.income_tax_label.text.split(" JPY")[0])
        pension = int(self.root.ids.pension_label.text.split(" JPY")[0])
        health = int(self.root.ids.health_label.text.split(" JPY")[0])
        total = int(self.root.ids.salary_label.text.split(" JPY")[0].split('.')[0])
        hash = self.root.ids.hash.text

        query = f"INSERT into payments(base, inhabitant, income_tax, pension, health, total, hash) values('{int(base)}', '{inhabitant}', '{income_tax}', '{pension}', '{health}', '{total}', '{hash}')"
        db = database_worker("payments.db")
        db.run_save(query)
        db.close()
        self.root.ids.hash.text = f"Payment saved"

    def clear(self):
        for label in ["base", "inhabitant", "income_tax", "pension", "health"]:
            self.root.ids[label].text = ""
            self.root.ids[label + "_label"].text = " JPY"

        self.root.ids["salary_label"].text = " JPY"
        self.root.ids.hash.text = "----"


    def fraud(self):
        data = database_worker("payments.db")
        query = "SELECT * from payments"
        result = data.search(query)
        data.close()
        print(len(result))
        for column in result:
            base = column[1]
            inhabitant = column[2]
            income_tax = column[3]
            pension = column[4]
            health = column[5]
            total = column[6]
            hash = column[7]
            hash = hash[-50:]
            hash_to_check = f"base{base},inhabitant{int(inhabitant)//int(base) * 100},income_tax{int(income_tax)//int(base) * 100},pension{int(pension)//int(base)*100},health{int(health)//int(base)*100},total{int(total)//int(base)*100}"
            encrypted_hash = encrypt(hash_to_check)
            if encrypted_hash[-50:] == hash:
                print(f"payment {column[0]} ")
            else:
                print(f"fraudulent payment {column[0]} ")
m = quiz046()
create = """CREATE TABLE if not exists payments(
            id INTEGER PRIMARY KEY,
            base int,
            inhabitant int,
            income_tax int,
            pension int,
            health int
            total int,
            hash text
    )"""
m.fraud()
m.run()


create = """CREATE TABLE if not exists payments(
        id Interger PRIMARY KEY
        inhabitant INT,
        base INT,
        health INT,
        pension INT,
        hash TEXT,
        total INT
        
     )"""
my_lib= DatabaseWorker("payments.db")
my_lib.run_query(create)
my_lib.close


```

**kivy code**

quiz047.kv


#test　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/ezgif.com-video-to-gif-converter%20(1).gif)


