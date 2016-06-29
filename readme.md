---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class? 

Member variables can be accessed w/o creating an instance. member variables are available to everything in/under the parent class, whereas class variables are available to the child class

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables? 

Private: it makes sense to write getters so that you can let others access the variable without being able to change its value, but there's not much point in writeing setters because they won't work

Public: it makes sense to do both

3. What are some benefits of making member variables `private`?

- so that others can't change their values


4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

Class B is the super, or parent class' which makes Class A the sub, or child class.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

it means that the child class can access the methods and/or variables of the parent class

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

  this will call an error because the method is called in main, which doesn't inherit from Refrigerator.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

In a concrete class you need to implement all of the implementations and mthods of the parent abstract class. In a child abstract class you don't. 

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

you can't implement methods in an interface because they have no scope, but you can declare methods.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

I don't think so, unless it's just semantics in that whenever you create an instance of a subclass that you also by default create an instance of the superclass. 

a final class can't be abstract because an abstract class has variables that chage with different instances; otherwise, there'd be no point to abstact classes. 

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

 when a method ovverrides another method, the overriding method essentially "replaces" the original method
 - same name: the child class will be executed.


11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

They're all collections types, but arraylists and linkedlists are types of lists. If there's a method call of a method that specifies a list input, we can call the method with arraylist or linkedlist, so using a list as the original input type allows more flexibility when calling the method.


#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
