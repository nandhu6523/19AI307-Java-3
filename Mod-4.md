
# Exp No - 4

## TITLE : Interface

### AIM :
To demonstrate interface implementation and polymorphism using different weather prediction bots.

### ALGORITHM :

STEP 1 : Start

STEP 2 : Define interface WeatherBot with method predict()

STEP 3 : Implement SunBot and RainBot classes

STEP 4 : Read temperature and bot type

STEP 5 : Create object based on bot type

STEP 6 : Call predict() method

STEP 7 : Display result

STEP 8 : End

### PROGRAM :
```
import java.util.Scanner;

// Common interface
interface WeatherBot {
    String predict(int temperature);
}

// SunBot implementation
class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}

// RainBot implementation
class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}

public class WeatherPrediction {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int temperature = sc.nextInt();
        int botType = sc.nextInt();
        
        WeatherBot bot;
        
        if (botType == 1) {
            bot = new SunBot();
        } else if (botType == 2) {
            bot = new RainBot();
        } else {
            System.out.println("Unknown bot type");
            sc.close();
            return;
        }
        
        System.out.println(bot.predict(temperature));
        sc.close();
    }
}

```

### OUTPUT :

<img width="329" height="159" alt="image" src="https://github.com/user-attachments/assets/bf992011-b775-4751-b6a5-9f07a4db6b5c" />

### RESULT :

Thus to demonstrate interface implementation and polymorphism using different weather prediction bots was successfully created.
