---
tags:
  - Python
  - لغات_برمحية
مسار التعلم: سطر.كود
مسار: AI
---


مسار: AI
مسار التعلم: سطر.كود

## Python 101

### Variables | المتغيرات

طرق الكتابة

```python
name = "d"
age = 14
name , age = "d" , 14
```

### **Inputs and Outputs | المدخلات والمخرجات**

طرق الكتابة 

```python
input()
# يكمن كتابةالمطلوب من المستخدم داخلها
input("input your name")
# نضعه في متغير 
name = input("input your name")
print("hallo" , name)
```

### Operators Type | انواع المعاملات

المعاملات الحسابيّة Arithmetic Operators

```python
#الجمع
result = 2 + 5
#الطرح
result = 4 - 10
#الضرب
result = 2 * 2
#القسمة
result = 2 / 6
#باقي القسمة
result = 10 % 3
print(result)
# هناك ايضا اختصارات مثل اختصار هذه المعادلة 
result = 10
result = result - 5
#في هذه المعادلة
result -= 5

```

معاملات المقارنة Comparison Operators

```python
#معامل التساوي
result = 6 == 3
print(result)
#معامل عدم التساوي
result = 8 != 7
print(result)
#معامل اكبر من
result = 3 > 2
print(result)
#معامل اصغر من 
result = 1 < 4
print(result)
# معامل اكبر من او يساوي
result = 3 >= 3
print(result)
#معامل اصغر من او يساوي
result = 7 <= 3
print(result)
```

المعاملات المنطقية Logical Operators

```python
#معامل And
not_raining = True
not_foggy = True
is_sunny = not_raining and not_foggy
print(is_sunny) #Ture
#قيمة واحدة صحيحه والباقي خطأ
#معامل Or
is_raining = True
is_foggy = False
not_sunny = is_raining or is_foggy
print(not_sunny) #Ture
#قيمة واحدة خطأ والباقي صحيح
#معامل Not
is_student = True
print(not is_student) #Flase
#يغير القمية من صحيحه الى خطأوالعكس
```

### Data Types | انواع  البيانات

- النوع String: يمثل هذا النوع البيانات النصيّة مثل
- النوع Integer: يمثل هذا النوع البيانات الرقميّة من الأعداد الصحيحة
- النوع Float: يمثل هذا النوع البيانات الرقميّة من الأعداد ذات النقاط العشرية
- النوع Complex: يمثل هذا النوع البيانات الرقمية من الاعداد المركبة
- النوع Boolean: يمثل هذا النوع إحدى القيمتين True أو False.
- النوع None: يدل هذا النوع على عدم وجود قيمة.

```python
name = 'Ahmed' #<class 'Str'>
age = 20 #<class 'int'>
age = 20.00 #<class 'Float'>
num = 15j #<class 'complex'>
is_student = True #<class 'bool'>
is_employee = False #<class 'bool'>
home_address = None #<class 'none'>
```

str() داله تقوم بتحويل البيانات الى string

int() دالة تقوم بتحويل البيانات الى integer

float() دالة تقوم بتحويل البيانات الى float

### **Advanced Data Type | أنواع البيانات المتقدمة**

sequence هو متغير به مجموعه من البيانات على هيئة

- list
    - 
    
    ```python
    names = [ "eslam" , 20 , True , 4.9 ]
    #يمكن تعديل القوائم بعد انشائها
    #تعتبر نوع من انواع البيانات
    print(type(names)) #<calss 'list' >
    #index هو موقع العنصر في القائمة فالعنصر الاول 0 والثاني 1 وهكذا
    print(names[2]) # True
    #لتغيير عنصر معين 
    names[1] = "Ahmed"
    print(names) # [ eslam , Ahmed , True , 4,9 ]
    #الدالة append() تضيف عنصر الى نهاية القائمة 
    names.append(20)
    print(names) #[ "eslam" , "Ahmed" , True , 4,9 , 20]
    #الدالة insert(index , value) تستقبل قيمتين الموقع المراد اضافة العنصر به والعصنر
    names.insert(2 , "Mohamed")
    print(names) #[ "eslam" , "Ahmed" , "MOhamed" , True , 4,9 , 20]
    #الدالة remove( value ) تقوم بحذف عنصر  معين من الدالة
    names.remove(4.9)
    print(names) #[ "eslam" , "Ahmed" , "MOhamed" , True , 20]
    #الدالة clear() تقوم بمسح جميع عناصر القائمة 
    names.clear()
    print(names) #[]
    ```
    
