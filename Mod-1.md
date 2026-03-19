
# Exp No - 1

## TITLE : Packages,Inheritance and Aggregation

### AIM : 
To demonstrate inheritance and method overriding using Employee, Manager, and Developer classes.

### ALGORITHM :

STEP 1 : Start

STEP 2 : Define base class Employee with id, name, salary

STEP 3 : Create subclasses Manager and Developer extending Employee

STEP 4 : Add extra fields (department / language)

STEP 5 : Override display() method in subclasses

STEP 6 : Read input details

STEP 7 : Check type (Manager/Developer)

STEP 8 : Create corresponding object and display details

STEP 9 : End

### PROGRAM :
```
import java.util.*;

public class Main {
    static class Employee {
        int id;
        String name;
        double salary;
        Employee(int id, String name, double salary) {
            this.id = id;
            this.name = name;
            this.salary = salary;
        }
        void display() {
            System.out.println("ID: " + id);
            System.out.println("Name: " + name);
            System.out.println("Salary: " + salary);
        }
    }

    static class Manager extends Employee {
        String department;
        Manager(int id, String name, double salary, String dept) {
            super(id, name, salary);
            this.department = dept;
        }
        void display() {
            super.display();
            System.out.println("Department: " + department);
        }
    }

    static class Developer extends Employee {
        String language;
        Developer(int id, String name, double salary, String lang) {
            super(id, name, salary);
            this.language = lang;
        }
        void display() {
            super.display();
            System.out.println("Programming Language: " + language);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Only one input for now, since your test shows just one Manager
        String type = sc.nextLine().trim();
        int id = Integer.parseInt(sc.nextLine().trim());
        String name = sc.nextLine().trim();
        double salary = Double.parseDouble(sc.nextLine().trim());
        String extra = sc.nextLine().trim();

        if(type.equalsIgnoreCase("Manager"))
            new Manager(id, name, salary, extra).display();
        else
            new Developer(id, name, salary, extra).display();

        sc.close();
    }
}

```

### OUTPUT :

<img width="814" height="533" alt="image" src="https://github.com/user-attachments/assets/78ec6f90-259e-481f-85d3-61a0f146ecfb" />

### RESULT :

Thus to demonstrate inheritance and method overriding using Employee, Manager, and Developer classes was successfully created.
