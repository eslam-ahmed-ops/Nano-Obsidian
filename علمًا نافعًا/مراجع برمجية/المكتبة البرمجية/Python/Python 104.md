
## Python 104

### Intro to Scope

- مفهوم scope
    - عند تعريف اي متغير في الكود سيكون هناك نطاق يقدر يوصله وهذا هو المنظور
    - ولا نقدر نوصل للمتغير خارج النطاق
    
    ```python
    
    ```
    
- مفهوم Local Scope
    - حدود محدوده لا يمكن الوصول اليها خارج النطاق
    
    ```python
    def func():
    		name = "Eslam"
    		print(name)
    		
    func()#Eslam
    print(name)#Erro
    name = "A"
    print(name)#A
    ```
    
- مفهوم Global Scope
    - نقدر نوصل للمتغير من اي مكان في الكود
    
    ```python
    name = "Eslam"
    def func()
    		print(name)
    		
    func()#Eslam
    print(name)#Eslam
    
    ```
    
- الكلمة المحجوزة Global
    - للوصول للمغير المحلي وجعله عالمي نستخدم كلمه global ويكتب بعدها اسم المتغير المراد جعله عالمي
    
    ```python
    def func():
    		global name
    		name = "Eslam"
    		print(name)
    		
    func()#Eslam
    print(name)#Eslam
    ```
    

### Intro to Module

- مقدمة في Module
    - عباره عن ملف بايثون يحتوي على مجموعه من اكواد بايثون ويكون له نفس الامتداد
    - يساعدنا على تقسيم البرنامج الى عدة اقسام على عدة ملفات بدل ملف واحد
    - نتوجه الى مجلد المشروع وننشأ ملف ونجعل امتداده .py
    
    ```python
    def hi():
    		print("hello")
    		
    def print_name(name):
    		print("hello, " + name)
    ```
    
- استخدام import
    - لاستخدام module نتجه الى ملف الاكواد الرئيسي او اي ملف ونكتب import name_module
    - ونكتب اسم الmodule وجوارها نقطه وسيظهر كل الدوال الموجوده بها
    - ستقوم import باستدعاء كل الدوال والاكواد بالموديول في الملف
    
    ```python
    import mymodule
    mymodule.hi()#hello
    ```
    
- استخدام Form , import
    - استخراج كود او داله معينه من الموديول دون باقي الاجزاء نستخدم كلمه From لكتابة اسم الامديول وimport لاستخدام اسم الدالة في المراد استخداماه
    - لاستخدام اكثر من داله نستخدم الفاصله بين اسماء الدوال
    - وعند استدعاء دالة واحده لا يشترط كتابة اسم الموديول ثم نقطه واسم الدالة
    
    ```python
    from mymodule import print_name, hi
    
    mymodule.print_name()#error
    print_name("Eslam")#hello, Eslam
    ```
    
- استخدام as
    - لاعادة تسمية اسم المديول في ملف واحد ولن يتغير اسمه الفعلي نستخدم as ثم نكتب الاسم المستعار
    
    ```python
    import mymodule as Eslam
    mymodule.hi() #Error
    Eslam.hi()#hello
    ```
    

### Intro to File

- مقدمة في Files
    - سنتعلم كيفية عمل ملف باي امتداد وكيفية التعامل معه
    
    ```python
    
    ```
    
- فتح ملف
    - open(”file name”,”mode”)
    - تستخدم لفتح او انشاء ملف
    - نقدر ندخل اكثر من مدخل في الدالة ولكن سنتعامل مع مدخلين اسم الملف في المدخل الاول وmode وهو مدخل اختيار سيتيح لنا كيفية التعامل مع الملف
    - ويجب كتابة اسم الملف مع امتداده
    - اما في mode سمكن كتابة حرف واحد مثل “r” ومعناه قراءه الملف فقط وهي ايضا القيمة الافتراضية  للمود حتلى لو لم نكتبها
    - اما “w” فهي للكتابة في الملف وسيقوم بحذف الاكواد الموجوده فيه عند الكتابة ولو الملف مش موجو سوف ينشأه
    - اما “x” انشاء ملف لو غير موجود
    - اما “a”فتح الملف للكتابه عليه في اخره ولو كان غير موجود سوف ينشأه
    
    ```python
    file = open("n.txt", "w")
    ```
    
- الكتابة على الملف
    - 
    
    ```python
    file = open("n.txt", "w")
    file.write("hello world")# سيفتح الملف وسنكد الكلمة مكتوبه به
    ```
    
- القراءة من الملف
    - 
    
    ```python
    file = open("n.txt", "w")
    print(file.read())# سوف يكتب في terminal الكلمات الموجوده في الملف دون فتح الملف
    # a يمكن تمرمر ارقام داخل الداله وسيقوم بطباعة عدد الاحرف المكتوبه 
    print(file.read(2))#he
    ```
    
- اغلاق الملف
    - 
    
    ```python
    file = open("n.txt", "w")
    file.close() #سيغلق الملف
    ```
    

### Intro to Excption Handing

