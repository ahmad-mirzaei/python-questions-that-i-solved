
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

**`20`**.  برنامه ای‌ که‌ یک ‌عدد‌ چهار رقمی‌ را‌ خوانده، ‌اگر‌ حاصل‌ ضرب رقم های‌ ‌اول‌ و‌ چهارم،‌
برابر‌ حاصل‌ جمع‌ ارقام‌ دوم‌ و‌ سوم‌ باشد‌ `Yes` و گرنه‌، `No` را‌ نمایش ‌میدهد‌‌‌
<br />

```python
number = [int(i) for i in input("Please enter a four-digit number : ")]
print("YES") if number[0] * number[3] == number[1] + number[2] else print("NO")
```
<br />

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


<!-- 
**``**. 
<br />

```python

```
<br />

--- -->