
# Exp No - 5

## TITLE : Inner Class,Wrapper Class ,enums,enum Constructor,enum Strings

### AIM :
To check whether a given number is an Armstrong number.

### ALGORITHM :
STEP 1 : Start

STEP 2 : Read integer num

STEP 3 : Convert number to string and find number of digits

STEP 4 : Initialize sum = 0

STEP 5 : For each digit:
         Extract digit
         Add (digit ^ number of digits) to sum

STEP 6 : If sum == num → print Armstrong number

STEP 7 : Else → print not an Armstrong number

STEP 8 : End

### PROGRAM :
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        
        String numStr = Integer.toString(num);
        int digits = numStr.length();
        int sum = 0;
        
        for (int i = 0; i < digits; i++) {
            int digit = Character.getNumericValue(numStr.charAt(i));
            sum += Math.pow(digit, digits);
        }
        
        if (sum == num) {
            System.out.println(num + " is an Armstrong number.");
        } else {
            System.out.println(num + " is not an Armstrong number.");
        }
    }
}

```

### OUTPUT :

<img width="770" height="245" alt="image" src="https://github.com/user-attachments/assets/d4237deb-1d6d-4725-ab65-1b439c62e0d7" />

### RESULT :

Thus to check whether a given number is an Armstrong number was successfully created.
