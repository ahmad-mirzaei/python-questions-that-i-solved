
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

<a id="go-to-the-question-list"></a>

## ✍️ I have categorized the questions so that you have better access to both the questions and the index.
| `1 - 50` | `55 - 105` | `110 - 160` |  |  |  |  |  |  |  |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| [1](#1) | [55](#55) | [110](#110) |  |  |  |  |  |  |  |
| [5](#5) | [60](#60) | [115](#115) |  |  |  |  |  |  |  |
| [10](#10) | [65](#65) | [120](#120) |  |  |  |  |  |  |  |
| [15](#15) | [70](#70) | [125](#125) |  |  |  |  |  |  |  |
| [20](#20) | [75](#75) | [130](#130) |  |  |  |  |  |  |  |
| [25](#25) | [80](#80) | [135](#135) |  |  |  |  |  |  |  |
| [30](#30) | [85](#85) | [140](#140) |  |  |  |  |  |  |  |
| [35](#35) | [90](#90) | [145](#145) |  |  |  |  |  |  |  |
| [40](#40) | [95](#95) | [150](#150) |  |  |  |  |  |  |  |
| [45](#45) | [100](#100) | [155](#155) |  |  |  |  |  |  |  |
| [50](#50) | [105](#105) | [160](#160) |  |  |  |  |  |  |  |

---

## ❓ Questions

## <a id="1"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="5"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="10"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="15"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="20"></a>
**`20`**. Write a program that reads a four-digit number. If the product of the first and fourth digits equals the sum of the second and third digits, print `Yes`; otherwise, print `No`.
<br />

```python
number = [int(i) for i in input("Please enter a four-digit number : ")]
print("YES") if number[0] * number[3] == number[1] + number[2] else print("NO")
```
<br />

[list of questions](#go-to-the-question-list)👆

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

## <a id="25"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="30"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="35"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="40"></a>
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

[list of questions](#go-to-the-question-list)👆

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

## <a id="45"></a>
**`45`**. Write a program that receives the length and width of a rectangle from the input and calculates and prints its area and perimeter.
<br />

```python
length = int(input("Enter The Length Of The Rectangle : "))
width = int(input("Enter The Widthh Of The Rectangle : "))
area = length*width
perimeter = ((length+width)*2)
print(f"area is : {area}\nperimeter is : {perimeter}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`46`**. Write a program that takes two numbers. If both of them are divisible by 3 or both are divisible by 7, print "Yes"; otherwise, print "No".
<br />

```python
number_1 = int(input("Enter number : "))
number_2 = int(input("Enter number : "))
if number_1 %3 ==0 and number_2 %3 == 0 or\
number_1 %7 ==0 and number_2 %7 == 0: print("YES")
else: print("NO")
```
<br />

---

**`47`**. Write a program that takes a number. If both its units and tens digits are even, print "Yes"; otherwise, print "No".
<br />

```python
# step 1
pop1 = []
pop2 = []
userNumber = [int(i) for i in input("Enter Number : ")]
for i in userNumber:
    pop1 = userNumber.pop()
    pop2 = userNumber.pop()
    if pop1 %2 == 0 and pop2 %2 == 0: print(pop1,",", pop2, "-> YES")
    else: print(pop1,",", pop2, "-> NO")
 
# step 2
userNumber = int(input("Enter Number : "))
if (userNumber %2 == (userNumber//10)%2): print("YES")
else: print("NO")
```
<br />

---

**`48`**. Write a program that takes two numbers. If both are greater than 20, print "Yes".
<br />

```python
number_1 = int(input("Enter number : "))
number_2 = int(input("Enter number : "))
if number_1 and number_2 > 20: print("YES")
else: print("NO")
```
<br />

---

**`49`**. Write a program that takes two numbers and displays the larger one.
<br />

```python
number_1 = int(input("Enter Number :"))
number_2 = int(input("Enter Number :"))
print(max(number_1, number_2))
```
<br />

---

## <a id="50"></a>
**`50`**. Write a program that takes the number of canned goods and determines how many full cartons of 6 can be made and how many cans will be left without a carton.
<br />

```python
numberOfCans = int(input("Enter The Number Of Cans : "))
print("cartons : ", numberOfCans // 6,"\n\
Remnants : ", numberOfCans%6)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`51`**. Write a program that keeps taking numbers from the user until zero is entered. Then, it calculates and prints the average of the entered numbers (excluding zero from the calculation).
<br />

```python
sumVar = 0
countVar = 0
while True:
    userNumbers = int(input("Enter Numbers : "))
    if userNumbers == 0: break
    else:
        countVar+=1
        sumVar+=userNumbers
print("Avg is :", sumVar//countVar)
```
<br />

--- 

**`52`**. Write a program that takes two numbers and determines how many multiples of 7 exist between them.
<br />

```python
number_1 = int(input("Enter Number : "))
number_2 = int(input("Enter Number : "))
for i in range(number_1, number_2+1):
    if i % 7 == 0:
        print(i, end= ' ')
```
<br />

--- 

**`53`**. Write a program that takes four numbers. If an even number of them are multiples of 3, print "Yes".
<br />

```python
##step -> 1
count = 0
for i in range(1, 5):
    numbers = int(input("Enter Numbers : "))
    if numbers % 3 == 0:
        count+=1
print("YES") if count % 2 ==0 else print("NO")
 
##step -> 2
numbersList = []
appendList = []
for i in range(1, 5):
    numbers = int(input("Enter Numbers : "))
    numbersList.append(numbers)
for i in numbersList:
        if i % 3 == 0:
            appendList.append(i)
            numbersList.remove(i)
for i in appendList:
        for j in numbersList:
            if i and j %3 == 0:
                print(i,"and",j, "-> YES")
                break
```
<br />

---

**`54`**. Write a function that takes a number as an input parameter and prints its reverse as output.
<br />

```python
def reverse_number(n):
    if len(n) == 1:
        return int(n)
    return int(n[::-1])
    
n = input("Enter number : ")
print(reverse_number(n))
```
<br />

---

## <a id="55"></a>
**`55`**. Write a program that takes a number as input and determines whether it is even or odd.
<br />

```python
n = int(input("Enter Your Number : "))
print("number is Even!!") if n %2 == 0 else print("number is Odd!!")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`56`**. Write a program that takes the radius of a circle as input, calculates its area and circumference, and prints the results.
<br />

```python
radius = eval(input("Enter The Radius of The Circle : "))  ## شعاع
area = ((radius**2)*3.14) ## مساحت
circumference = ((3.14*2)*radius)  ## محیط
print(f"area is : {area}\ncircumference is : {circumference}")
```
<br />

---

**`57`**. Write a program that takes a number as input and displays a message if it is not a three-digit number.
<br />

```python
##step -> 1
userNumber = [int(i) for i in input("Enter Number : ")]
print("Yes") if len(userNumber) == 3 else print("NO")

##step -> 2
i = 1
userNumber = int(input("Enter Number : "))
while userNumber >= 10**i:
    i+=1
if i == 3:
    print("YES")
else:
    print("NO")
```
<br />

---

**`58`**. Write a program that takes a list of numbers and displays them in descending order.
<br />

```python
lst = []
user_input = int(input("Specify The Number Of Numbers : "))
for i in range(1, user_input+1):
    n = int(input("Enter Numbers : "))
    lst.append(n)
lst.sort()
lst.reverse()
print(lst)
```
<br />

---

**`59`**. Write a program that keeps taking numbers as input until the user enters -1 and then displays the sum of the entered numbers.
<br />

```python
sum = 0
while True:
    n = int(input("Enter Number : "))
    if n < 0: break
    else: sum += n
print(f"sum is : {sum}")
```
<br />

---

## <a id="60"></a>
**`60`**. Write a program that takes your age in years, months, and days as input and converts it into minutes.
<br />

```python
year = int(input("Enter years : "))
mounths = int(input("Enter mounths : "))
day = int(input("Enter days : "))
yourYears = ((((year*12)*30)*1440))
yourMounths = ((mounths*30)*1440)
yourDays = (day*1440)
print("you have lived","[",yourYears+yourMounths+yourDays,"]","minutes so far!!!")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`61`**. Write a program that asks for the lengths of the three sides of a triangle and determines whether it is an isosceles, equilateral, or scalene triangle.
<br />

```python
sideSet = set()
for i in range(1, 4):
    Side = int(input("Enter The Side 1 : "))
    sideSet.add(Side)
if len(sideSet) == 1:
    print("equilateral triangle")
elif len(sideSet) == 2:
    print("isosceles triangle")
else:
    print("scalene triangle")
```
<br />

---

**`62`**. Write a function that takes two numbers as input and returns their sum as output.
<br />

```python
def Num(a, b):
    return a + b
num1 = int(input("Enter Number : "))
num2 = int(input("Enter Number : "))
print(Num(num1, num2))

##step -> 2
num = lambda a, b: a + b
num1 = int(input("Enter Number : "))
num2 = int(input("Enter Number : "))
print(num(num1, num2))
```
<br />

---

**`63`**. Write a program that takes a number as input in the main function, calculates the largest digit of the number in a separate function, and then displays the result in the main function.
<br />

```python
# step -> 1
def max_number(a): return max(a)
n = [int(i) for i in input("Enter Number : ")]
print(max_number(n))

# step -> 2
max_number = lambda a : max(a)
n = [int(i) for i in input("Enter Number : ")]
print(max_number(n))
```
<br />

---

**`64`**. Write a function that:

1. Takes the grades of five courses for a student.  
2. If the score is between 17 and 20 → "A"  
3. If the score is between 15 and 17 → "B"  
4. If the score is between 12 and 15 → "C"  
5. If the score is 12 or below → "D"  
6. Displays the grade along with the corresponding score in order.
<br />

```python
def get_number():
    for i in range(5):
        n = eval(input("Enter score : "))
        if n in range(17, 21): 
            print(f"{n} ---> (A)")
        elif n in range(15, 18): 
            print(f"{n} ---> (B)")
        elif n in range(12, 16): 
            print(f"{n} ---> (C)")
        elif n in range(0, 12): 
            print(f"{n} ---> (D)")
        else:
            print("Error!!! Enter Number Between 0 - 20")

get_number()
```
<br />

---

## <a id="65"></a>
**`65`**. Ali has a large number of books and wants to pack them in sets of 4.
Write a program that: Takes the number of books as input from the user. Determines how many full packs of 4 books can be made. Calculates how many books will remain unpacked.
<br />

```python
books = int(input("Enter The Number Of Your Books : "))
print(f"packs : {books//4} and left over : {books % 4}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`66`**. Write a program that takes a number as input, calculates its factorial, and prints the result.
<br />

```python
##step -> 1 with while loop
n = eval(input("Enter yor number : "))
i = 1
factorial = 1
while i <= n:
    factorial*=i
    i+=1
    print(factorial)

##step -> 2 with math library
from math import factorial
n = eval(input("Enter yor number : "))
print(factorial(n))
```
<br />

---

**`67`**. Write a program that prints the two-digit multiples of 5.
<br />

```python
for i in range(100):
    if i % 5 == 0:
        print(i, end='  ')
```
<br />

---

**`68`**. Write a program that generates the following output.
```bash
1 2 3 4 5 6 7  
1 2 3 4 5 6  
1 2 3 4 5  
1 2 3 4  
1 2 3  
1 2  
1  
```
<br />

```python
row = 7

for i in range(1, row + 1):
    for j in range(1, row + 1):
        print(j, end = " ")
    print()
    row -= 1
```
<br />

---

**`69`**. Write a program that takes a 5-digit number as input and prints its reverse without using functions like reverse().
<br />

```python
n = input("Enter 5-digit number : ")
print(int(n[::-1]))
```
<br />

---

## <a id="70"></a>
**`70`**. Write a simple calculator that takes two numbers as input and then allows the user to choose one of the operators (`+`, `-`, `//`, `*`) to get the desired result.
<br />

```python
try:
    while True:
        x = eval(input("Enter Number 1 : "))
        choice = input("addition\t [ + ]\nminus\t\t [ - ]\nmultiple\t [ * ]\ndivision\t [ // ]\n")
        y = eval(input("Enter Number 2 : "))
        
        if choice == "+":
            print(x + y)
        elif choice == "-":
            print(x - y)
        elif choice == "*":
            print(x * y)
        elif choice == "//":
            print(x // y)
        to_continue = input("Do you want to continue ? (y/n) : ")
        if to_continue == "n":
            break
except ZeroDivisionError as error:
    print(error)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`71`**. Write a program that prints the following pattern:
<br />

```bash
1  
1 2  
1 2 3 4  
1 2 3 4 5  
1 2 3 4 5 6  
1 2 3 4 5  
1 2 3 4  
1 2 3  
1 2  
1 
```
<br />

```python
row = 7
for i in range(1, 7):
    for j in range(1, i+1):
        print(j, end=' ')
    print()
for k in range(1, 7):
    row-=1
    for h in range(1, row):
        print(h, end=' ')
    print()
```
<br />

---

**`72`**. Write a program that takes a string as input and removes all spaces from it.
<br />

```python
join_string = ''.join(input("Enter Your String : ").split())
print(join_string)
```
<br />

---

**`73`**. Write a program that takes a string as input, checks for vowels (`a, e, i, o, u`), prints them if found, and also displays their frequency.
<br />

```python
counter = dict()
letters = ['A', 'a', 'I', 'i', 'U', 'u', 'E', 'e', 'O', 'o ']
user_input = [i for i in input("Enter Your Strings : ")]
for i in letters:
    for j in user_input:
        if i == j:
            if i in counter:
                counter[i]+=1
            else:
                counter[i]=1
print(counter)
```
<br />

---

**`74`**. Write a program that receives a natural number NN and determines how many of its digits are even, how many are odd, and how many are zero.
<br />

```python
user_number = [int(i) for i in input("Enter Number : ")]
even = [even for even in user_number if even % 2 == 0]
odd = [odd for odd in user_number if odd % 2 != 0]
zero = [zero for zero in user_number if zero == 0]
print(f"even {len(even)} : {even}\nodd {len(odd)} : {odd}\nzero {len(zero)} : {zero}")
```
<br />

---

## <a id="75"></a>
**`75`**. Write a program using a single for loop that outputs even numbers from 30 to 1 in descending order and odd numbers from 1 to 30 in ascending order.
<br />

```python
even_list = []
odd_list = []

for i in range(1, 30 + 1):
    even_list.append(i) if i % 2 == 0 else odd_list.append(i)

odd_list.reverse()

print(f"even numbers : {even_list}")
print(f"odd numbers : {odd_list}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`76`**. Write a program that takes two numbers as input and raises the first number to the power of the second number.
<br />

```python
# step 1
x = int(input("Enter first number : "))
y = int(input("Enter second number : "))

z = x ** y
print(z)

# step 2
x = int(input("Enter first number : "))
y = int(input("Enter second number : "))

z = pow(x, y)
print(z)

```
<br />

---

**`77`**. Write a program that takes a two-digit number as input and:  
1. First, outputs all numbers before that number.  
2. Then, outputs all two-digit odd numbers before that number and all two-digit even numbers before that number separately.
<br />

```python
def get_number(n):
    for i in range(1, n):
        print(i, end = " ")
    print()
    
    for i in range(11, n):
        if i % 2 != 0:
            print(i, end = " ")
    print()
    
    for i in range(10, n):
        if i % 2 == 0:
            print(i, end = " ")

get_number(int(input("Enter 2-digit nymber : ")))
```
<br />

---

**`78`**. Write a program that takes a string as input and checks if it is a palindrome.  
(A palindrome is a word or phrase that reads the same backward as forward, such as "level.")
<br />

```python
st = input("please enter a string : ")
if st == st[::-1]:
    print("palindrome")
else:
    print("not palindrome")
```
<br />

---

**`79`**. Write a program that takes a temperature in Fahrenheit or Celsius and converts it accordingly.  
First, the program should ask the user whether they want to convert Fahrenheit to Celsius or Celsius to Fahrenheit. After the user makes a selection, the conversion should be performed.
<br />

```python
print("fahrenheit or centigrade --> f/c")
userInput = input()
if userInput == "f":
    f = int(input("Please Enter fahrenheit weather :"))
    print((f-32)/1.8)
elif userInput == "c":
    c = int(input("Please Enter centigrade weather :"))
    print(c*1.8+32)
```
<br />

---

## <a id="80"></a>
**`80`**. Ali wants to write a program for a university that sorts students' names alphabetically.  
The program will be used for attendance lists in classes with ten students.  
How would you write the program if you were in his place?
<br />

```python
name_list = []
for i in range(1, 11):
    names = input("Enter names : ")
    name_list.append(names)
sortList = name_list.sort()
for i in name_list:
    print(i, end='  --  ')
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`81`**. Write a program that defines a function accepting a variable number of inputs; the inputs must be tuples and contain strings. The function should then check for palindromic strings and print those that are palindromes.
<br />

```python
def palindrome(*tu):
    for i in tu:
        if i == i[::-1]:
            print(f"palindrome worlds : {i}")
            print(type(tu))
palindrome("level", "darsman", "madam", "python", "kayak")
```
<br />

---

**`82`**. Write a program that takes a variable number of numerical inputs and then prints them in sorted order.
<br />

```python
# # step 1
def sort_numbers():
    numbers = []
    for num in range(5):
        numbers.append(int((input("Enter Your Number : "))))
    return sorted(numbers)
print(sort_numbers())

# # step 2
def sort_numbers(*n):
    n = list(n)
    n = sorted(n)
    n = tuple(n)
    return n
print(sort_numbers(2, 5, 7, 9, 10, 44, 3, 22))

# # step 3
print(sorted([eval(input(f"{x}. Enter number : ")) for x in range(1, 5+1)]))
```
<br />

---

**`83`**. Write a program that converts a two-dimensional array into a one-dimensional array.
<br />

```python
l1 = [[1, 2, 3], [5, 6, 7]]
l2 = []
for i in l1:
    for j in i:
        l2.append(j)
print(l2)
```
<br />

---

**`84`**.  Write a program that takes the number of sides as input and prints the sum of its interior angles.
**Input:**  
`12`  
**Output:**  
`1800`  

**Input:**  
`4`  
**Output:**  
`360`
<br />

```python
number_of_sides = int(input("Enter the number of sides : "))
internal_sides = 180 * (number_of_sides - 2)
print(internal_sides)
```
<br />

---

## <a id="85"></a>
**`85`**. Write a program that takes a list of numbers, checks all possible triplets, and prints the ones whose sum equals 30.
<br />

```python
import itertools
l1 = []
user_input = int(input("How many numbers does your list have? "))
for i in range(user_input):
    l1.append(int(input("Enter Your Numbers : ")))
l2 = list(itertools.combinations(l1, 3))
for i in l2:
        if sum(i) == 30:
            print(f"{i} : sum : {sum(i)}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`86`**. Write a program that prints all two-digit odd numbers in descending order.
<br />

```python
# step 1
i = 101
while i >= 2:
    i-=2
    print(i, end=' ')

# step 2
for i in range(99, 10, -2):
    print(i, end = " ")
```
<br />

---

**`87`**. Write a program that prints all two-digit odd numbers in descending order. If both digits of a number are the same and odd, store them in a list instead of printing, and display the list at the end.
<br />

```python
lst = []
for i in range(99, 10, -2):
    if str(i)[0] == str(i)[1]:
        lst.append(i)
        continue
    print(i, end = " ")
print()
print(lst)
```
<br />

---

**`88`**. Write a program that takes a number as input and prints that many stars (`*`).
<br />

```python
star_number = int(input("Please Enter Yur Number : "))
print(star_number * "* ")
```
<br />

---

**`89`**. Write a program that:  

- Takes an unspecified number of integer or floating-point inputs, each on a separate line.  
- Continues taking inputs until the word `"Done"` is entered.  
- Outputs four lines displaying, in order:  
  1. The sum of the entered numbers.  
  2. The maximum number.  
  3. The minimum number.  
  4. The average of the numbers.
<br />

```python
userInput = []
numbers = []
while True:
    # Take input and append it to userInput variable
    userInput.append(input(("Enter Your Number : ")))
    if "Done" in userInput:
        # Pop() the last input from the variable before breaking
        userInput.pop()
        break
# Convert strings to numbers with the eval() function
for i in userInput:
    numbers.append(eval(i))
print(f"sum is : {sum(numbers)}")
print(f"max is : {max(numbers)}")
print(f"min is : {min(numbers)}")
print(f"avrage is : {sum(numbers)/len(numbers)}")
```
<br />

---

## <a id="90"></a>
**`90`**. Write a program that prints the three-digit multiples of both 3 and 5.
<br />

```python
three = [i for i in range(1000) if i % 3 == 0]
five = [i for i in range(1000) if i % 5 == 0]
print(f"For Three : {three}")
print(f"For Five : {five}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`91`**. Write a program that takes two numbers from the user and performs addition, subtraction, multiplication, and division on them.
<br />

```python
def calculator(x, y):
	print(f"Total is : {x + y}")
	print(f"Subtraction is : {x - y}")
	print(f"Multiplication is : {x * y}")
	print(f"Division is : {x / y}")
x = eval(input("Enter x : "))
y = eval(input("Enter y : "))
calculator(x, y)
```
<br />

---

**`92`**. Write a program that takes a string expression like `45+23` as input and performs the calculation based on the operator in the expression (operators include `+`, `-`, `*`, `/`).
<br />

```python
num = eval(input("Enter Number --> for example --> 23 + 45 : "))
print(num)
```
<br />

---

**`93`**. Write a program that takes two numbers as input and prints the Fibonacci sequence from the first number to the second number.
<br />

```python
count = 2
x = int(input("from the number : "))
y = int(input("up to the number : "))
i = 0
j = 1
print(i)
print(j)
for num in range(x, y - 1):
    fibo = i + j
    print(fibo)
    i = j
    j = fibo
    count += 1
```
<br />

---

**`94`**. Write a program that first takes the number of courses a student has, then receives the credit hours and grade for each course, and finally calculates the student's GPA.
<br />

```python
numberOfLessons = int(input("Enter the number of lessons : "))
nameOfCourse = []
totalScores = 0
theUnit = 0
for i in range(numberOfLessons):
    nameOfCourse.append(input("Enter Name Of Course : "))
    score = float(input("Enter The Score : "))
    unit = int(input("Enter The Unit : "))
    totalScores += (score * unit)
    theUnit += unit
print("Your Average Is : ",totalScores / theUnit)
```
<br />

---

## <a id="95"></a>
**`95`**. Write a program that takes the user's birth year and the current year as input and calculates how many years, months, days, hours, minutes, and seconds they have lived.
<br />

```python
from datetime import date
yearOfBirth = int(input("In What Year Were You Born? "))
toDay = date.today()
yourAgeInYears = toDay.year - yearOfBirth
yourAgeInMonths = yourAgeInYears * 12
yourAgeInWeeks = ((yourAgeInMonths * 30) // 7)
yourAgeInDay = yourAgeInMonths * 30
yourAgeInHours = yourAgeInDay * 24
yourAgeInMinutes = yourAgeInHours * 60
yourAgeInSeconds = yourAgeInMinutes * 60
print(f"your Age In Years {yourAgeInYears}")
print(f"your Age In Months {yourAgeInMonths}")
print(f"your Age In Weeks {yourAgeInWeeks}")
print(f"your Age In Day {yourAgeInDay}")
print(f"your Age In Hours {yourAgeInHours}")
print(f"your age in minutes {yourAgeInMinutes}")
print(f"your Age In Seconds {yourAgeInSeconds}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`96`**. Maryam is an economical girl who wants to calculate the cost of her SMS messages.

According to the tariff of the operator she uses:

    The base cost of each SMS is 100 Rials.
    For every 24 English characters, an additional 274 Rials is added.
    If the character count for an additional charge is less than 24, the cost is waived (rounded down).

Input:
A text message that Maryam wants to send.

Output:
The final cost of the SMS in Tomans, displayed as a decimal number.

Example:

Input:

slm bbkhshid shoma?

Output:

10.0
<br />

```python
from math import floor
initialCost = 100
costPerSubsequentCharacters = 274
sms = input('Enter Your Massage : ')
smsList = list(sms)
chrList = []

for chr in smsList:
    if chr.isalpha():
        chrList.append(chr)

smsCost = (100 + floor(len(chrList) // 24) * 274) // 10
print(f"The Characters Of This Message : {len(chrList)}")
print(f"The Final Cost Is : {smsCost} Tooman")
```
<br />

---

**`97`**. Define a class for the geometric shape of a rectangle, with two methods to calculate its perimeter and area.
<br />

```python
class Rectangle:
    def __init__(self, length, width):
        self.lemgth = length
        self.width = width
    
    def parimeter(self):
        return 2 * (self.lemgth + self.width)
    
    def area(self):
        return self.lemgth * self.width

length = int(input("enter length : "))
width = int(input("enter width : "))

rect = Rectangle(length, width)

print(f"parimeter : {rect.parimeter()}")
print(f"area : {rect.area()}")
```
<br />

---

**`98`**. Write a program that takes 5 grades of a student as input, calculates their average, and prints it. Additionally, if the average is greater than 17, print `Excellent`; if it is between 15 and 17, print `Good`; if it is between 10 and 15, print `Poor`; and if it is less than 10, print `Very Poor`.
<br />

```python
num_list = [int(input(f"Enter grade {x} : ")) for x in range(1, 6)]

avg = sum(num_list) / len(num_list)

print(f"avg is : {avg}")

if 17 < avg <= 20:   
    print('Ecellent')
elif 15 < avg <= 17:
    print('Medium')
elif 10 < avg <= 15:
    print('Bad')    
elif avg <= 10:
    print('Very bad') 
```
<br />

---

**`99`**. Write a function that is polymorphic and can accept up to 3 arguments.
<br />

```python
def func_name(x = 0, y = 0, z = 0):
    # if statements
        return x + y + z

print(func_name(2, 4, 6))
print(func_name(2, 4))
print(func_name(2))
print(func_name())
```
<br />

---

## <a id="100"></a>
**`100`**. تابعی که نمرات ده دانش آموز را بگیرد و میانگین را محاسبه کند و کوچکترین و بزرگترین را چاپ کند.
<br />

```python
def student_avg(n):
    print(sum(n) / len(n))
    print(f"Max is : {max(n)} & Min is : {min(n)}")
score = []
for num in range(10):
    score.append(int(input("Enter Score : ")))
student_avg(score)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`101`**. Write a program that takes the grades of ten students and indicates which ones passed and which ones failed. The passing grade is above 10.
<br />

```python
studentInfo = {}
for i in range(10):
	name =  input("Enter the student's name : ")
	score = int(input("Enter the student's Score : "))
	studentInfo[name] = score
acceptedStudents = [x for x in studentInfo if studentInfo[x] >= 10]
rejectedStudents = [x for x in studentInfo if studentInfo[x] < 10]
print(f"Accepted students : {acceptedStudents}")
print(f"Rejected Students : {rejectedStudents}")
```
<br />

---

**`102`**. Write a program that reads a three-digit number from the input and prints twice its reverse in the output. Ensure that the input is definitely a three-digit number, and the output should be the number multiplied by 2.
<br />

```python
number = input("Enter a three-digit number : ")
if int(number) >= 100:
    reverseNumber = int(number[::-1])
    print(f"Reverse Number is : {reverseNumber}")
    print(f"Reverse Number * 2 = {reverseNumber * 2}")
else:
	print(f"Your Number is : {number}")
	print("Please Enter Three-Digit Number And Try Again!")
```
<br />

---

**`103`**. Write a program that takes a number from the user, calculates the count of its digits, and then calculates the sum of its digits.
<br />

```python
n = input("Enter number : ")
list_number = list(n)
print(f"number of digits : {len(list_number)}")
sum_num = 0
for i in list_number:
	sum_num += int(i)
print(f"Sum is : {sum_num}")
```
<br />

---

**`104`**. Write a program that produces the following output.
```bash
A

AB

ABC

ABCD

ABCDE

ABCDEF
```
<br />

```python
# step 1
n = int(input("How many times should i move? "))
i = 1
temp = ""
ch = chr(65)
while i <= n:
	temp += ch
	print(temp, "\n")
	ch = chr(65 + i)
	i += 1

# step 2
from string import ascii_uppercase

n = int(input("How many times should i move? "))

for i in range(1, n + 1):
    for j in range(i):
        print(ascii_uppercase[j], end="")
    print("\n")
```
<br />

---

## <a id="105"></a>
**`105`**. Write a program that takes the birth date in the Gregorian (Western) calendar as input and displays the user's age in the output.
<br />

```python
from datetime import date

your_birth = int(input("Enter the year of birth : For example : 1999 --->   "))
date_time_now = date.today()
i = 0
while your_birth < date_time_now.year:
    your_birth += 1
    i += 1
print(f"your age : {i}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`106`**. Write a program that, upon receiving a positive odd number, prints the corresponding alphabet triangle.
<br />

```python
input_number = int(input('Enter Num : '))
if input_number % 2 == 1 and input_number > 0:
    for i in range(input_number):
        for j in range(i + 1):
            print(chr(j + 97), end = " ")
        print()
else:
	print(f"Enter an odd number or a number greater than zero!!! And Try Again...")
```
<br />

---

**`107`**. In 2013, the first year after 1987 that does not have repeating digits. You are asked to write a program that takes a year as input from the user and prints the first year without repeating digits after that year.
<br />

```python
input_year = int(input(" Enter Year : "))
listOfInputYear = list(str(input_year))
for i in range(input_year):
    input_year += 1
    if len(set(str(input_year))) == 4:
        print(input_year)
        break
```
<br />

---

**`108`**. Write a program that outputs the number of days between two dates.
Example:
The days between the dates `2025-06-01` and `2025-06-09` are equal to 8 days.
<br />

```python
from datetime import datetime

# example --> 2025-06-01 - 2025-06-09

date_format = '%Y-%m-%d'
first_day = datetime.strptime("2025-06-09", date_format)
second_day = datetime.strptime("2025-06-01", date_format)
print (f"days : {(first_day - second_day).days}")
```
<br />

---

**`109`**. Write a program that combines the elements of the two lists below into separate tuples, and the condition for output is that only values greater than 0.9 are printed.
<br />

```python
actions = ["write", "read", "walk", "sing", "laugh", "talk", "dance", "eat", "Whistling", "clap"]
values = [1.65227288, 1.33215619, -0.52259578, -0.67266119, 1.42021427, -0.4017421, 0.9653853, 1.09278474, 1.11503941, -0.44975633]

zip_list = zip(actions, values)
for i in zip_list:
    if i[1] > 0.9:
        print(i, end = " ")
```
<br />

---

## <a id="110"></a>
**`110`**. Write a program that takes 10 numbers from the user and finds the smallest and largest among them.
<br />

```python
num_list = []
n = int(input("How many numbers should I get? "))
for num in range(1, n + 1):
    num_list.append(int(input(f"{num}. Enter numbers : ")))
print(f"Max is : {max(num_list)}\nMin is : {min(num_list)}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`111`**. Write a program that prints the first 10 multiples of 7 that are greater than 200.
<br />

```python
# step 1
i = 200
counter = 1
while counter <= 10:
    i += 1
    if i % 7 == 0:
        print(i, end = " ")
        counter += 1

# step 2
counter = 0
for i in range(200, 300):
    if counter == 10:
        break
    else:
        if i % 7 == 0:
            print(i, end = " ")
            counter += 1
```
<br />

---

**`112`**. Write a program that takes an integer n as input and prints a right-angled triangle of stars in the output, where n is the number of rows in the triangle. The direction of the triangle should be like this: 📐.
<br />

```python
# step 1
n = int(input("Entr row : "))
for row in range(n + 1):
    for col in range(row):
        print("*", end = " ")
    print()

# step 2
n = int(input("Entr row : "))
for row in range(n + 1):
        print(row * "* ")
```
<br />

---

**`113`**. Write a program that takes 10 numbers, stores them in a list, and prints them from end to beginning.
<br />

```python
# step 1
def reverse_list():
    lst = []
    for num in range(1, 11):
        lst.append(int(input(f"Enter numbers {num} : ")))
    return str(lst[::-1])

print(reverse_list())

# step 2
numList = []
i = 0
while i < 10:
	n = int(input("Enter number : "))
	numList.append(n)
	i += 1

numList.reverse()
print(numList)
```
<br />

---

**`114`**. برنامه ای بنویسید که از ورودی انواع نوع داده ای را بگیرد و در یک لیست ذخیره کند و سپس تمامی انواع داده ای رشته ای را به خروجی ببرد.
<br />

```python
lst = []
for st in range(10):
    n = input("Enter input : ")
    if n.isalpha(): 
        lst.append(n)
    else:
        continue
print(f"Your list : {lst}")
```
<br />

---

## <a id="115"></a>
**`115`**. Write a program that takes several positive numbers from the user and calculates their average (using for and break). That is, when a negative number is entered, the loop should exit.
<br />

```python
counter = 0
numbers = 0
sumNum = 0
for i in range(1000):
	numbers = int(input("Enter number : "))
	if numbers < 0:
		break
	sumNum += numbers
	counter += 1
	
print(f"avrage : {sumNum / counter}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`116`**. Panjali is one of the best programmers in a company in Miami, USA, and is about to write the following program for her friend Alex, who has recently started programming classes. The program is as follows:
There are two lists of integers, each with 10 elements, where each list contains both duplicate and non-duplicate numbers:
Now, imagine you are Panjali and want to use a loop or loops to output the duplicate elements of both lists into the first list and the non-duplicate elements into the second list, sorted in order.
<br />

```python
list_1 = [1,2,3,4,4,5,6,1,12,34]
list_2 = [3,5,4,7,7,9,12,9,6,10]

temp_1 = list_1 + list_2
print(sorted(set(temp_1)))

temp_2 = []
for i in list_1:
    if i in list_2:
        temp_2.append(i) 
print(sorted(set(temp_2)))
```
<br />

---

**`117`**. Write a program that takes a list of any size from the user, finds the largest and smallest elements, removes them from the list, and calculates the average of the remaining numbers (using a function).
<br />

```python
def del_min_max(n):
    numList = []
    for num in range(1, n + 1):
        numList.append(int(input(f"{num}. Enter numbers : ")))
    print(f"list before del min & max --> {numList}")
    print(f"Max is : {max(numList)}\tMin is : {min(numList)}")
    numList.remove(max(numList))
    numList.remove(min(numList))
    print(f"list after del min & max --> {numList}")
    print(f"List Avg is : {sum(numList) / len(numList)}")

n = int(input("How many? "))
del_min_max(n)
```
<br />

---

**`118`**. Write a program that takes a two-digit number as input, doubles it, and then displays its reverse in the output.
<br />

```python
number = int(input("Entr number : "))
print(f"mul : {number} * 2 = {number * 2}\nReverse number : {str(number * 2)[::-1]}")
```
<br />

---

**`119`**. Write a program that takes a three-digit number as input. If the most significant digit and the least significant digit are equal, print the number itself; otherwise, print the reverse of the number.
<br />

```python
try:
    number = int(input("Enter a three-digit number : "))
except ValueError as error:
    print(f"ValueError : {error}")
else:
    if str(number)[0] == str(number)[2]:
        print(f"number : {number}")
    else:
        print(f"{number} ---> {str(number)[::-1]}")
```
<br />

---

## <a id="120"></a>
**`120`**. Write a program that outputs the second list based on the index numbers provided in the first list.
```bash
list_1 = [3, 5, 6, 8, 9, 12]
list_2 = ["a", "b", "c", "p", "e", "y", "t", "", "h", "o", "w", "i", "n", "l"]
```
<br />

```python
# # step 1
list_1 = [3 ,5 , 6, 8, 9, 12]
list_2 = ["a", "b", "c", "p", "e", "y", "t", "", "h", "o", "w", "i", "n", "l"]
indexList = []
for i in list_1:
    indexList.append(list_2[i])
print("".join(indexList))

# # step 2
def index_list():
    list_1 = [3 ,5 , 6, 8, 9, 12]
    list_2 = ["a", "b", "c", "p", "e", "y", "t", "", "h", "o", "w", "i", "n", "l"]
    indexList = []
    for i in list_1:
        indexList.append(list_2[i])
    return "".join(indexList)

print(index_list())
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`121`**. Write a function that takes a list and a number as input, adds the number to each item in the list that is a number, and then displays the list.
<br />

```python
def sum_list(n):
    numList = []
    number = int(input("How many do you want? "))
    for i in range(1, number + 1):
        numList.append(input(f"{i}. Enter number : "))
    for j in numList:
        if j.isdigit():
            print(int(j) + n, end = " ")

sum_list(20)
```
<br />

---

**`122`**. Write a program that takes a number from the user and determines whether the number is a power of 3 or not.
<br />

```python
n = int(input("Enter number : "))
for i in range(1, n + 1):
    if (i**3) == n:
        print("Yes, This number is a power of 3")
        print(f"{n} is : {i} ** 3 ")
        break
else:
    print("This number is (NOT) a power of 3")
```
<br />

---

**`123`**. Write a program that takes several numbers from the user and calculates their sum and average until the user enters 'no'.
<br />

```python
numList = []
while True:
    num = input("Enter number : ")
    if num == "no":
        break
    numList.append(int(num))
print(f"Sum : {sum(numList)}")
print(f"Avg : {sum(numList) / len(numList)}")
```
<br />

---

**`124`**. Write the following algorithm in Python:

1. Take the username from the user.
2. Take the password from the user.
3. If the username is equal to 'teacher' and the password is equal to '12345', print 'welcome to teacher panel'.
4. Otherwise, if the username is equal to 'students' and the password is equal to '12345', print 'welcome to students panel'.
5. Otherwise, print 'username or password is incorrect'.
<br />

```python
userName = input("Enter user name : ")
try: 
    password = int(input("Enter password : "))
    if userName == "teacher" and password == 12345:
        print("welcome to teacher panel...")
    elif userName == "student" and password == 12345:
        print("welcome to students panel...")
    else:
        print("Username or password is wrong...")
except ValueError as error:
    print(error)
```
<br />

---

## <a id="125"></a>
**`125`**. Write two programs: in the first program, take the user's birth year and output their age, and in the second program, take the birth year in the Jalali calendar and display the age in the output.
<br />

```python
# Age calculation based on Gregorian calendar
import datetime
 
birthDay = int(input("Enter your year of birth : "))
today = datetime.datetime.now()
age = today.year - birthDay
print(f"today is : {today.year} and your {age} years old")
 
# Age Calculation based on Jalali calendar
import jdatetime
 
birthDay = int(input("Enter your year of birth : "))
today = jdatetime.datetime.now()
age = today.year - birthDay
print(f"today is : {today.year} and your {age} years old")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`126`**. Write a program that reads a number from the input and prints the largest digit in it.
<br />

```python
# step 1
n = input("Enter number : ")
if n.isdigit():
    print(max(list(n)))
else:
    print("enter a number and try again...")

# step 2
n = input('Enter Number : ')
print(max(list(n)))
```
<br />

---

**`127`**. Write a program that performs the multiplication of two numbers without using the multiplication operator.
<br />

```python
first_number = eval(input("Enter number : "))
secend_number = eval(input("Enter number : "))

i = 0
mul = 0
while i < secend_number:
    mul += first_number
    i += 1
print(mul)
```
<br />

---

**`128`**. Write a program that outputs the two smallest elements of a list.
<br />

```python
lst = [1, 8, 12, 5, 4, 76, 28, 5, 6, 1, 7,  9, 8]
minLst = []
setLst = set(lst)
for i in range(2):
    minLst.append(min(setLst))
    setLst.remove(min(setLst))
print(f"Two small list elements : {minLst}")
```
<br />

---

**`129`**. Write a program that finds all numbers divisible by 7 but not multiples of 5. The resulting numbers should be printed in a single line, separated by commas.
Additional details:
The range of numbers should be between 100 and 200.
<br />

```python
# step 1
lst = []
for i in range(100, 201):
    if (i%7==0) and (i%5!=0):
        lst.append(str(i))
 
print(",".join(lst))

# step 2
print([x for x in range(100,200) if x%7==0 and x%5!=0])
```
<br />

---

## <a id="130"></a>
**`130`**. Company X, with 73 employees, plans to increase the salary of its married employees, who all receive the same salary, by 5%.
Calculate the number of married employees and output it.
Calculate how much capital needs to be injected into the company's treasury for the salary increase of married employees.
Additional notes:
a. Single and married employees in this question are represented by odd and even numbers, respectively.
b. The base salary for married employees is 10 million Tomans
<br />

```python
def numbers_of_married(company):
    married = 0
    for person in range(1, company+1):
        if (person%2==0):
            married += 1
    return married

def salary_calculation(married):
    companyTreasury = ((married*10000000) * 0.05)
    return companyTreasury

company = 73
print(f"The number of married people working in this company : {numbers_of_married(company)}")
print(f"The amount that should be considered for the treasury of the company : {salary_calculation(numbers_of_married(company))}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`131`**. Write a program that accepts a sequence of comma-separated numbers from the console and creates a list and a tuple containing each number.
Assume the following input is provided to the program:
34,67,55,33,12,98
Then the output should be as follows:
['34', '67', '55', '33', '12', '98']
('34', '67', '55', '33', '12', '98')
<br />

```python
# step 1
tuple_numbers = tuple(eval(input("Enter numbers : ")))
print(tuple_numbers)
list_numbers = list(eval(input("Enter numbers : ")))
print(list_numbers)

# step 2
number = input("Enter values seprate with , : ").split(',')

print(tuple(number))
print(list(number))
```
<br />

---
**`132`**. Write a program that reads a string and, using a function, calculates and prints the sum of the digits present in the string.
<br />

```python
def sum_num():
    sum_of_numbers = 0
    n = input("Enter : ")
    for ch in n:
        if ch.isdigit():
            sum_of_numbers += int(ch)
    print(sum_of_numbers)

sum_num()
```
<br />

---
**`133`**. Write a program that reads a string from the input and displays the count of digits in the string.
<br />

```python
n = input("Enter number : ")
numbers = [int(x) for x in n if x.isdigit()]
print(f"The number is {len(numbers)} digits")
```
<br />

---

**`134`**. If we have a list: [1, 1, 2, 5, 6, 6, 8, 8, 8, 7, 7], and we want to extract the numbers that are repeated exactly twice, what should we do?
<br />

```python
lst = [1,2,3,4,5,6,5,3,1,8,9,9,9]
for i in range(len(lst)+1):
    if lst.count(i) == 2:
        print(f"There are two of this item --> {i}")
```
<br />

---
## <a id="135"></a>
**`135`**. Write a program that takes an integer with an unspecified number of digits from the user and prints each digit as many times as its value.
<br />

```python
def print_numbers():
    n = list(input("Enter number : "))
    for i in n:
        print(f"({i}). ", end = "")
        for j in range(1, int(i)+1):
            print(j, end = " ")
        print()

print_numbers()
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`136`**. Write a program that takes a number as input and generates a dictionary within the range of that number, where the dictionary contains {i: i*i}.
Assume the input 8 is provided to the program; then the output should be as follows:

{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}

In your program, include error handling for possible input errors.
<br />

```python
try:
    number = int(input("Enter number : "))
    dic = {i : i*i for i in range(1, number + 1)}
    print(dic)
except ValueError as error:
    print(error)
```
<br />

---
**`137`**. Write a program that takes the number of students in a class as input, receives the GPA of each student as input, calculates the average GPA of the class, and prints it.
<br />

```python
students = int(input("Number of students : "))
avg = 0
for i in range(1, students+1):
    avg += eval(input(f"{i}. Enter Avg : "))
print(f"Avg of the whole class : {avg / students}")
```
<br />

---
**`138`**. Write a program that first creates three dictionaries with initial values as shown below, then combines these three dictionaries into a fourth dictionary, stores it, and prints it.

```python
dic1 = {"ali":34,"mehdi":42,"reza":27}
dic2 = {3:3000,5:12000}
dic3 = {100:True,200:False,500:False}
```
<br />

```python
# step 1
dic1 = {"ali":34,"mehdi":42,"reza":27}
dic2 = {3:3000,5:12000}
dic3 = {100:True,200:False,500:False}

dic4 = dic1 | dic2 | dic3
print(dic4)

# step 2
dic1 = {"ali":34,"mehdi":42,"reza":27}
dic2 = {3:3000,5:12000}
dic3 = {100:True,200:False,500:False}

dic4 = dict()
for dic in (dic1, dic2, dic3):
    dic4.update(dic)

print(dic4)
```
<br />

---
**`139`**. If the students' grades are stored in a dictionary as shown below, write a program that adds one unit (one grade) to each student's grade and prints the resulting dictionary. (Do not add to grades above 19, and preferably use list comprehension).

```python
students = [
    {"ali": [12.5, 16.75 ,19, 8.25, 13.75]},
    {"mehdi": [18.75, 16.5, 19.25, 17.75, 18.25, 20]},
    {"sahar":[17, 13.5, 16, 12.25, 14, 19.25]}
        ]
```
<br />

```python
students = [
    {"ali": [12.5, 16.75 ,19, 8.25, 13.75]},
    {"mehdi": [18.75, 16.5, 19.25, 17.75, 18.25, 20]},
    {"sahar":[17, 13.5, 16, 12.25, 14, 19.25]}
        ]

def print_items(lst):
    for i in lst:
        for j in i:
            for k in j:
                print(k, end = "\t")
        print()

students_items = [[[k + 1 if k < 19 else k for k in j] for j in i.values()] for i in students]

print_items(students_items)
```
<br />

---

## <a id="140"></a>
**`140`**. If the students' information is stored in a list of dictionaries as shown below, display the average GPA and the oldest age.

```python
student = [
    {"id":1,"name":"ali","avg":15.5,"age":23},
    {"id":2 ,"name":"reza","avg":16,"age":19},
    {"id":3 ,"name":"mehdi","avg":19.25,"age":42}
]
```

<br />

```python
student=[
        {"id":1,"name":"ali","avg":15.5,"age":23},
        {"id":2 ,"name":"reza","avg":16,"age":19},
        {"id":3 ,"name":"mehdi","avg":19.25,"age":42}
]

# age & avg
print(f"(age & avg) - Average is : {max([((item['avg'] + item['age']) / 2) for item in student])}")

# max age
print(f"max age is : {max([(item['age']) for item in student])}")

# avg
print(f"avg is : {sum([((item['avg']) / 3) for item in student])}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`141`**. Write a program that takes 5 consecutive numbers as input in one line and then displays them in sorted order in the output.
<br />

```python
# step 1 with function
def sort_numbers():
    numbers = []
    for num in range(5):
        numbers.append(int((input("Enter Your Number : "))))
    return sorted(numbers)
print(sort_numbers())

# step 2 with list comprehension
print(sorted([eval(input(f"{x}. Enter number : ")) for x in range(1, 5+1)]))
```
<br />

---

**`142`**. Write a program that takes the grades of several students from the user. If the entered grade is between 0 and 70, display 'fail'; if the entered grade is between 71 and 80, display 'good'; if the entered grade is between 81 and 90, display 'very good'; and if the entered grade is between 91 and 100, display 'excellent'.
<br />

```python
try:
    students = int(input("number of students : "))
    for i in range(1, students + 1):
        score = float(input(f"{i}. Enter Score : "))
        if score < 0 or score > 100:
            print("The entered number < 0 or number > 100")
        elif score in range(0, 71):
            print("Fail")
        elif score in range(71, 81):
            print("Good")
        elif score in range(81, 91):
            print("Very Good")
        elif score in range(91, 101):
            print("Excellent")
except RuntimeError  as error:
    print(error)
except ValueError as error:
    print(error)
```
<br />

---

**`143`**. Without using modules:

Write a program using a recursive function that can calculate the factorial of a number entered by the user.

Also, write the same program using a Generator Function.
<br />

```python
# step 1
# recursive function
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)
 
print(factorial(4))
 
# step 2
# Generator fanction
def factorial():
    x = 1
    y = 1
    while True:
        x *= y
        yield x
        y += 1
 
fact = factorial()
for i in range(10):
    print(next(fact))
```
<br />

---

**`144`**. Write a program that accepts a sequence of space-separated words as input and prints the words after removing all duplicate words and sorting them alphabetically.

Assume the following input is provided to the program:

`python is the best programming language python is a simple language`
<br />

```python
# step 1
words = "python is the best programming language python is a simple language"
set_words = set(words.split(" "))
print(" ".join(sorted(set_words)))

# step 2
print(" ".join(sorted(set(input("Enter words seprate with , : ").split(' ')))))
```
<br />

---

## <a id="145"></a>
**`145`**. Define a class that has two methods:

`get_string` : to receive a string from input

`print_string` : to print the input string in uppercase letters

<br />

```python
class UpperString:
    def get_string(self):
        return input("Enter a string : ")

    def print_string(self):
        return self.get_string().upper()

string = UpperString()
print(string.print_string())
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`146`**. Write a program that takes a sequence of comma-separated words as input and prints the words in alphabetical order in a comma-separated sequence.

Assume the following input is provided to the program:

`without`, `hello`, `bag`, `world`

Then the output should be as follows:

`bag`, `hello`, `without`, `world`

<br />

```python
words = input("Enter words (for example : a, b, c, d) :  ")
split_space = words.split(" ")
join_split_space = "".join(split_space)
split_comma = join_split_space.split(",")

print(", ".join(sorted(split_comma)))
```
<br />

---

**`147`**. Write a program that outputs all numbers between 2000 and 4001 where `all digits` are even.

The resulting numbers should be printed in a single line, separated by commas.

Sample output:
...2006, 2004, 2002

<br />

```python
# step 1
lst = []
for item in range(2000, 4001):
    if int(str(item)[0]) % 2 == 0 and int(str(item)[1]) % 2 == 0 and \
        int(str(item)[2]) % 2 == 0 and int(str(item)[3]) % 2 == 0:
            lst.append(item)
print(lst)

# step 2
lst = [x for x in range(2000, 4000) if x % 2 == 0]
print(list(
    filter(
        lambda x : str(x)[0] in ('0','2','4','6','8') and str(x)[1] in ('0','2','4','6','8') and 
                    str(x)[2] in ('0','2','4','6','8') and str(x)[3] in ('0','2','4','6','8'), 
                    lst
                    )
    ))
```
<br />

---

**`148`**. Using list comprehension, write a program that takes two digits X and Y as input and generates a two-dimensional array.

Assume the following inputs are given to the program:

3,5

Also, write a function that displays each element of the output array on a new line.
<br />

```python
# for array print
def print_array(array):
    for row in range(1, x + 1):
        print()
        for coll in range(1, y + 1):
            print(coll, end = "\t")
            
x = int(input("Enter x : ")) # 3
y = int(input("Enter y : ")) # 5
#comprehension list
comperhension_array = [[j for j in range(1, y+1)]for i in range(1, x+1)]
#calling function
print_array(comperhension_array)
```
<br />

---

**`149`**. Write a program that takes a set 'a' containing an n-digit number and determines the count of digits (n) using a while loop without any additional elements (we can also use 'function').
<br />

```python
def number_of_digits(n):
    i = 0
    while n != 0:
        n = n // 10
        i += 1
    return i
    
a = 97867564534231

print(f"number of digits : {number_of_digits(a)}")
```
<br />

---

## <a id="150"></a>
**`150`**. Write a program that takes a password as input (containing both letters and numbers). If the input is correct, output it; if the input contains only numbers or only letters, the program should continue until a valid password is entered.
<br />

```python
while True:
    password = input("Enter your password : ")
    if not password.isalpha() and not password.isdigit():
        break
    print("your password is not True. Please try again!")
print(f"password is True : {password}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`151`**. Write a list comprehension that takes a multi-digit number as input and outputs its largest digit.
<br />

```python
print(max([int(i) for i in input("Enter Number : ")]))
```
<br />

---

**`152`**. Write a program that takes a 4-digit number as input, determines how many unique 4-digit numbers can be formed using its digits, and outputs those numbers.
<br />

```python
import itertools

numbers = [int(x) for x in input("Enter 4 digits : ")]

num_list = list(itertools.permutations(numbers, 4))

counter = 0
for i in num_list:
    print(i, end = "\t")
    counter += 1
print(f"counter : {counter}")
```
<br />

---

**`153`**. Write a program that can use map() and filter() to create a list where each element is the square of an even number from the list [1, 2, 3, 4, 5, 6, 7, 8, 9, 10].

Notes:

Use map() to create the list.
Use filter() to filter elements of a list.
You must use filter() inside map().

<br />

```python
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list(map(lambda x: x * x, filter(lambda y: y % 2 == 0, lst))))
```
<br />

---

**`154`**. Write a filter that performs the following operation in just one line:

Output the odd numbers from the range 1 to 20.

<br />

```python
print(list(filter(lambda x: x % 2 !=0, range(1, 21))))
```
<br />

---

## <a id="155"></a>
**`155`**. برنامه ای بنویسید که یه عدد تصادفی از ۱ تا ۳۰ تولید کند؛

سپس در محدوده ی آن عدد لیستی از ارقام تولید کند و ارقام مثبت را به خروجی ببرد.

نکته:

برای حل این سوال از  تابع فیلتر استفاده شود.
<br />

```python
import random
print(list(filter(lambda x: (x%2==0), range(1, random.randint(1, 30) + 1))))
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`156`**. Write a program to generate and print another tuple containing only the even numbers from a given tuple.

Sample Output:
Given Tuple: (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
Second Tuple: (2, 4, 6, 8, 10)

Notes:
The program must be written using the filter() function.

<br />

```python
print(tuple(filter(lambda x: (x%2==0), range(1, int(input("What is the range of the tuple?  "))+ 1))))
```
<br />

---

**`157`**. Write a program that generates a random number from 1 to 20; then creates a tuple within the range of that random number; if the length of the created tuple is even, output the first and second halves of the tuple separately; and if the length of the created tuple is odd, output the first half, second half, and the middle number separately.
<br />

```python
import random
randNum = random.randint(1, 20)

tu = [tuple(x for x in range(1, randNum + 1))]
if len(tu[0]) == 1:
    print(f"number one : {tu[0]}")
elif (len(tu[0])%2==0):
    n = len(tu[0])//2
    print("len is Even...")
    print(f"first half : {tu[0][:n]}")
    print(f"the second half : {tu[0][n:]}")
else:
    n = len(tu[0])//2
    print("len is Odd...")
    print(f"first half : {tu[0][:n]}")
    print(f"middle number : {tu[0][n:n+1]}")
    print(f"the second half : {tu[0][n+1:]}")
```
<br />

---

**`158`**. Define a class with a generator method that can iterate through numbers divisible by 7 within the range of 0 and n.
<br />

```python
class Generator:
    def __init__(self, n):
        self.n = n
    
    def div_to_seven(self):
        i = 1
        while i <= self.n:
            if (i%7==0):
                yield i
            i += 1

gen = Generator(100)
for item in gen.div_to_seven():
    print(item, end = ", ")
```
<br />

---

**`159`**. Write a program that calculates the net balance of a bank account based on transaction records input by the user. The transaction format is shown as follows:

'deposit' means deposit and 'withdraw' means withdrawal.

Assume the following input is provided to the program:

deposit 300

deposit 300

withdraw 200

deposit 100

Then the output should be as follows:

Balance 500

<br />

```python
from Khayyam import  JalaliDate

while True:
    deposit = eval(input("deposit amount : "))
    withdraw = eval(input("withraw amount  :"))
    if withdraw > deposit:
        print("The withdrawal amount is more than the balance...")
        break
    print(f"your account balance {deposit - withdraw}", JalaliDate.today())
    userContinue = input("do you want to continue? (y/n) ")
    if userContinue == "y":
        continue
    elif userContinue == "n":
        break
    else:
        print("error")
```
<br />

---

## <a id="160"></a>
**`160`**. Use list comprehension to square each odd number in a list. The list is entered as a sequence of comma-separated numbers.

Assume the following input is provided to the program:

1,2,3,4,5,6,7,8,9

Then the output should be as follows:

81, 49, 25, 9, 1

<br />

```python
pow_list = [int(i)**2 for i in input("Enter numbers : ").split(",") if int(i)%2!=0]
print(pow_list)
```
<br />

[list of questions](#go-to-the-question-list)👆

---