- مقدمة في Excption Handing
    - انواع الاخطاء
    - كتابة امر من اوامر اللغة بشكل خاطئ syntax error
    - طوقع نتيجة وتظهر نتيجه اخري logical error
    - يحدث خطأ اثناء حدوث البرنامج مثل عندما يقسم المستخدم على صفر في برنامج الاله Exception error
    
    ```python
    prit("hi")#syntax error
    n = input()#1
    m = input()#2
    print(n + m)#12 logical error 
    
    ```
    
- استخدام try, except
    - لحل المشكلة نكتب في الدالة try كل الاحتمالات الوارد حدوث بها خطأ ويكتب معها except او finally
    - اما داخل except نكتب جملة طباعة وقت حدوث الخطأ
        
        ```python
        try: 
        		n1 = int(input("Enter num 1: "))
        		n2 = int(input("Enter num 2: "))
        		print("the result = " + n1/n2)
        
        except: 
        		print("Error!")
        		
        print("End of program")
        ```
        
- استخدام else
    - في حال عدم وجود اي خطأ نكتب بها ماذا نريد ان يحدث
    
    ```python
    try: 
    		n1 = int(input("Enter num 1: "))
    		n2 = int(input("Enter num 2: "))
    		print("the result = " + n1/n2)
    
    except: 
    		print("Error!")
    		
    else:
    		print("No Error")
    ```
    
- استخدام finally
    - في حال حدوث او عدم حدوث خطأ نكتب هذه الدالة
    
    ```python
    try: 
    		n1 = int(input("Enter num 1: "))
    		n2 = int(input("Enter num 2: "))
    		print("the result = " + n1/n2)
    
    except: 
    		print("Error!")
    		
    else:
    		print("No Error")
    		
    finally:
    		print("End of program")
    ```
    
- استخدام except مع تحديد نوع الخطأ
    - يمكن اضافة اكثر من except لتحديد نوع الخطأ
    
    ```python
    mylist = [1, 2, 0]
    
    try:
    		print("the result = ", mylist[4] / mylist[2])
    		
    except ZeroDivisionError:
    		print("zeroDivisionError!")
    		
    except IndexError:
    		print("IndexError!")
    ```
    
- استخدام assert
    - هو امر ي حال عدم حدوث الشرط يعمل استثناء
    - نريد ان نضع استثناء في حال عدم حدوث الشرط ينفذ except
    - في حال النتيجة fulse ينفذ except وفي حال true ينفذ try
    
    ```python
    try:
    		n= int(input("Enter a num: "))
    		assert num %2 == 0
    except: 
    		print("not an even number")
    else:
    		evenNumber = n / 2
    		print(evenNumber)
    ```
    
- استخدام raise
    - نريد ان نضح استثناء في حال عدم حدوث الشرط يوقف البرنامج
    - 
    
    ```python
    age = int(input("Enter your age: "))
    
    if age < 18:
    		raise Exception("sorry, this game for more than 18 age")
    		
    print("start game")
    #sorry, this game for more than 18 age
    #start game
    age = int(input("Enter your age: "))
    
    if age < 18:
    		raise Exception("sorry, this game for more than 18 age")
    		
    print("start game")
    
    #error
    #Exception: sorry, this game for more than 18 age
    ```
    

### Intro to Synchronous , Asynchronous

- مقدمة في Synchronous , Asynchronous
    - ا. synchronous : هو تنفيذ الاوامر سطر بسطر بالترتيب ولا ينفذ الامر التالى الا عند الانتهاء من الامر الحالى
    - ب. asynchronous : هو تنفيذ الاوامر بطريقة غير متزامنه بحيث كل امر من الكود لا يعتمد على الثاني
    - مثلا هناك داله تتنفذ يمكن وقف هذه الدالة وننفذ دالة اخري ثم نستأنف الدالة الموقوفه
    
    ```python
    
    ```
    
- مقدمة في Synchronous
    - 
    
    ```python
    def main():
    		print('hi')
    		print("Welcome to world!")
    		
    def name():
    		print('Eslam')
    		
    def sync():
    		main()
    		name()
    		
    	
    sync()
    #hi
    #Welcome to world!
    #Eslam
    ```
    
- مقدمة في Asynchronous
    - تنفيذ الاكواد بطريقه غير متزامنه
    - كل امر من الاوامر لا يعتمد على الامر الذي قبله
    - لتنفيذ هذه الخاصية نحتاج استخدام مكتبة من مكاتب بايثون وهي (docs.python.org/3/library/asyncio.html)
    - سيعطيك اوامر وشرح كيفية تطبيق
    - يجب استخدام async قبل تعريف الدالة لتنفيذها بشكل غير متزامن
    - يستخدم امر await بعد تنفيذ الامر في السطر ال4 انتظر وبعدها نحدد الوقت الذي سينتظره بالامر الموضح تاليا
    - ومثلا نكتب انتظر الى حين تنفيذ داله معينه
    
    ```python
    import asyncio
    
    async def main():
    		print('Hello ...')
    		await asyncio.sleep(1)
    		print('... World!')
    		
    #python 3.7+
    asyncio.run(main())
    ```