- tuple
    - 
    
    ```python
    co = ( "Eslam" , 20 , "ahmed" )
    # لا يمكن التعديل عليها بعد انشائها 
    #تعتبر نوع من انواع البيانات
    print(type(co)) #<calss 'tuple' >
    #index هو موقع العنصر في القائمة فالعنصر الاول 0 والثاني 1 وهكذا
    print(names[2]) # Ahmed
    # لا يمكن استخدام دوال الاضافة والحذف 
    # يمكن كتابتها بدون الاقواس
    co = "Eslam" , 20 , "ahmed"
    print(type(co)) #<calss 'tuple' >
    ```
    
- ****Dictionary
    - 
    
    ```python
    p = {"name" : "Eslam" , "age" : 20 }
    #وصول اكثر سهولة للبيانات الضخمة
    # تعتبر نوع من انواع البيانات 
    print(type(p)) #<class 'dict'>
    # للوصول الى عنصر استخدم المفتاح الخاص به 
    print(p["name"])
    # الدالة values() تقوم باحضار جميع عناصر القاموس
    print(p.vlaues) #dict_values(['Eslam', 20])
    # الدلة keys() لطباعة جميع مفاتيح الوصول الموجوده في القاموس
    print(p.keys) #dict_keys(['name', 'age'])
    #لا يمكن أن يحتوي القاموس على عنصرين بنفس المفتاح
    ```
    

### Condition | الشروط

if statement | الجمل الشرطية

```python
path = "computer"
#if الشرط . المتغير:
if path == "computer":
	print("web dev") #hi
#elif اذا كنت ترغب في اضافة اكثر من شرط
#elif الشرط . المتغير:
elif path == "ios":
	print("photograph")
elif path == "android":
	print("games")
#else في حال أردنا تنفيذ أمر برمجي مُعيّن عند عدم تحقق الشرط
else:
	print("fi") #web dev
# مللاحظة يجب ان تكون نفس الدالة
```

### Loop | التكرار

عندما نريد طباعة امر برمجي اكثر من مرة

```python
#while دالة تكرار وتكتب على الهيئة التالية
pp = 1 
while pp <= 5:
	print(pp)
	pp+= 1 
#سيقوم بطباعة المتغير عدد لا نهائي من المرات فاذا كنت تريد الى حد معيد ضع السطر الخامس

#for العصنر in المتغير:
# يقوم بطباعة عنصر واحد من الدالة في  كل دورة
gg = [ "qw" , "we" , "er" ]
for s in gg:
	print(s)

#for in range() تقوم بطباعة على حسب النطاقات
# عند طلب طباعة 10 فانه يعاملها على انها index
for q in range(10):
	print(q) # 0 , 1 , 2 , .... , 9
#range(start, end , step)
#range(start , end)
```

### Functions | الدوال

الدالة عبارة عن مجموعة من الأوامر البرمجيّة مصممة لأداء مهمة معينة ويتم تنفيذ الدالة عند استدعائها باسمها، وتهدف الدوال إلى تقسيم الأوامر البرمجيّة الكبيرة إلى مجموعات صغيرة تتشارك لتكون برنامجًا واحدًا.

```python
# هي مجموعة من الاومر البرمجية لا تنفذ الا عند استدعائها
# def اسم الدالة():

def cut(): 
	name = input("Enter your Name ")
	time = input("Enter the Time ")
	print("good " + time + "," +name + "!")

cut() #good night,Eslam! 

# يمكن استدعاء الدالة في اي وقت واي مكان في الكود وحتي اكثر من مره
# عند التعديل على الدالة يتم تعديل مخرجات الاستدعائات ايضا
# وتعد ميزه وعيب في نفس الوقت

# يمكن استقبال مدخلات في الدالة عن طريق الاقواس
# def اسم الدالة(qاسم المتغير):

def print_number(s):
		for i in range(s):
				print(i)
#سيقوم بطباعة الدالة من index 0 حتي قيمة المتغير المكتوبه 
print_number(9)
print_number(5)
print_number(2)

# يمكن ان تستقبل اكثر من مدخل ارقام او نصوص
def s(num1 , num2):
		print(num1 +num2)

s(1, 4) #5
s("Hi ","p") #Hi p

# return امر ارجاع الاستدعاء فعند استدعاء الدالة يقوم براجاع القيم ثم يقوم بحسابها
def qq(n1 , n2):
		ra = n1 + n2
		return ra
	
value = qq(1,2)
print(value)#3
# يمكن ايضا
value2 = qq(1,2) + qq(1,2)
print(value2)#6

# يمكن استخدام مخرجات دالة كمدخلات داله اخري
print_number(value)
```

### Project Python 101

