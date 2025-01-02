# Write a Java Program with the Following Requirements:

## Methods to Implement:
1. **Method to Count Factors**  
   - **Signature:**  
     ```java
     public static int getFactorCount(int number)
     ```
   - **Description:**  
     This method should return the count of factors of the given number.

2. **Method to Check if a Number is Prime**  
   - **Signature:**  
     ```java
     public static boolean isPrime(int factorCount)
     ```
   - **Description:**  
     This method should return `true` if the given factor count indicates a prime number (exactly 2 factors), and `false` otherwise.

3. **Method to Retrieve All Factors**  
   - **Signature:**  
     ```java
     public static int[] getFactors(int number, int factorCount)
     ```
   - **Description:**  
     This method should return an integer array containing all the factors of the given number.

4. **Main Method**  
   - **Signature:**  
     ```java
     public static void main(String[] args)
     ```
   - **Description:**  
     This method should:
     1. Prompt the user to input a number.
     2. Use `getFactorCount` to calculate the total number of factors and print the result.
     3. Use `isPrime` to check if the number is prime and print `true` for prime or `false` otherwise.
     4. Use `getFactors` to retrieve all the factors of the number and print them.

## Expected Output Example:
If the user enters the number `10`, the program should display:

![](./assets/1.png)

---
If the user enters the number `2`, the program should display:

![](./assets/2.png)

---
If the user enters the number `17`, the program should display:

![](./assets/3.png)

---
If the user enters the number `20`, the program should display:

![](./assets/4.png)

## Constraints:
- The program should handle any positive integer input.
- Provide meaningful error messages for invalid inputs (e.g., negative numbers or non-numeric inputs).

## Hints:
- A **factor** of a number is an integer that divides the number without leaving a remainder.
- A **prime number** is a number with exactly 2 factors: `1` and the number itself.
- Use arrays to store the factors of the number.