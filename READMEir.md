
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

## 🤝 مشارکت

__اگر سوالات بیشتری دارید یا می‌خواهید راه‌حل‌های بهتری پیشنهاد دهید، خوشحال می‌شوم که مشارکت کنید! لطفاً یک `Pull Request` ارسال کنید.__
<br />
<br />

---

<a id="go-to-the-question-list"></a>

## ✍️ سوالات را تقسیم بندی کرده ام که هم به سوالات و هم به فهرست دسترسی بهتری داشته باشید.
| `1 - 50` | `55 - 105` | `110 - 160` | `165 - 215` |  |  |  |  |  |  |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| [1](#1) | [55](#55) | [110](#110) | [165](#165) |  |  |  |  |  |  |
| [5](#5) | [60](#60) | [115](#115) | [170](#170) |  |  |  |  |  |  |
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

**`93`**. برنامه ای بنویسید که  دو عدد از ورودی بگیرد و دنباله ی فیبوناچی را از عدد اول تا عدد دوم به خروجی ببرد.
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

**`94`**. برنامه ای بنویسید که در ابتدا تعداد درس های یک دانشجو و تعداد واحد هر درس و نمره هر درس را دریافت نماید و معدل دانشجو را محاسبه کند.
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
**`95`**.  برنامه ای که سال تولد کاربر و سال فعلی را از ورودی خوانده و مشخص
می کند چند سال، چند ماه، چند روز، چند ساعت، چند دقیقه و چند
ثانیه عمر کرده است.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`96`**. مریم دختر اقتصادی هست او میخواد هزینه پیامک های خود راحساب کند

طبف تعرفه اپراتوری که مریم از ان استفاده میکند هزینه اولبه هر پیامک ۱۰۰ ریال میباشد و به ازای هر ۲۴ کاراکتر انگلیسی ورودی ۲۷۴ ریال هم به هزینه اش اضافه میشود (محاسبه هزینه ۲۴ کاراکتر به این صورت است که هزینه روبه پایین گرد میشود  یعنی اگر ۲۳ کاراکتر باشد هزینه ان بخشوده میشود

ورودی این برنامه  متنی است که مریم میخواهد پیامک کند

و خروجی این برامه هرینه نهایی این پیامک هست که برحسب تومان و به اعشاری میباشد

مثال

ورودی

slm bbkhshid shoma?

خروجی

۱۰٫۰
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

**`97`**. یک کلاس برای شکل هندسی مستطیل، با دو متد برای به دست آوردن محیط و مساحت آن تعریف کنید.
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

**`98`**. برنامه ای بنویسید که ۵ نمره ی یک دانشجو را از ورودی دریافت کند، معدل آن را محاسبه و چاپ کند؛
همچنین اگر معدل آن بیشتر از ۱۷ بود پیغام `خیلی خوب`، بین ۱۵ و ۱۷ پیغام `متوسط`، بین ۱۰ و ۱۵ پیغام `بد` و کمتر از ۱۰ پیغام `خیلی بد` چاپ شود. 
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

**`99`**. یک تابع بنویسید که چند ریختی باشد و نهایتا 3 آرگومات بتوان در آن وارد کرد.
<br />

```python
def func_name(x = 0, y = 0, z = 0):
    # if statements:
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`101`**. برنامه ای بنویسید که نمره ده دانش آموز را بگیرد و نشان دهد که کدوم قبول و کدوم مردوده؟ نمرهی قبولی بالا 10 است.
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

**`102`**. برنامه بنوسید که یک عدد سه رقمی از ورودی بخواند و دو برابر عکس آن را درخروجی چاب کند اطمینان کنید که ورودی حتما عدد سه رقمی است در خروجی عدد ضرب ۲ شود.
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

**`103`**. برنامه ای بنویسید که عددی را از کاربر بگیرد تعداد ارقام و سپس جمع ارقام را محاسبه کند.
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

**`104`**. برنامه ای بنویسید که خروجی زیر را به خروجی ببرد.
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
**`105`**. برنامه ای بنویسید که تاریخ تولد را به میلادی گرفته و سن کاربر را در خروجی نمایش دهد. 
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`106`**. برنامه‌ای بنویسید که با دریافت یک عدد فرد مثبت، مثلث الفبایی متناظر آن را چاپ کند.
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

**`107`**. در سال ۲۰۱۳ اولین سال بعد از سال ۱۹۸۷ می باشد که رقم تکراری ندارد . از شما خواسته شده است برنامه‌ای بنویسید تا یک سال را در ورودی از کاربر بگیرد و در خروجی اولین سال بدون رقم تکراری بعد از آن را چاپ کند .
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

**`108`**. برنامه ای بنویسید که تعداد روزهای بین دو تاریخ را به خروجی ببرد.
مثال:
روزهای بین تاریخ `2025-06-01` و `2025-06-09` برابر است با 8 روز.
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

**`109`**. برنامه ای بنویسید که عناصر هر دو لیست زیر را به صورت تاپل های جداگانه با هم تلفیق کند و شرط به خروجی بردن این است که مقادیری که از مقدار 0.9 بیشتر هستند به خروجی بروند.
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
**`110`**. برنامه ای که از کاربر 10 عدد بگیرد و کمترین و بیشترین آنهارا پیدا کند.
<br />

```python
num_list = []
n = int(input("How many numbers should I get? "))
for num in range(1, n + 1):
    num_list.append(int(input(f"{num}. Enter numbers : ")))
print(f"Max is : {max(num_list)}\nMin is : {min(num_list)}")
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`111`**.  برنامه ای بنویسید که 10 مضرب 7 بزرگتر از 200 را چاپ نماید.
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

**`112`**. برنامه ای بنویسید که عدد صحیح n را دریافت کند و یک مثلث قایم ازاویه از ستاره ها در خروجی چاپ کند، بطوریکه n تعداد سطر های مثلث باشد. جهت مثلث به این صورت باشد: 📐
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

**`113`**. برنامه ای بنویسید که 10 عدد را بگیرد در لیست قرار دهد و از انتها به ابتدا چاپ کند.
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
**`115`**. برنامه ای بنویسید که تعدادی عدد مثبت از کاربر دریافت کند و میانگین این اعداد را محاسبه کند (با کمک for و break)یعنی وقتی عدد منفی بود از حلقه خارج شود.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`116`**. پنجعلی یکی از بهترین برنامه نویسان شرکتی در میامی آمریکا می باشد و قرار است برنامه ی زیر را برای دوستش الکس، که به تازگی وارد کلاسهای برنامه نویسی شده است بنویسد؛  برنامه به این شکل است که:
دو لیست از اعداد صحیح، با ۱۰ المان وجود دارد که هر یک از لیست ها دارای اعداد تکراری و غیر تکراری هستند:
حال، تصور کنید به جای پنجعلی هستید و می‌خواهید با استفاده از حلقه یا حلقه ها، المانهای تکراری هر دو لیست را درون لیست اول، و المانهای غیر تکراری آنها را، درون لیست دوم، به صورت مرتب شده به خروجی ببرید.
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

**`117`**. برنامه ای بنویسید که یک لیست از کاربر به تعداد دلخواه گرفته بزرگترین و کوچکترین عنصر ان را پیدا کرده و ان هارا از لیست حذف کند و میانگین بقیه اعداد را به دست اورد(با استفاده از تابع).
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

**`118`**. برنامه ای بنویسید که یک عدد دو رقمی از ورودی بگیرد و آن را دو برابر کند و سپس معکوس آن را در خروجی نمایش بدهد.
<br />

```python
number = int(input("Entr number : "))
print(f"mul : {number} * 2 = {number * 2}\nReverse number : {str(number * 2)[::-1]}")
```
<br />

---

**`119`**. برنامه ای بنویسید که یک عدد سه رقمی از ورودی گرفته در صورتی که رقم پر ارزش و کم ارزش برابر باشد خود عدد در غیر این صورت معکوس عدد چاپ شود.
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
**`120`**. برنامه ای بنویسید که لیست دوم را بر اساس شماره اندیس هایی که در لیست اول قرار دارند، به خروجی ببرد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`121`**. تابعی بنویسید که یک لیست و یک عدد را دریافت کندو هر یک از ایتم های لیست که عدد بودند را با عدد دریافت شده جمع کند سپس لیست را نمایش دهد.
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

**`122`**. برنامه ای بنویسید که عددی را از کاربر بگیرد و نشان دهد که این عدد توانی از ۳ هست یا خیر؟.
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

**`123`**. برنامه ای بنویسید که تعدادی عدد را از کاربر بگیرد و جمع و میانگین آنها را تا زمانیکه کاربر مقدار no را وارد کند محاسبه کند.
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

**`124`**. الگوریتم زیر را به زبان پایتون بنویسید:

۱ نام کاربری را از کاربر دریافت کن

۲ پسورد را از کاربر دریافت کن

۳ اگر نام کاربری برابر با “teacher” و پسورد برابر با “۱۲۳۴۵” بود

چاپ کن welcome to teacher panel

۴ در غیر اینصورت اگر نام کاربری برابر بود با “students” و پسورد برابر بود با “۱۲۳۴۵”

چاپ کن welcome to students panel

۵ در غیر اینصورت چاپ کن
نام کاربری یا پسورد اشتباه است
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
**`125`**.  دو برنامه بنویسید که در یک برنامه سال تولد کاربر را گرفته و سن او را به خروجی میبرد و در برنامه ی دوم سال تولد را به جلالی گرفته و سن را در خروجی نمایش دهد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`126`**. برنامه ای بنویسید که عددی از ورودی خوانده و بزرگترین رقم آن را چاپ کند.
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

**`127`**. برنامه ای بنویسید که عمل ضرب دو عدد را بدون استفاده از عملگرد ضرب انجام دهید.
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

**`128`**. برنامه ای بنویسید که دو عنصر کوچک یک لیست را به خروجی ببرد.
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

**`129`**. برنامه ای بنویسید که تمام اعدادی را که بر ۷ بخش پذیرند اما مضرب ۵ نیستند را پیدا کند.
اعداد به دست آمده باید در یک توالی جدا شده با کاما در یک خط چاپ شوند.
توضیحات تکمیلی:
محدوده ی حرکت روی اعداد، بین ۱۰۰ تا ۲۰۰ باشد.
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
**`130`**. شرکت X با ۷۳ کارمند، قرار است که حقوق کارمندان متاهل خود که همگی حقوق یکسانی دریافت میکنند را به مقدار ۵ درصد افزایش دهد؛
۱. تعداد کارمندان متاهل را حساب کرده، و به خروجی ببرید؛
۲. حساب کنید که برای اضافه حقوق کارمندان متاهل، چه مقدار سرمایه باید به خزانه ی شرکت تزریق شود؛
نکات تکمیلی:
ا _ کارمندان مجرد و متاهل در این سوال، به ترتیب اعداد فرد و زوج می باشند؛
ب _ حقوق پایه برای کارمندان متاهل، ۱۰ میلیون تومان می باشد.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`131`**. برنامه ای بنویسید که دنباله ای از اعداد جدا شده با کاما را از ورودی بپذیرد و یک لیست و یک تاپلی ایجاد کند که شامل هر عدد باشد.
فرض کنید ورودی زیر به برنامه ارائه شده است:
34,67,55,33,12,98
سپس خروجی باید به صورت زیر باشد:
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

**`132`**. برنامه ای بنویسید که رشته ای را خوانده با استفاده از تابع، مجموع ارقام موجود در رشته را محاسبه و چاپ کند.
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

**`133`**. برنامه ای بنویسید که رشته را از ورودی خوانده و تعداد ارقام رشته را نمایش دهد.
<br />

```python
n = input("Enter number : ")
numbers = [int(x) for x in n if x.isdigit()]
print(f"The number is {len(numbers)} digits")
```
<br />

---

**`134`**. اگه یک لیست : [1, 1, 2, 5, 6, 6, 8, 8, 8, 7, 7] داشته باشیم

و بخواهیم از درون آن لیست اعدادی که فقط دو بار تکرار شده اند را بیرون بکشیم باید چه کنیم؟
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
**`135`**. برنامه‌ای بنویسید که یک عدد صحیح را که تعداد ارقامش مشخص نیست از کاربر گرفته و هر رقم را به تعداد آن رقم چاپ کند.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`136`**. برنامه ای بنویسید که از ورودی یک عدد بگیرد و در محدوده ی آن عدد، دیکشنری تولید کند که این دیکشنری حاوی {i : i*i} باشد.
فرض کنید ورودی 8 به برنامه ارائه شده است؛ سپس خروجی باید به صورت زیر باشد:

{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}

در برنامه ی خود، مدیریت خطاهای احتمالی در ورودی را لحاظ کنید.
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

**`137`**. برنامه ای بنویسید که تعداد دانشجویان یک کلاس را دریافت کند.معدل تک تک آنها را به عنوان ورودی دریافت کرده و میانگین معدل کلاس را محاسبه و چاپ نماید.
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

**`138`**. برنامه ای بنویسید که در آن ابتدا سه دیکشنری مانند شکل زیر با مقداری اولیه ایجاد کرده و سپس ترکیب این سه دیکشنری را درون دیکشنری چهارم ذخیره و چاپ کند.

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

**`139`**. اگر اطلاعات نمرات دروس دانشجویان در قالب دیکشنری مانند زیر باشد، می خواهیم برنامه ای بنویسید که به نمره هر فرد یک واحد (یک نمره) اضافه کرده و دیکشنری حاصل را چاپ کند.(به نمرات بالای ۱۹ اضافه نمی شود و ترجیحاً از list comparison استفاده کنید).

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
**`140`**. اگر اطلاعات دانشجویان در قالب لیستی از دیکشنریها مانند زیر قرار داشته باشد، میانگین معدل و بزگترین سن را نمایش دهید.

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`141`**. برنامه ای بنویسید که در یک خط ورودی 5 عدد پیاپی دریافت کند و سپس آنها را در خروجی به صورت مرتب شده نمایش بدهد. 
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

**`142`**. برنامه ای بنویسید که نمره تعدادی دانشجو را از کاربر بگیرد. چنانچه نمره وارد شده بین ۰ تا ۷۰ بود پیغام fail چنانچه نمره وارد شده بین ۷۱ تا ۸۰ بود پیغام good چنانچه نمره وارد شده بین ۸۱ تا ۹۰ بود very good چنانچه نمره وارد شده بین ۹۱ تا ۱۰۰ بود پیغام excellent را نشان دهد.
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

**`143`**. بدون استفاده از ماژولها:

با تابع بازگشتی برنامه ای بنویسید که بتواند فاکتوریل یک عدد که توسط کاربر وارد میشود را محاسبه کند.

همچنین همین برنامه را با Generator Function بنویسید.
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

**`144`**. برنامه ای بنویسید که دنباله ای از کلمات جدا شده اسپیس را به عنوان ورودی بپذیرد و کلمات را پس از حذف همه ی کلمات تکراری و مرتب کردن آنها به صورت الفبایی چاپ کند.

فرض کنید ورودی زیر به برنامه ارائه شده است:

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
**`145`**. کلاسی را تعریف کنید که دو متد داشته باشد:

`get_string` : برای دریافت یک رشته از ورودی

`print_string` : برای چاپ رشته ی ورودی با حروف بزرگ

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`146`**. برنامه ای بنویسید که دنباله ای از کلمات جدا شده با کاما را به عنوان ورودی بپذیرد و کلمات را پس از مرتب سازی بر اساس حروف الفبا در یک دنباله جدا شده با کاما چاپ کند.

فرض کنید ورودی زیر به برنامه ارائه شده است:

`without`, `hello`, `bag`, `world`

سپس خروجی باید به صورت زیر باشد:

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

**`147`**. برنامه ای بنویسید که تمام این اعداد را بین ۲۰۰۰ تا ۴۰۰۱ به خرجی ببرد؛ به طوری که `تمام ارقام` زوج باشند.

اعداد به دست آمده باید در یک توالی جدا شده با کاما در یک خط چاپ شوند.

نمونه خروجی:

… .۲۰۰۶, ۲۰۰۴, ۲۰۰۲

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

**`148`**. با comperhension list برنامه ای بنویسید که ۲ رقم X,Y را به عنوان ورودی دریافت کند و یک آرایه دو بعدی تولید کند.

فرض کنید ورودی های زیر به برنامه داده شده است:

۳،۵

یک تابع بنویسید که خروجی کد بالا را زیر هم نمایش بدهد.
<br />

```python
# for array print
def print_array(array):
    for row in range(1, x + 1):
        print()
        for coll in range(1, y + 1):
            print(coll, end = "\t")
            
x = int(input("Enter x : "))
y = int(input("Enter y : "))
#comprehension list
comperhension_array = [[j for j in range(1, y+1)]for i in range(1, x+1)]
#calling function
print_array(comperhension_array)
```
<br />

---

**`149`**. برنامه ای بنویسید که مجموعه a که شامل یک عدد n رقمی است را بگیرد و با چرخه while و بدون المان دیگری تعداد اعداد(n) را مشخص کند( میتوانیم از تابع هم استفاده کنیم )
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
**`150`**. برنامه ای بنویسید که یک پسوورد از ورودی بگیرد که شامل حروف و اعداد هستند؛ اگر ورودی درست بود به خروجی ببرد و اگر ورودی فقط از اعداد یا از حروف بودند برنامه ادامه پیدا کند تا زمانی که یگ پسوورد صحیح وارد شود.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`151`**. یک لیست کامپرینشن بنویسید که از ورودی یک عدد چند رقمی دریافت کند و بزرگترین رقم آن را به خروجی ببرد.
<br />

```python
print(max([int(i) for i in input("Enter Number : ")]))
```
<br />

---

**`152`**. برنامه ای بنویسید که یک عدد 4 رقمی از ورودی دریافت کند و مشخص کند با 4 رقم آن عدد چند عدد 4 رقمی میتوان تولید کرد و آن عدد ها را به خروجی ببرد.
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

**`153`**. برنامه ای بنویسید که بتواند با  ()map و ()filter لیستی بسازد که عناصر آن مربعی از عدد زوج در این لیست [۱,۲,۳,۴,۵,۶,۷,۸,۹,۱۰] باشد.

نکات:

از map() برای ایجاد لیست استفاده کنید.

از filter() برای فیلتر کردن عناصر یک لیست استفاده کنید.

شما باید از ()filter درون ()map استفاده کنید.

<br />

```python
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list(map(lambda x: x * x, filter(lambda y: y % 2 == 0, lst))))
```
<br />

---

**`154`**. فیلتری بنویسید که فقط در یک خط عملیات زیر را انجام بدهد:

اعداد فرد را از رنج ۱ تا ۲۰ به خروجی ببرد.

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`156`**. برنامه ای بنویسید تا یک تاپل دیگر تولید و چاپ کند که مقادیر آن اعداد زوج در تاپل داده شده باشد

نمونه خرجی:

تاپل داده : (۱،۲،۳،۴،۵،۶،۷،۸،۹،۱۰).

تاپل دوم : (۱۰, ۹, ۸, ۶, ۴, ۲)

نکات:

برنامه با تابع فیلتر نوشته شود.

<br />

```python
print(tuple(filter(lambda x: (x%2==0), range(1, int(input("What is the range of the tuple?  "))+ 1))))
```
<br />

---

**`157`**. برنامه ای بنویسید که یک عدد تصادفی از ۱ تا ۲۰ تولید کند؛

سپس در محدوده ی آن عدد تصادفی، یک تاپل ایجاد کند؛

اگر طول تاپل ایجاد شده زوج باشد، نمیه ی اول و دوم تاپل به صورت جداگانه به خروجی برود؛

و اگر طول تاپل ایجاد شده فرد باشد، نیمه ی اول و نیمه ی دوم و عدد وسط به صورت جداگانه به خروجی بروند.

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

**`158`**. کلاسی را با یک متد جنریتور تعریف کنید که می تواند اعدادی را که بر ۷ بخش پذیر هستند بین محدوده ۰ و n تکرار کند.
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

**`159`**. برنامه ای بنویسید که مقدار خالص یک حساب بانکی را بر اساس گزارش تراکنش از ورودی کاربر محاسبه کند. فرمت گزارش تراکنش به صورت زیر نشان داده شده است:

deposit به معنای سپرده و withdraw

به معنای برداشت است.

فرض کنید ورودی زیر به برنامه ارائه شده است:

deposit 300

deposit 300

withdraw 200

deposit 100

سپس خروجی باید به صورت زیر باشد:

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
**`160`**. از comprehension list برای مربع هر عدد فرد در یک لیست استفاده کنید.

لیست با دنباله ای از اعداد جدا شده با کاما وارد می شود.

فرض کنید ورودی زیر به برنامه ارائه شده است:

۱،۲،۳،۴،۵،۶،۷،۸،۹

سپس خروجی باید به صورت زیر باشد:

۸۱, ۴۹, ۲۵, ۹, ۱

<br />

```python
pow_list = [int(i)**2 for i in input("Enter numbers : ").split(",") if int(i)%2!=0]
print(pow_list)
```
<br />

👆[برو به فهرست](#go-to-the-question-list)

---

**`161`**. برنامه ای بنویسید که جمله را از ورودی بگیرد و تعداد حروف بزرگ و کوچک را محاسبه کنید.

فرض کنید ورودی زیر به برنامه ارائه شده است:

pYthOn ProGraMmiNg

سپس خروجی باید به صورت زیر باشد:

حروف بزرگ ۶

حرف کوچک ۱۱

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

**`162`**. برنامه ای بنویسید که جمله را بپذیرد و تعداد حروف و ارقام و اسپیس را محاسبه کنید.

فرض کنید ورودی زیر به برنامه ارائه شده است:

python programming 123

سپس خروجی باید به صورت زیر باشد:

حروف ۱۷

ارقام ۳

اسپیس ۲

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

**`163`**. برنامه ای بنویسید که تمام اعداد را بین ۲۰۰۰ تا ۴۰۰۱ به خرجی ببرد؛ به طوری که تمام ارقام زوج باشند.

اعداد به دست آمده باید در یک توالی جدا شده با کاما در یک خط چاپ شوند.

نمونه خروجی:

….۲۰۰۶, ۲۰۰۴, ۲۰۰۲
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

**`164`**. برنامه ای بنویسید که دنباله ای از کلمات جدا شده اسپیس را به عنوان ورودی بپذیرد و کلمات را پس از حذف همه ی کلمات تکراری و مرتب کردن آنها به صورت الفبایی چاپ کند.

فرض کنید ورودی زیر به برنامه ارائه شده است:

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
**`165`**. برنامه ای بنویسید که دنباله ای از کلمات جدا شده با کاما را به عنوان ورودی بپذیرد و کلمات را پس از مرتب سازی بر اساس حروف الفبا در یک دنباله جدا شده با کاما چاپ کند.

فرض کنید ورودی زیر به برنامه ارائه شده است:

without, hello, bag, world

سپس خروجی باید به صورت زیر باشد:

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

👆[برو به فهرست](#go-to-the-question-list)

---

**`166`**. کلاسی را تعریف کنید که دو متد داشته باشد:

get_string : برای دریافت یک رشته از ورودی

print_string : برای چاپ رشته ی ورودی با حروف بزرگ
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

**`167`**. با comperhension list برنامه ای بنویسید که ۲ رقم X,Y را به عنوان ورودی دریافت کند و یک آرایه دو بعدی تولید کند.

فرض کنید ورودی های زیر به برنامه داده شده است:

۳،۵

یک تابع بنویسید که خروجی کد بالا را زیر هم نمایش بدهد.
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

**`168`**. برنامه ای بنویسید تا لیستی با ۵ عدد تصادفی بین ۱۰۰ تا ۲۰۰ ایجاد کند.

نکات:

از ()random.sample برای ایجاد لیستی از مقادیر تصادفی استفاده کنید
<br />

```python
from random import sample
print(sample([x for x in range(100, 201)], 5))
```
<br />

---

**`169`**. با استفاده از ژنراتور برنامه ای بنویسید تا اعدادی را که می توانند بر ۵ و ۷ بخش پذیر باشند را در محدوده ی ۰ تا n، تولید و به خروجی ببرد.

مثال:

اگر ۱۰۰ زیر به عنوان ورودی برنامه داده شود:

ظاهر خروجی برنامه دقیقاً باید به صورت زیر باشد:

۰,۳۵,۷۰
<br />

```python
print(list((x for x in range(int(input("Enter number : "))) if x%5==0 and x%7==0)))
```
<br />

---

## <a id="170"></a>
**`170`**. یک لیست کامپرینشن بنویسید که:

یک عدد از ورودی میگیرد و در محدوده ی آن عدد، اولین عدد زوجی که به صورت تصادفی انتخاب میشود را به خروجی ببرد.

نکات:

پس از وارد کردن ماژول در برنامه، کامپرینشن را بااااید در یک خط بنویسید.

مدیریت خطاهای احتمالی را اعمال کنید.

راهنمایی:

برای محاسبه ی اولین عدد زوج تصادفی، میتوانید از ()random.choice کمک بگیرید.
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

👆[برو به فهرست](#go-to-the-question-list)

---

**`171`**. برنامه ای بنویسید که:

۱. یک عدد تصادفی بین ۱ تا ۱۰۰ تولید کند؛

۲. ژنراتوری بنویسید که در محدوده ی عدد تصادفی حرکت کرده و توان ۲ اعداد فرد را محاسبه، و به صورت جدا شده با کاما چاپ کند؛

نکته:

a. خروجی دقیقاً باید شبیه به خروجی زیر باشد.

b. اگر فرضا عدد ۱۰ به صورت تصادفی انتخاب شده باشد، خروجی برنامه باید به صورت زیر باشد: 1,9,25,49,81
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

**`172`**. برنامه ای بنویسید که بتواند با  ()map و ()filter لیستی بسازد که عناصر آن مربعی از عدد زوج در این لیست [۱,۲,۳,۴,۵,۶,۷,۸,۹,۱۰] باشد.

نکات:

از map() برای ایجاد لیست استفاده کنید.

از filter() برای فیلتر کردن عناصر یک لیست استفاده کنید.

شما باید از ()filter درون ()map استفاده کنید.
<br />

```python
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list(map(lambda x: (x*x), filter(lambda y: (y%2==0), lst))))
```
<br />

---

**`173`**. فیلتری بنویسید که فقط در یک خط عملیات زیر را انجام بدهد:

اعداد فرد را از رنج ۱ تا ۲۰ به خروجی ببرد.
<br />

```python
print(list(filter(lambda x: x%2!=0, range(1, 21))))
```
<br />

---

**`174`**. برنامه ای بنویسید که یه عدد تصادفی از ۱ تا ۳۰ تولید کند؛

سپس در محدوده ی آن عدد لیستی از ارقام تولید کند و ارقام مثبت را به خروجی ببرد.

نکته:

برای حل این سوال از  تابع فیلتر استفاده شود.
<br />

```python
import random
print(list(filter(lambda x: (x%2==0), range(1, random.randint(1, 30) + 1))))
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