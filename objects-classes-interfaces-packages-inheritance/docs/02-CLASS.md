# What is a class
In the applications you may find thousands of objects of the same kind. For example, you may have 
a lot of bicycles, all the same kind. Each bicycle is built from the same set of blueprints 
and therefore contains the same components. In object-oriented terms, a single bicycle is an 
instance of the class of objects knows as bicycles. A class is a blueprint from which individual 
objects are created.

The following Bicycle class is one possible implementation of a bicycle:
```java
class Bicycle {
  int cadence = 0;
  int speed = 0;
  int gear = 1;
  
  void setCadence(int cadence) {
    this.cadence = cadence;
  }
  
  void setSpeed(int speed) {
    this.speed = speed;
  }
  
  void setGear(int gear) {
    this.gear = gear;
  }
}
```

This is not an application, but just a blueprint for creating bicycles. 
```java
class BicycleDemo {
  public static void main(String[] args) {
    Bicycle bike1 = new Bicycle();
    Bicycle bike2 = new Bicycle();
  }
}
```