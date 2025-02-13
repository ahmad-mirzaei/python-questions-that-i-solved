
# 🐍 سوالات پایتونی که من حل کردم  
<br />

## توضیحات
_این ریپوزیتوری شامل مجموعه‌ای از سوالات پایتون است که من از سطح مقدماتی و پیشرفته حل کرده ام که باعث شد در حل مسائل پایتونی پیشرفت خوبی داشته باشم. هدف از این پروژه، آشنایی با چالش های مختلف و توانا شدن در حل مسائل است._
<br />
<br />

## 🚀 نحوه‌ی استفاده  

- ریپوزیتوری را کلون کنید:

```bash
git clone https://github.com/ahmad-mirzaei/python-questions-that-i-solved.git

```
<br />

---

- ## **نسخه های ترجمه شده**
    - [Persian Version - فارسی](READMEir.md)

---

## 🤝 مشارکت

__اگر سوالات بیشتری دارید یا می‌خواهید راه‌حل‌های بهتری پیشنهاد دهید، خوشحال می‌شوم که مشارکت کنید! لطفاً یک `Pull Request` ارسال کنید.__
<br />
<br />

---

## ❓ سوالات 

**`1`**. برنامه ای بنویسید که اطلاعات ۳ دانشجو (شامل شماره دانشجویی، نام ، نام خانوادگی و معدل) را درون یک لیستی از دیکشنری (Dictionary) ذخیره کرده و سپس آنها را به شکل زیر چاپ کنید.

`Input` : ندارد

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

**`2`**. برنامه ای بنویسید که عدد N را از ورودی گرفته و یک دیکشنری ایجاد کند، که کلیدها اعداد بین ۱ تا N باشند و مقادیر مربع کلیدها.

`Input` : Enter Number : 9

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

**`3`**. برنامه ای بنویسید که عدد صحیح و مثبت N را از ورودی گرفته و سپس دیکشنری (انگلیسی به فارسی) با N لغت را با دریافت لغات و معانی آنها از کاربر ایجاد کرده و در انتها آنرا چاپ کند.

`Input` :

Enter Number : 3

Enter English word 1 : book

Enter Persian word 1: ketab

Enter English word 2: chair

Enter Persian word 2: sandali

Enter English word 3: bag

Enter Persian word 3: kif


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

**`4`**. برنامه ای بنویسید که ۵ عدد صحیح مثبت از ورودی گرفته و درون یک لیست قرار دهد، سپس توسط یک تابع همه عناصر لیست را ۱۰ برابر کرده و توسط برنامه اصلی لیست حاصل را چاپ کند.

`Input` :

Enter Number : 143

Enter Number : 69

Enter Number : 21

Enter Number : 567

Enter Number : 48


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

**`5`**. برنامه ای بنویسید که توسط تابع یک لیست از اعداد صحیح غیر از صفر از ورودی گرفته و سپس توسط تابع دیگر بزرگترین و کوچکترین عنصر لیست را پیدا کرده و چاپ کند (شرط پایان دریافت اعداد وارد شدن عدد صفر توسط کاربر باشد)

`Input` :

Enter Number : 25

Enter Number : 9

Enter Number : 83

Enter Number : 6

Enter Number : -12

Enter Number : 17

Enter Number : 0


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

**`6`**. برنامه ای بنویسید که بزرگترین عدد وردی را چاپ کند؛ عدد ورودی بین 10 تا 90 است و تا زمانی که در ورودی -1 وارد نشده است، گرفتن ورودی ادامه داشته باشد.
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

**`7`**. برنامه ای بنویسید که یک رشته شامل چند کلمه از ورودی بگیرد و حرف اول تمامی کلمات را با حروف بزرگ به خروجی ببرد.
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

**`8`**. برنامه ای بنویسید که یک عدد به عنوان شماره روز سال ازورودی گرفته مشخص کند آن روز در چه فصلی از سال می باشد؟

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

**`9`**. برنامه ای بنویسید که سه عدد از ورودی گرفته عدد وسطی یا max دوم راچاپ کند.

 
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

**`10`**. برنامه ای بنویسید که عدد صحیح n را از ورودی گرفته و n جمله اول دنباله فیبوناچی زیر را چاپ کند.

(دنباله فیبوناچی به این ترتیب تولید میشود که دو جمله اول آن یک و برای تولید جملات بعدی هر جمله از جمع دو جمله قبلی خودش بدست می آید)

 
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