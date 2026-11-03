---
tags:
  - لغات_برمحية
  - Python
---
## Python 102

### Dates and Numbers | التواريخ والارقام

```python
# لايجاد القيمة المطلقة 
print(abs(-999)) #999
# للتقريب لاقرب رقم صحيح
print(round(3.673)) #4
# للتقريب لاقرب علامه عشرية
print(round(3.673, 2)) #3.67
# لرفع رقم لاس معين 
print(pow(3, 2)) # 9
# لايجاد اكبر قيمة 
print(max(10 , 25 , 9 , 5))#25
# لايجاد اصغر قمية 
print(min(10, 25 ,9 ,5))#5
# لجمع مجموعه من الارقام 
print(sum(10, 5 , 5))#20
# لايجاد الجزر التربيعي يجب استدعاد مكتبة الرياضيات
import math
print(math.sqrt(144))#12.00
# لايجاد باقي القسمة 
import math
print(math.remiander(26, 5))# 1.00
# للحصول على رقم عشوائي
import random
print(random.randint(1,100))#random number
#انشاء تواريخ
import datatime
date = datatime.data(2020, 2, 13)
print(data) #2020-02-13
print(data.year)#2020
print(data.month)#2
print(data.day)#13
# انشاء الوقت
import datatime
time = datatime.time(14, 33 , 15)
print(time)#14:33:15
print(time.hour)#14
print(time.minute)#33
print(time.second)#15
#معرفة الوقت الحالى
import datatime
now =datatime.datatime.today()
print(now)#الوقت الحالى
print(now.year)#السنة الحالية
print(now.month)#الشعر الحالى
print(now.day)#اليوم الحالى
print(now.hour)#الساعه الحالية
print(now.minute)#الدقيقة الحالية
print(now.second)#الثانية الحالية
# تحويل التاريخ الى نص
date = datatime.data(2020, 2, 13)
time = datatime.time(14, 5 , 17)
vvvvvvvvvvvvvvvvv
DATA = data.strftime('%A %8 %Y')
print(DATA)#Thursday February 2020
TIME = time.strftime('%I %M %S')
print(TIME)#02 05 17

```

![image.png](image.png)

### Advanced Sequence | أنواع البيانات المتقدمة بشكل اعمق

- مفهوم indexing الوصول الى العناصر في List, stirng, tuple
    - العد في لغات البرمجة يبدأ من 0 واذا اردت البدء من الاخير فالعد من -1
    
    ```python
    #تعبر عن index باقواس مربعه []
    alphabet = "abcdefghijklmnopqrstuvwxyz"
    print(alphabet[0])#a
    the_list = [1, 2 , 3]
    the_tuple = (1, 2, 3)
    print(the_list[1])#2
    print(the_tuple[-2])#2
    ```
    
- مفهوم slicing الوصول الى نطاق معين من العناصر بدلا من عنصر واحد
    - 
    
    ```python
    #نطاق مغلق [from نفس النقطه: to ما قبلها]
    text = "this is python cousre"
    print(text[8:14])#python
    # نطاق مفتوح [from : ]
    #او [ ;to]
    #او [:]
    text = "this is python cousre"
    print(text[8:])#python cousre
    print(text[:14])#this is python
    print(text[:])#this is python cousre
    print(text[-6:])#cousre
    the_list = [1, 2 , 3, 4, 5]
    the_tuple = (1, 2, 3, 4, 5)
    print(the_list[2:])#[3, 4, 5]
    print(the_tuple[:2])#(1, 2, 3)
    print(the_list[:])#[1, 2 , 3, 4, 5]
    print(the_tuple[-3:])#(3, 4, 5)
    #[from:to:step]
    alphabet = "abcdefghijklmnopqrstuvwxyz"
    print(alphabet[0:7:2])#aceg
    print(alphabet[5:0:-1])#fedcb
    the_list = [1, 2 , 3, 4, 5,6]
    the_tuple = (1, 2, 3, 4, 5, 6)
    print(the_list[3:0:-2])#[4, 2]
    print(the_tuple[-1:-6:-2])#(6, 4, 2)
    
    ```
    
