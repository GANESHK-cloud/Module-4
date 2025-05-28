# Experiment No: 4a Create Dictionary of Squares
 
## AIM  
To write a Python program that creates a dictionary with integers from 1 to `n` as keys and their squares as values.

---  
 
### ALGORITHM  
1. Begin the program.  
2. Define a function `create_square_dict(n)` that uses dictionary comprehension.  
3. Use a `for` loop with `range(1, n+1)` to generate keys.  
4. Assign each key’s value as its square.  
5. Return the dictionary.  
6. Read integer `n` from the user.  
7. Call the function with `n` and print the returned dictionary.  
8. Terminate the program.

---

### 🧾 PROGRAM

```python
def create_square_dict(n):
    return {i: i**2 for i in range(1, n+1)}

n = int(input())
result = create_square_dict(n)
print(result)

```

### OUTPUT
![image](https://github.com/user-attachments/assets/e26eac2e-6b19-4969-976b-15d49dee3e46)

### RESULT
Thus, the Python program that creates a dictionary of squares from 1 to n has been implemented and executed successfully.


# Experiment No: 4b User Defined Exception for Number Guessing

## AIM  
To write a Python program that raises a user-defined exception for the guessing number problem where the user has to guess the number 10.

---

## ALGORITHM  
1. Begin the program.  
2. Define the target number (10).  
3. Read an integer input from the user.  
4. Use `try-except` to handle exceptions.  
5. If the entered number is greater than 10, raise an exception with message "This value is too large, try again!".  
6. If it is equal to 10, print "Congratulations! You guessed it correctly.".  
7. If it is less than 10, print "This value is too small, try again!".  
8. Print the exception message in the `except` block.  
9. Terminate the program.

---

## 🧾 PROGRAM

```python
a = int(input())

try:
    if a > 10:
        raise Exception("This value is too large, try again!")
    elif a == 10:
        print("Congratulations! You guessed it correctly.")
    else:
        print("This value is too small, try again!")
except Exception as e:
    print(e)
```

### OUTPUT
![image](https://github.com/user-attachments/assets/11ca81a6-afe7-4492-afe8-52501a719217)

### RESULT
Thus, the Python program to raise a user-defined exception for the guessing number problem has been implemented and executed successfully.


# Experiment No: 4c Count Words in a File

## AIM  
To write a Python program to read a file and count the number of words in it.

---

## ALGORITHM  
1. Begin the program.  
2. Define a function `create_file(file_path, content)` that writes content into the given file.  
3. Define another function `count_words_in_file(file_path)` that reads the content from the file.  
4. Read input string from the user.  
5. Call `create_file()` with file path and input string.  
6. Call `count_words_in_file()` to count the number of words.  
7. Display the result.  
8. Terminate the program.

---

## 🧾 PROGRAM

```python
def create_file(file_path, content):
    with open(file_path, 'w') as file:
        file.write(content)

def count_words_in_file(file_path):
    with open(file_path, 'r') as file:
        content = file.read()
    words = content.split()
    return len(words)

file_path = 'test_case_1.txt'
file_content = input()
create_file(file_path, file_content)
print('the no of words in the file is:', count_words_in_file(file_path))

```


### OUTPUT
![image](https://github.com/user-attachments/assets/074683e0-5a8d-4b62-879d-135bcc29fbcb)

### RESULT
Thus, the Python program to read a file and count the number of words in it has been implemented and executed successfully.


# Experiment No: 4d-Area of Circle using Class

## AIM  
To write a Python program that takes the radius from the user and finds the area of the circle using a class named 'pen' and a function named 'stationary'.

---

## ALGORITHM  
1. Begin the program.  
2. Define a class `pen` with a function `stationary(radius)` that calculates the area of the circle using the formula:  
   - `area = π * radius^2`
3. Read the radius of the circle from the user.
4. Create an instance of the `pen` class and call the `stationary()` function.
5. Print the area of the circle to the user, formatted to 2 decimal places.
6. Terminate the program.

---

## 🧾 PROGRAM

```python
import math

class pen:
    def stationary(self, radius):
        area = math.pi * radius * radius
        return area

radius = float(input())
circle = pen()
area = circle.stationary(radius)
print(f"Area of circle: {area:.2f}")

```

### OUTPUT
![image](https://github.com/user-attachments/assets/eab62d6c-caf8-452d-a05f-e5e847d11828)

### RESULT
Thus, the Python program to calculate the area of the circle using a class and function has been implemented and executed successfully.


# Experiment No: 4e – SEB-Multiplication and Floor Division Using Class and Conditional Statements

## AIM  
To write a Python program using class and conditional statements to perform multiplication and floor division based on user choice.

---

### ALGORITHM  
1. Define a class `CSE` with the following methods:  
   - `setvalues(a, b)` to set instance variables.  
   - `mul()` to return the multiplication of `a` and `b`.  
   - `div()` to return the floor division result of `a` by `b`.  
2. Create an object of the `CSE` class.  
3. Read two integer inputs from the user and set them using `setvalues()`.  
4. Start an infinite loop.  
5. Read the user’s choice:  
   - If choice is `1`, call `mul()` and display result.  
   - If choice is `2`, call `div()` and display result.  
   - If choice is `0`, display “Exiting!” and break the loop.  
   - For any other input, print “invalid choice”.  
6. Terminate the program.

---

### 🧾 PROGRAM

```python
class CSE:
    def setvalues(self, a, b):
        self.a = a
        self.b = b

    def mul(self):
        return self.a * self.b

    def div(self):
        return self.a // self.b

n = CSE()
a = int(input())
b = int(input())
n.setvalues(a, b)

while True:
    c = int(input())
    if c == 1:
        res = n.mul()
        print(f"Result:  {res}")
    elif c == 2:
        res = n.div()
        print(f"Result:  {res}")
    elif c == 0:
        print("Exiting!")
        break
    else:
        print("invalid choice")

```

### OUTPUT
![image](https://github.com/user-attachments/assets/ec015c1d-4088-4892-8482-a583d75d52a9)

### RESULT
Thus, the Python program using class and conditional statements to perform multiplication and floor division has been implemented and executed successfully.
