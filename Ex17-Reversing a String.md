# Ex17 Reversing a String Using Stack Data Structure
## DATE:20.8.2026
## AIM:
To write a Java program that reverses an input string using a stack, without using built-in reverse functions.

## Algorithm
Start the program. Read the input string from the user. Create an empty stack of characters. Traverse the string and push each character onto the stack. Pop each character from the stack and append it to a new string — this gives the reversed string. Display the reversed string. Stop the program.   

## Program:
```
/*
Program to reverses an input string using a stack
Developed by:MERLIN M 
RegisterNumber:  212225240084
*/
import java.util.Scanner;
import java.util.Stack;

public class ReverseStringWithStack {

    public static String reverseString(String input) {
         Stack<Character> stack=new Stack<>();
        for(char ch:input.toCharArray())
        {
            stack.push(ch);
        }
        StringBuilder rev=new StringBuilder();
        while(!stack.isEmpty())
        {
            rev.append(stack.pop());
        }
        return rev.toString();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String reversed = reverseString(input);
        System.out.println(reversed);

        scanner.close();
    }
}
```

## Output:
<img width="452" height="162" alt="image" src="https://github.com/user-attachments/assets/3d3b3fb3-8a0d-46e2-8bdb-3933a7563d5d" />



## Result:
Thus, the program successfully reverses the given string using a stack without relying on built-in reverse functions.