- الدالة slicing
    - 
    
    ```python
    alphabet = "abcdefghijklmnopqrstuvwxyz"
    print(alphabet[0:5])#abcde
    s= slice(0, 5)
    print(alphabet[s])#abcde
    s= slice(0, 5, 2)
    print(alphabet[s])#ace
    the_list = [1, 2 , 3, 4, 5, 6]
    the_tuple = (1, 2, 3, 4, 5, 6)
    s= slice(0, 5, 2)
    print(the_list[s])#[1, 3, 5]
    print(the_tuple[s])#(1, 3, 5)
    ```
    
- الدالة index
    - البحث عن عنصر معين موجود ام لا اذا كان موجود ستعطيني رقم الindex له واذا لا ستعطي error
    - هذه الداله تعطي اول تطابق لا غير
    
    ```python
    text= "lorem ipsum dolor sit amet, consecteur adioiscing elit, sed do"
    the_list = [1, 2 , 2, 3]
    the_tuple = (4, 5)
    
    print(text.index("do"))#12
    print(text.index("DO"))#Error
    print(the_list.index(2))#1
    print(the_tuple.index(4))#0
    
    ```
    
- الدالة len
    - عدد العناصر
    
    ```python
    alphabet= "abcdefghijklmnopqrstuvwxyz"
    the_list = [1, 2 , 3, 4]
    the_tuple = (1, 2, 3)
    print(len(alphabet))#26
    print(len(the_list))#26
    print(len(the_tuple))#26
    
    ```
    
- الدالة count
    - كم مره تكرر العنصر المعين
    
    ```python
    the_string= "This is the student Noora"
    the_list= [1, 2, 2 ,3, 3, 3, 3]
    the_tuple= (4, 4, 4, 4, 5, 5, 5, 5, 5)
    print(the_string.count("s"))#3
    print(the_string.count("S"))#0
    print(the_string.count("Noora"))#1
    print(the_list.count(2))#2
    print(the_tuple.count(4))#4
    ```
    
- المعامل in
    - عنصر ما أو مجموعة من العناصر المعينة موجودة ام لا
    
    ```python
    text= "lorem ipsum dolor sit amet, consecteur adioiscing elit, sed do"
    print("do" in text)#true
    print("DO" in text)#false
    print("do" not in text)#false
    the_list= [1, 2, 3]
    the_tuple= (4, 5)
    print(1 in the_list)#true
    print(1 not in the_tuple)#true
    
    ```
    
- الدمج والتكرار
    - 
    
    ```python
    n1= "Eslam"
    n2= 'Ahmed'
    print(n1 + n2)#EslamAhmed
    print(n1 + ' ' +n2)#Eslam Ahmed
    print(n1*3)#EslamEslamEslam
    l1= [1, 2, 3]
    l2=[4, 5, 6]
    t1= (1, 2, 3)
    t2=(4, 5, 6)
    print(l1 +l2)#[1, 2, 3, 4, 5, 6]
    print(t1 +t2)#(1, 2, 3, 4, 5, 6)
    print(l1*3)#[1, 2, 3, 1, 2, 3, 1, 2, 3]
    ```
    

### Advanced String | النصوص  بشكل اعمق

- البحث ياستخدام الدالة find
    - البحث عن نص معين
    - اذا وجد ستعطينه index
    - اذا لا -1
    
    ```python
    text= "lorem ipsum dolor sit amet, consecteur adioiscing elit, sed do"
    print(text.find('do'))#12
    print(text.rfind('do'))#12 اخر تطابق
    print(text.find('DO'))#-1
    print(text.find('it', 50, 60))#53
    ```
    
