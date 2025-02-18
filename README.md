
# 🐍 Python Questions I Solved
<br />

## Description
_This repository contains a collection of Python questions that I have solved, ranging from beginner to advanced levels. Solving these problems has helped me improve my Python problem-solving skills. The goal of this project is to get familiar with different challenges and become proficient in solving problems._
<br />
<br />

## 🚀 How to Use

- Clone the repository:
```bash
git clone https://github.com/ahmad-mirzaei/python-questions-that-i-solved.git

```
<br />

---

- ## **Translated versions**
    - [Persian Version - فارسی](READMEir.md)

---

## 🤝 Contribution

__If you have more questions or would like to suggest better solutions, I’d be happy to collaborate! Please feel free to submit a `Pull Request`.__
<br />
<br />

---

## ❓ Questions

**`1`**. Write a program that stores the information of three students (including student ID, first name, last name, and GPA) in a list of dictionaries and then prints them in the following format.
<br />

`Input` : None
<br />

`Output` :

9823567      ali          ahmadi      16.25

9781294      reza        ghasemi      13.75

9976239      mehdi       tavakoli     18.32
<br />

```python
nested_dictionaries = {
    "student1" : {"studentID" : 9823567, "studentFirstName" : "ali",\
        "studentLastName" : "ahmadi","studentAvrage" : 16.25},
    "student2" : {"studentID" : 9781294, "studentFirstName" : "reza",\
    "studentLastName" : "ghasemi", "studentAvrage" : 13.75},
    "student3" : {"studentID" : 9976239, "studentFirstName" : "mehdi",\
    "studentLastName" : "tavakoli", "studentAvrage" : 18.32}
}

for student in nested_dictionaries:
    for item in nested_dictionaries[student].values():
        print(item, end= " ")
    print()
```
<br />

---

**`2`**. Write a program that takes the number N as input and creates a dictionary where the keys are the numbers from 1 to N, and the values are the squares of the keys.
<br />

`Input` : Enter Number : 9
<br />

`Output` : {1: 1, 2: 4, 3: 9, 4: 16, 5: 15, 6: 36, 7: 49, 8: 64, 9: 81}
<br />

```python
# step 1
n = int(input("Enter Number : "))
dictionary = {}
for i in range(1, n+1):
    dictionary[i] = i*i
print(dictionary)

# step 2
n = int(input("Enter Number : "))
dictionary = {x: x*x for x in range(1, n+1)}
print(dictionary)
```
<br />

---

**`3`**. Write a program that takes a positive integer N as input, then creates an English-to-Persian dictionary with N words by receiving words and their meanings from the user, and finally prints the dictionary.
<br />

`Input` :

Enter Number : 3

Enter English word 1 : book

Enter Persian word 1: ketab

Enter English word 2: chair

Enter Persian word 2: sandali

Enter English word 3: bag

Enter Persian word 3: kif
<br />

`Output` : {'book': 'ketab', 'chair': 'sandali' , 'bag': 'kif'}
<br />

```python
dictionary = {}
n = int(input("Enter Number : "))
for myDict in range(1, n+1):
    en_to_ir = input("Enter English Word : ")
    ir_to_en = input("Enter Persian Word : ")
    dictionary[en_to_ir] = ir_to_en
print(dictionary)
```
<br />

---

**`4`**. Write a program that takes 5 positive integers as input and stores them in a list. Then, using a function, multiply all elements of the list by 10, and finally, print the resulting list in the main program.
<br />

`Input` :

Enter Number : 143

Enter Number : 69

Enter Number : 21

Enter Number : 567

Enter Number : 48
<br />

`Output` : [1430 , 690 , 210 , 5670 , 480]
<br />

```python
def multiply_list_elements(lst):
    lst = [i * 10 for i in lst]
    return lst

lst = []
for i in range(1, 6):
    n = int(input("Enter Number : "))
    lst.append(n)

print(multiply_list_elements(lst))
```
<br />

---

