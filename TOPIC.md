# Data Encapsulation
## What exactily is data encapsulation?
As defined in Wikipedia, Data Encapsulation is
>Data encapsulation, also known as data hiding, is the mechanism whereby the implementation details of a class are kept hidden from the user.

To make it short and sweet, Data Encapsulation is hiding your classes from the user. 


# Access Modifers
An important part of Data Encapsulation are Access Modifers. Access Modifers are used to determine whenever a class can use a particular field or a method. In Java there are 4 kinds of access modifers

+ Private - Can only be accessed within it's own class
+ Public - Anyone Can Access it
+ Protected - Cannot be accessed outside package without a child class
+ Default (no modifer) - Can be accessed by anything in the package

[You can learn more about Access Modifers here](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)
  
# Using Get and Set
The get method (getDate) returns the value of the varible date while the set method (setDate) takes the paramter (newName) and assigns it the date variable. The "this" keyword is used to refer to current object. 

Date.Java
```Java
public class Date {
  private String date;

  // Get Method
  public String getDate() {
    return date;
  }

  // Set Method
  public void setDate(String newDate) {
    this.date = newDate;
  }
}
```
#### Error Example
What happens when we try to access the date variable? Take the below code "BadClass" for example.

#### BadClass.Java
```Java
public class BadClass {
  public static void main(String[] args) {
    Date myObj = new Date();
    myObj.date = "Tuesday";
    System.out.println(myObj.date);
  }
}
```
#### BadClass Output
```
MyClass.java:4: error: name has private access in Date
    myObj.date = "Tuesday";
         ^
MyClass.java:5: error: name has private access in Person
    System.out.println(myObj.date);
                  ^
2 errors

```
This will not work because of the private field access, we will need to use the setter method we created earlier (setDate). The code below shows the correct usage without running into any errors.

#### GoodClass.Java
```Java
public class GoodClass {
  public static void main(String[] args) {
    Date myObj = new Date();
    myObj.setDate("Monday");
    System.out.println(myObj.getDate());
  }
}
```
#### GoodClass Output
```
Monday
```

Because we used .setDate, we were able to set the name of the date variable. 

# Benefits of Encapsulation

+ Allows code to be more flexible
+ Added layer of security
+ Makes code easier to maintain
+ Reduces human errors

