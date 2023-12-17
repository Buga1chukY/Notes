# Jar Practice

    
### 1.  What is the  `String args[]`  parameter in the main method?
* The String[] args parameter in the main method is an array of strings that allows the program to accept command-line arguments.
    
### 2.  What is Jar / War / Ear?
* JAR (Java Archive), WAR (Web Archive), and EAR (Enterprise Archive) are file formats used to package and distribute Java applications.
    
### 3.  Make the program that request args, but based on the jar.

1. **Take java program that requesr args**

		public class simpleProgram {
			public static void main (String[] args) {
	    		if (args.length == 2) {
	    			int num1 = Integer.parseInt(args[0]);
	    			int num2 = Integer.parseInt(args[1]);
	    			int sum = num1 + num2;
	    			System.out.println("Sum: " + sum);	
	    		} else {
	    			System.out.println("There is no args");
	    		}
	    	}
        }


2.  **Save program**
		
	Save program with name: `simpleProgram.java`
    
4.  **Compile this program**
		
	Compile the program with the command: `javac <file name>`

5.  **Make file MANIFEST.MF**
	
	Make file with the name `MANIFEST.MF` and add next  content: 
	* `Manifest-Version: 1.0`
    * `Main-Class: simpleProgram`

6.  **Pack class and MANIFEST.MF in JAR-file**

	Pack class and MANIFEST.MF in JAR-file with the command: 
	`jar cfm SimpleProgram.jar MANIFEST.MF SimpleProgram.class`

7. **Run jar file**

	Run jar file with the command: `java -jar SimpleProgram.jar`