**`5`**. Write a program that takes a list of nonzero integers as input using a function. Then, using another function, find and print the largest and smallest elements of the list. (The input process should stop when the user enters zero.)
<br />

`Input` :

Enter Number : 25

Enter Number : 9

Enter Number : 83

Enter Number : 6

Enter Number : -12

Enter Number : 17

Enter Number : 0
<br />

`Output` :
Max is : 83
Min is  : -12
<br />

```python
list_of_numbers = []
def get_number(list_of_numbers):
    while True:
        n = int(input("Enter Number : "))
        list_of_numbers.append(n)
        if n == 0:
            break
def min_and_max():
    print(f"max is : {max(list_of_numbers)}")
    print(f"min is : {min(list_of_numbers)}")

get_number(list_of_numbers)
min_and_max()
```
<br />

---

**`6`**. Write a program that prints the largest input number. The input numbers are between 10 and 90, and the input process should continue until -1 is entered.
<br />

```python
lst = []
print("pleas select number from 10 to 90")
while True:
    n = int(input("Enter Number : "))
    if n in range(10, 91):
        lst.append(n)
    elif n < 0:
        break
    else:
        print("pleas select number from 10 to 90")
print("max is : ", max(lst))
```
<br />

---

**`7`**. Write a program that takes a string containing multiple words as input and outputs the string with the first letter of each word capitalized.
<br />

```python
# step 1
user_input = input("Enter a word : ")
print(user_input.title())

# step 2
user_input = input("Enter a word : ").split()
print(" ".join([word.capitalize() for word in user_input]))
```
<br />

---

**`8`**. Write a program that takes a number as the day of the year from the input and determines in which season that day falls.
<br />

`Input` : 154
<br />

`Output` : Summer
<br />

```python
# step_1
number_of_day = int(input("Enter Number Of Day : "))
# spring, summer, fall, winter = 93 + 93 + 90 + 89 = 365
if number_of_day in range(1, 94): 
    print("spring")
elif number_of_day in range(94, 187):
    print("summer")
elif number_of_day in range(187, 277):
    print("fall")
elif number_of_day in range(277, 366):
    print("winter")
else:
    print("Your Number Is Wrong!!!\nPlease Try Again")

# step_2
number_of_day = int(input("Enter Number Of Day : "))
if (1 <= number_of_day <= 93):
    print("spring")
elif (94 <= number_of_day <= 186):
    print("summer")
elif (187 <= number_of_day <= 276):
    print("fall")
elif (276 <= number_of_day <= 365):
    print("winter")
else:
    print("Your Number Is Wrong!!!\nPlease Try Again")
```
<br />

---

**`9`**. Write a program that takes three numbers as input and prints the middle number (the second largest).
<br />

`Input` : 20 - 35 - 17
<br />

`Output` : 20
<br />

```python
# step 1 ----> max(), min() 
num_1 = int(input(" Enter Your Number : "))
num_2 = int(input(" Enter Your Number : "))
num_3 = int(input(" Enter Your Number : "))
if (num_2 < num_1 > num_3):
    print(max(num_2, num_3))
elif (num_1 < num_2 > num_3):
    print(max(num_1, num_3))
else:
    print(max(num_1, num_2))

# step 2 
mylist = []
for i in range(0, 3):
    number = int(input("enter number : "))
    mylist.append(number)
mylist.remove(max(mylist))
mylist.remove(min(mylist))
print(f"your number is : {mylist}")

# step 3 ----> with array, remove() max() and min()
num_1 = int(input("Enter Your Number : "))
num_2 = int(input("Enter Your Number : "))
num_3 = int(input("Enter Your Number : "))
array = [num_1, num_2, num_3]
array.remove(max(array))
array.remove(min(array))
print(array)

# step 4
num_1 = int(input("enter number : "))
num_2 = int(input("enter number : "))
num_3 = int(input("enter number : "))
if (num_1 > num_2) and (num_1 > num_3) and (num_2 > num_3):
    print(num_2)
elif (num_1 > num_2) and (num_1 > num_3) and (num_3 > num_2):
    print(num_3)
elif (num_2 > num_1) and (num_2 > num_3) and (num_1 > num_3):
    print(num_1)
elif (num_2 > num_1) and (num_2 > num_3) and (num_3 > num_1):
    print(num_3)
elif (num_3 > num_1) and (num_3 > num_2) and (num_1 > num_2):
    print(num_1)
elif (num_3 > num_1) and (num_3 > num_2) and (num_2 > num_1):
    print(num_2)
else:
    print("error")

# step 5
a = int(input("enter number : "))
b = int(input("enter number : "))
c = int(input("enter number : "))
if a > b > c or c > b > a:
    print(b)
elif b > a > c or c > a > b:
    print(a)
elif a > c > b or b > c > a:
    print(c)
else:
    print("wrong!")
```
<br />

