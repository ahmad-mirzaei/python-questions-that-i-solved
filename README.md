
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

`Input` : None

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