
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

<a id="go-to-the-question-list"></a>

## ✍️ سوالات را تقسیم بندی کرده ام که هم به سوالات و هم به فهرست دسترسی بهتری داشته باشید.
| `1-50` | `55-105` |  |  |  |  |  |  |  |  |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| [1](#1) | [55](#55) |  |  |  |  |  |  |  |  |
| [5](#5) | [60](#60) |  |  |  |  |  |  |  |  |
| [10](#10) | [65](#65) |  |  |  |  |  |  |  |  |
| [15](#15) | [70](#70) |  |  |  |  |  |  |  |  |
| [20](#20) | [75](#75) |  |  |  |  |  |  |  |  |
| [25](#25) | [80](#80) |  |  |  |  |  |  |  |  |
| [30](#30) | [85](#85) |  |  |  |  |  |  |  |  |
| [35](#35) | [90](#90) |  |  |  |  |  |  |  |  |
| [40](#40) |  |  |  |  |  |  |  |  |  |
| [45](#45) |  |  |  |  |  |  |  |  |  |
| [50](#50) |  |  |  |  |  |  |  |  |  |

---

## ❓ سوالات 

## <a id="1"></a>
**`1`**. برنامه ای بنویسید که اطلاعات ۳ دانشجو (شامل شماره دانشجویی، نام ، نام خانوادگی و معدل) را درون یک لیستی از دیکشنری (Dictionary) ذخیره کرده و سپس آنها را به شکل زیر چاپ کنید.
<br />

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`2`**. برنامه ای بنویسید که عدد N را از ورودی گرفته و یک دیکشنری ایجاد کند، که کلیدها اعداد بین ۱ تا N باشند و مقادیر مربع کلیدها.
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

**`3`**. برنامه ای بنویسید که عدد صحیح و مثبت N را از ورودی گرفته و سپس دیکشنری (انگلیسی به فارسی) با N لغت را با دریافت لغات و معانی آنها از کاربر ایجاد کرده و در انتها آنرا چاپ کند.
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

**`4`**. برنامه ای بنویسید که ۵ عدد صحیح مثبت از ورودی گرفته و درون یک لیست قرار دهد، سپس توسط یک تابع همه عناصر لیست را ۱۰ برابر کرده و توسط برنامه اصلی لیست حاصل را چاپ کند.
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
**`5`**. برنامه ای بنویسید که توسط تابع یک لیست از اعداد صحیح غیر از صفر از ورودی گرفته و سپس توسط تابع دیگر بزرگترین و کوچکترین عنصر لیست را پیدا کرده و چاپ کند (شرط پایان دریافت اعداد وارد شدن عدد صفر توسط کاربر باشد)
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

👆[برو به فهرست](#go-to-the-question-list)

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

**`9`**. برنامه ای بنویسید که سه عدد از ورودی گرفته عدد وسطی یا max دوم راچاپ کند.
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
**`10`**. برنامه ای بنویسید که عدد صحیح n را از ورودی گرفته و n جمله اول دنباله فیبوناچی زیر را چاپ کند.
<br />
(دنباله فیبوناچی به این ترتیب تولید میشود که دو جمله اول آن یک و برای تولید جملات بعدی هر جمله از جمع دو جمله قبلی خودش بدست می آید)
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`11`**. برنامه ای بنویسید که دو عدد صحیح و مثبت a و b را از ورودی گرفته و سپس عدد a را به توان عدد b رسانده و نتیجه را چاپ کند.
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

**`12`**. برنامه ای بنویسید که از ورودی یک عدد بگیرد و در محدوده ی آن عدد شبیه خروجی زیر را تولید کند.
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

**`13`**. با حلقه ی while برنامه ای بنویسید که 20 عدد دریافت کند و سپس مجموع آنها را به خروجی ببرد.
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

**`14`**. برنامه ای بنویسید که تعدادی عدد صحیح مثبت از ورودی گرفته و سپس مجموع و میانگین اعداد را چاپ کند(نکته: در محاسبه اعداد تکراری در نظر گرفته نشوند، و همچنین شرط پایان دریافت عدد از کاربر وارد کردن عدد منفی توسط کاربر می باشد)
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
**`15`**. برنامه ای بنویسید که هشت نام از ورودی گرفته و درون یک لیست ذخیره کند، سپس اسامی که ابتدای آنها حرف m و انتهای آنها حرف d یا i وجود دارد را درون یک مجموعه (Set) ذخیره کرده و چاپ کند.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`16`**. یک حلقه ی for بنویسید که در آن از ورودی اعدادی دریافت کند و درون یک لیست قرار دهد و هر زمان مجموع آن اعداد بیشتر از 50 شد، break کرده و برنامه را متوقف کند.
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

**`17`**. برنامه ای بنویسید که از ورودی یک عدد بگیرد و شبیه خروجی زیر را برگرداند.
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

**`18`**.  برنامه ای‌ که‌ تعداد‌ کالا‌ و‌ قیمت‌ هر‌  کالا‌را‌ خوانده،‌ مبلغ‌ فروش‌ را‌ نمایش ‌میدهد‌ (مبلغ ‌
فروش‌ برابر‌ با‌ تعداد‌ کالا‌ *‌ قیمت ‌کالا‌ است‌).
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

**`19`**. برنامه ای که شکل زیر را در خروجی نمایش دهد:
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
**`20`**.  برنامه ای‌ که‌ یک ‌عدد‌ چهار رقمی‌ را‌ خوانده، ‌اگر‌ حاصل‌ ضرب رقم های‌ ‌اول‌ و‌ چهارم،‌
برابر‌ حاصل‌ جمع‌ ارقام‌ دوم‌ و‌ سوم‌ باشد‌ `Yes` و گرنه‌، `No` را‌ نمایش ‌میدهد‌‌‌
<br />

```python
number = [int(i) for i in input("Please enter a four-digit number : ")]
print("YES") if number[0] * number[3] == number[1] + number[2] else print("NO")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`21`**.  برنامه ای‌ که‌ یک‌ عدد‌ ‌سه‌ رقمی‌ را‌ خوانده،‌ اگر‌ مجموع‌ رقم های‌ اول‌ و‌ سوم‌ برابر‌ رقم‌
دوم‌ باشد‌ `Yes` وگرنه‌ `No` را‌ چاپ‌ می کند‌
<br />

```python
number = [int(i) for i in input("Please enter a three-digit number : ")]
print("YES") if number[0] + number[2] == number[1] else print("NO")
```
<br />

---

**`22`**. برنامه ای بنویسید که عددی از ورودی دریافت و صفر های عدد را حذف کند.
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

**`23`**. برنامه ای بنویسید a و b را بگیرد سپس عدد کوچکتر را به توان عدد بزرگتر رسانیده و حاصل را
نمایش دهد.
<br />

```python
a = int(input("Enter Number : "))
b = int(input("Enter Number : "))
print(a**b) if a < b else print(b**a)
```
<br />

---

**`24`**. برنامه ای بنویسید که نام و نام خانوادگی و حقوق ۱۰ نفر را از ورودی دریافت نماید و نام و نام خانوادگی فردی که بیشترین حقوق را دارد در خروجی نمایش دهد.
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
**`25`**. برنامه ای‌ که‌ نمره های‌ دانشجویی‌ را‌ دریافت‌ کرده،‌ اگر‌ نمره‌ کمتر‌ ‌از‌‌ ۱۱ بود،‌ کلمه‌
`Failed` و گرنه‌ کلمه‌ `Passed` را‌ نمایش ‌میدهد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`26`**. برنامه ای بنویسید که دو عدد دو رقمی بگیرد و بگوید آیا هیچ رقم مشابهی بین دو عدد وجود دارد یا خیر؟
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

**`27`**. برنامه ای بنویسید تا عددی را از ورودی دریافت نموده و بگوید عدد چند رقمی است، عدد وارد شده از سوی کاربر حداکثر ۵ رقمی خواهد بود.
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

**`28`**. برنامه ای بنویسید که یک رشته را به عنوان ورودی گرفته و فاصله های اضافی بین کلمات آن را حذف کند.
<br />

```python
user_input = ''.join(input("Enter Your String : ").split(' '))
print(user_input)
```
<br />

---

**`29`**. برنامه ای بنویسید که پس از دریافت عددی در برنامه اصلی، بزرگترین رقم عدد را در تابع فرعی
محاسبه و سپس در برنامه اصلی نمایش دهد.
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
**`30`**. برنامه ای بنویسید که سه ورودی از کاربر بگیرد و بزرگترین , کوچکترین و مجموع آنها را به خروجی ببرد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`31`**. برنامه ای بنویسید که یک عدد 6 رقمی بگیرد و بزرگترین عدد درون 6 رقم را به خروجی ببرد
<br />

```python
n = [int(i) for i in input("Enter number : ")] 
print(max(n))
```
<br />

---

**`32`**. برنامه ای بنویسید که 10 عدد را دریافت کند تعداد اعداد صفر تعداد اعداد مثبت و منفی را نمایش دهد.
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

**`33`**. برنامه ای‌ که‌ شعاع‌ دایره‌ را‌ خوانده‌، محیط‌، مساحت‌ و‌ قطر‌ آن‌ را‌ نمایش ‌می‌دهد‌
<br />

```python
radius = eval(input("Enter The Radius of The Circle : ")) # شعاع
area = ((radius**2)*3.14) # مساحت
circumference = ((3.14*2)*radius)  # محیط
diameter = radius*2 # قطر
print(f"area is : {area}\ncircumference is : {circumference}\n\
diameter is : {diameter}")
```
<br />

---

**`34`**. برنامه ای بنویسید که دو عدد از ورودی بگیرد و سپس 4 عمل جمع، تفریق، ضرب و تقسیم را روی آن انجام داده و به خروجی ببرد.
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
**`35`**. برنامه ای بنویسید که سه عدد بگیرد و مجموع اعداد فرد را محاسبه کرده و نمایش دهد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`36`**. تابعی بنویسید که با ورودی گرفتن عدد صحیح n، مجموع اعداد ۱ تا n را به عنوان خروجی بازگرداند.
<br />

```python
def sum_of_numbers():
	n = int(input("Enter Number : "))
	return sum(range(1, n + 1))

print(sum_of_numbers())
```
<br />

---

**`37`**. برنامه ای ‌که ‌دو‌ ضلع ‌موازی‌ و‌ ارتفاع‌ ذوزنقه‌ را‌ دریافت‌ کرده،‌ مساحت‌ آن‌ را‌ محاسبه‌ می کند.
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

**`38`**. برنامه ای بنویسید که عددی بگیرد و جمع دهگان و صدگان آن را حساب کرده و نمایش دهد. 
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

**`39`**. برنامه ای بنویسید که یک عدد چند رقمی از ورودی بگیرد و در خروجی معکوس آن عدد را نمایش دهد.
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
**`40`**. برنامه ای بنویسید که دو عدد x و y را از رودی دریافت کرده و مقادیر آنها را با هم جابجا کنید. 
<br />

```python
# جابجایی متغیر ها
x = int(input("Enter x : "))
y = int(input("Enter y : "))
x, y = y, x  
print(f"x : {x} and y : {y}")

# جابجایی مقدار با متغیر کمکی
x = int(input("Enter x : "))
y = int(input("Enter y : "))
temp = x 
x = y
y = temp
print(f"x : {x} and y : {y}")

# جابجایی مقدار با عملیات جمع و تفریق
x = int(input("x : "))
y = int(input("y : "))
x = x + y   
y = x - y
x = x - y
print(f"x : {x} and y : {y}")

# جابجایی مقادیر با عملگر بیتی
x = int(input("Enter x : "))
y = int(input("Enter y : "))
x = x^y   
y = x^y
x = x^y
print(f"x : {x} and y: {y}")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`41`**. برنامه ای بنویسید که اعداد بین دو عدد را نمایش دهد.
<br />

```python
x = int(input("Enter First Number : "))
y = int(input("Enter Second Number : "))

print([i for i in range(x+1, y)])
```
<br />

---

**`42`**. برنامه ای بنویسید که از 10 تا 100، اعدادی دو رقمی که رقم اول و دوم آنها با هم برابر است را به خروجی ببرد.
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

**`43`**. برنامه ای بنویسید که چهار عدد بگیرد و کوچکترین آنها را نمایش دهد.
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

**`44`**. برنامه ای بنویسید که ۴ عدد بگیرد و اولین عدد زوج در میان آن ها را نمایش دهد.
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
**`45`**. برنامه ای بنویسید که طول و عرض یک مستطیل را از ورودی دریافت کرده و مساحت و محیط آن را محاسبه و چاپ نماید.
<br />

```python
length = int(input("Enter The Length Of The Rectangle : "))
width = int(input("Enter The Widthh Of The Rectangle : "))
area = length*width
perimeter = ((length+width)*2)
print(f"area is : {area}\nperimeter is : {perimeter}")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`46`**. برنامه ای بنویسید که دو عدد بگیرد، اگر هر دو آنها بر ۳ و یا هر دو آنها بر ۷ بخش پذیر بودند پیغام “Yes” وگرنه پیغام “No” دهد.
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

**`47`**. برنامه ای بنویسید که عددی بگیرد، اگر یکان و دهگانش زوج بود پیغام Yes دهد و در غیر این صورت
پیغام No دهد.
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

**`48`**. برنامه ای بنویسید دو عدد بگیرد و اگر هر دو بیشتر از ۲۰ بودند پیغام “Yes” دهد.
<br />

```python
number_1 = int(input("Enter number : "))
number_2 = int(input("Enter number : "))
if number_1 and number_2 > 20: print("YES")
else: print("NO")
```
<br />

--- 

**`49`**. برنامه ای بنویسید که دو عدد را بگیرد و عدد بزرگتر را نمایش دهد.
<br />

```python
number_1 = int(input("Enter Number :"))
number_2 = int(input("Enter Number :"))
print(max(number_1, number_2))
```
<br />

---

## <a id="50"></a>
**`50`**. برنامه ای بنویسید که تعداد قوطی های کنسرو را بگیرد و بگوید چند کارتن ۶ تایی درست می شود و چند قوطی بی کارتن می ماند.
<br />

```python
numberOfCans = int(input("Enter The Number Of Cans : "))
print("cartons : ", numberOfCans // 6,"\n\
Remnants : ", numberOfCans%6)
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`51`**. برنامه ای بنویسید که تا وقتی عدد صفر وارد نشده، از کاربر عدد بگیرد و سپس معدل اعداد گرفته شده را چاپ کند. (برنامه صفر را نباید جزء معدل حساب کند، صفر صرفا نشان دهنده پایان اعداد است).
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

**`52`**. برنامه ای بنویسید که دو عدد بگیرد و بگوید بین آن دو عدد، چند مضرب ۷ وجود دارد.
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
 
**`53`**. برنامه ای بنویسید که چهار عدد بگیرد، اگر تعداد زوجی از آنها مضرب ۳ بودند پیغام “Yes” دهد.
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

**`54`**. تابعی بنویسید که عددی را به عنوان پارامتر ورودی دریافت کند و مقلوب آن در خروجی چاپ شود.
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
**`55`**. برنامه ای بنویسید که عددی بگیرد و بگوید زوج است یا فرد.
<br />

```python
n = int(input("Enter Your Number : "))
print("number is Even!!") if n %2 == 0 else print("number is Odd!!")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`56`**. برنامه ای بنویسید که شعاع یک دایره را از ورودی دریافت کرده و مساحت و محیط آن دایره را
محاسبه و چاپ نماید.
<br />

```python
radius = eval(input("Enter The Radius of The Circle : "))  ## شعاع
area = ((radius**2)*3.14) ## مساحت
circumference = ((3.14*2)*radius)  ## محیط
print(f"area is : {area}\ncircumference is : {circumference}")
```
<br />

---

**`57`**. برنامه ای بنویسید که عددی بگیرد، اگر سه رقمی نبود پیغام دهد.
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

**`58`**. برنامه ای بنویسید که لیستی از اعداد را از بزرگ به کوچک نمایش دهد.
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

**`59`**.  برنامه ای بنویسید که تا زمانی که کاربر ۱- وارد نکرده عدد بگیرد و جمع اعداد را نمایش دهد.
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
**`60`**. برنامه ای بنویسید که سن تان را به سال، ماه و روز گرفته و به دقیقه تبدیل نماید.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`61`**. برنامه ای بنویسید که اندازه سه ضلع مثلث را بپرسد و بگوید این مثلث متساوی الساقین، متساوی الاضلاع و یا معمولی است.
<br />

```python
sideSet = set()
for i in range(1, 4):
    Side = int(input("Enter The Side 1 : "))
    sideSet.add(Side)
if len(sideSet) == 1:
    print("Mosalase MotaVazi Al'azla")
elif len(sideSet) == 2:
    print("Mosalase MtaSavi Al'saghein")
else:
    print("Mosalase Skalen")
```
<br />

---

**`62`**. تابعی بنویسید که دو عدد بگیرد و مجموع آنها را به عنوان خروجی باز گرداند.
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

**`63`**. برنامه ای بنویسید که پس از دریافت عددی در برنامه اصلی، بزرگترین رقم عدد را در تابع فرعی
محاسبه و سپس در برنامه اصلی نمایش دهد.
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

**`64`**. تابعی بنویسید که:

1- نمره های ۵ درس یک دانشجو را دریافت کند.

2- اگر نمره ی وارد شده بین ۱۷ تا ۲۰ بود — A ،

3- اگر از ۱۵ تا ۱۷ بود — B ،

4- اگر از ۱۲ تا ۱۵ بود — C ،

5- و اگر از ۱۲ به پایین بود حرف D چاپ شود.

6- نکته: کیفیت نمرات به همراه نمره ی مورد نظر، به ترتیب در خروجی نمایش داده شود.
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
**`65`**. علی مقدار زیادی کتاب دارد که میخواهد آنها را در پک های ۴ تایی بسته بندی کند.
برنامه ای برای او بنویسید که تعداد کتابها را از او (کاربر) دریافت کرده و مشخص کند که با تعداد کتاب های او چند تا پک ۴ تایی می توان بسته بندی کرد و چه مقدار از کتابها باقی می ماند.
<br />

```python
books = int(input("Enter The Number Of Your Books : "))
print(f"packs : {books//4} and left over : {books % 4}")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`66`**. برنامه ای بنویسید که یک عدد از ورودی بگیرد و فاکتوریل آن را به محاسبه و به خروجی ببرد.
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

**`67`**. برنامه ای بنویسید که مضارب دو رقمی عدد 5 را به خروجی ببرد.
<br />

```python
for i in range(100):
    if i % 5 == 0:
        print(i, end='  ')
```
<br />

---

**`68`**. برنامه ای‌ که‌ خروجی‌ زیر‌ را‌ ایجاد‌می کند.‌
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

**`69`**. بدون استفاده از توابعی نظیر reverse() برنامه ای بنویسید که یک عدد ۵ رقمی از ورودی بگیرد و معکوس آن را در خروجی نمایش دهد.
<br />

```python
n = input("Enter 5-digit number : ")
print(int(n[::-1]))
```
<br />

---

## <a id="70"></a>
**`70`**. یک ماشین حساب ساده بنویسید که :
دو عدد بگیرد و سپس کاربر با انتخاب یکی از عملگر های (`+` ، `–` ، `//` ،` *`) با نتیجه ی دلخواه، روبرو شود.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`71`**. برنامه ای که شکل زیر را درخروجی نمایش دهد:
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

**`72`**. برنامه ای بنویسید که یک رشته را به عنوان ورودی گرفته و تمامی فاصله های موجود در آن را حذف کند.
<br />

```python
join_string = ''.join(input("Enter Your String : ").split())
print(join_string)
```
<br />

---

**`73`**. برنامه ای بنویسید که یک رشته از کاربر بگیرد و اگر دارای حروف صدادار بود، به خروجی ببرد ( حروف صدا دار: `a`, `e`, `i`, `o`, `u`).
همچنین، تعداد تکرار آن حروف را نمایش دهد.
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

**`74`**. الگوریتمی بنویسید که عدد طبیعی N را دریافت کند و معین کند چند رقم ان زوج است و چند رقم ان فرد و چند رقم ان صفر می باشد
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
**`75`**. با یک for برنامه ای بنویسید که : اعداد زوج از ۳۰ تا ۱ را به صورت نزولی، و اعداد فرد از ۱ تا ۳۰ را به صورت صعودی به خروجی ببرد..
نکته: برنامه، فقط با یک حلقه نوشته شود.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`76`**. برنامه ای بنویسید که 2 عدد از ورودی بگیرد و عدد اول را به توان عدد دوم کند.
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

**`77`**. برنامه ای بنویسید که یک عدد دو رقمی بگیرد و:
۱- ابتدا اعداد ماقبل از آن عدد را به خروجی ببرد
۲- سپس اعداد فرد دو رقمی ماقبل از آن عدد و اعداد زوج دو رقمی ماقبل از آن عدد را به خروجی ببرد.
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

**`78`**. برنامه ای بنویسید که یک رشته بگیرد و پالیندرم بودن آن بررسی کند.
(پالیندرم عبارتی است که برعکس آن برابر با خودش باشد مثل: level)
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

**`79`**. برنامه ای بنویسید که درجه فارنهایت یا سانتی گراد را گرفته، و تبدیل کند.
ابتدا باید از کاربر سوال شود که میخواهد فارنهایت را به سانتی گراد یا سانتی گراد را به فارنهایت تبدیل کند و بعد از انتخاب کاربر، عملیات تبدیل را انجام دهد.
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
**`80`**. علی میخواهد برای یک دانشگاه برنامه ای بنویسد که اسامی دانشجویان را بر اساس حروف الفبا مرتب کند.
قرار است برنامه ی او برای لیست حضور و غیاب کلاس های با تعداد ده نفر مورد استفاده قرار بگیرد.
اگر شما به جای او باشید برنامه را به چه صورت مینویسید؟

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`81`**. برنامه ای بنویسید که در یک تابع به تعداد دلخواه ورودی بگیرد؛ ورودی باید از نوع داده ای  تاپل و به صورت رشته باشند و سپس ورودی هایی که پالیندرم هستند را به خروجی ببرد.
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

**`82`**. برنامه ای بنویسید که به تعداد دلخواه ورودی عددی بگیرد و سپس آنها را مرتب شده به خروجی ببرد.
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

**`83`**. برنامه ای بنویسید که یک آرایه ی دو بعدی را به یک آرایه ی یک بعدی تبدیل کند.
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

**`84`**. برنامه ای بنویسید که تعداد اضلاع را دریافت کند و در نتیجه مجموع زوایای داخلی آن را چاپ کند.  
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
**`85`**. برنامه ای بنویسید که یک لیست از اعداد را بگیرد و سپس سه تا سه تا بررسی کند که مجموع کدام سه عدد برابر با عدد 30 می شود و سپس آنها را به خروجی ببرد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`86`**. برنامه ای بنویسید که اعداد فرد دو رقمی را به صورت نزولی به خروجی ببرد.
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

**`87`**. برنامه ای بنویسید که اعداد فرد دو رقمی را به صورت نزولی به خروجی ببرد و هرجا که هر دو رقم فرد شبیه به هم بودند به جای چاپ آن، آنها را درون یک لیست ریخته و سپس در خروجی نمایش بدهد.
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

**`88`**. برنامه ای بنویسید که از ورودی یک عدد بگیرد و به تعداد آن عدد ستاره چاپ.
<br />

```python
star_number = int(input("Please Enter Yur Number : "))
print(star_number * "* ")
```
<br />

---

**`89`**.  برنامه ای بنویسید که مجموع، ماکسیمم، مینیمم، میانگین تعدادی عدد را محاسبه و چاپ کند.
ورودی ها:
ورودی ها شامل تعداد نامشخصی عدد صحیح یا اعشاری است که در سطر های جداگانه داده میشوند.
ورودی گرفتن تا زمانی که کلمه `Done` وارد نشده باشد، ادامه خواهد داشت.
<br />

خروجی:
خروجی برنامه دارای چهار سطر بوده که هر سطر به ترتیب مجموع، ماکسیمم، مینیمم و میانگین اعداد ورودی را نشان میدهد.
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
**`90`**. برنامه ای بنویسید که مضارب سه رقمی عدد ۳ و ۵ را چاپ کند
<br />

```python
three = [i for i in range(1000) if i % 3 == 0]
five = [i for i in range(1000) if i % 5 == 0]
print(f"For Three : {three}")
print(f"For Five : {five}")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`91`**. برنامه ای بنویسید که ۲ عدد از کاربر بگیرد و ۲ عدد را : جمع، تفریق، ضرب و تقسیم کند.
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

**`92`**. برنامه ای بنویسید که یک عبارت رشته ای مثل `45+23` را از ورودی بگیرد و عملیات محاسباتی را براساس عملگر داخل عبارت انجام بدهد (عملگرها شامل `+` ،`/`، `*` ، `-`)
<br />

```python
num = eval(input("Enter Number --> for example --> 23 + 45 : "))
print(num)
```
<br />

---









<!-- 
**``**. 
<br />

```python

```
<br />

--- -->