
**QUIZ 050** 

✦　　　.　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 

50. Create a class for a flight:


　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦
**python code**

```.py
class flight():
    def __init__(self, flight_number, origin, destination, departure_time, duration):
        self.flight = flight_number
        self.origin = origin
        self.destination = destination
        self.duration = duration
        self.departure_time = departure_time


    def get_duration(self, duration,destination):
        hours = duration[0]
        minutes = duration[1]
        seconds = duration[2]
        return f"{hours} hours {minutes} minutes {seconds} seconds remaining for {destination}"

m = flight(flight_number = "CA908", origin = "Madrid", destination = "Beijing International Airport", departure_time = "11.30 AM",duration = [10, 57, 12])
r= flight(flight_number = "IB64", origin = "Madrid", destination = "Bilbao Aireportuak", departure_time = "8.30 AM",duration = [1, 40, 35])

print(m.get_duration(duration = r.duration,destination=r.destination))

print(r.get_duration(duration = m.duration,destination=m.destination))
```
**proof of work**　　. 　 ˚　.　　　　　 . ✦　　　 　˚　　　　 . ★⋆. ࿐࿔ 
　　　.   　　˚　　 　　*　　 　　✦　　　.　　.　　　✦　˚ 　　　　 ˚　.˚　　　　✦

![](https://github.com/marinamen/unit3/blob/main/images/Screenshot%202024-02-19%20at%2008.38.22.png)
