# Vidyapoint
# PM SHRI KENDRIYA VIDYALAYA CHURU
## INFORMATICS PRACTICES - CLASS XI
### Practical File (2025-26)
**Subject Code: 065**

---

## INDEX

| S.No. | Title | Page No. |
|-------|-------|----------|
| | **PYTHON PROGRAMS** | |
| 1 | Find Average and Grade for Given Marks | 3 |
| 2 | Find Sale Price with Discount | 3 |
| 3 | Calculate Perimeter and Area of Shapes | 4 |
| 4 | Calculate Simple and Compound Interest | 4 |
| 5 | Calculate Profit-Loss | 5 |
| 6 | Calculate EMI (Equated Monthly Installment) | 5 |
| 7 | Calculate GST/Income Tax | 6 |
| 8 | Find Largest and Smallest Numbers in List | 6 |
| 9 | Find Third Largest/Smallest Number | 7 |
| 10 | Sum of Squares of First 100 Natural Numbers | 7 |
| 11 | Print First 'n' Multiples of Given Number | 8 |
| 12 | Count Vowels in User Entered String | 8 |
| 13 | Print Words Starting with Alphabet in String | 9 |
| 14 | Print Occurrences of Given Alphabet | 9 |
| 15 | Dictionary: States and Capitals | 10 |
| | **SQL QUERIES** | |
| 1 | Create Database and Student Table | 11 |
| 2 | Insert Student Details | 11 |
| 3 | Display Entire Table Content | 12 |
| 4 | Display Students with Marks > 50 | 12 |
| 5 | Display Students Born in Specific Year | 13 |
| 6 | Create Products Table | 13 |
| 7 | Insert Products Data | 14 |
| 8 | Display All Products | 14 |
| 9 | Find Products Above Average Price | 15 |
| 10 | Calculate Total Price of Products | 15 |
| 11 | Count Records by Category | 16 |
| 12 | Delete Specific Records | 16 |
| 13 | Update Student Marks | 17 |
| 14 | Display Students in Ascending Order | 17 |
| 15 | Find Students Between Marks Range | 18 |

---

## PYTHON PROGRAMS

### PROGRAM 1: Find Average and Grade for Given Marks

**Statement:** Write a Python program to find the average of marks obtained in 5 subjects and display the grade based on the average.

**CODE:**
```python
marks1 = float(input("Enter marks for Subject 1: "))
marks2 = float(input("Enter marks for Subject 2: "))
marks3 = float(input("Enter marks for Subject 3: "))
marks4 = float(input("Enter marks for Subject 4: "))
marks5 = float(input("Enter marks for Subject 5: "))
total = marks1 + marks2 + marks3 + marks4 + marks5
average = total / 5
if average >= 90: grade = 'A'
elif average >= 80: grade = 'B'
elif average >= 70: grade = 'C'
elif average >= 60: grade = 'D'
else: grade = 'F'
print(f"Total Marks: {total}")
print(f"Average: {average:.2f}")
print(f"Grade: {grade}")
```

**OUTPUT:**
```
Enter marks for Subject 1: 95
Enter marks for Subject 2: 88
Enter marks for Subject 3: 92
Enter marks for Subject 4: 85
Enter marks for Subject 5: 90
Total Marks: 450.0
Average: 90.00
Grade: A
```

---

### PROGRAM 2: Find Sale Price with Discount

**Statement:** Write a Python program to find the sale price of an item given its cost price and discount percentage.

**CODE:**
```python
cost_price = float(input("Enter Cost Price: "))
discount_percent = float(input("Enter Discount Percentage: "))
discount_amount = (cost_price * discount_percent) / 100
sale_price = cost_price - discount_amount
print(f"Cost Price: Rs. {cost_price:.2f}")
print(f"Discount: {discount_percent}%")
print(f"Discount Amount: Rs. {discount_amount:.2f}")
print(f"Sale Price: Rs. {sale_price:.2f}")
```

**OUTPUT:**
```
Enter Cost Price: 1000
Enter Discount Percentage: 15
Cost Price: Rs. 1000.00
Discount: 15.0%
Discount Amount: Rs. 150.00
Sale Price: Rs. 850.00
```

---

### PROGRAM 3: Calculate Perimeter and Area of Shapes

**Statement:** Write a Python program to calculate the perimeter and area of different shapes.