---

**`10`**. Write a program that takes an integer n as input and prints the first n terms of the Fibonacci sequence.
<br />
(The Fibonacci sequence is generated by starting with two terms of 1, and each subsequent term is the sum of the previous two terms.)
<br />

`Input` : 8
<br />

`Output` : 1 - 2 - 3 - 5 - 8 - 13 - 21
<br />

```python
# step_1 ----> with function
def fibo(n):
    if (n < 0):
        print("Error")
    elif (n == 0):
        return 0
    elif (n == 1):
        return 1
    else:
        return fibo(n-1) + fibo(n-2)
user_number = int(input("Enter Number : "))
print(fibo(user_number))

# step_2 ----> with while
f1 = 1
f2 = 1
i = 3
user_number = int(input("enter number : "))
print(f1, f2)
while (i <= user_number):
    f3 = (f1 + f2)
    print(f3, end=" ")
    f1 = f2
    f2 = f3
    i += 1
```
<br />

---


**`11`**. Write a program that takes two positive integers, a and b, as input, then raises a to the power of b and prints the result.
<br />

`Input` : 2 - 6
<br />

`Output` : 64
<br />

```python
# step 1
a = int(input("Enter Number : "))
b = int(input("Enter Number : "))
print(a**b)

# step 2
def expoent(a, b):
    return a ** b
a = int(input("Enter Number : "))
b = int(input("Enter Number : "))
print(expoent(a, b))
```
<br />

---

**`12`**. Write a program that takes a number as input and generates an output similar to the example within the range of that number.
<br />

```bash
*
* *
* * *
* * * *
* * * * *
```
<br />

```python
# step 1 ----> with for
n = int(input("Enter Number : "))
for i in range(n + 1):
    print("* " * i)

# step 2 ----> with while
i = 0
n = int(input("Enter Number : "))
while i <= n:
    print("* " * i)
    i+=1

#step 3 ----> nested loops
n = int(input(" Enter Number : "))
for i in range(n):
    for j in range(i+1):
        print("*" * 1, end=" ")
    print()
```
<br />

---

**`13`**. Write a program using a while loop that takes 20 numbers as input and then outputs their sum.
<br />

```python
sum = 0
i = 1
while i <= 20:
    n = int(input("Enter Your Number : "))
    sum += n
    i += 1
print(sum)
```
<br />

---

**`14`**. Write a program that takes multiple positive integers as input, then calculates and prints the sum and average of the unique numbers.  
<br />

**Notes:**  
- Duplicate numbers should be counted only once.  
- The input process stops when the user enters a negative number. 
<br />

`Input` : \
Enter Number : 8 \
Enter Number : 2 \
Enter Number : 3 \
Enter Number : 8 \
Enter Number : 1 \
Enter Number : 2 \
Enter Number : -4 \
<br />

`Output` : \
sum : 14 \
avg  : 3.5
<br />