- تحويل النص الى قائمة
    - split()
    - يفصل عن وجود مسافة
    - تكتب القيمة التي يراد الفصل عندها وتختفي من القائمة
        
        ```python
        text= 'A, B, C'
        stl= text.split()
        print(stl)#['A, ', 'B, ', 'C']
        stl2= text.split(',')
        print(stl2)#['A', ' B', ' C']
        tex2t= 'This is a string'
        stl3= tex2t.split('s')
        print(stl3)#['thi', ' i', ' a ', ' tring]
        stl3= tex2t.split('s', 1)
        print(stl3)#['thi', 'is a string]
        ```
        
- التحويل الى نص
    - join()
    - تحويل List، Tuple و Dictionary
    
    ```python
    the_list=['A', 'B', 'C']
    lts= ' '.join(the_list)
    print(lts)#A B C
    lts= '#'.join(the_list)
    print(lts)# A#B#C 
    ```
    
- التحقق من النص
    - نص ام ارقام ام حروف كبيرة ام صغيرة
    
    ```python
    v= "A987"
    print(v.isalnum())#ture تحتوي على حروف وارقام فقط
    print(v.isdigit())#false هل تحتوي على ارقام فقط
    ```
    
    ![image.png](image%201.png)
    
- الدالة replace
    - أخذ نص معين والتغيير عليه
    
    ```python
    values = '1\n2\n3\n4'
    print(values)
    #1
    #2
    #3
    #4
    print(values.replece('\n', ','))#1,2,3,4
    print(values.replece('\n', ',', 2))
    #1,2
    #3
    #4
    ```
    
- الدالة strip
    - ازالة المسافات أو نص معين
    
    ```python
    teee = "    py   "
    print(teee.strip())#py
    print(teee.lstrip())#py   
    print(teee.rstrip())#    py
    ```
    
- التلاعب في النص
    - 
    
    ```python
    sss = "This is Python"
    print(sss.upper())#THIS IS PYTHON
    print(sss.lower())#this is python
    print(sss.swapcase())#tHIS IS pYTHON
    print(sss.title())#This Is Python
    ```
    
- مفهوم Raw string
    - R, r
    
    ```python
    ss = '\t Python'
    print(ss)#   Python
    ss1 = r'\t Python'
    print(ss1)#\tPython
    sss = 'c:\\xfolder\\xsub\\txt.f'
    print(SSS)#c:\xfolder\xsub\txt.f
    ss2 = r'c:\xfolder\xsub\txt.f'
    print(SS2)#c:\xfolder\xsub\txt.f
    s1 = r'\'
    print(s1)#error 
    ```
    
- الدالة format
    - 
    
    ```python
    f_na ='eslam'
    l_na ='ahmed'
    age = 21
    print('im {} {}, and im {} '.format(f_na, l_na, age))
    #im eslam ahmed, and im 21
    print('im {2} {1}, and im {0} '.format(f_na, l_na, age))
    #im 21 ahmed, and im eslam
    print('im {ff} {ll}, and im {aa} '.format(ff=f_na, ll=l_na, aa=age))
    #im eslam ahmed, and im 21
    print(f'im {f_na} {l_na}, and im {age} ')
    #im eslam ahmed, and im 21
    #str = {:s}
    #num = {:d}
    #float = {:f}
    #{:_d}555_111_444
    #{:.2f}10.00{:3f]10.000
    #{index:.2f}
    #python{:.2s} py
    
    ```
    

### Advanced Lists | القوائم  بشكل اعمق

- القوائم ثنائية الابعاد
    - 
    
    ```python
    vv = [1, ture, 'py']
    print(vv[0])#1
    v1 = [[1, 2, 3], ture, 'py']
    print(v2[0])#[1, 2, 3]
    v2 = [[1, 2, 3], ture, 'py']
    print(v2[0][2])#3 
    v3 = [[1, 2, 3],
    			[4, 5, 6],
    			[7, 8, 9]
    			]
    print(v3[1][1])#5
    ```
    