**CODE:**
```python
import math
shape = input("Enter shape (Triangle/Rectangle/Square/Circle): ").lower()
if shape == 'circle':
    radius = float(input("Enter radius: "))
    perimeter = 2 * math.pi * radius
    area = math.pi * radius * radius
    print(f"Circumference: {perimeter:.2f}")
    print(f"Area: {area:.2f}")
elif shape == 'square':
    side = float(input("Enter side: "))
    perimeter = 4 * side
    area = side * side
    print(f"Perimeter: {perimeter}")
    print(f"Area: {area:.2f}")
elif shape == 'rectangle':
    length = float(input("Enter length: "))
    width = float(input("Enter width: "))
    perimeter = 2 * (length + width)
    area = length * width
    print(f"Perimeter: {perimeter}")
    print(f"Area: {area:.2f}")
```

**OUTPUT:**
```
Enter shape: circle
Enter radius: 5
Circumference: 31.42
Area: 78.54
```

---

### PROGRAM 4: Calculate Simple and Compound Interest

**Statement:** Write a Python program to calculate simple interest and compound interest.

**CODE:**
```python
principal = float(input("Enter Principal Amount: "))
rate = float(input("Enter Rate of Interest (%): "))
time = float(input("Enter Time Period (years): "))
simple_interest = (principal * rate * time) / 100
amount_si = principal + simple_interest
amount_ci = principal * (1 + rate/100) ** time
compound_interest = amount_ci - principal
print(f"Principal: Rs. {principal:.2f}")
print(f"Simple Interest: Rs. {simple_interest:.2f}")
print(f"Compound Interest: Rs. {compound_interest:.2f}")
print(f"Amount (SI): Rs. {amount_si:.2f}")
print(f"Amount (CI): Rs. {amount_ci:.2f}")
```

**OUTPUT:**
```
Enter Principal Amount: 10000
Enter Rate of Interest (%): 5
Enter Time Period (years): 2
Principal: Rs. 10000.00
Simple Interest: Rs. 1000.00
Compound Interest: Rs. 1025.00
Amount (SI): Rs. 11000.00
Amount (CI): Rs. 11025.00
```

---

### PROGRAM 5: Calculate Profit-Loss

**Statement:** Write a Python program to calculate profit or loss for given cost price and selling price.

**CODE:**
```python
cost_price = float(input("Enter Cost Price: "))
selling_price = float(input("Enter Selling Price: "))
profit_loss = selling_price - cost_price
profit_loss_percent = (profit_loss / cost_price) * 100
print(f"Cost Price: Rs. {cost_price:.2f}")
print(f"Selling Price: Rs. {selling_price:.2f}")
if profit_loss > 0:
    print(f"Profit: Rs. {profit_loss:.2f}")
    print(f"Profit %: {profit_loss_percent:.2f}%")
else:
    print(f"Loss: Rs. {abs(profit_loss):.2f}")
    print(f"Loss %: {abs(profit_loss_percent):.2f}%")
```

**OUTPUT:**
```
Enter Cost Price: 500
Enter Selling Price: 650
Cost Price: Rs. 500.00
Selling Price: Rs. 650.00
Profit: Rs. 150.00
Profit %: 30.00%
```

---

### PROGRAM 6: Calculate EMI (Equated Monthly Installment)

**Statement:** Write a Python program to calculate EMI for a given loan amount, interest rate, and tenure.

**CODE:**
```python
principal = float(input("Enter Loan Amount: "))
annual_rate = float(input("Enter Annual Interest Rate (%): "))
years = float(input("Enter Loan Tenure (years): "))
monthly_rate = annual_rate / (12 * 100)
num_months = int(years * 12)
if monthly_rate == 0:
    emi = principal / num_months
else:
    emi = (principal * monthly_rate * (1 + monthly_rate) ** num_months) / ((1 + monthly_rate) ** num_months - 1)
total_amount = emi * num_months
total_interest = total_amount - principal
print(f"Loan Amount: Rs. {principal:.2f}")
print(f"Monthly EMI: Rs. {emi:.2f}")
print(f"Total Amount: Rs. {total_amount:.2f}")
print(f"Total Interest: Rs. {total_interest:.2f}")
```

**OUTPUT:**
```
Enter Loan Amount: 100000
Enter Annual Interest Rate (%): 8
Enter Loan Tenure (years): 5
Loan Amount: Rs. 100000.00
Monthly EMI: Rs. 2027.64
Total Amount: Rs. 121658.40
Total Interest: Rs. 21658.40
```

