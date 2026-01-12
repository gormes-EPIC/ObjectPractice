# Practice with Objects

## Weight on Other Planets

Write a program that will determine the user’s weight on another planet. The program should ask the user to enter their weight (on earth) via the keyboard and then present a menu of planets to choose. Then the user will select one of the planets and the program will display their weight on the planet. 

To find their new weight, multiply their Earth weight by the values in the table (or look up values for other planets)

| Planet  | Multiplier |
| ------- | ---------- |
| Mars    | 0.38       |
| Venus   | 0.90       |
| Jupiter | 2.4        |


A typical output screen will be similar to:
```
What is your weight on Earth? 150
1. Mars
2. Venus
3. Jupiter
Selection? 1
Your weight on Mars would be 
```

Remember to get input from the user we can use a `Scanner` object shown below

```
Scanner scanner = new Scanner();
String line = scanner.nextLine();
double number = scanner.nextDouble();
```

## Gas Mileage Simulation

Create a class `Automobile` with the **private instance variables**:

- `String make`: Describes the make of the car
- `String model`: Describes the model of the car
- `double mileage`: Represents the car's gas mileage in miles per gallon
- `double fuelTank`: Represents the maximum capacity of the car's fuel tank in gallons
- `double fuel`: Represents the car's current fuel level in gallons 

`Automobile` also has the following **methods**:
- `Automobile(String mk, String mdl, double m, double fT)`: This constructor should set all of the instance variables. Assume the tank is full.
- `fillUp(double gallons)`: Adds `gallons` gallons of fuel to the tank. If a user tries to overfill the tank, only fill it to its maximum capacity.
- `takeTrip(double miles)`: Removes gas from the tank as result of driving a `miles` miles.
- `reportFuel()`: Returns how much fuel is remaining in the car.

Test your `Automobile` class by creating a `TestAutomobile` class as follows:

```java
public class TestAutomobile {  
    public static void main(String[] args) {  
  
		// Creates a car with 35mpg and a max capacity of 8 gallons of gas. 
        Automobile myCar = new Automobile("Toyota", "Prius", 35, 8);  
  
		// Uses myCar to call takeTrip method. Passes argument of 100 miles driven  
	    myCar.takeTrip(100);  
	    
        // Uses myCar to call fillUp method. Passes argument of 2 gallons  
        myCar.fillUp(2);  
  
        // Uses myCar to call the reportFuel method. It returns a double of the amount of gas remaining in the tank  
        double fuelLeft = myCar.reportFuel();  
  
        // Prints the fuelLeft variable. For this example, it is equal to 7.14285714286
        System.out.println(fuelLeft);  
    }  
}
```