- الدالة filter
    - تستقبل مدخلين
    - داله تحتوي على شرط وقائمة
    - والعناصر التي تتطابق مع الشرط هتطبع
    
    ```python
    age = [30, 9, 15, 22, 17, 44, 26, 5]
    #طريقة عادية
    adults = []
    
    def filtered_ages(ages):
    		for age in ages:
    				if age >= 18:
    						adults.append(age)
    						
    		return adults
    		
    print(filtered_ages(ages))#[30, 22, 44, 26]
    
    #طريقة الدالة filter
    def filtered_ages(ages):
    		return age >= 18
    print(filter(filtered_ages, ages))
    #filrer object at dgfgasgnfig
    print(list(filter(filtered_ages, ages)))
    #[30, 22, 44, 26]
    ```
    
- الدالة map
    - تستقبل function, list
    - والعناصر التي تتطابق مع الشرط هتطبع
    
    ```python
    numbers = [5, 10, 20, 25, 50]
    #طريقة طويلة
    sq_numbers = []
    
    def square(numbers):
    		for num is numbers:
    				sq_numbers.append(num**2)
    				
    		return sq_numbers
    		
    print(sq_numbers)#[25, 100, 400, 625, 2500]
    
    #طريقة الدالة map
    def square(numbers):
    		return num ** 2
    print(map(square, numbers))##filrer object at dgfgasgnfig
    print(list(map(square, numbers)))
    #[25, 100, 400, 625, 2500]
    ```
    
- الدالة sort
    - ترتب تصاعديا
    - تنازلي باستخدام reverse
    
    ```python
    l1 = [9, 5, 1, 8]
    l2 = ['eslam', 'ahmed', 'sss']
    print(l1.sort())#[1, 5, 8, 9]
    print(l2.sort())#['ahmed', 'eslam', 'sss']
    print(l1.sort(reverse=ture))#[9, 8, 5, 1]
    print(l2.sort(reverse=ture))#['sss', 'eslam', 'ahmed']
    
    ```
    
- الدالة reverse
    - 
    
    ```python
    n1 = ['a', 'b', 'c', 'd']
    print(n1.reverse())#['d', 'c', 'b', 'a']
    ```
    
- مفهوم list comprehension
    - انشاء قائمة بداخلها قائمة موجوده
    
    ```python
    lst = [1, 2, 3, 4]
    #طريقة طويلة
    multiplied_list = []
    
    for num in lst:
    		multiplied_list.append(num*2)
    
    print(multiplied_list)#[2, 4, 6, 8]
    
    #طريقة list comprehension
    multiplied_list = [num*2 for num in lst]
    print(multiplied_list)#[2, 4, 6, 8]
    
    #طريقة طويلة مع شرط معين
    multiplied_list = []
    
    for num in lst:
    		if(num > 3):
    		multiplied_list.append(num*2)
    
    print(multiplied_list)#[8]
    
    #طريقة list comprehension
    multiplied_list = [num*2 for num in lst if num > 3]
    print(multiplied_list)#[8]
    
    #طريقة طويلة مع اكثر من شرط معين
    multiplied_list = []
    
    for num in lst:
    		if(num > 3) and num % 5 == 0:
    		multiplied_list.append(num*2)
    
    print(multiplied_list)#[10]
    
    #طريقة list comprehension
    multiplied_list = [num*2 for num in lst if num > 3 and num % 5 == 0]
    print(multiplied_list)#[10]
    ```
    

### Advanced Functions | الدوال  بشكل اعمق

- مفهوم Positional Arguments
    - تعرف ايضا بRequired Argument
    - يتم تمرير المدخلات يتم استقبالاها بنفس الترتيب الموجود في الباراميتر
    - يجب ان تتوافق عدد المدخلات مع عددها في تعريف الداله
    - 
    
    ```python
    def info (name, age)
    	print('my name is ' ,+ name +, 'and I am ' ,age, 'years old') #my name is Eslam and I am 21 years old
    	
    info ('Eslam', 21)
    
    info (21, 'Eslam')#my name is 21 and I am Eslam years old وهذا خاطئ
    
    ```
    
