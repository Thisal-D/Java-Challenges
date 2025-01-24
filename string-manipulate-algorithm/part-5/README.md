# **Java String Manipulation Program**

## **Objective**  
Develop a Java program that performs two essential string manipulation tasks:  

- **Convert a given string to lowercase.**  
- **Convert a given string to uppercase.**  

---

## **Requirements**  

### **1. Implement the following methods:**  

#### **Method 1: Convert String to Lowercase**  
- **Method Signature:**  
  ```java
  public static String toLowerCase(String value)
  ```
- Description:
  - This method converts the given string into lowercase without using built-in string manipulation methods.


#### **Method 2: Convert String to Uppercase**  
- **Method Signature:**  
  ```java
  public static String toUpperCase(String value)
  ```
- Description:
  - This method converts the given string into uppercase without using built-in string manipulation methods.



#### Implement the Main Method
- **Method Signature:**
  ```java
  public static void main(String[] args)
  ```
- Functionality:
  1. Prompt the user to input a string.
  2. Call toLowerCase() to convert the string to lowercase.
  3. Call toUpperCase() to convert the string to uppercase.
  4. Display both the lowercase and uppercase results.

---

## Constraints
- The program should handle all possible string inputs without restrictions.
- Do not use built-in string manipulation methods such as `toLowerCase()`, `toUpperCase()`, `substring()`, or `toCharArray()`.
- The only allowed method from the String class is `length()`.
- You must use loops (`for` or `while`) to iterate through the string and manipulate characters.
  
---

## **Hints: Using [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map) for Character Conversion**

### **Why Use [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map) ?**  
A [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map)  is an efficient way to store character mappings because:  
- It provides **O(1) lookup time**, making conversions fast.  
- It allows us to **map uppercase letters (`A-Z`) to lowercase (`a-z`)** and vice versa.  

### **How Does the Conversion Work?**  
- In ASCII, uppercase and lowercase letters differ by **32**:
  - `'A' (65)` → `'a' (97)`, `'B' (66)` → `'b' (98)`, etc.
  - Lowercase letters (`a-z`) can be mapped back to uppercase using the same logic.

### **Steps to Implement Using [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map)**
1. **Create Two [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map)  Objects**  
   - `lowerMap`: Maps uppercase letters (`A-Z`) to lowercase (`a-z`).  
   - `upperMap`: Maps lowercase letters (`a-z`) to uppercase (`A-Z`).  

2. **Populate the Maps**  
   - Iterate through uppercase letters (`A-Z`), mapping each to its lowercase counterpart.
   - Repeat for lowercase letters (`a-z`), mapping them to uppercase.

3. **Perform the Conversion**  
   - Iterate through the string, checking each character in the respective map.
   - If a character is found in the map, replace it; otherwise, keep it unchanged.

---

### **Alternative Approach Without [`HashMap`](https://github.com/Thisal-D/Java-Data-Structures/tree/main/non-primitive-data-types/collections/Map/Hash-Map)**
- If `HashMap` is not used, the conversion can be done using **ASCII arithmetic**:
  - If a character is between `'A'` and `'Z'`, add `32` to convert it to lowercase.
  - If a character is between `'a'` and `'z'`, subtract `32` to convert it to uppercase.