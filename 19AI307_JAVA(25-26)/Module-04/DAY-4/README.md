# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

<img width="1266" height="230" alt="Screenshot 2025-11-25 143748" src="https://github.com/user-attachments/assets/de4cc280-43b2-465d-974d-fee5ea9003fd" />


## AIM:

To implement the Abstract Factory Design Pattern for creating UI components (Button and Checkbox) for two different themes: Dark and Light.

## ALGORITHM :

1.Start

2.Create two product interfaces:

Button (with a paint() method)

Checkbox (with a paint() method)

3.Create an abstract factory interface UIFactory with methods:

createButton()

createCheckbox()

4.Implement two concrete factories:

DarkFactory → returns DarkButton and DarkCheckbox

LightFactory → returns LightButton and LightCheckbox

5.Create concrete product classes:

DarkButton, DarkCheckbox

LightButton, LightCheckbox

6.In the main program:

Read user input for theme (e.g., "dark", "light")

If input is "dark", instantiate DarkFactory

If input is "light", instantiate LightFactory

7.Using the selected factory:

Call createButton() and display its type

Call createCheckbox() and display its type

8.End



## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Manisha selvakumari.S.S.
RegisterNumber:  212223220055
*/

import java.util.*;
interface Button {
    void display();
}

interface Checkbox {
    void display();
}
class DarkButton implements Button {
    public void display() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void display() {
        System.out.println("Dark Checkbox created");
    }
}
class LightButton implements Button {
    public void display() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void display() {
        System.out.println("Light Checkbox created");
    }
}
interface UIComponentFactory {
    Button createButton();
    Checkbox createCheckbox();
}
class DarkThemeFactory implements UIComponentFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIComponentFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim();

        UIComponentFactory factory;

        if (theme.equalsIgnoreCase("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equalsIgnoreCase("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            return;
        }

        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();

        button.display();
        checkbox.display();
    }
}



```



## OUTPUT:

<img width="1014" height="290" alt="Screenshot 2025-11-25 144217" src="https://github.com/user-attachments/assets/b1ac2b73-6850-43ae-8029-3ec6679a1983" />



## RESULT:

The program successfully executed to implement the Abstract Factory Design Pattern for creating UI components 
