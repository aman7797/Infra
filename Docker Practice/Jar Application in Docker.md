# JAR Application in Docker
Let start by creating JAR file

## Creatin JAR File
1. Create a java file, I have created project.java or you can refer the below given code.

    ```java
    public class project {
    public static void main(String[] args){
        System.out.println("Trying JAR in Docker - Aman Lalpuria");
    }
    }
    ```
2. Save and compile it in the command line. From the directory in which you have created your project.java, run the command 
    ```java 
    javac project.java.
    ```
3. create a simple `manifest.txt` to make it packed right
4. Now to create the JAR file type the following code in the terminal
    ```java
    jar cfm project.jar manifest.txt project.class
    ```
