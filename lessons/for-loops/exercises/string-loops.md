## Exercise

1) The following code sample takes a String as an input, and uses a while loop to check if it is a palindrome. Modify the code's logic to use a for loop instead.

```java
public static boolean isPalindrome(String input){
  input = input.toLowerCase();
  String reversed = "";
  int index = input.length() - 1;

  while(index >= 0){
     reversed += input.charAt(index);
     index--;
  }

  return reversed.equals(input);
}
```






2) The following function takes a String as a parameter, and is supposed to return the number of vowels (a, e, i, o, u) within the string. It's implementation is missing some details. Fix it.


public int countVowels(String input){
  String vowels = "aeiouAEIOU";
  int vowelCount = 0;


  return vowelCount;
}
