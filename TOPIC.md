# Data Encapsulation
## What exactily is data encapsulation?
As defined in Wikipedia, Data Encapsulation is
>Data encapsulation, also known as data hiding, is the mechanism whereby the implementation details of a class are kept hidden from the user.

So in short, Data Encapsulation is hiding your classes from the user. 


# Access Modifers
An important part of Data Encapsulation are Access Modifers. Access Modifers are used to determine whenever a class can use a particular field or a method. In Java there are 4 kinds of access modifers

+Private - Can only be accessed within it's own class
+Public - Anyone Can Access it
+Protected - Cannot be accessed outside package without a child class
+Default (no modifer) - Can be accessed by anything in the package

[You can learn more about Access Modifers here](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)
  
# Using Get and Set
The get method (getDate) returns the value of the varible date while the set method (setDate) takes the paramter (newName) and assigns it the date variable. The "this" keyword is used to refer to current object. 


# Our Date.Java Function
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
  

### While Loop Example
```C
#include <stdio.h>
 
int main () {

   // Declaring variable 
   int x = 0;

   // While loop that increments value of our variable
   while( x <= 5 ) 
   {
      printf("The value of our variable is %d ! \n", x);
      x++;
   }
 
   return 0;
}
```
### When executed, the output should look like this! 
---

```
The value of x is 0 !
The value of x is 1 !
The value of x is 2 !                       
The value of x is 3 !                      
The value of x is 4 !                                                    
The value of x is 5 ! 
```

# For Loop
A for loop is is simlar to a while loop. While both loops are use to repeat a section of code, a for loop will run a certain number of times unlike the while loop, which will run until the condition is no longer true. The syntax for a For Loop goes as followed:
```C
for (init; condition; increment)
{
    //code
}
    
```    
### For Loop Example
```c
#include <stdio.h>
 
int main () {

   // Declaring Variable
   int x; 
	
   // For loop that increments variable by one until it reaches 10, also prints value of variable	
   for( x = 0; x <= 5; x++ )
   {
      printf("The value of x is %d ! \n", x);
   }
 
   return 0;
}
```
### When executed, the output should look like this! 
---
```
The value of x is 0 !
The value of x is 1 !
The value of x is 2 !                       
The value of x is 3 !                      
The value of x is 4 !                                                    
The value of x is 5 ! 
```
# Do While Loop
A do while loop is a bit different from both a while loop and a for loop. One of the main differences being is that the do while will execute the code at least once. Afterwards it will then test the condition, if it's true it'll execute the loop again until the condition becomes false. The syntax for a Do Loop goes as followed:
```c
do 
{
//code
} while( condition );
```

### Do While Loop Example 
```c
int main () {

   // Declaring Variable
   int x = 0;

   // do loop, prints value of variable while also increments variable until it is equal to 5
   do {
      printf("the value of x is %d !\n", x);
      x++;
   }while( x <= 5 );
 
   return 0;
}
```
### When executed, the output should look like this!
---
```
The value of x is 0 !
The value of x is 1 !
The value of x is 2 !                       
The value of x is 3 !                      
The value of x is 4 !                                                    
The value of x is 5 ! 
```