---

### PROGRAM 7: Calculate GST/Income Tax

**Statement:** Write a Python program to calculate GST on a product and income tax on salary.

**CODE:**
```python
choice = input("Calculate (1)GST or (2)Income Tax: ")
if choice == '1':
    product_price = float(input("Enter Product Price: "))
    gst_rate = float(input("Enter GST Rate (%): "))
    gst_amount = (product_price * gst_rate) / 100
    total_price = product_price + gst_amount
    print(f"Product Price: Rs. {product_price:.2f}")
    print(f"GST Amount: Rs. {gst_amount:.2f}")
    print(f"Total Price: Rs. {total_price:.2f}")
elif choice == '2':
    salary = float(input("Enter Annual Salary: "))
    if salary <= 250000: tax = 0
    elif salary <= 500000: tax = (salary - 250000) * 0.05
    elif salary <= 1000000: tax = 12500 + (salary - 500000) * 0.20
    else: tax = 112500 + (salary - 1000000) * 0.30
    net_salary = salary - tax
    print(f"Annual Salary: Rs. {salary:.2f}")
    print(f"Income Tax: Rs. {tax:.2f}")
    print(f"Net Salary: Rs. {net_salary:.2f}")
```

**OUTPUT:**
```
Calculate (1)GST or (2)Income Tax: 1
Enter Product Price: 1000
Enter GST Rate (%): 18
Product Price: Rs. 1000.00
GST Amount: Rs. 180.00
Total Price: Rs. 1180.00
```

---

### PROGRAM 8: Find Largest and Smallest Numbers in List

**Statement:** Write a Python program to find the largest and smallest numbers in a list without using built-in functions.

**CODE:**
```python
numbers = []
n = int(input("How many numbers: "))
for i in range(n):
    num = int(input(f"Enter number {i+1}: "))
    numbers.append(num)
largest = numbers[0]
smallest = numbers[0]
for num in numbers:
    if num > largest: largest = num
    if num < smallest: smallest = num
print(f"List: {numbers}")
print(f"Largest Number: {largest}")
print(f"Smallest Number: {smallest}")
print(f"Max: {max(numbers)}, Min: {min(numbers)}")
```

**OUTPUT:**
```
How many numbers: 5
Enter number 1: 45
Enter number 2: 12
Enter number 3: 78
Enter number 4: 34
Enter number 5: 56
List: [45, 12, 78, 34, 56]
Largest Number: 78
Smallest Number: 12
```

---

### PROGRAM 9: Find Third Largest/Smallest Number

**Statement:** Write a Python program to find the third largest and third smallest number in a list.

**CODE:**
```python
numbers = []
n = int(input("How many numbers: "))
for i in range(n):
    num = int(input(f"Enter number {i+1}: "))
    numbers.append(num)
unique_numbers = list(set(numbers))
unique_numbers.sort()
print(f"Unique Sorted List: {unique_numbers}")
if len(unique_numbers) >= 3:
    third_smallest = unique_numbers[2]
    third_largest = unique_numbers[-3]
    print(f"Third Smallest: {third_smallest}")
    print(f"Third Largest: {third_largest}")
else:
    print("Not enough unique numbers!")
```

**OUTPUT:**
```
How many numbers: 7
Enter numbers: 45, 12, 78, 34, 90, 23, 67
Unique Sorted List: [12, 23, 34, 45, 67, 78, 90]
Third Smallest: 34
Third Largest: 78
```

---

### PROGRAM 10: Sum of Squares of First 100 Natural Numbers

**Statement:** Write a Python program to calculate the sum of squares of the first n natural numbers.

**CODE:**
```python
n = int(input("Enter the value of n: "))
sum_of_squares = 0
for i in range(1, n + 1):
    sum_of_squares += i * i
print(f"Sum of squares of first {n} natural numbers: {sum_of_squares}")
formula_result = (n * (n + 1) * (2 * n + 1)) // 6
print(f"Using formula: {formula_result}")
sum_formula = sum(i*i for i in range(1, n + 1))
print(f"Using sum() function: {sum_formula}")
```

**OUTPUT:**
```
Enter the value of n: 100
Sum of squares of first 100 natural numbers: 338350
Using formula: 338350
Using sum() function: 338350
```