- مشروع
    
    **نهاية هذا المشروع سيكون الطالب قادرًا على**
    
    1. فهم آلية عمل الدوال.
    2. التعامل مع القواميس Dictionary.
    3. استخدام loop مع Dictionary.
    4. فهم طريقة عمل loop مع if statement.
    
    # **المتطلبات Requirements**
    
    قم ببناء برنامج يُمثل دليل الهاتف، بحيث يقوم باستقبال رقم الهاتف، ويعود لنا باسم صاحب الرقم يُمكن الاستعانة بالجدول التالي:
    
    | **الاسم** | **الرقم** |
    | --- | --- |
    | Amal | 1111111111 |
    | Mohammed | 2222222222 |
    | Khadijah | 3333333333 |
    | Abdullah | 4444444444 |
    | Rawan | 5555555555 |
    | Faisal | 6666666666 |
    | Layla | 7777777777 |
    
    في حال تم إرسال رقم موجود في الدليل سيتم طباعة اسم صاحب الرقم المُدخل، وفي حال تم إدخال رقم غير موجود بدليل الهاتف، تطبع الرسالة:
    
    ```python
    Sorry, the number is not found
    
    ```
    
    في حال كان رقم الهاتف أقل أو أكثر من ١٠ أرقام، أو قيمة أُخرى (يحتوي على أحرف ورموز وقيم منطقيّة على سبيل المثال) سيتم طباعة الجملة:
    
    ```python
    This is invalid number
    
    ```
    
    أسئلة إضافيّة:
    
    - البحث باسم الشخص.
    - اجعل البرنامج يقوم بالسماح للمستخدم بإضافة مستخدم جديد مع رقمه للدليل.
- حل المشروع
    
    ```python
    phone_book = {
        "1111111111": "Amal",
        "2222222222": "Mohammed",
        "3333333333": "Khadijah",
        "4444444444": "Abdullah",
        "5555555555": "Rawan",
        "6666666666": "Faisal",
        "7777777777": "Layla"
    }
    # دالة التحقق من صحة الرقم 
    def is_valid_number(number):
        count = 0
        for char in number:
            count += 1
        if count != 10:
            return False
        for char in number:
            if char < '0' or char > '9':
                return False
        return True
    # دالة البحث عن الاسم باستخدام الرقم 
    def find_name_by_number():
        phone_number = input("Enter the phone number: ")
        if is_valid_number(phone_number):
            for number in phone_book:
                if phone_number == number:
                    print(phone_book[phone_number])
                    return
            print("Sorry, the number is not found")
        else:
            print("This is invalid number")
    
    دالة البحث عن الرقم باستخدام الاسم
    
    def find_number_by_name():
        name = input("Enter the name:")
        for number, owner in phone_book.items():
            if owner == name:
                print(number)
                return
        print("Sorry, the name is not found")
    
    دالة إضافة جهة اتصال جديدة
    
    def add_new_contact():
        new_name = input("Add new name:")
        new_number = input("Add new number:")
        if is_valid_number(new_number):
            phone_book[new_number] = new_name
            print("Contact added successfully!")
        else:
            print("This is invalid number")
    
    استدعاء الدالات
    
    find_name_by_number()
    find_number_by_name()
    add_new_contact()
    ```
    
- اجابتي
    
    ```python
    phone_book = {
          "1111111111": "Amal",
          "2222222222": "Mohammed",
          "3333333333": "Khadijah",
          "4444444444": "Abdullah",
          "5555555555": "Rawan",
          "6666666666": "Faisal",
          "7777777777": "Layla"
    }
    
    #a دالة التحقق من الرقم 
    def check_number (number) :
        count = 0
        for i in number:
            count += 1
        if count != 10:
            return False
        for i in number:
            if char < '0' or char > '9':
                return False
        return True
    
    #b دالة البحث عن الاسم باستخدام الرقم
    def find_name_by_num () :
        phone_number = input("Enter the phone number: ")
        if check_number(phone_number):
            for number in phone_book:
                if phone_number == number:
                    print(phone_book[phone_number])
                    return
            print("Sorry, the number is not found")
        else:
            print("This is invalid number")
    
    #c دالة البحث عن الرقم باستخدام الاسم
    def find_num_by_name ()
        name = input("Enter the name:")
        for number, owner in phone_book.items():
            if owner == name:
                print(number)
                return
        print("Sorry, the name is not found")
    
    #d دالة اضافة جهة اتصال جديدة
    
    def add_new_content ()
        new_name = input("Add new name:")
        new_number = input("Add new number:")
        if is_valid_number(new_number):
            phone_book[new_number] = new_name
            print("Contact added successfully!")
        else:
            print("This is invalid number")
    
    #e استدعاء الدالات
    find_name_by_num ()
    find_num_by_name ()
    add_new_content ()
         
          
    ```
    