- مفهوم Keyword Arguments
    - هي تزويد الدالة بالبيانات عن طريق كتابة اسم الباراميتر متبوعه بالقيمة التي سيأخذها
    - لا يفرق فيها ترتيب لاني كتبت المتغير وقيمته ولكن يجب ان يكون بنفس المسمي والعدد
    - لو عابز poistinal argument وkeyword مع بعض لازم ال poisitional يبقي الاول  ويجب ان اعدلها ايضا في تعريف الداله
    
    ```python
    def info (name, age)
    		print('my name is ' ,+ name +, 'and I am ' ,age, 'years old') #my name is Eslam and I am 21 years old
    	
    info (name = 'Eslam', age = 21)
    info (age = 21 , name = 'Eslam')# هي هي
    
    def info (ageو name)
    	print('my name is ' ,+ name +, 'and I am ' ,age, 'years old') #my name is Eslam and I am 21 years old
    	
    info (21, name = 'Eslam')#poistional -> keyword
    ```
    
- مفهوم Default Parameter
    - عندما يقوم المبرمج بعمل الداله ممكن يعطي قيم افتراضية للباراميتر وسيتم تمرير هذه القيم ما لم يتم تمرير
    - ممكن تاخد مدخل واحد والباقي من الاعداد الافتراضي
    - ويرتب مثل poisitional ما لم اكتبها مثل keyword
    
    ```python
    def info (name = ُ'Mohamed', age = 14, course = 'c')
    		print('my name is ' ,+ name +, 'and I am ' ,age, 'years old and I am taking about ',+ course +,'course') #my name is Mohamed and I am 14 years old and I am taking about c
    
    info ()
    def info (name = ُ'Mohamed', age = 14, course = 'c')
    	print('my name is ' ,+ name +, 'and I am ' ,age, 'years old and I am taking about ',+ course + ,'course') #my name is Eslam and I am 21 years old and I am taking about Python
    info (name = 'Eslam', age = 21)
    ```
    
- مفهوم Argument Packing
    - استقبال عدد غير محدد من المدخلات في الباراميتر واحد
    - يقوم هذا الباراميتر بحفظهم علي شكل tuple
    - 
    
    ```python
    def (x,y,z)
    #a اصبحت الدالة لحساب متوسط 3 اعداد فقط
    #b لن تعمل الدالة عند تمرير اكثر من 3 اعداد
    
    def (x, y=0,z=0)
    #c لن تعرف الداله على اي عدد تقسم
    
    def (nums_list)# المدخل على هيئة قائمة 
    #d سيتوجب علي مستخدم دالتك ان يعلم انه عليه ان يجمع ارقامه في قائمة
    #e الحل هو packing
    
    def foo(*param) : #(*) يدل علي اني سوف استقبل عدد غير محدود من المدخلات
    		pass
    
    foo(x,y,z,....,n)
    #ex
    def avg(*args):
    		total = sum(agrs)
    		leng = len(args)
    		
    		average = total / leng
    		
    		print(average)
    		print(type(args))
    
    avg(2,6)#4.0
    avg(2,6,4)#4.0
    #tuple
    ```
    
- مفهوم Argument UnPacking
    - هو فصل العناصر في list,tuple, sting واستخدام عناصؤها في poisitional argument
    - 
    
    ```python
    def info (name1, name2, name3)
    		print("First Student's name: " , name1)
    		print("First Student's name: " , name2)
    		print("First Student's name: " , name3)
    
    names = 'Ahmed' , 'Eslam' , 'Mohamed'
    info (names[0], names[1], names[2]) #تساوي اللي تحتها
    info (*names)
    ```
    
- استخدام Packing و Unpacking
    - في نفس الوقت
    
    ```python
    def my_func (*items):
    		print(items)
    my_func('a', 'b', 'c') # ('a', 'b', 'c') tuple
    
    def my_func (*items):
    		print(items)
    items = ['a', 'b', 'c']
    my_func(items) #['a', 'b', 'c'] list تم اخذه كمدخل واحد وهو 
    
    def my_func (*items):
    		print(items)
    items = ['a', 'b', 'c']
    my_func(*items) #('a', 'b', 'c') تم اخذها كمداخل منفصله 
    ```
    