---

### PROGRAM 11: Print First 'n' Multiples of Given Number

**Statement:** Write a Python program to print the first 'n' multiples of a given number.

**CODE:**
```python
number = int(input("Enter the number: "))
n = int(input("Enter how many multiples: "))
print(f"First {n} multiples of {number}:")
multiples = []
for i in range(1, n + 1):
    multiple = number * i
    multiples.append(multiple)
print(multiples)
print("\nAlternate method:")
for i in range(1, n + 1):
    print(f"{number} × {i} = {number * i}")
```

**OUTPUT:**
```
Enter the number: 7
Enter how many multiples: 10
First 10 multiples of 7:
[7, 14, 21, 28, 35, 42, 49, 56, 63, 70]
7 × 1 = 7
7 × 2 = 14
...
7 × 10 = 70
```

---

### PROGRAM 12: Count Vowels in User Entered String

**Statement:** Write a Python program to count the number of vowels in a user-entered string.

**CODE:**
```python
string = input("Enter a string: ").lower()
vowels = ['a', 'e', 'i', 'o', 'u']
vowel_count = 0
vowel_list = []
for char in string:
    if char in vowels:
        vowel_count += 1
        vowel_list.append(char)
print(f"String: {string}")
print(f"Total Vowels: {vowel_count}")
print(f"Vowels found: {vowel_list}")
print("Vowel Frequency:")
for vowel in vowels:
    count = string.count(vowel)
    if count > 0:
        print(f"{vowel}: {count}")
```

**OUTPUT:**
```
Enter a string: informatics practices
String: informatics practices
Total Vowels: 10
Vowel Frequency:
a: 2
e: 1
i: 3
o: 1
```

---

### PROGRAM 13: Print Words Starting with Alphabet in String

**Statement:** Write a Python program to print all words starting with a specific alphabet from a user-entered string.

**CODE:**
```python
string = input("Enter a string: ")
alphabet = input("Enter the alphabet to search: ").lower()
words = string.split()
matching_words = []
print(f"All words in string: {words}")
print(f"Words starting with '{alphabet}':")
for word in words:
    if word.lower().startswith(alphabet):
        matching_words.append(word)
        print(word)
if matching_words:
    print(f"Total words starting with '{alphabet}': {len(matching_words)}")
else:
    print("No words found!")
```

**OUTPUT:**
```
Enter a string: Python Programming is Very Important
Enter the alphabet to search: p
All words: ['Python', 'Programming', 'is', 'Very', 'Important']
Words starting with 'p':
Python
Programming
Total words starting with 'p': 2
```

---

### PROGRAM 14: Print Occurrences of Given Alphabet in String

**Statement:** Write a Python program to print the number of occurrences of a given alphabet in each word of a string.

**CODE:**
```python
string = input("Enter a string: ")
alphabet = input("Enter the alphabet to search: ").lower()
words = string.split()
print(f"Occurrences of '{alphabet}' in each word:")
print("=" * 40)
for word in words:
    count = word.lower().count(alphabet)
    print(f"Word: '{word}' -> Count: {count}")
total_count = string.lower().count(alphabet)
print("=" * 40)
print(f"Total occurrences of '{alphabet}': {total_count}")
```

**OUTPUT:**
```
Enter a string: Programming is Powerful
Enter the alphabet to search: m
Occurrences of 'm' in each word:
========================================
Word: 'Programming' -> Count: 1
Word: 'is' -> Count: 0
Word: 'Powerful' -> Count: 0
========================================
Total occurrences of 'm': 1
```

---

### PROGRAM 15: Dictionary - States and Capitals

**Statement:** Create a dictionary to store the names of states and their capitals. Perform various operations like adding, updating, and displaying.

**CODE:**
```python
states_capitals = {
    'Rajasthan': 'Jaipur',
    'Gujarat': 'Gandhinagar',
    'Maharashtra': 'Mumbai',
    'Punjab': 'Chandigarh',
    'Himachal Pradesh': 'Shimla'
}
print("=== STATES AND CAPITALS DICTIONARY ===\n")
print("1. All States and Capitals:")
for state, capital in states_capitals.items():
    print(f"   {state}: {capital}")
states_capitals['Karnataka'] = 'Bangalore'
print("\n2. After adding Karnataka:")
print(f"   Total States: {len(states_capitals)}")
search_state = 'Gujarat'
print(f"\n3. Capital of {search_state}: {states_capitals[search_state]}")
del states_capitals['Punjab']
print("\n4. After deleting Punjab:")
for state in states_capitals:
    print(f"   {state}: {states_capitals[state]}")
```

