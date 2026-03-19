
# Exp No - 2

## TITLE :  Polymorphism,Method Overloading,Method Overriding

### AIM :
To demonstrate method overloading by calculating the area of square, rectangle, and circle.

### ALGORITHM :

STEP 1 : Start

STEP 2 : Create a class with overloaded area() methods

STEP 3 : Define methods for square, rectangle, and circle

STEP 4 : Read inputs (side, length & breadth, radius)

STEP 5 : Call respective area() methods

STEP 6 : Display the results

STEP 7 : End

### PROGRAM :
```
import java.util.Scanner;

public class AreaCalculator {

    // Method to calculate area of square
    public int area(int side) {
        return side * side;
    }

    // Method to calculate area of rectangle
    public int area(int length, int breadth) {
        return length * breadth;
    }

    // Method to calculate area of circle
    public double area(double radius) {
        return Math.PI * radius * radius;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator calc = new AreaCalculator();

        // First input: Square side
        int squareSide = sc.nextInt();
        System.out.println("Area of square: " + calc.area(squareSide));

        // Second input: Rectangle length and breadth
        int rectLength = sc.nextInt();
        int rectBreadth = sc.nextInt();
        System.out.println("Area of rectangle: " + calc.area(rectLength, rectBreadth));

        // Third input: Circle radius
        double circleRadius = sc.nextDouble();
        System.out.println("Area of circle: " + calc.area(circleRadius));

        sc.close();
    }
}

```

### OUTPUT :

<img width="834" height="389" alt="image" src="https://github.com/user-attachments/assets/0fa2fa52-f7bb-4407-b6bd-b312fd3dd66c" />


### RESULT :

Thus to demonstrate method overloading by calculating the area of square, rectangle, and circle was successfully created.