```python
mySet = set()
while True:
    n = int(input("Enter Your Number : "))
    mySet.add(n)
    if n < 0:
        break
mySum = sum(mySet)
len_mySet = len(mySet)
avg = mySum / len_mySet
print(f"sum is : {mySum} and avg is : {avg}")

# print("sum is :", mySum, "and avg is : ", avg)
# print("sum is : %i and avg is : %d" %(mySum, avg))
# print("sum is : {0} and avg is : {1}".format(mySum, avg))
```
<br />

---

**`15`**. Write a program that takes eight names as input and stores them in a list. Then, it filters the names that start with the letter **'m'** and end with either **'d'** or **'i'**, storing them in a **set**, and finally prints the set.
<br />

```python
lst = []
mySet = set()
i = 0
while (i < 8):
    userName = input("Enter Your Name : ")
    lst.append(userName)
    i += 1
#List Comprehension
list2 = [item for item in lst if 'm' == item[0] and 'd' == item[-1] or 'm' == item[0] and 'i' == item[-1]] 
mySet.update(list2)
print(mySet)

# step 2
lst = []
mySet = set()
i = 0
while (i < 8):
    userName = input("Enter Your Name : ")
    lst.append(userName)
    i += 1
#startswith() and endswith()
for item in lst:
    if item.startswith('m') and item.endswith('d') or\
        item.startswith('m') and item.endswith('i'):
        mySet.add(item)
print(mySet)
```
<br />

---

**`16`**. Write a `for` loop that takes numbers as input and stores them in a list. The loop should stop (using `break`) when the sum of the numbers exceeds 50.
<br />

```python
lst = []

while True:
    lst.append(int(input("enter number : ")))
    if sum(lst) >= 50:
        print("sum is >= 50")
        break
```
<br />

---

**`17`**. Write a program that takes a number as input and returns an output similar to the following.
<br />

```bash
*         
* *       
* * *     
* * * *   
* * * * * 
* * * *
* * *
* *
*
```
<br />

```python
n = int(input("enter number : "))

for i in range(n):
    print("* " * i)
for j in range(n, 0, -1):
    print("* " * j)
```
<br />

---

**`18`**. Write a program that reads the number of items and the price of each item, then calculates and displays the total sales amount (total sales = number of items * price per item).
<br />

```python
sum = 0
number_of_goods = int(input("Enter The Number Of Goods : "))
for counter in range(number_of_goods):
    cost_of_goods = int(input("Enter The Cost Of Goods : "))
    sum += cost_of_goods
print(number_of_goods * sum)
```
<br />

---

**`19`**. Write a program that prints the following shape in the output.
<br />

```bash
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```
<br />

```python
n = int(input("enter number : "))

for i in range(1, n + 1):
	for j in range(1, i + 1):
		print(j, end=' ')
	print()
```
<br />

---

**`20`**. Write a program that reads a four-digit number. If the product of the first and fourth digits equals the sum of the second and third digits, print `Yes`; otherwise, print `No`.
<br />

```python
number = [int(i) for i in input("Please enter a four-digit number : ")]
print("YES") if number[0] * number[3] == number[1] + number[2] else print("NO")
```
<br />

---

**`21`**. Write a program that reads a three-digit number. If the sum of the first and third digits equals the second digit, print `Yes`; otherwise, print `No`.
<br />

```python
number = [int(i) for i in input("Please enter a three-digit number : ")]
print("YES") if number[0] + number[2] == number[1] else print("NO")
```
<br />

---

**`22`**. Write a program that takes a number as input and removes all zeros from it.
<br />

```python
n = [int(i) for i in input("Enter Number : ")]
for i in n:
    if i == 0:
        n.remove(0)
for i in n:
    print(i, end='')
```
<br />

---

**`23`**. Write a program that takes two numbers, `a` and `b`, as input. It raises the smaller number to the power of the larger number and displays the result.
<br />

```python
a = int(input("Enter Number : "))
b = int(input("Enter Number : "))
print(a**b) if a < b else print(b**a)
```
<br />

---