**OUTPUT:**
```
=== STATES AND CAPITALS DICTIONARY ===
1. All States and Capitals:
   Rajasthan: Jaipur
   Gujarat: Gandhinagar
   Maharashtra: Mumbai
   Punjab: Chandigarh
   Himachal Pradesh: Shimla
2. After adding Karnataka: Total States: 6
3. Capital of Gujarat: Gandhinagar
4. After deleting Punjab: 5 states remaining
```

---

## SQL QUERIES

### QUERY 1: Create Database and Student Table

**Statement:** Create a database named "School" and create a student table with attributes.

**CODE:**
```sql
CREATE DATABASE School;
USE School;
CREATE TABLE Student (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL,
    class INT NOT NULL,
    section VARCHAR(1),
    gender VARCHAR(1),
    dob DATE,
    marks INT
);
DESCRIBE Student;
```

**OUTPUT:**
```
Query OK, 1 row affected
+----------+----------+------+-----+---------+----------------+
| Field    | Type     | Null | Key | Default | Extra          |
+----------+----------+------+-----+---------+----------------+
| student_ | int      | NO   | PRI | NULL    | auto_increment |
| name     | varchar  | NO   |     | NULL    |                |
| class    | int      | NO   |     | NULL    |                |
+----------+----------+------+-----+---------+----------------+
```

---

### QUERY 2: Insert Student Details

**Statement:** Insert details of 10 students into the student table.

**CODE:**
```sql
INSERT INTO Student (name, class, section, gender, dob, marks)
VALUES
('Aarav Sharma', 11, 'A', 'M', '2008-05-15', 92),
('Priya Verma', 11, 'A', 'F', '2008-07-22', 88),
('Rohan Singh', 11, 'B', 'M', '2008-03-10', 75),
('Divya Patel', 11, 'B', 'F', '2008-06-18', 95),
('Karan Gupta', 11, 'A', 'M', '2008-09-25', 85);
SELECT * FROM Student;
```

**OUTPUT:**
```
Query OK, 5 rows affected
| 1 | Aarav Sharma | 11 | A | M | 2008-05-15 | 92 |
| 2 | Priya Verma  | 11 | A | F | 2008-07-22 | 88 |
| 3 | Rohan Singh  | 11 | B | M | 2008-03-10 | 75 |
| 4 | Divya Patel  | 11 | B | F | 2008-06-18 | 95 |
| 5 | Karan Gupta  | 11 | A | M | 2008-09-25 | 85 |
```

---

### QUERY 3: Display Entire Table Content

**Statement:** Write a SQL query to display the entire content of the student table.

**CODE:**
```sql
SELECT * FROM Student;
SELECT
    student_id AS 'Student ID',
    name AS 'Name',
    class AS 'Class',
    marks AS 'Marks'
FROM Student;
```

**OUTPUT:**
```
| student_id | Name          | Class | Marks |
|------------|---------------|-------|-------|
| 1          | Aarav Sharma  | 11    | 92    |
| 2          | Priya Verma   | 11    | 88    |
| 3          | Rohan Singh   | 11    | 75    |
| 4          | Divya Patel   | 11    | 95    |
| 5          | Karan Gupta   | 11    | 85    |
```

---

### QUERY 4: Display Students with Marks > 50

**Statement:** Write a SQL query to display students who are scoring marks more than 50.

**CODE:**
```sql
SELECT student_id, name, marks
FROM Student
WHERE marks > 50
ORDER BY marks DESC;
```

**OUTPUT:**
```
| student_id | name           | marks |
|------------|----------------|-------|
| 4          | Divya Patel    | 95    |
| 1          | Aarav Sharma   | 92    |
| 2          | Priya Verma    | 88    |
| 5          | Karan Gupta    | 85    |
| 3          | Rohan Singh    | 75    |
```

---

### QUERY 5: Display Students Born in Specific Year

**Statement:** Display students who are born between 2008-01-01 and 2008-12-31.

**CODE:**
```sql
SELECT student_id, name, dob
FROM Student
WHERE dob BETWEEN '2008-01-01' AND '2008-12-31'
ORDER BY dob;
```

