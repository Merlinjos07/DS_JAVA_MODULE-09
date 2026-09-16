# Ex19 Palindrome Check Using Deque
## DATE:20.8.2026
## AIM:
To design a program that checks whether a given message is a palindrome by removing all non-alphanumeric characters, converting all characters to lowercase, and using a deque data structure for comparison.

## Algorithm

Start the program. Read an input string from the user. Remove all non-alphanumeric characters from the string. Convert all characters to lowercase for uniform comparison. Create a deque (double-ended queue). Insert each character of the cleaned string into the deque. While the deque has more than one element: Remove one character from the front and one from the rear. Compare both characters. If they are not equal, the string is not a palindrome. If all pairs match, the string is a palindrome. Display the result.
## Program:
```
/*
Program to checks whether a given message is a palindrome by removing all non-alphanumeric characters.
Developed by: MERLIN M
RegisterNumber:  212225240084
*/
import java.util.*;

public class PalindromeChecker {
    
    public static boolean isPalindrome(String message) {
        // Convert to lowercase and remove non-alphanumeric characters
        message = message.toLowerCase().replaceAll("[^a-z0-9]", "");
        
        Deque<Character> deque = new ArrayDeque<>();
        
        // Add all characters to the deque
        for (char c : message.toCharArray()) {
            deque.addLast(c);
        }
        
        // Compare characters from both ends
        while (deque.size() > 1) {
            if (deque.pollFirst() != deque.pollLast()) {
                return false;  // Mismatch found
            }
        }
        
        return true;  // All characters matched
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        //System.out.println("Enter a message:");
        String input = scanner.nextLine();

        if (isPalindrome(input)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a palindrome");
        }

        scanner.close();
    }
}
```

## Output:

<img width="470" height="157" alt="image" src="https://github.com/user-attachments/assets/87c34402-7ed5-4a9a-a737-68e95034d4e6" />


## Result:
The program successfully removes all non-alphanumeric characters, converts the text to lowercase, and uses a deque to efficiently compare characters from both ends. Hence, it determines whether the string is a palindrome.
