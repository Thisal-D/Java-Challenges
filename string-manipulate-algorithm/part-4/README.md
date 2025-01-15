## Java String Manipulation Program

**This program demonstrates two key string manipulation tasks:**

- Checking if a character already exists in a string.
- Removing duplicate characters from a string.

---

## Methods to Implement:

### 1. **Check if a Character Exists in a String**
- **Signature:**  
  ```java
  public static bool isExists(String value, char find)
  ```

  - **Description:**  
    This method checks whether the specified character (`find`) exists in the input string (`value`).It returns `true` if the character is found and `false` otherwise.

### 2. **Remove Duplicate characters in a String**
- **Signature:**  
  ```java
  public static String removeDuplicates(String value)
  ```

  - **Description:**  
    This method removes all duplicate characters from the input string and retains only the first occurrence of each character.
I   nternally, the method uses the `isExists` method to determine whether a character has already been processed.
  - **Example:**
    Input: `"programming"`
    Output: `"progamin"`


### 3. **Main Method**  
  - **Signature:**  
    ```java
    public static void main(String[] args)
    ```
    - **Description:**  
      1. Prompts the user to input a string.
      2. Uses the removeDuplicates method to remove duplicate characters.
      3. Displays the original string and the result after duplicate removal.


## Expected Output Example:

![](./assets/1.png)

---

![](./assets/2.png)

---

## Constraints:
- The program should handle all possible string inputs without restrictions.
- Use only `for loops` or `while loops` to implement the tasks.
- Avoid using any `built-in` string manipulation methods such as `substring`, `toCharArray`, or `others`.
- The only allowed method is `length()` to determine the length of the string
 
## Hints:
- Inside the `removeDuplicates` method, you can use the isExists method to check whether a character has already been processed.
- The `isExists` method should loop through the previously processed characters to determine if the current character already exists.