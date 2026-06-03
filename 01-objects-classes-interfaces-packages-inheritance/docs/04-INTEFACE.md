# What is an interface
Objects interact with the outside world through the methods. Methods form object's interface - 
a contract on how to interact with it. The buttons on TV set are an interface between you and the 
electrical wiring on the other side of the plastic casing. You press 'power' button, and TV
turns on and off.

In its most common form, an interface is a group of related methods with empty bodies. For example, 
if we want to describe a bicycle as an interface, it would look like this:
```java
interface Bicycle {
  void setGear(int gear);
  void setSpeed(int speed);
  void brake(int force);
  void turn(int angle);
}
```

You can now use this interface to be implemented by some another class.
```java
class MyBicycle implements Bicycle {
  int gear = 1;
  // more fields here...
  
  // You must implement all the methods, or the compilation will fail.
  void setGear(int gear) {
    this.gear = gear;
  }
  
  // more methods here...
}
```
Interfaces make the class more formal on what behavior they expose to the outside world.
If your class implements an interface, it must implement all the methods that the interface 
defines. Another note, the code above won't compile if you don't specify `public` keyword, but 
that's another story.