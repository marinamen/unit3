**QUIZ 044** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

44. Download the database brokenbank.db from the learning Log, and write the SQL statements to solve mystery of the transaction that bankrupted the bank:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

**python code**
```.py

select sum(amount) from transactions where transaction_type is "deposit" group by account_id;
select sum(amount) from transactions where transaction_type is "withdraw" group by account_id;
select balance from accounts;
select * from customers where customer_id is 12;

```

**proof of work**　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/ezgif.com-video-to-gif-converter%20(2).gif)

#uml diagram　　✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
<img src="https://github.com/marinamen/unit3/blob/main/images/Untitled.jpg" width=50% height=50%>