**`24`**. Write a program that takes the first name, last name, and salary of 10 people as input. It then displays the name and surname of the person with the highest salary.
<br />

```python
lst = []
for counter in range(1, 11):
    full_name = input("Enter Your First Name And Last Name: ")
    salary = int(input("Enter Your Salary : "))
    lst.append([full_name, salary])
# print(lst)
for i in lst:
    for j in lst:
        print("Most Salaries : ", j) if j[1] > i[1] else print()
```
<br />

---

**`25`**. Write a program that receives a student's grade. If the grade is less than 11, it displays the word `Failed`; otherwise, it displays `Passed`.
<br />

```python
i = 1
number_of_lessons = int(input("Enter The Number Of Lessons : "))
while i <= number_of_lessons:
    score = int(input("Enter Your Score : "))
    print("Failed") if score < 11 else print("Passed")
    i+=1
print("Finish")
```
<br />

---

**`26`**. Write a program that takes two two-digit numbers and determines whether they share any common digits.
<br />

```python
num1 =[int(i) for i in input("Please enter a two-digit number :  ")]
num2 = [int(i) for i in input("Please enter a two-digit number : ")]
for i in num1:
	for j in num2:
		if i == j:
			print("Similar Number is -> ", i)
```
<br />

---

**`27`**. Write a program that takes a number as input and determines how many digits it has. The input number will have a maximum of 5 digits.
<br />

```python
lst = []
while True:
	user_input = [int(i) for i in input("Please Enter a 5-Digit Number : ")]
	lst = user_input
	if len(lst) in range(1, 6):
		print(f"The number entered is {len(lst)} digits")
		break
	else:
		print("Error\nPlease Try Again")
```
<br />

---

**`28`**. Write a program that takes a string as input and removes any extra spaces between its words.
<br />

```python
user_input = ''.join(input("Enter Your String : ").split(' '))
print(user_input)
```
<br />

---

**`29`**. Write a program that takes a number as input in the main program, calculates the largest digit of the number in a separate function, and then displays the result in the main program.
<br />

```python
def max_number(n):
    return max(n)
n = [int(i) for i in input("Enter Number : ")]
print(max_number(n))
```
<br />

---

**`30`**. Write a program that takes three inputs from the user and outputs the largest, smallest, and the sum of the numbers.
<br />

```python
lst = []
for n in range(3):
    lst.append(int(input("Enter number : ")))
print(f"max is : {max(lst)}")
print(f"min is : {min(lst)}")
print(f"sum is : {sum(lst)}")
```
<br />

---

**`31`**. Write a program that takes a six-digit number as input and outputs the largest digit within the number.
<br />

```python
n = [int(i) for i in input("Enter number : ")] 
print(max(n))
```
<br />

---

**`32`**. Write a program that takes 10 numbers as input and displays the count of zero, positive, and negative numbers.
<br />

```python
zero = 0
positive = 0
negative = 0

try:
    for i in range(10):
        n = int(input("Enter number : "))
        if n == 0:
            zero += 1
        elif n > 0:
            positive += 1
        elif n < 0:
            negative += 1
    print(f"zero : {zero} - positive : {positive} - negative : {negative}")
except ValueError as error:
    print(error)
```
<br />

---

**`33`**. Write a program that takes the radius of a circle as input and displays its circumference, area, and diameter.
<br />

```python
radius = eval(input("Enter The Radius of The Circle : "))  # Radius
area = ((radius**2)*3.14) # Area
circumference = ((3.14*2)*radius)  # Circumference
diameter = radius*2 # Diameter
print(f"area is : {area}\ncircumference is : {circumference}\n\
diameter is : {diameter}")
```
<br />

---

**`34`**. Write a program that takes two numbers as input, performs the four operations (addition, subtraction, multiplication, and division) on them, and displays the results.
<br />

```python
num1 = int(input("Enter First Number : "))
num2 = int(input("Enter Second Number : "))
print(f"addition is : {num1 + num2}\ndivition is : {num1 // num2}\n\
multiple is : {num1 * num2}\nexponet is : {num1 - num2}")
```
<br />