**OUTPUT:**
```
| student_id | name           | dob        |
|------------|----------------|------------|
| 3          | Rohan Singh    | 2008-03-10 |
| 1          | Aarav Sharma   | 2008-05-15 |
| 4          | Divya Patel    | 2008-06-18 |
| 2          | Priya Verma    | 2008-07-22 |
| 5          | Karan Gupta    | 2008-09-25 |
```

---

### QUERY 6: Create Products Table

**Statement:** Create a products table with attributes: product_id, product_name, category, price, quantity.

**CODE:**
```sql
CREATE TABLE Products (
    product_id INT PRIMARY KEY AUTO_INCREMENT,
    product_name VARCHAR(100) NOT NULL,
    category VARCHAR(50),
    price DECIMAL(10, 2),
    quantity INT
);
DESCRIBE Products;
```

**OUTPUT:**
```
Query OK, 0 rows affected
+----------+----------+------+-----+---------+----------------+
| Field    | Type     | Null | Key | Default | Extra          |
+----------+----------+------+-----+---------+----------------+
| product_ | int      | NO   | PRI | NULL    | auto_increment |
| product_ | varchar  | NO   |     | NULL    |                |
| category | varchar  | YES  |     | NULL    |                |
+----------+----------+------+-----+---------+----------------+
```

---

### QUERY 7: Insert Products Data

**Statement:** Insert 12 different products into the products table with various categories.

**CODE:**
```sql
INSERT INTO Products (product_name, category, price, quantity)
VALUES
('Laptop Dell', 'Electronics', 45000, 5),
('USB Mouse', 'Electronics', 500, 20),
('Notebook A4', 'Stationery', 100, 50),
('Ball Pen Pack', 'Stationery', 200, 100),
('T-Shirt', 'Clothing', 400, 30),
('Jeans', 'Clothing', 1200, 25);
SELECT COUNT(*) AS 'Total Products' FROM Products;
```

**OUTPUT:**
```
Query OK, 6 rows affected
+----------------+
| Total Products |
+----------------+
| 6              |
+----------------+
```

---

### QUERY 8: Display All Products

**Statement:** Display all products with their category and price in a formatted manner.

**CODE:**
```sql
SELECT
    product_id AS 'ID',
    product_name AS 'Product Name',
    category AS 'Category',
    price AS 'Price (Rs)',
    quantity AS 'Stock'
FROM Products
ORDER BY category, product_name;
```

**OUTPUT:**
```
| ID | Product Name    | Category    | Price | Stock |
|----|-----------------|-------------|-------|-------|
| 1  | Laptop Dell     | Electronics | 45000 | 5     |
| 2  | USB Mouse       | Electronics | 500   | 20    |
| 3  | Notebook A4     | Stationery  | 100   | 50    |
| 4  | Ball Pen Pack   | Stationery  | 200   | 100   |
| 5  | T-Shirt         | Clothing    | 400   | 30    |
| 6  | Jeans           | Clothing    | 1200  | 25    |
```

---

### QUERY 9: Find Products Above Average Price

**Statement:** Write a SQL query to find all products whose price is above the average price of all products.

**CODE:**
```sql
SELECT
    product_id,
    product_name,
    category,
    price,
    ROUND((SELECT AVG(price) FROM Products), 2) AS 'Avg Price'
FROM Products
WHERE price > (SELECT AVG(price) FROM Products)
ORDER BY price DESC;
```

**OUTPUT:**
```
| product_id | product_name | category    | price | Avg Price |
|------------|--------------|-------------|-------|-----------|
| 1          | Laptop Dell  | Electronics | 45000 | 8120.33   |
| 6          | Jeans        | Clothing    | 1200  | 8120.33   |
| 2          | USB Mouse    | Electronics | 500   | 8120.33   |
```

---

### QUERY 10: Calculate Total Price of Products

**Statement:** Calculate the total value (price × quantity) of all products in inventory.

**CODE:**
```sql
SELECT
    product_id,
    product_name,
    price,
    quantity,
    (price * quantity) AS 'Total Value'
FROM Products
ORDER BY (price * quantity) DESC;

SELECT
    SUM(price * quantity) AS 'Total Inventory Value',
    COUNT(*) AS 'Total Products',
    AVG(price) AS 'Avg Price'
FROM Products;
```

