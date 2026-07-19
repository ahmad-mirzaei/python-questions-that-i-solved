
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
| `1 - 50` | `55 - 105` | `110 - 160` | `165 - 215` |  |  |  |  |  |  |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| [1](#1) | [55](#55) | [110](#110) | [165](#165) |  |  |  |  |  |  |
| [5](#5) | [60](#60) | [115](#115) | [170](#170) |  |  |  |  |  |  |
| [10](#10) | [65](#65) | [120](#120) | [175](#175) |  |  |  |  |  |  |
| [15](#15) | [70](#70) | [125](#125) | [180](#180) |  |  |  |  |  |  |
| [20](#20) | [75](#75) | [130](#130) | [185](#185) |  |  |  |  |  |  |
| [25](#25) | [80](#80) | [135](#135) | [190](#190) |  |  |  |  |  |  |
| [30](#30) | [85](#85) | [140](#140) | [195](#195) |  |  |  |  |  |  |
| [35](#35) | [90](#90) | [145](#145) | [200](#200) |  |  |  |  |  |  |
| [40](#40) | [95](#95) | [150](#150) | [205](#205) |  |  |  |  |  |  |
| [45](#45) | [100](#100) | [155](#155) | [210](#210) |  |  |  |  |  |  |
| [50](#50) | [105](#105) | [160](#160) | [215](#215) |  |  |  |  |  |  |

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

**`161`**. Write a program that takes a sentence as input and counts the number of uppercase and lowercase letters.

Assume the following input is provided to the program:

'pYthOn ProGraMmiNg'

Then the output should be as follows:

Uppercase letters 6
Lowercase letters 11
<br />

```python
sentence = "pYthOn ProGraMmiNg".split(" ")
join_sentence = "".join(sentence)
upper_words = 0
lower_words = 0

for item in join_sentence:
    if item == item.upper():
        upper_words += 1
    else:
        lower_words += 1

print(f"Upper Words : {upper_words}")
print(f"Lower Words : {lower_words}")
```
<br />

---

**`162`**. Write a program that accepts a sentence and counts the number of letters, digits, and spaces.

Assume the following input is provided to the program:

'python programming 123'

Then the output should be as follows:

Letters 17

Digits 3

Spaces 2
<br />

```python
sentence = "python programming 123"
words = 0
numbers = 0
spaces = 0
 
for i in sentence:
    if i.isalpha():
        words += 1
    elif i.isdigit():
        numbers += 1
    else:
        spaces += 1
 
print(f"words : {words}")
print(f"numbers : {numbers}")
print(f"spaces : {spaces}")
```
<br />

---

**`163`**. Write a program that prints all the numbers between 2000 and 4001 such that all of their digits are even.

The resulting numbers should be printed on a single line as a comma-separated sequence.

Sample output:

2002, 2004, 2006, ...
<br />

```python
numList = []
for item in range(2000, 4001):
    if int(str(item)[0])%2==0 and \
     int(str(item)[1])%2==0 and \
      int(str(item)[2])%2==0 and \
       int(str(item)[3])%2==0:
        numList.append(item)
print(numList)
```
<br />

---

**`164`**. Write a program that accepts a sequence of space-separated words as input, removes all duplicate words, sorts the remaining words in alphabetical order, and prints them.

Assume the following input is provided to the program:

python is the best programming language python is a simple language
<br />

```python
words = "python is the best programming language python is a simple language"
setWords = set(words.split(" "))
print(" ".join(sorted(setWords)))
```
<br />

---

## <a id="165"></a>
**`165`**. Write a program that accepts a sequence of comma-separated words as input and prints the words in a comma-separated sequence after sorting them in alphabetical order.

Assume the following input is provided to the program:

without, hello, bag, world

Then, the output should be:

bag, hello, without, world
<br />

```python
words = input("Enter words (for example : a, b, c, d) :  ")
splitSpace = words.split(" ")
joinSplitSpace = "".join(splitSpace)
splitComma = joinSplitSpace.split(",")
 
print(", ".join(sorted(splitComma)))
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`166`**. Define a class that has the following two methods:

get_string: Accepts a string as input from the user.
print_string: Prints the input string in uppercase.
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

---

**`167`**. Write a program using list comprehension that accepts two integers, X and Y, as input and generates a two-dimensional array.

Assume the following input is provided to the program:

3,5

Then, write a function that displays the generated two-dimensional array, printing each row on a separate line.
<br />

```python
# for array print
def print_array(array):
    for row in range(1, x+1):
        print()
        for coll in range(1, y+1):
            print(coll, end = "\t")
            
x = 3
y = 5
#comprehension list
comperhensionArray = [[j for j in range(1, y+1)]for i in range(1, x+1)]
#calling function
print_array(comperhensionArray)
```
<br />

---
**`168`**. Write a program that generates a list of 5 random numbers between 100 and 200.

Note:

Use random.sample() to generate the list of random values.
<br />

```python
from random import sample
print(sample([x for x in range(100, 201)], 5))
```
<br />

---
**`169`**. Write a program that uses a generator to produce all numbers between 0 and n (inclusive) that are divisible by both 5 and 7, and print them.

Example:

If the following input is provided to the program:

100

Then the output should be exactly:

0,35,70
<br />

```python
print(list((x for x in range(int(input("Enter number : "))) if x%5==0 and x%7==0)))
```
<br />

---

## <a id="170"></a>
**`170`**. Write a list comprehension that:

Accepts an integer as input.
Within the range from 0 to that number, randomly selects and prints the first even number chosen.

Notes:

After importing the required module, the list comprehension must be written on a single line.
Implement appropriate error handling for possible exceptions.

Hint:

To randomly select the first even number, you may use random.choice().
<br />

```python
from random import choice
try:
    print(choice([x for x in range(1, int(input("Enter number : "))) if (x%2==0)]))
# If the user enters a string or decimal number
except ValueError as error:
    print(error)
# If the user enters numbers one and two
except IndexError as error:
    print(error)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`171`**. Write a program that:

Generates a random integer between 1 and 100.
Defines a generator that iterates through the range from 0 to the generated number, computes the square of each odd number, and prints the results as a comma-separated sequence.

Notes:

a. The output format must match the example exactly.

b. If the randomly generated number is 10, the output should be:

1,9,25,49,81
<br />

```python
from random import randint

n = randint(1, 100)

def pow_random(n):
    i = 1
    while i <= n:
        if i % 2 != 0:
            yield i ** 2
        i += 1

print(",".join(str(num) for num in pow_random(n)))
```
<br />

---

**`172`**. Write a program that uses map() and filter() to create a list whose elements are the squares of the even numbers in the following list:

[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

Notes:

Use map() to create the new list.
Use filter() to filter the elements of the list.
You must use filter() inside map().
<br />

```python
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list(map(lambda x: (x*x), filter(lambda y: (y%2==0), lst))))
```
<br />

---

**`173`**. Write a filter expression that performs the following operation in a single line:

Output the odd numbers in the range from 1 to 20.
<br />

```python
print(list(filter(lambda x: x%2!=0, range(1, 21))))
```
<br />

---

**`174`**. Write a program that:

Generates a random integer between 1 and 30.
Creates a list of numbers in the range from 0 to the generated number.
Prints only the positive numbers from the list.

Note:

Use the filter() function to solve this problem.
<br />

```python
import random
print(list(filter(lambda x: (x%2==0), range(1, random.randint(1, 30) + 1))))
```
<br />

---

## <a id="175"></a>
**`175`**. Write a program that:

Generates a random number between 1 and 20.
Creates a tuple in the range of that random number.
If the length of the tuple is even, print the first half and the second half separately.
If the length of the tuple is odd, print the first half, the middle element, and the second half separately.
<br />

```python
from random import randint

n = randint(1, 20)

t = tuple(range(1, n + 1))

mid = len(t) // 2

if len(t) % 2 == 0:
    print(t[:mid], t[mid:])
else:
    print(t[:mid], t[mid], t[mid+1:])
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`176`**. Write a program that produces and prints another tuple whose values are the even numbers from the given tuple.

Sample output:

Given tuple:

(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

Second tuple:

(10, 9, 8, 6, 4, 2)

Notes:

The program must be written using the filter() function.
<br />

```python
print(tuple(filter(lambda x: (x%2==0), range(1, int(input("What is the range of the tuple?  "))+ 1))))
```
<br />

---

**`177`**. You must write a program that sorts several tuples in the format (name, age, score) in ascending order. You may use modules to solve this problem.

Name is a string.
Age and score are numbers.
Tuples are entered by the user.
Sorting criteria:
Sort by name
Then by age
Then by score

Priority order: name > age > score

Example input:
Tom,19,80  
John,20,90  
Jony,17,91  
Jony,17,93  
Json,21,85
<br />
<br />
Expected output:
<br />
[('John', '20', '90'), ('Jony', '17', '91'), ('Jony', '17', '93'), ('Json', '21', '85'), ('Tom', '19', '80')]
<br />

```python
from operator import itemgetter

tuList = ("Tom", 19, 80), ("John", 20, 90), ("Jony", 17, 91), ("Jony", 17, 93), ("Json", 21, 85)

print(sorted(tuList, key = itemgetter(0, 1, 2)))
```
<br />

---

**`178`**. Write a program that extracts and prints:

the words enclosed in parentheses, and
the words that are preceded and followed by a period (.)

from the following text:

Lorem ipsum is (typically) a corrupted version of De .finibus. bonorum et malorum, a 1st-century BC (text) by the Roman .statesman and .philosopher. Cicero, with (words) altered, added, and removed to make it .nonsensical. and improper .Latin. The first two words. (themselves) are a truncation of dolorem ipsum (pain itself).

Note:

You may use the re module.
<br />

```python
import re

text = """
Lorem ipsum is (typically) a corrupted version of De
.finibus. bonorum et malorum, a 1st-century BC (text) by the Roman
.statesman and .philosopher. Cicero, with (words) altered, added, and removed to make it
.nonsensical. and improper .Latin. The first two words.
(themselves) are a truncation of dolorem ipsum (pain itself).
"""

# Words inside parentheses
parentheses = re.findall(r"\((.*?)\)", text)

# Words enclosed by dots
dots = re.findall(r"\.([A-Za-z]+)\.", text)

print(parentheses)
print(dots)
```
<br />

---

**`179`**. Write a program that:

Reads the first name, last name, and mobile phone number of 10 people from the user.
Saves this information in a text file named info.txt.
Then, in the same directory, creates a folder named validation_info.
Inside that folder, saves the names of the people with valid mobile phone numbers in another text file named finally_info.txt.

Note:

Before creating the folder, check whether it already exists.
Use the os and re modules.
<br />

```python
from os import path, mkdir
import re

# Write information of 10 people to info.txt
with open("info.txt", "w") as info:
    for _ in range(10):
        name = input("Enter your name: ")
        family = input("Enter your family: ")
        phone = input("Enter your phone number: ")

        info.write(f"name:{name},family:{family},phoneNumber:{phone}\n")

# Create folder if it does not exist
if not path.exists("validation_info"):
    mkdir("validation_info")

# Regular expression for a valid record
pattern = r"name:[A-Za-z]+,family:[A-Za-z]+,phoneNumber:09\d{9}"

# Read info.txt and save valid records
with open("info.txt", "r") as source, \
     open("validation_info/finally_info.txt", "w") as dest:

    for line in source:
        if re.fullmatch(pattern, line.strip()):
            dest.write(line)
```
<br />

---

## <a id="180"></a>
**`180`**. Write a program that validates the following email addresses and prints the valid ones.

john90@yahoo.com

emily@gmail2.com

123jimmy@yahoo.com

kangarzehtab@gmail.com

panjali@yahho.com

maryam@gmail.c

programmer@yahoo.com

html@gahoo.com

naghi.mamooli123@gmail.com

Note:

You may use the re module to validate the email addresses.
<br />

```python
import re

emails = """
john90@yahoo.com
emily@gmail2.com
۱۲۳jimmy@yahoo.com
kangarzehtab@gmail.com
panjali@yahho.com
maryam@gmail.c
programmer@yahoo.com
html@gahoo.com
naghi.mamooli123@gmail.com
"""

pattern = r"[A-Za-z][A-Za-z0-9.]*@(gmail|yahoo)\.com"

for email in emails.splitlines():
    if re.fullmatch(pattern, email):
        print(email)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`181`**. Write a program that:

Creates a list containing the numbers in the range specified by the user.
Generates a randomized list from the created list.
Then, using the reduce() function, outputs:
the sum of the numbers,
the smallest number,
and the largest number.

Notes:

a. Use random.sample() to generate the randomized list.
b. Handle possible exceptions appropriately.
<br />

```python
from random import sample, randint
from functools import reduce
 
try:
    userNumber = [x for x in range(1, int(input("Enter number : "))+1)]
    listNumber = sample(userNumber, randint(1, len(userNumber)))
    print(f"Sum Of Numbers : {reduce(lambda x, y: (x+y), listNumber)}")
    if len(listNumber) >= 2:
        print(f"Max : {reduce(lambda x, y: x if x > y else y, listNumber)}")
        print(f"Min : {reduce(lambda x, y: y if y < x else x, listNumber)}")
    else:
        print("Entered does not have max and min...\nTest with a larger number...")
except ValueError as error:
    print(error)
```
<br />

---

**`182`**. Write a program that:

First outputs the duplicate elements, and then the non-duplicate elements of the two lists below.

list1 = [1, 3, 6, 78, 35, 55, 24]
list2 = [12, 24, 35, 24, 88, 120, 155, 6]

<br />

```python
from operator import countOf

list1 = [1, 3, 6, 78, 35, 55, 24]
list2 = [12, 24, 35, 24, 88, 120, 155, 6]

list3 = list1 + list2

duplicateNumbers = []
nonRepeatingNumbers = []

for i in list3:
    if countOf(list3, i) > 1:
        if i not in duplicateNumbers:
            duplicateNumbers.append(i)
    else:
        nonRepeatingNumbers.append(i)

print("Non Repeating Numbers:", nonRepeatingNumbers)
print("Duplicate Numbers:", duplicateNumbers)
```
<br />

---

**`183`**. Write a program that:

Generates three random single-digit numbers
Prints all possible permutations of these three numbers

Note:

You can use the itertools module to solve this problem.
<br />

```python
from random import sample
from itertools import permutations

print(list(permutations(sample(range(9), 3))))
```
<br />

---

**`184`**. Write a program that:

Counts the lowercase letters of the English alphabet.
The output should be a dictionary where:
keys are letters
values are numbers

Example:

{'a': 0, 'b': 1, 'c': 2, ...}

Note:
You can use the string module to solve this problem.
<br />

```python
# Step 1 (Algorithmic)
from string import ascii_lowercase

asciDict = {}
i = 0
while i < len(ascii_lowercase):
    asciDict[ascii_lowercase[i]] = i
    i += 1
print(asciDict)


# Step 2 (Pythonic)
from string import ascii_lowercase

asciDict = {ch: i for i, ch in enumerate(ascii_lowercase)}
print(asciDict)
```
<br />

---

## <a id="185"></a>
**`185`**. Write a program that:

Takes an integer n from the user
Computes the expression:
n + nn + nnn
For example, if the user enters 2, the result is:
222 + 22 + 2 = 246
Then uses the filter() function to check whether the result is divisible by n or not
<br />

```python
n = input("Enter number: ")

result = int(n) + int(n*2) + int(n*3)

is_divisible = list(filter(lambda x: x % int(n) == 0, [result]))

print(result)
print(bool(is_divisible))
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`186`**. Write a program that forms sentences using corresponding indexes of lists.

subjects = ["I", "You"]
verbs = ["Play", "Love"]
objects = ["Hockey", "Football"]
Requirements:

Method 1:

Use direct indexing like list[index] to construct sentences.

Method 2:

After solving Method 1, also construct sentences using map().

<br />

```python
subjects = ["I", "You"]
verbs = ["Play", "Love"]
objects = ["Hockey","Football"]

for i in subjects:
    for j in verbs:
        for k in objects:
            print(i, j, k)

sentense = [subjects[i]+" "+verbs[i]+" "+objects[i] for i in range(len(subjects))]
print(sentense)

print(list(map(lambda s, v, o: s+" "+v+" "+o, subjects, verbs, objects )))
```
<br />

---

**`187`**. Write a program that:

Randomly generates a list of 10 even numbers between 100 and 300
Use random.sample() to create the list of random values
<br />

```python
from random import sample

print(sample(range(100, 301, 2), 10))
```
<br />

---

**`188`**. Write a program using dictionary comprehension that converts the following text into a dictionary, where the keys are numbers and the values are the characters of the text.

text = "Python Dictionary Comprehension"

Note:
Spaces should not be counted when creating the dictionary.
<br />

```python
# step 1 
text = "".join("Python Dictionary Comprehension".split())

result = {i: text[i] for i in range(len(text))}

print(result)


# step 2
text = "Python Dictionary Comprehension".replace(" ", "")

print({i: ch for i, ch in enumerate(text)})
```
<br />

---

**`188`**. با comprehension برنامه ای بنویسید که متن زیر را تبدیل به دیکشنری کند به گونه ای که اعداد کلید دیکشنری و حروف متن، مقدار باشند.
<br />
text = “Python Dictionary Comprehension”
<br />
نکته:
خطوط فاصله در ساخت دیکشنری محاسبه نشوند.
<br />

```python
# step 1 
text = "".join("Python Dictionary Comprehension".split())

result = {i: text[i] for i in range(len(text))}

print(result)


# step 2
text = "Python Dictionary Comprehension".replace(" ", "")

print({i: ch for i, ch in enumerate(text)})
```
<br />

---

**`189`**. Write a program that converts the following list into a dictionary using dictionary comprehension.

data = [
    ("sirvan", 23),
    ("maryam", 15),
    ("lily", 8),
    ("behroz", 4),
    ("jimmy", 20),
    ("jasem", 87)
]
<br />

```python
# step 1
data = [
    ("sirvan", 23),
    ("maryam", 15),
    ("lily", 8),
    ("behroz", 4),
    ("jimmy", 20),
    ("jasem", 87)
]

dataDict = {x[0]: x[1] for x in data}

print(dataDict)


# step 2
data = [
    ("sirvan", 23),
    ("maryam", 15),
    ("lily", 8),
    ("behroz", 4),
    ("jimmy", 20),
    ("jasem", 87)
]

dataDict = {name: age for name, age in data}

print(dataDict)
```
<br />

---

## <a id="190"></a>
**`190`**. Write a program that:

Converts all English alphabet letters into a dictionary, where:
<br />
uppercase letters are the keys
<br />
lowercase letters are the values
<br />
Then finds and prints all vowel letters, both uppercase and lowercase.
<br />

```python
from string import ascii_lowercase, ascii_uppercase
lettersDict = {ascii_uppercase[letters]:ascii_lowercase[letters] for letters in range(len(ascii_uppercase))}
print(lettersDict)

print(f"lower vowels: {[vowels for vowels in lettersDict.values() if vowels in 'aeiou']}")
print(f"upper vowels: {[vowels for vowels in lettersDict.keys() if vowels in 'AEIOU']}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`191`**. Write a program that computes the square of every number in the following dictionary and replaces the original values with their squares.

dictionary = {
    "a": [10, 20, 30, 40, 50],
    "b": {"1": 4, "2": 7, "3": 12},
    "c": (18, 35, 98, 15, 56, 11)
}
<br />

```python
dictionary = {
    "a": [10, 20, 30, 40, 50],
    "b": {"1": 4, "2": 7, "3": 12},
    "c": (18, 35, 98, 15, 56, 11)
}

for key, value in dictionary.items():
    if isinstance(value, list):
        dictionary[key] = [x**2 for x in value]

    elif isinstance(value, dict):
        dictionary[key] = {k: v**2 for k, v in value.items()}

    elif isinstance(value, tuple):
        dictionary[key] = tuple(x**2 for x in value)

print(dictionary)
```
<br />

---

**`192`**. Write a program that calculates the sum of the following dictionary:

dictionary = {
    "a": 100,
    "b": 200,
    "c": 300,
    "d": 29,
    "e": 92,
    "f": 58
}

Note:
Use the reduce() function to solve this problem.
<br />

```python
from functools import reduce

dictionary = {
    "a": 100,
    "b": 200,
    "c": 300,
    "d": 29,
    "e": 92,
    "f": 58
}

print(reduce(lambda x, y: x + y, dictionary.values(), 0))
```
<br />

---

**`193`**. Write a program that:

Finds the number of characters in the following text.
Finds the number of words in the text.
Finds the number of sentences in the text.
Finds and prints the most frequently repeated character in the text along with its repetition count.
text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
<br />

```python
# step 1
from string import ascii_letters
from collections import defaultdict

text = """Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."""


def most_repeated_letter(text):
    d = defaultdict(int)

    for char in text.lower():
        if char in ascii_letters:
            d[char] += 1

    return max(d.items(), key=lambda x: x[1])


print("Most repeated letter:", most_repeated_letter(text))
print("Number of letters:", sum(1 for char in text if char in ascii_letters))
print("Number of words:", len(text.split()))
print("Number of sentences:", text.count("."))


# step 2
from collections import Counter
import re

text = """
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
"""

letters = re.findall(r"[a-zA-Z]", text)
print("Number of letters:", len(letters))

words = re.findall(r"\b[a-zA-Z]+\b", text)
print("Number of words:", len(words))

sentences = re.findall(r"[.!?]", text)
print("Number of sentences:", len(sentences))

letter_count = Counter(letters)
most_common_letter = letter_count.most_common(1)[0]

print("Most repeated letter:", most_common_letter)
```
<br />

---

*`194`**. Write a program that:

Generates a random number between 1 and 500.

Creates a dictionary from 1 to the generated random number.
Example:

{1: "1", 2: "2", 3: "3", ...}
Calculates all divisors (factors) of the random number and saves them in a file named divisor.txt as a comma-separated sequence.

Note:
You can use the random module to generate the random number.
<br />

```python
from random import randint


randomNumber = randint(1, 500)

numberDict = {
    key: str(key)
    for key in range(1, randomNumber + 1)
}

print(numberDict)

num = ",".join(
    str(key)
    for key in numberDict
    if randomNumber % key == 0
)

with open("divisor.txt", "w") as divisor:
    divisor.write(num)
```
<br />

---

## <a id="195"></a>
**`195`**. Write a program for the following dictionary:

dictionary = {
    "a": [1, 2, 54, 100, 32, 73],
    "b": [82, 34, 12, 67, 90, 37],
    "c": (9, 8, 7, 6, 78, 65, 13)
}

Your program should:

Find and print the maximum and minimum values of each dictionary key separately.
Compute the sum of the numbers under each key, then print the maximum and minimum among these sums.
Modify the dictionary as follows:
Add 10 to every element in key "a".
Subtract 10 from every element in key "b".
Multiply every element in key "c" by 2.

Note:
Do not confuse a dictionary with a set. 😉
<br />

```python
dictionary = {
    'a': [1, 2, 54, 100, 32, 73],
    'b': [82, 34, 12, 67, 90, 37],
    'c': (9, 8, 7, 6, 78, 65, 13)
}

# Find the maximum, minimum, and sum for each dictionary key
for key, value in dictionary.items():
    print(f"{key}:")
    print("Max:", max(value))
    print("Min:", min(value))
    print("Sum:", sum(value))
    print()

# Calculate the maximum and minimum of the sums
sums = [sum(value) for value in dictionary.values()]
print("Max Sum:", max(sums))
print("Min Sum:", min(sums))

# Modify the values in each key
dictionary['a'] = [x + 10 for x in dictionary['a']]
dictionary['b'] = [x - 10 for x in dictionary['b']]
dictionary['c'] = tuple(x * 2 for x in dictionary['c'])

# Print the updated dictionary
print(dictionary)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`196`**. Write a program that converts the following two lists into a dictionary.

keys = ["one", "six", "five", "ten", "nine", "three", "four", "eight", "two", "seven"]

values = [6, 7, 1, 2, 9, 4, 10, 3, 8, 5]

Note:
Before creating the dictionary, sort both lists, then combine the corresponding elements into a dictionary.
<br />

```python
from n2w import convert

key = ["one", "six", "five", "ten", "nine", "three", "four", "eight", "two", "seven"]
value = [6, 7, 1, 2, 9, 4, 10, 3, 8, 5]

value.sort()

numDict = {}

for i in value:
    numDict[i] = convert(i)

print(numDict)
```
<br />

---

**`197`**. Write a program that:

Finds and prints the first non-repeating element in the following list:
myList = [1, 2, 9, 85, 6, 2, 0, 1, 25, 9, 385, 85, 385, 3]
<br />

```python
from operator import countOf

myList = [1, 2, 9, 85, 6, 2, 0, 1, 25, 9, 385, 85, 385, 3]
countOfnumber = [x for x in myList if countOf(myList, x) == 1]

if countOfnumber:
    print(countOfnumber[0])
else:
    print("No non-repeating element found")
```
<br />

---

**`198`**. Write a function that finds all palindrome numbers from 100 to 1000 and stores them in a tuple.

Note:

A number is considered a palindrome if its hundreds digit is equal to its units digit.

Since a tuple is an immutable data type, find a way to store all palindrome numbers in a tuple.
<br />

```python
def palindrome():
    return tuple(number for number in range(100, 1000) if (int(str(number)[0]) == int(str(number)[2])))
print(palindrome())
```
<br />

---

**`199`**. Write a function that finds all numbers with an even tens digit in the range 300 to 500 and stores them in a set.

Note:
Store the results in a set (not a list).
<br />

```python
def middle_number():
    return {x for x in range(300, 501) if (x // 10) % 10 % 2 == 0}

print(middle_number())
```
<br />

---

## <a id="200"></a>
**`200`**. Write a function that takes the following tuple as input and creates a dictionary within its range, where the sorted tuple values are the keys and the English alphabet letters are the values.
<br />

```python
# step 1 
from string import ascii_lowercase

def tuple_to_dict(tu):
    return {item: ascii_lowercase[item - 1] for item in sorted(tu)}

tu = (10, 1, 4, 9, 6, 3, 5, 8, 2, 7)

print(tuple_to_dict(tu))


# step 2
from string import ascii_lowercase

def tuple_to_dict(tu):
    return dict(zip(sorted(tu), ascii_lowercase))
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`201`**. Write a function that takes the following dictionary as input and produces:

A sorted list of the dictionary keys.
<br />
A sorted list of the dictionary values.
<br />
```python
dictionary = {
    'maryam': 20,
    'jimmy': 9,
    'naghi': 13,
    'bagher': {1, 2, 3, 4, 5},
    'maziyar': 0,
    'mostafa': {1: 'a', 2: 'b', 3: 'c'}
}
```
<br />

```python
# step 1
def key_value(dictionary):
    keys = sorted(dictionary.keys())
    values = sorted(dictionary.values(), key=str)

    return keys, values

keys, values = key_value(dictionary)

print("Keys:", keys)
print("Values:", values)

# step 2
def key_value(dictionary):
    return sorted(dictionary.keys()), sorted(dictionary.values(), key=str)
```
<br />

---

**`202`**. Write a program that flattens the following nested list into a single list and displays it in sorted order.

lst = [[7, 1, 9], [3, 6, 2], [5, 8, 4]]

Expected output:

[1, 2, 3, 4, 5, 6, 7, 8, 9]
<br />

```python
# step 1
lst = [[7, 1, 9], [3, 6, 2], [5, 8, 4]]

lst2 = []

for i in lst:
    for j in i:
        lst2.append(j)

print(sorted(lst2))

# step 2
lst = [[7, 1, 9], [3, 6, 2], [5, 8, 4]]

lst2 = [item for sublist in lst for item in sublist]

print(sorted(lst2))

# step 3
lst = [[7, 1, 9], [3, 6, 2], [5, 8, 4]]

print(sorted(item for sublist in lst for item in sublist))

# step 4
from itertools import chain

lst = [[7, 1, 9], [3, 6, 2], [5, 8, 4]]

print(sorted(chain.from_iterable(lst)))
```
<br />

---

**`203`**. Write a program that:
<br />
Takes an integer as input from the user.
<br />
Creates a random list within the range of that number.
<br />
Then writes a generator comprehension that finds the odd numbers in the random list.
<br />

```python
from random import sample

number = int(input("Enter number: "))

print(
    list(
        x for x in sample(range(1, number + 1), number)
        if x % 2 != 0
    )
)
```
<br />

---

**`204`**. Write a program that converts the following list into a set comprehension.
<br />
lst = [1, 2, 3, 4, 4, 5, 6, 6, 6, 7, 7, 8, 9, 9, 8, 7]
<br />

```python
lst = [1, 2, 3, 4, 4, 5, 6, 6, 6, 7, 7, 8, 9, 9, 8, 7]

print({x for x in lst})
```
<br />

---

## <a id="205"></a>
**`205`**. Write a program that:

Takes an integer as input from the user.
Generates a random number in the range 1 to the entered number.
Finds all even numbers in the range 1 to the generated random number.
Use list comprehension as much as possible.
<br />

```python
from random import randint

number = int(input("Enter Number: "))
random_number = randint(1, number)

print(f"Random Number: {random_number}")
print(f"Even Numbers: {[x for x in range(1, random_number + 1) if x % 2 == 0]}")
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`206`**. Write a program using dictionary comprehension that converts the following text into a nested dictionary.
<br />
text = "GFG"
<br />
Expected output:
<br />
{
    'G': {'G': 'GG', 'F': 'GF'},
    'F': {'G': 'FG', 'F': 'FF'}
}
<br />
Note:
<br />
Since dictionaries cannot have duplicate keys, the repeated 'G' in "GFG" appears only once in the output.
<br />

```python
# step 1
text = "GFG"

result = {
    i: {j: i + j for j in set(text)}
    for i in set(text)
}

print(result)


# step 2
text = "GFG"

letters = list(dict.fromkeys(text))

result = {
    i: {j: i + j for j in letters}
    for i in letters
}

print(result)
```
<br />

---

**`207`**. Write a program using dictionary comprehension that converts the following text into a dictionary such that:
<br />
The keys are the uppercase letters.
The values are the corresponding lowercase letters repeated three times.
<br />
text = "programmer"
<br />
Expected output:
<br />
{
    'P': 'ppp',
    'R': 'rrr',
    'O': 'ooo',
    'G': 'ggg',
    'A': 'aaa',
    'M': 'mmm',
    'E': 'eee'
}
<br />
Note:
<br />
Since dictionaries do not allow duplicate keys, repeated letters (such as r and m) appear only once in the output.
<br />

```python
# step 1
print({"programmer"[x].upper(): "programmer"[x] * 3
       for x in range(len("programmer"))})
```
```python
# step 2
text = "programmer"

print({text[i].upper(): text[i] * 3 for i in range(len(text))})
```
```python
# step 3 --> better
text = "programmer"

print({char.upper(): char * 3 for char in text})
```
<br />

---

**`208`**. Write a program using lambda to calculate the square and cube of the numbers in the following list.
<br />
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
<br />
Expected output:
<br />
Squares
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
<br />
Cubes
[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
<br />

```python
# step 1
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

squareNumbers = lambda lst: [x ** 2 for x in lst]
cubeOfNumbers = lambda lst: [x ** 3 for x in lst]

print("Square Numbers:", squareNumbers(lst))
print("Cube Numbers:", cubeOfNumbers(lst))
```
```python
# step 2
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

squareNumbers = list(map(lambda x: x ** 2, lst))
cubeNumbers = list(map(lambda x: x ** 3, lst))

print("Square Numbers:", squareNumbers)
print("Cube Numbers:", cubeNumbers)
```
<br />

---

**`209`**. Write a program using lambda to count the number of even and odd numbers in the following list.
<br />
lst = [1, 2, 3, 5, 7, 8, 9, 10]
<br />

```python
# step 1
lst = [1, 2, 3, 5, 7, 8, 9, 10]

oddCount = lambda lst: len([x for x in lst if x % 2 != 0])
evenCount = lambda lst: len([x for x in lst if x % 2 == 0])

print("Odd Numbers:", oddCount(lst))
print("Even Numbers:", evenCount(lst))
```
```python
# step 2 with filter
lst = [1, 2, 3, 5, 7, 8, 9, 10]

oddCount = lambda lst: len(list(filter(lambda x: x % 2 != 0, lst)))
evenCount = lambda lst: len(list(filter(lambda x: x % 2 == 0, lst)))

print("Odd Numbers:", oddCount(lst))
print("Even Numbers:", evenCount(lst))
```
<br />

---

## <a id="210"></a>
**`210`**. Write a program using lambda to calculate the sum of the corresponding elements of the following two lists.
<br />
a = [1, 5, 8, 14]
<br />
b = [3, 54, 12, 7]
<br />

```python
# step 1
a = [1, 5, 8, 14]
b = [3, 54, 12, 7]

func = lambda a, b: [a[i] + b[i] for i in range(len(a))]
print(func(a, b))
```
```python
# step 2
a = [1, 5, 8, 14]
b = [3, 54, 12, 7]

func = lambda a, b: [x + y for x, y in zip(a, b)]

print(func(a, b))
```
```python
# step 3 with map
a = [1, 5, 8, 14]
b = [3, 54, 12, 7]

print(list(map(lambda x, y: x + y, a, b)))
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`211`**. Write a program that outputs the numbers divisible by 13 from the following list.
<br />
lst = [19, 65, 57, 39, 152, 639, 121, 44, 90, 190]
<br />

```python
# step 1 
lst = [19, 65, 57, 39, 152, 639, 121, 44, 90, 190]

func = lambda lst: [x for x in lst if x % 13 == 0]

print(func(lst))
```
```python
# step 2 with filter
lst = [19, 65, 57, 39, 152, 639, 121, 44, 90, 190]

print(list(filter(lambda x: x % 13 == 0, lst)))
```
<br />

---

**`212`**. Write a program using lambda to output the palindromes from the following list.
<br />
lst = [
    "php",
    "jimmiji",
    "Python",
    "abcdcb",
    "JavavJ",
    "aaa",
    "2345432",
    "pip",
    "lala"
]
<br />
A palindrome is a string that reads the same forwards and backwards.
<br />

```python
# step 1
lst = ['php', 'jimmiji', 'Python', 'abcdcb', 'JavavJ', 'aaa', '2345431', 'pip', 'lala']
func = lambda lst: [st for st in lst if(st==st[::-1])]
print(func(lst))
```
```python
# step 2 with filter
lst = ['php', 'jimmiji', 'Python', 'abcdcb', 'JavavJ', 'aaa', '2345431', 'pip', 'lala']

print(list(filter(lambda x: x == x[::-1], lst)))
```
<br />

---

**`213`**. Write a function that outputs the anagrams from the following list.
<br />
lst = ['bcda', 'abce', 'cbda', 'cbea', 'adcb']
<br />
Expected output:
<br />
['bcda', 'cbda', 'adcb']
<br />
Two words are anagrams if they contain exactly the same letters with the same frequencies, regardless of their order.
<br />

```python
# step 1 
def find_anagrams(lst):
    sign = "".join(sorted(lst[0]))

    return [word for word in lst if "".join(sorted(word)) == sign]


lst = ["bcda", "abce", "cbda", "cbea", "adcb"]

print(find_anagrams(lst))
```
```python
# step 2
def anagrams(lst):
    base = sorted(lst[0])
    return [word for word in lst if sorted(word) == base]

lst = ['bcda', 'abce', 'cbda', 'cbea', 'adcb']

print(anagrams(lst))
```
<br />

---

**`214`**. Write a program that creates a new list called typeList containing the data types of the elements inside the following list.
<br />
lst = [{1:"py"}, 23, "Python", 23.98, [1, 2], {"a", "b"}, True, 5j, (1,)]
<br />
The new list should contain the type of each element in lst.
<br />

```python
# step 1
lst = [{1:"py"}, 23, "Python", 23.98, [1, 2], {"a", "b"}, True, 5j, (1,)]

typeList = [type(item) for item in lst]

print(typeList)
```
```python
# step 2
lst = [{1:"py"}, 23, "Python", 23.98, [1, 2], {"a", "b"}, True, 5j, (1,)]

typeList = [type(item).__name__ for item in lst]

print(typeList)
```
<br />

---

## <a id="215"></a>
**`215`**. Write one or more functions that take the following text as input and:
<br />
Determine the number of consonants.
<br />
Determine the frequency of each consonant.
<br />
Determine the number of uppercase and lowercase letters.
<br />
Store all words that start with an uppercase letter in a list named myInfo and print it.
<br />
text = “lorem ipsum is typically You corrupted version of Are definos , a century boC tExt by the roman statesman and philosopher The cicero, witH the Best words altered, added, and removed to make it nonsensical and Programmer and improper latin.”
<br />

```python
# step 1 --> standard
from collections import Counter

def number_of_consonants(text):
    vowels = "aeiouAEIOU"
    consonants = [c for c in text if c.isalpha() and c not in vowels]
    return consonants


def consonant_count(consonants):
    return Counter(consonants)


def upper_lower_count(text):
    upper = sum(ch.isupper() for ch in text)
    lower = sum(ch.islower() for ch in text)
    return upper, lower


def upper_words(text):
    return [word.strip(".,") for word in text.split() if word[0].isupper()]


text = """lorem ipsum is typically You corrupted version of Are definos,
a century boC tExt by the roman statesman and philosopher The cicero,
witH the Best words altered, added,
and removed to make it nonsensical and Programmer and improper latin."""

consonants = number_of_consonants(text)

print("Number Of Consonants:", len(consonants))
print("Consonant Repetitions:", consonant_count(consonants))

upper, lower = upper_lower_count(text)
print("Upper Letters:", upper)
print("Lower Letters:", lower)

myInfo = upper_words(text)
print("myInfo:", myInfo)
```
```python
# step 2 --> with counter
from collections import Counter

text = """lorem ipsum is typically You corrupted version of Are definos,
a century boC tExt by the roman statesman and philosopher The cicero,
witH the Best words altered, added,
and removed to make it nonsensical and Programmer and improper latin."""

vowels = "aeiouAEIOU"

consonants = [c for c in text if c.isalpha() and c not in vowels]

counter = Counter(consonants)

upper = sum(map(str.isupper, text))
lower = sum(map(str.islower, text))

myInfo = [w.strip(".,") for w in text.split() if w[0].isupper()]

print("Number Of Consonants:", len(consonants))
print(counter)
print("Upper:", upper)
print("Lower:", lower)
print(myInfo)
```
```python
# step 3 --> pythonic
from collections import Counter

text = """lorem ipsum is typically You corrupted version of Are definos,
a century boC tExt by the roman statesman and philosopher The cicero,
witH the Best words altered, added,
and removed to make it nonsensical and Programmer and improper latin."""

vowels = set("aeiouAEIOU")

consonants = [c for c in text if c.isalpha() and c not in vowels]

print(len(consonants))

print(Counter(consonants))

print(sum(c.isupper() for c in text))
print(sum(c.islower() for c in text))

myInfo = [w.strip(".,") for w in text.split() if w[0].isupper()]
print(myInfo)
```
```python
# step 4 --> only with functions & without counter
def analyze(text):
    vowels = "aeiouAEIOU"

    consonants = [c for c in text if c.isalpha() and c not in vowels]

    repetition = {}

    for c in consonants:
        repetition[c] = repetition.get(c, 0) + 1

    upper = sum(c.isupper() for c in text)
    lower = sum(c.islower() for c in text)

    myInfo = [w.strip(".,") for w in text.split() if w[0].isupper()]

    print("Number Of Consonants:", len(consonants))
    print("Repetitions:", repetition)
    print("Upper:", upper)
    print("Lower:", lower)
    print("myInfo:", myInfo)


text = """lorem ipsum is typically You corrupted version of Are definos,
a century boC tExt by the roman statesman and philosopher The cicero,
witH the Best words altered, added,
and removed to make it nonsensical and Programmer and improper latin."""

analyze(text)
```
<br />

[list of questions](#go-to-the-question-list)👆

---

**`216`**. Write a function that takes a text as a parameter and outputs the number of vowels and the number of consonants in that text.
<br />
Note:
<br />
For the text:
<br />
"pythonlobby"
<br />
the number of vowels is 2, and the number of consonants is 9.
<br />

```python
# step 1 --> standard
def vowels_and_consonants(text):
    vowels = "aeiou"

    vowels_count = len([c for c in text.lower() if c in vowels])
    consonants_count = len([c for c in text.lower() if c.isalpha() and c not in vowels])

    print("Vowels:", vowels_count)
    print("Consonants:", consonants_count)


vowels_and_consonants("pythonlobby")
```
```python
# step 2 --> pro
from collections import Counter

def vowels_and_consonants(text):
    letters = [c.lower() for c in text if c.isalpha()]
    counter = Counter("vowel" if c in "aeiou" else "consonant" for c in letters)

    print(counter["vowel"])
    print(counter["consonant"])


vowels_and_consonants("pythonlobby")
```
```python
# step 3 --> Pythonic
def vowels_and_consonants(text):
    text = text.lower()

    vowels = sum(c in "aeiou" for c in text)
    consonants = sum(c.isalpha() and c not in "aeiou" for c in text)

    return vowels, consonants


print(vowels_and_consonants("pythonlobby"))
```
```python
# step 4 --> with filter & lambda
def vowels_and_consonants(text):
    vowels = len(list(filter(lambda c: c.lower() in "aeiou", text)))
    consonants = len(list(filter(lambda c: c.isalpha() and c.lower() not in "aeiou", text)))

    print("Vowels:", vowels)
    print("Consonants:", consonants)


vowels_and_consonants("pythonlobby")
```
```python
# step 5 --> with comperhention
def vowels_and_consonants(text):
    return f"""vowels: {len([x for x in text if (x=="a" or x=="e" or x=="i" or x=="o" or x=="u")])}
consonants: {len([y for y in text if (y!="a" and y!="e" and y!="i" and y!="o" and y!="u")])}"""
print(vowels_and_consonants("pythonlobby"))
```
<br />

---