- مفهوم Dictionary Packing
    - استقبال keyword arguments في باراميتر على شكل قاموس dictionary
    - لتطبيقها يتم استخدام (**)
    - الاسم في keyword arguments يقابله اسم key في dictionary
    - والقيمة في keyword arguments يقابلها القيمة value في dictionary
    - تستخدم التسمية (kwargs) عادةً لتسمية الباراميتر في هذا المفهوم
    - هذه الداله لا تستقبل poisitional argument
    - لا يوجد حد للمدخلات التي سوف تكتبها
    
    ```python
    def info(**kwargs)
    		print(kwargs)
    		print(type(kwargs))
    		
    info(name = 'Eslam' , age= 21)#{'name': 'Eslam' , 'age': 21} <class 'dict'>
    
    def info(**kwargs)
    		print('My name is' , kwargs['name'])
    		
    info(name = 'Eslam' , age= 21)#My name is Eslam
    ```
    
- مفهوم Dictionary Unpacking
    - سيتم تفكيك القاموس كأني ممرته ك keyword arguments
    
    ```python
    def info(name, age):
    		print('my name is ' ,+ name +, 'and I am ' ,age, 'years old')
    		
    d = {'name': 'ahmed', 'age': 21}
    info(**d)	
    ```
    

### Project Python 102

## **بنهاية هذا المشروع سيكون الطالب قادرًا على**:

1. التعامل مع التواريخ Dates.
2. التعامل مع الأرقام Numbers.
3. التعامل مع أنواع البيانات المتقدمة Sequence والدوال الخاصة بها.
4. التعامل مع الدوال بشكل أعمق.

## المتطلبات Requirements

قم ببناء برنامج يقوم باستقبال عدد لا محدود من أسماء الأشخاص مع 
أعمارهم. يقوم البرنامج بحساب العُمر، بحيث يقوم باستقبال التاريخ، ويعود 
لنا بالعُمر الحالي، كذلك اسم اليوم الذي وُلد فيه. يقوم البرنامج أيضًا 
بطباعة عمر أكبر شخص وأصغر شخص، ومجموع الأشخاص الذين تم تمريرهم. في حال 
تم تمرير شخص واحد فقط، لا يتم حساب أكبر وأصغر شخص، ويتم طباعة العبارة `There is no oldest or youngest person`.
يتم أيضًا التأكد من قيمة التاريخ، أي أن قيمة السنة، الشهر واليوم يجب أن تكون قيم صحيحة (مثال: قيمة الشهر `14` غير صحيحة)، وأيضاً لا تحتوي على رموز أو قيم سالبة، وفي حال ذلك يتم إرجاع الرسالة `Invalid date`، مصحوبًا باسم الشخص ذو التاريخ الخاطئ.

## مثال:

**المُدخلات**

- khalid, 1-2-1989
- Nouf, 2-9-2004
- Ali, 9-12-2009

**المُخرجات المتوقعة**

```python
Khalid is 31 years old and she/he was born on Saturday
Nouf is 16 years old and she/he was born on Thursday
Ali is 11 years old and she/he was born on Wednesday
The oldest one is Khalid
The youngest one is Ali
Total People: 3
```

**ملاحظة**

- المخرجات أعلاه تم حسابها بناءً على التاريخ 2021-1-1
- التاريخ أعلاه يتبع النظام dd-mm-yyyy

## أسئلة إضافية:

- قم بترتيب الأشخاص من الأكبر للأصغر وطباعة نتيجتهم.
- قم بطباعة نفس المدخلات التي تم تمريرها، ولكن بشكل عكسي.
- قم بطباعة أسماء الأشخاص الذين ولدوا في يوم الأحد فقط.

---