---

**`35`**. Write a program that takes three numbers as input, calculates the sum of the odd numbers, and displays the result.
<br />

```python
odd_number = 0

try:
    for _ in range(3):
        x = int(input("Enter number : "))
        if x % 2 != 0:
            odd_number += x
    if odd_number != 0:
        print(f"odd number : {odd_number}")
    elif odd_number == 0:
        print("No odd numbers")
except ValueError as error:
    print(error)
```
<br />

---

**`36`**. Write a function that takes an integer `n` as input and returns the sum of the numbers from 1 to `n`.
<br />

```python
def sum_of_numbers():
	n = int(input("Enter Number : "))
	return sum(range(1, n + 1))

print(sum_of_numbers())
```
<br />

---

**`37`**. Write a program that takes the two parallel sides and the height of a trapezoid as input and calculates its area.
<br />

```python
def Trapezoid(a, b , h):
    return (((a+b)/2)*h)
a = float(input("Enter The Big Rule : "))
b = float(input("Enter The Small Rule : "))
h = float(input("Enter The Height : "))
print(Trapezoid(a, b, h))
```
<br />

---

**`38`**. Write a program that takes a number as input, calculates the sum of its tens and hundreds digits, and displays the result.
<br />

```python
sum = 0
n = [int(i) for i in input("Enter Yor Number : ")]
n.pop()
sum += n.pop()
sum += n.pop()
print(sum)
```
<br />

---

**`39`**. Write a program that takes a multi-digit number as input and outputs its reverse.
<br />

```python
#step 1
n = input("Enter Number : ")
# print(type(userNumber))
print(n[::-1])

#step 2
n_list = [int(i) for i in input("Enter Number : ")]
# print(type(userNumber))
n_list.reverse()
print(n_list)
```
<br />

---

**`40`**. Write a program that takes two numbers, `x` and `y`, as input and swaps their values.
<br />

```python
# Swapping variables.
x = int(input("Enter x : "))
y = int(input("Enter y : "))
x, y = y, x  
print(f"x : {x} and y : {y}")

# Swapping values using a temporary variable.
x = int(input("Enter x : "))
y = int(input("Enter y : "))
temp = x 
x = y
y = temp
print(f"x : {x} and y : {y}")

# Swapping values using addition and subtraction operations.
x = int(input("x : "))
y = int(input("y : "))
x = x + y   
y = x - y
x = x - y
print(f"x : {x} and y : {y}")

# Swapping values using bitwise XOR operator.
x = int(input("Enter x : "))
y = int(input("Enter y : "))
x = x^y   
y = x^y
x = x^y
print(f"x : {x} and y: {y}")
```
<br />

---

**`41`**. Write a program that displays the numbers between two given numbers.
<br />

```python
x = int(input("Enter First Number : "))
y = int(input("Enter Second Number : "))

print([i for i in range(x+1, y)])
```
<br />

---

**`42`**. Write a program that outputs the two-digit numbers between 10 and 100 where the first and second digits are equal.
<br />

```python
# step 1
for i in range(10, 100):
    if str(i)[0] == str(i)[1]:
        print(i, end = '  ')

# step 2
n = [str(i) for i in range(10, 100)]
for i in n:
    if i[0] == i[1]:
        print(int(i), end = '  ')
```
<br />

---

**`43`**. Write a program that takes four numbers as input and displays the smallest one.
<br />

```python
num_list = []
for i in range(1, 5):
    n = int(input("Enter Numbers : "))
    num_list.append(n)
print("min is : ", min(num_list))
```
<br />

---

**`44`**. Write a program that takes 4 numbers and displays the first even number among them.
<br />

```python
positive_numbers = [int(input("enter number : ")) for i in range(4)]
for i in positive_numbers:
    if i % 2 == 0:
        print(i)
        break
    else:
        continue
```
<br />

---