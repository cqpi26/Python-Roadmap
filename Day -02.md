markdown
# 🐍 Day 2: Variables & Data Types (A to Z Complete Guide)

> **📅 তারিখ:** [এখানে আজকের তারিখ লিখো]  
> **🎯 লক্ষ্য:** Variable কী, কীভাবে তৈরি করে, Data Type কী কী এবং কীভাবে ব্যবহার করে — সম্পূর্ণ শেখা।  
> **⏱️ সময়:** প্রায় ২-৩ ঘণ্টা  
> **👨‍💻 লেখক:** Muttakin Ahemed

---

## 📖 সূচিপত্র

1. [Variable কী?](#১-variable-কী)
2. [Variable তৈরি ও ব্যবহার](#২-variable-তৈরি-ও-ব্যবহার)
3. [Variable Naming Rules](#৩-variable-naming-rules)
4. [Data Type কী?](#৪-data-type-কী)
5. [Python-এর প্রধান Data Types](#৫-python-এর-প্রধান-data-types)
6. [Type Checking ও Type Conversion](#৬-type-checking-ও-type-conversion)
7. [Constants](#৭-constants)
8. [ইন্টারভিউ প্রশ্ন ও উত্তর](#৮-ইন্টারভিউ-প্রশ্ন-ও-উত্তর)
9. [প্র্যাকটিস টাস্ক](#৯-প্র্যাকটিস-টাস্ক)
10. [সারসংক্ষেপ](#১০-সারসংক্ষেপ)

---

## ১. Variable কী?

**Variable** হলো একটি **নামযুক্ত মেমোরি লোকেশন**, যেখানে আমরা ডেটা সংরক্ষণ করি। সহজ কথায়, Variable হলো একটি **বাক্স**, যার একটি নাম আছে এবং ভেতরে আমরা মান (value) রাখি।

### বাস্তব উদাহরণ:
ভাবো, তোমার একটি বাক্স আছে যার গায়ে লেখা `age`। সেই বাক্সের ভেতরে তুমি `20` রাখলে। এখন `age` বললেই কম্পিউটার `20` বের করে আনবে।

```python
age = 20
name = "Muttakin"
এখানে:

age এবং name হলো Variable

20 এবং "Muttakin" হলো Value

= হলো Assignment Operator (মান বসানোর চিহ্ন)

Python-এ Variable-এর বৈশিষ্ট্য:
Python Dynamically Typed — অর্থাৎ Variable-এর Type আলাদা করে বলতে হয় না, মান দিলেই Type বোঝা যায়।

Variable ব্যবহারের আগে Declare করতে হয় না।

Variable-এর Type পরিবর্তনযোগ্য (একই Variable-এ পরে ভিন্ন Type-এর মান রাখা যায়)।

python
x = 10       # x এখন Integer
x = "hello"  # x এখন String (Type পরিবর্তন হয়ে গেল)
২. Variable তৈরি ও ব্যবহার
Syntax:
python
variable_name = value
উদাহরণ:
python
# Variable তৈরি
name = "Muttakin"
age = 22
height = 5.8
is_student = True

# Variable ব্যবহার
print(name)
print(age)
print(height)
print(is_student)
আউটপুট:
text
Muttakin
22
5.8
True
একাধিক Variable একসাথে তৈরি:
python
x, y, z = 10, 20, 30
print(x, y, z)
আউটপুট: 10 20 30

একই মান একাধিক Variable-এ:
python
a = b = c = 100
print(a, b, c)
আউটপুট: 100 100 100

Variable-এর মান পরিবর্তন:
python
score = 50
print(score)   # 50

score = 75
print(score)   # 75 (নতুন মান বসে গেল)
Variable দিয়ে অঙ্ক:
python
a = 10
b = 20
sum = a + b
print("Sum:", sum)
আউটপুট: Sum: 30

৩. Variable Naming Rules
Python-এ Variable-এর নাম দেওয়ার কিছু নিয়ম আছে:

নিয়ম	উদাহরণ (✅ সঠিক)	উদাহরণ (❌ ভুল)
অক্ষর বা _ দিয়ে শুরু হবে	name, _age	1name, $age
সংখ্যা মাঝে/শেষে থাকতে পারে	name1, age_2	1name
শুধু A-Z, a-z, 0-9, _ ব্যবহার হবে	my_var	my-var, my var
Case Sensitive	Name ও name আলাদা	—
Keyword ব্যবহার করা যাবে না	my_if	if, for, class
ভালো অভ্যাস:
Snake Case ব্যবহার করো: student_name, total_marks

অর্থপূর্ণ নাম দাও: x এর বদলে age লেখো

ছোট হাতের অক্ষরে লেখো

python
# ভালো
student_name = "Muttakin"
total_marks = 450

# খারাপ
sn = "Muttakin"
tm = 450
৪. Data Type কী?
Data Type হলো এক ধরনের মান (value) যা একটি Variable ধারণ করে। Python-এ প্রতিটি মানের একটি নির্দিষ্ট Type আছে।

কেন Data Type জানা দরকার?
কোন Operation করা যাবে তা নির্ধারণ করে

Memory কতটা লাগবে তা ঠিক করে

Code-এ Bug কমায়

৫. Python-এর প্রধান Data Types
Python-এ প্রধানত ৫টি Built-in Data Type আছে:

(১) Integer (int)
সম্পূর্ণ সংখ্যা (positive, negative, zero)।

python
age = 22
marks = -50
big_number = 1000000

print(type(age))   # <class 'int'>
(২) Float (float)
দশমিক সংখ্যা।

python
height = 5.8
pi = 3.14159
price = -99.99

print(type(height))   # <class 'float'>
(৩) String (str)
অক্ষর, শব্দ, বাক্য — যা ' ' বা " " এর ভেতরে থাকে।

python
name = "Muttakin"
city = 'Dhaka'
message = "I am learning Python"

print(type(name))   # <class 'str'>
(৪) Boolean (bool)
শুধু দুটি মান — True বা False।

python
is_student = True
is_logged_in = False

print(type(is_student))   # <class 'bool'>
(৫) NoneType (None)
কোনো মান নেই বোঝাতে ব্যবহার হয়।

python
result = None
print(type(result))   # <class 'NoneType'>
এক নজরে সব Data Type:
Type	উদাহরণ	ব্যবহার
int	10, -5, 0	গণনা, বয়স
float	3.14, -0.5	উচ্চতা, দাম
str	"hello", 'a'	নাম, বাক্য
bool	True, False	শর্ত (Condition)
NoneType	None	খালি মান
আরও কিছু Data Type (পরে বিস্তারিত আসবে):
list — [1, 2, 3]

tuple — (1, 2, 3)

set — {1, 2, 3}

dict — {"name": "Muttakin"}

৬. Type Checking ও Type Conversion
Type Checking:
type() ফাংশন দিয়ে কোনো Variable-এর Type জানা যায়।

python
x = 10
print(type(x))       # <class 'int'>

y = "hello"
print(type(y))       # <class 'str'>
Type Conversion (Casting):
এক Type থেকে অন্য Type-এ রূপান্তর করা।

(১) Integer-এ রূপান্তর:
python
x = int(3.7)        # 3 (দশমিক কেটে ফেলে)
y = int("100")      # 100
print(x, y)
(২) Float-এ রূপান্তর:
python
x = float(10)       # 10.0
y = float("3.14")   # 3.14
print(x, y)
(৩) String-এ রূপান্তর:
python
x = str(100)        # "100"
y = str(3.14)       # "3.14"
print(x, y)
(৪) Boolean-এ রূপান্তর:
python
x = bool(1)         # True
y = bool(0)         # False
z = bool("")        # False
w = bool("hello")   # True
print(x, y, z, w)
⚠️ সতর্কতা:
python
x = int("hello")   # ❌ Error: invalid literal for int()
শুধু সংখ্যা-সদৃশ স্ট্রিং-কেই Integer-এ রূপান্তর করা যায়।

৭. Constants
Constant হলো এমন একটি মান যা পরিবর্তন হয় না। Python-এ আলাদা Constant Type নেই, তবে Convention হলো সব বড় হাতের অক্ষরে লেখা।

python
PI = 3.14159
MAX_SIZE = 100
GRAVITY = 9.8
💡 Note: Python-এ Constant আসলে পরিবর্তন করা যায়, কিন্তু Convention অনুযায়ী এটি পরিবর্তন করা উচিত নয়।

৮. ইন্টারভিউ প্রশ্ন ও উত্তর
প্রশ্ন ১: Python-এ Variable কী?
উত্তর: Variable হলো একটি নামযুক্ত মেমোরি লোকেশন, যেখানে ডেটা সংরক্ষণ করা হয়। Python-এ Variable Declare করতে হয় না, মান দিলেই তৈরি হয়।

প্রশ্ন ২: Python কি Statically Typed না Dynamically Typed?
উত্তর: Python Dynamically Typed। অর্থাৎ Variable-এর Type আগে থেকে বলে দিতে হয় না; মান দিলেই Type নির্ধারিত হয়।

প্রশ্ন ৩: Python-এর প্রধান Data Types কী কী?
উত্তর: int, float, str, bool, NoneType। এছাড়াও list, tuple, set, dict।

প্রশ্ন ৪: type() ফাংশন কী করে?
উত্তর: type() কোনো Variable বা মানের Data Type জানায়। যেমন: type(10) → <class 'int'>।

প্রশ্ন ৫: Type Conversion কী?
উত্তর: এক Data Type থেকে অন্য Data Type-এ রূপান্তর করাকে Type Conversion বা Casting বলে। যেমন: int("100") → 100।

প্রশ্ন ৬: int(3.9) এর ফলাফল কী?
উত্তর: 3।因为它 দশমিক অংশ কেটে ফেলে (Round করে না)।

প্রশ্ন ৭: bool("") এবং bool("hello") এর ফলাফল কী?
উত্তর: bool("") → False (খালি স্ট্রিং), bool("hello") → True (অখালি স্ট্রিং)।

প্রশ্ন ৮: Python-এ Constant কীভাবে লেখে?
উত্তর: Python-এ Constant-এর আলাদা সাপোর্ট নেই, তবে Convention হলো সব বড় হাতের অক্ষরে লেখা। যেমন: PI = 3.14159।

প্রশ্ন ৯: a = b = c = 10 এর মানে কী?
উত্তর: তিনটি Variable a, b, c — সবগুলোতেই 10 রাখা হলো।

প্রশ্ন ১০: Variable Name if দেওয়া যাবে কি?
উত্তর: না। if হলো Python-এর Reserved Keyword, তাই এটি Variable Name হিসেবে ব্যবহার করা যাবে না।

৯. প্র্যাকটিস টাস্ক
টাস্ক ১: বেসিক Variable তৈরি
নিচের Variable তৈরি করে প্রিন্ট করো:

তোমার নাম (String)

তোমার বয়স (Integer)

তোমার উচ্চতা (Float)

তুমি স্টুডেন্ট কি না (Boolean)

python
# তোমার কোড এখানে লেখো
name = "Muttakin Ahemed"
age = 22
height = 5.8
is_student = True

print("Name:", name)
print("Age:", age)
print("Height:", height)
print("Student:", is_student)
প্রত্যাশিত আউটপুট:

text
Name: Muttakin Ahemed
Age: 22
Height: 5.8
Student: True
টাস্ক ২: Type Check
নিচের প্রতিটি মানের Type type() দিয়ে প্রিন্ট করো:

python
a = 100
b = 3.14
c = "Python"
d = False
e = None

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
প্রত্যাশিত আউটপুট:

text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
<class 'NoneType'>
টাস্ক ৩: Type Conversion
নিচের Conversion করো এবং প্রিন্ট করো:

python
# String থেকে Integer
x = int("50")
print(x, type(x))

# Integer থেকে String
y = str(100)
print(y, type(y))

# Float থেকে Integer
z = int(9.99)
print(z, type(z))

# Integer থেকে Float
w = float(5)
print(w, type(w))
প্রত্যাশিত আউটপুট:

text
50 <class 'int'>
100 <class 'str'>
9 <class 'int'>
5.0 <class 'float'>
টাস্ক ৪: Variable Swap (বোনাস)
দুটি Variable-এর মান অদল-বদল করো:

python
a = 10
b = 20
print("আগে:", a, b)

# Swap
a, b = b, a
print("পরে:", a, b)
প্রত্যাশিত আউটপুট:

text
আগে: 10 20
পরে: 20 10
টাস্ক ৫: চ্যালেঞ্জ (নিজে করো)
নিচের কোডটি লিখে আউটপুট কী আসে দেখো:

python
x = 10
y = 3
result = x / y
print(result)
print(type(result))

result2 = x // y
print(result2)
print(type(result2))
💡 ইঙ্গিত: / দশমিক ফল দেয়, // শুধু পূর্ণসংখ্যা দেয়।

১০. সারসংক্ষেপ
✅ Variable কী এবং কীভাবে তৈরি করে

✅ Variable Naming Rules

✅ Python-এর ৫টি প্রধান Data Type: int, float, str, bool, NoneType

✅ type() দিয়ে Type Checking

✅ int(), float(), str(), bool() দিয়ে Type Conversion

✅ Constant কীভাবে লেখে

✅ ১০টি ইন্টারভিউ প্রশ্ন ও উত্তর

✅ ৫টি প্র্যাকটিস টাস্ক
