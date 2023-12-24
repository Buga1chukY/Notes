# Jar Practice. Multiple Class Files

### 1. Class  `Main`  receives 2 arguments from CLI.
```java
public class Main {
	public static void main(String[] args) {
		Calculator calculator = new Calculator();

		int num1 = Integer.parseInt(args[0]);
		int num2 = Integer.parseInt(args[1]);
		int sum = calculator.sum(num1,num2);

		System.out.println("First num:" + num1);
		System.out.println("Second num:" + num2);
		System.out.println("The sum:" + sum);
	}
}
```
### 2. Class  `Calculator`  has method  `sum`. Receives 2 integers args and return sum.
```java
public class Calculator {
	public static int sum(int num1, int num2) {
		int sum = num1 + num2;

		return sum;
	}
}
```
### 3. In scope of the main method:

- Call the  `sum`  function. 
- Pass 2 input arguments and get the result.
- Run the `Main` method with the command `java <file name> <first arg> <second arg>`

### 4. Print 2 input CLI arguments and the result of `sum` method execution.
Output:
```
First num: 5
Second num: 10
The sum: 15
```
### 5. Create a jar file.
- Make file with the name `MANIFEST.MF` and add next content:
```
Manifest-Version: 1.0
Main-Class: <name of main-class>(without .java)
```
- Pack classes and `MANIFEST.MF` in JAR-file with the command `jar cfm Main.jar MANIFEST.MF Main.class Culculator.class`

-  Run jar file with the command `java -jar Main.jar <first arg> <second arg>`

