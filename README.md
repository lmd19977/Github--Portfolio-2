# Github--Portfolio-2
  Outline: 
Carly’s Catering provides meals for parties and special events 

1). Event.java 

-contains two public final static fields
One holds the price per guest ($35)
The other holds the cutoff value for a large event (50 guests)

Three private fields that hold 
a). an event number 
b). number of guests for the event
c). the price

-two public set methods
-three public get methods
-two overloaded constructors
a). One constructor accepts an event number and number of guests as parameters. It passes these values to the setEventNumber() and setGuests() methods, respectively. The setGuests() method will automatically calculate the event price. 
b). The other constructor is a default constructor that passes “A000” and 0 to the two-parameter constructor


 2). EventDemo.java 
Demonstrates using two Event objects (it instantiates two Event objects).

 -includes new methods in the class 
• Instantiates one object to retain the constructor default values. 
• Accepts user data for the event number and guests fields, and uses this data set to instantiate the second object. 

Displays all the details for both objects





Program: 

1). Class: Event.java 

Three private fields: Variables for the event number, the amount of guests, and the price of the event.
```
package eventdemo;
public class Event {
   private String EventNumber;
   private int GuestNumber;
   private int EventPrice;
```

Two public final static fields that hold: the price per guest ($35), and the cutoff value for a large event (50 guests). These are variables for the maximum price and the cutoff number of guests.
```
   public final static int price=35;
   public final static int cutoff=50;
   ```

This is a default constructor that passes “A000” and 0 to the two-parameter constructor. 
   ```Event()
   {
       EventNumber= "A000";
       GuestNumber= 0;
   };
   ```
   
   This constructor accepts an event number and number of guests as parameters.
   ```
   public void EventGuest(String a, int b)
   {
   EventNumber=a;
   GuestNumber=b;
   };
 ```

  Two public set methods 


This method sets the event number.
 ```  
   public void setEventNumber(String a)
   {
    EventNumber=a;
   };
   ```
   
   The setGuests() method automatically calculate the event price.
   ```
   public void setGuests()
   {
   EventPrice=price*GuestNumber;
   };
   ```
   
   This prompts the user to enter a number less than 50 guests.
   ```
   public void cutoff()
   {
   if(GuestNumber>cutoff)
   {
       System.out.println("The cutoff value is 50, please enter a number less than 50");
        System.exit(0);
   }
   };
   ```
   
   This displays the event number.
   ```
   public void getEventNumber()
   {
       System.out.println("The event number is: " + EventNumber);
   };
   ```
   
   This displays the amount of guests attending.
   ```
   public void getGuestNumber()
   {
       System.out.println("The amount of guest attending: " + GuestNumber);
   };
   ```
   
This displays the event price.
   
   ```
   public void getPriceNumber()
   {
       System.out.println("The event price is: " + EventPrice);

   };  
}
```

2). EventDemo.java 


package eventdemo;
import java.util.Scanner; 


This class contains the main function. It accesses the event class and the functions within it. 
  ```
public class EventDemo {

    public static void main(String[] args) {
   Event event1 = new Event();
   event1.cutoff();
   event1.getEventNumber();
   event1.getGuestNumber();
   event1.setGuests();
   event1.getPriceNumber();
   System.out.println (" ");
   Event event2 = new Event();
   event2.EventGuest("A001",49);
   event2.cutoff();
   event2.getEventNumber();
   event2.getGuestNumber();
   event2.setGuests();
   event2.getPriceNumber();
    } 
   ```
    