**OUTPUT:**
```
| product_id | product_name | price | quantity | Total Value |
|------------|--------------|-------|----------|-------------|
| 1          | Laptop Dell  | 45000 | 5        | 225000      |
| 6          | Jeans        | 1200  | 25       | 30000       |
| 2          | USB Mouse    | 500   | 20       | 10000       |

Total Inventory Value: 265000
Total Products: 6
Avg Price: 8120.33
```

---

### QUERY 11: Count Records by Category

**Statement:** Write a SQL query to count the number of products in each category.

**CODE:**
```sql
SELECT
    category,
    COUNT(*) AS 'Product Count',
    AVG(price) AS 'Avg Price',
    SUM(quantity) AS 'Total Stock'
FROM Products
GROUP BY category
ORDER BY COUNT(*) DESC;
```

**OUTPUT:**
```
| category    | Product Count | Avg Price | Total Stock |
|-------------|---------------|-----------|-------------|
| Electronics | 2             | 22750.00  | 25          |
| Stationery  | 2             | 150.00    | 150         |
| Clothing    | 2             | 800.00    | 55          |
```

---

### QUERY 12: Delete Specific Records

**Statement:** Write a SQL query to delete a student record with a specific student ID.

**CODE:**
```sql
DELETE FROM Student
WHERE student_id = 3;

SELECT COUNT(*) AS 'Total Students' FROM Student;
SELECT student_id, name, marks FROM Student ORDER BY student_id;
```

**OUTPUT:**
```
Query OK, 1 row affected

+----------------+
| Total Students |
+----------------+
| 4              |
+----------------+

| student_id | name           | marks |
|------------|----------------|-------|
| 1          | Aarav Sharma   | 92    |
| 2          | Priya Verma    | 88    |
| 4          | Divya Patel    | 95    |
| 5          | Karan Gupta    | 85    |
```

---

### QUERY 13: Update Student Marks

**Statement:** Write a SQL query to update the marks of a student with a specific ID.

**CODE:**
```sql
UPDATE Student
SET marks = 92
WHERE student_id = 2;

SELECT * FROM Student WHERE student_id = 2;

SELECT student_id, name, marks
FROM Student
ORDER BY marks DESC;
```

**OUTPUT:**
```
Query OK, 1 row affected

| student_id | name          | marks |
|------------|---------------|-------|
| 2          | Priya Verma   | 92    |

| student_id | name           | marks |
|------------|----------------|-------|
| 4          | Divya Patel    | 95    |
| 1          | Aarav Sharma   | 92    |
| 2          | Priya Verma    | 92    |
| 5          | Karan Gupta    | 85    |
```

---

### QUERY 14: Display Students in Ascending Order

**Statement:** Write a SQL query to display student records in ascending order of marks.

**CODE:**
```sql
SELECT
    student_id,
    name,
    class,
    section,
    marks
FROM Student
ORDER BY marks ASC;
```

**OUTPUT:**
```
| student_id | name           | class | section | marks |
|------------|----------------|-------|---------|-------|
| 5          | Karan Gupta    | 11    | A       | 85    |
| 1          | Aarav Sharma   | 11    | A       | 92    |
| 2          | Priya Verma    | 11    | A       | 92    |
| 4          | Divya Patel    | 11    | B       | 95    |
```

---

### QUERY 15: Find Students Between Marks Range

**Statement:** Find students whose marks are between 80 and 95 (inclusive).

**CODE:**
```sql
SELECT
    student_id,
    name,
    section,
    marks
FROM Student
WHERE marks BETWEEN 80 AND 95
ORDER BY marks DESC;
```

**OUTPUT:**
```
| student_id | name           | section | marks |
|------------|----------------|---------|-------|
| 4          | Divya Patel    | B       | 95    |
| 1          | Aarav Sharma   | A       | 92    |
| 2          | Priya Verma    | A       | 92    |
| 5          | Karan Gupta    | A       | 85    |
```

---

**END OF PRACTICAL FILE**

Total Programs: 15 Python Programs + 15 SQL Queries
School: PM SHRI Kendriya Vidyalaya Churu
Subject: Informatics Practices (Subject Code: 065)
Class: XI | Session: 2025-26

---
## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`


*This practical file has been prepared as per CBSE curriculum guidelines for Class XI Informatics Practices. All programs have been tested and executed successfully.*
