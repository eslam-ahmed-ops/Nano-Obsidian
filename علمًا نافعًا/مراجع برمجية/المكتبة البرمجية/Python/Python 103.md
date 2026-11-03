## Python 103

### Intro for object oriented programming

- مقدمة عن البرمجة الكائنية
    - هي افضل من البرمجة الاجرائية في لغات مثل C التي تستخدم الدوال كمعرف رئيسي لها وهي لا ت
    - اما في البرمجة الكائنية فهي صنعت لتحقيق اسطر اقل من الكود وتعزيز اعادة استخدامه
    - يعتمد على class الوحدة الاساسية في النمط
    
    ```python
    
    ```
    
- مقدمة عن class و object
    - اClass هو المخطط او الهيكل العام يتم انشاء Objects عن طريقه
    - اObject هو كيان حقيقي تم انشاءه من هذا الهيكل Class
    
    ```python
    #a مثال 
    name 
    age 
    number 
    #هذه class 
    # اما
    name = "Eslam"
    age = 21
    number = 123
    # اسلام و 21 و123 هي object
    # ال Class  الواحد يقدر يطلع اكتر من object
    ```
    
- مقدمة عن attrinutes و Methods
    - الخصائص او (attrinutes) يدل على اي خاصية تقوم بوصف class
    - ال(Methods) هو اي سلوك يقوم به class معين ويتم تمثيلها بالدوال ولكن تسمي في class بال methods
    
    ```python
    
    ```
    
- اشاء Class
    - اي كلمة في الclass يبدأ بحرف كبير وينتهي ب:
    
    ```python
    class Student :
    	 #لما نيجي نكتب الخصائص في الكلاس ننشيء هذه الدالة ولكي نكتب الخصائص نكتبها في الاقواس
    	 def _init_(self, name, age, id, grades) :
    			 self.name = name
    			 self.age = age
    			 self.id = id
    			 self.grades = grades
    			
     # create the methods
    	 def talk(self) :
    			 print('My name is ', self.name)
    	 
    ```
    
- انشاء Object
    - لانشاء object اكتب اسمه ثم  اسم class الذي سنحرر object منه ثم سنمرر قيم الخصائص منه
    
    ```python
    class Student :
    	 def _init_(self, name, age, id, grades) :
    			 self.name = name
    			 self.age = age
    			 self.id = id
    			 self.grades = grades
    			
    	 def talk(self) :
    			 print('My name is: ', self.name)
    			 
    std1 = Student('Eslam', 21, 'xx00', 95) #انشئنا 
    print (std1.name)#Eslam
    std1.talk()#My name is: Eslam
    ```
    
- نظرة على Self
    - كل دالة او methods في class لازم تستقبل متغير اسمه self
    - ويجب ان يكون اول متغير في الدالة ولا يجب ان تسمي self ممكن تسمي اي شيء وستؤدي نفس الغرض ولاكن اجعلها self افضل
    - هوعباره عن object الذي قام باستدعاء methods في هذه النقطة
    - اي ان object في std1.talk() هو من قام باستدعاء الدالة talk اذن قيمة الself تشير الى object std1
    - وعند تشغيلها سيمرر لنا اماكن حفظ هذه object في الذاكره
    
    ```python
    class Student :
    		def talk(x) :
    			  print(x)
    
    std1 = Student()
    std2 = Student()
    
    std1.talk() #<__main__.Student object at 0x1d1d151d5153>
    std2.talk() #<__main__.Student object at 0x1dr3efed5153>
    ```
    
- مفهوم Constructor الجزء الاول
    - كل ما ننشأ class سنضطر لمئ كل خاصية على حدي
    - والافضل ان نمرر قيم الخصائص في الobject عند انشائه
    - وهو يتم عن طريق مفهوم constructor
    
    ```python
    class Student :
    	 def talk(self) :
    			 print('My name is: ', self.name)
    					
    std1 = Student()
    
    std1.name = 'Eslam'
    std1.age = 21
    std1.id = 'xx00'
    std1.grages = 95
    ```
    
- مفهوم Constructor الجزء الثاني
    - ال constructor هو مفهوم شائع في الغات كائنية التوجه
    - هي دالة يتم استدعائها تلقائيا بشكل مباشر عند انشاء ال object
    - وفي بايثون تعرف بالدالة _init_ وهي اختصار ل  initionalisation
    - في حال لم تكن الدالة init موجوده في class لن يتم استدعائها عند انشاء object
    - يستفاد منها بتهئية الخصائص attributes بنفس وقت انشاء objects
    
    ```python
    #best ways
    class Student :
    	 def talk(self) :
    			 print('My name is: ', self.name)
    					
    std1 = Student("Eslam", 21, "xx00", 95)
    #print(std1.name)#error
    
    class Student :
    	 def _init_(self, name, age, id, grades) :
    			 self.name = name
    			 self.age = age
    			 self.id = id
    			 self.grades = grades
    			 
    	 def talk(self) :
    			 print('My name is: ', self.name)
    			 
    std1 = Student("Eslam", 21, "xx00", 95)
    print(std1.name)#Eslam
    ```
    
- مفهوم Encapsulation
    - عندما يتم انشاء class يتقم عزل الخصائص والدوال في مكان واحد هذا المكان يسمي Encapsulation
    - وعند التغليف يتم حجب البيانات عن باقي الكود
    - يدعم Data integrity لكي لا يجعل اي شيء يقوم بتغيير البيانات المخزنه داخله
    - سهوله التواصل عن طريق Founction Interface وهذا يسهل تفاصيل الخوض في فهم هذا الكود
    - مثل عندما نقوم استخدام زر تشغيل السياره (interface) ولن نخوض في تفاصيل كيف يقوم الزر بتشغيل السياره
    - يعتبر التغليف قيد اختياري وليس اجباري يمكن استخدامه او لا
    
    ```python
    class
    {
    	Attributes + Methods
    }
    ```
    
    - Project
        - project
            
            ## بنهاية هذا المشروع سيكون الطالب قادرًا على:
            
            1. معرفة الفرق بين نمط البرمجة كائنية التوجه Object Oriented Programming والبرمجة الإجرائية.
            2. إنشاء Class.
            3. إنشاء Object.
            4. التعامل مع الخصائص Attributes و Methods الخاصة في Objectمُعين.
            5. تطبيق المفهوم Encapsulation.
            
            ## المتطلبات Requirements
            
            الكود الموضح أدناه يمثل وصف للخصائص والسلوك الخاص بالدراجة في المصنع ذلك الوصف يتضمن:
            
            - خصائص الدراجة، مثل الوصف description، التكلفة cost، سعر البيع sale price، وحالة الدراجة condition.
            - إنشاء الدراجة في المصنع.
            - تحديث سعر الدراجة.
            - بيع الدراجة.
            
            تم كتابة الكود بنمط **البرمجة الإجرائية Procedure Oriented Programming** قم بإعادة كتابته ولكن باتباع نمط
              **البرمجة كائنية التوجه Object Oriented Programming**.
            
            ```python
                def update_sale_price(bike, sale_price):
                    if bike['sold'] == True:
                        print('Action not allowed, Bike has already been sold')
                    else:
                        bike['sale_price'] = sale_price
            
                def sell(bike):
                    bike['sold'] = True
            
                def create_bike(description, cost, sale_price, condition):
                    return {
                        'description': description,
                        'cost': cost,
                        'sale_price': sale_price,
                        'condition': condition,
                        'sold': False
                    }
            
                bike1 = create_bike('Univega Alpina, orange', cost=100, sale_price=500, condition=0.5)
                update_sale_price(bike1, 350)
                sell(bike1)
            ```
            
        - my sulotion
            
            ```python
            class Bike :
            			#attributes خصائص الدراجة
            			def _init_(self, description, cost, sale_price, condition, sold)
            					self.descripion = description
            					self.cost = cost
            					self.sale_price = sale_price
            					self.condition = condition
            					slef.sold = False
            			
            			#b دالة تحديث سعر الدراجة
            			def update_sale_price(self, new_price):
            					if self.sold :
                        print(f"Action not allowed: Bike '{self.description}' has already been sold.")
                    else:
                        self.sale_price = new_price
                        print(f"price updata for ' {self.description}' to: {self.sale_price}")
                  
                  #c دالة حالة البيع
                  def sell(self):
                      if self.sold:
            		         print("This bike is already marked as sold.")
            		       else :
            					      self.sold = True
            					      print(f"Bike '{self.discription}' has been sold successfully!")
            					      
            #d استدعاء الدوال وانشاء الكائن
            bike1 = Bike("Hyper, Red", 100, 500, 0.5)
            bike1.updata_sale_price(350)
            bike1.sell()
            #e تحديث بعد البيع
            bike1.updata_sale_price(400)
            
            ```
            
    

### Attributes and Methods | الخصائص والدوال

- الدالة dir
    - يرجع نفس الخصائص التي اخذها object من ال class
    
    ```python
    class Student:
    		def _init_(self, name, age, id, grades):
    				self.name = name
    				self.age = age
    				self.id = id
    				self.grades = grades
    		
    		def talk(self):
    				print("my name is: ", self.name)
    
    std1 = Student(Eslam, 21, "xx00", [99, 98, 95])
    std2 = Student(Ahmed, 30, "xx01", 97)
    
    print(dir(std2))
    ```
    
- اضافة Attribute
    - اضافة خاصية اخري لكائن بدون التأثير على الكائنات الاخري
    
    ```python
    class Student:
    		def _init_(self, name, age, id, grades):
    				self.name = name
    				self.age = age
    				self.id = id
    				self.grades = grades
    		
    		def talk(self):
    				print("my name is: ", self.name)
    
    std1 = Student(Eslam, 21, "xx00", [99, 98, 95])
    std2 = Student(Ahmed, 30, "xx01", 97)
    
    std2.v_hours = 16
    
    print(dir(std1))# لم تضاف
    print(dir(std2))# تم اضافتها
    ```
    
- حذف Attribute و Object
    - لحذف attribute استخدام del name.attribute
    - لحذف object استخدم del name
    
    ```python
    del std2.v_hours 
    print(dir(std2)) #تم حذف الخاصية المضافة
    
    del std2
    print(std2) #error: std2 is not defined
    ```
    
- مفهوم Class Attribute
    - هي اضافة خاصية واحده في class بدلا من اضافتها يدويا في كل كائن
    - خاصية مشتركة في جميع الكائنات
    - تسمي ايضا ب (static mebers) و (static data)
    
    ```python
    class Student:
    		university_name = "helwan university"
    		def _init_(self, name, age, id, grades):
    				self.name = name
    				self.age = age
    				self.id = id
    				self.grades = grades
    				
    std1 = Student(Eslam, 21, "xx00", [99, 98, 95])
    std2 = Student(Ahmed, 30, "xx01", 97)
    
    print(std1.university_name)# helwan university
    print(std1.university_name)# helwan university
    ```
    
- نظرة على Setter و Getter
    - هي كيفية الوصول للبيانات داخل Encapsulition المغلفة
    - للوصول نسخدم دوال getter
    - للتعديل نستخدم دوال setter
    - لانسند القيمة بشكل مباشر ولا الوصول اليها بشكل مباشر
    - ويتم هذا فقط ليتم الحفاظ على مفهوم Encapsulation نضمن اي لا شيء خارج الclass  يملك الوصول الى البيانات وتعديها
    - السبب الثاني: التواصل معه البيانات عن طريق  function interface لسهوله التواصل مع الكائن
    
    ```python
    class Myclass:
    		def set_val(self, value):
    				self.value = value
    		
    		def get_val(self):
    				return self.value
    				
    a = Myclass()
    a = Myclass()
    
    a.set_val(10) #اعطاء القيمة
    b.set_val(100)
    
    print(a.get_val()) # للوصول للقيمة
    print(b.get_val())
    ```
    
- تطبيق  Setter و Getter
    - 
    
    ```python
    class MyInteger:
    		#a. قبل ما ناخد القيمة ال (setter) تتأكد من اذا كانت القيمة (integer) ام لا
    		def set_val(self, val):
    				if (type(val) == int):
    						self.val = val
    				else:
    						print('The value is not an integer')
    						
    		def get_val(self):
    				return self.val
    		
    		#b. تقوم بتمرير القيمة لو ليست صحيحه ستعطي خطأ
    		def increment_val(self):
    				self.val+= 1
    
    i = MyInterger()
    
    #i.set_val(9)
    #print(i.get_val())#9
    i.set_val("Eslam")
    print(i.get_val())#The value is not an integer
    i.increment.val() #error			
    ```
    
- نظرة على Access Modifiers
    - طريقة لتقييد الوصول الى attirbute , methods
    - يجد 3 انواع
        - النوع public (قابلة للوصول، النوع الافتراضي لجميع الخصائص والدوال)
        - النوع الثاني protected (علامة علي انها privte ، ولكمها قابله للوصول )
        - النوع الثالث private (غير قابله للوصول)
    
    ```python
    #public
    x = 10
    #protected 
    _x = 10
    #
    __x
    ```
    
- تطبيق Access Modifiers مع الخصائص
    - ال setter , getter تحل مشكلة نوع private وعدم التعاون مع البيانات والوصول لها وتسمح للوصول لها
    
    ```python
    class Employee:
    		def _init_ (self, name):
    				self.name = name #public
    				self._tel = "01000" #protected
    				self.__salary = 1700 #private
    				
    emp1 = Employee("Ahmed")
    
    print(emp1.name) #Ahmed
    print(emp1._tel) #01000
    print(emp1.__salary) #Error
    
    emp1.__salay = 50
    print(emp1.__salay)
    
    #####=
    class Employee:
    		def _init_ (self, name):
    				self.name = name
    				self._tel = "01000"
    				self.__salary = 1700
    		
    		def get_salary(self):
    				return self.__salary
    				
    emp1 = Employee("Ahmed")
    print(emp1.get_salary)#1700
    ```
    
- تطبيق Access Modifiers مع الدوال
    - يمكن الوصول الى الدالة الخاصة عن طريق الدوال setter و getter
    - الفائدة من private عند التعامل مع البيانات والمشاريع الضخمة التي تحتوي على بيانات يتوجب حجب وصولها او التعديل عليها
    
    ```python
    class Employee:
    		def _init_ (self, name):
    				self.name = name
    				self._tel = "01000"
    				self.__salary = 1700
    		
    		def _jeb_title():
    				print("programmer")
    		
    		def __give_rasie(self):
    				self.__salary = self.__salary + 500
    				print ("your salary now is: ", self.__salary)
    		
    		def get_rasie(self):
    				self.__give_rasie()
    
    emp1 = Employee("Ahmed")
    print(emp1.get_salary)#1700
    
    emp1._job_title()#programmer
    emp1.__()#لا تظهر في الاختيارات ولو كتبناها يدوياهيظهر خطأ
    emp1.get_rasie#your salary now is: 2200
    ```
    

### Inheritance | الوارثة

- مقدمة عن الوراثة
    - في حال تشابه  class مع اخر مثل المثال اللى تحت بدل ما نكرر يتم وراثة من class واحد بدل ما نكتب نفس الكود اكثر من مره
    - ويسمي class ب parent class ,super class ,base class
    - وال class الوارثه منه هي child class, dirvied class, sub class
    - وهم جداااااا نحدد علاقتهم ويتم عن طريق استخدام (is a ) مثل  Car is a Vehicle
    - يقدر class او اكثر يورثون من اب واحد
    - يقدر يورث خاصية واحدة او اكثر
    
    ```python
    class Car:
    		def _init_(self, company, owner, color, speed):
    				self.company = company
    				self.owner = owner
    				self.color = color
    				self.speed = speed
    				
    		def move(self):
    				pass
    		
    		def stop(self):
    				pass
    				
    	class Truck:
    		def _init_(self, company, owner, color, speed):
    				self.company = company
    				self.owner = owner
    				self.color = color
    				self.speed = speed
    				
    		def move(self):
    				pass
    		
    		def stop(self):
    				pass
    ```
    
- تطبيق على الوراقة
    - لكي اجعل class يورث من class الاب اكتب بين قوسين في الابن اسم الاب child(parent)
    
    ```python
    class Vehicle:
    		def _init_(self, company, owner, color, current_speed):
    				self.company = company
    				self.owner = owner
    				self.color = color
    				self.speed = speed
    				
    		def move(self):
    				print("the car has moved")
    		
    		def stop(self):
    				print("the car has stopped")
    				
    class Car(Vehicle):
    		def display(self):
    				print("This is the Car class")
    				
    class Truck(Vehicle):
    		def display(self):
    				print("This is the Turck class")
    				
    car1 = Car("jeep", "Eslam", "Black", 0)
    truck1 = Truck("BMW", "Ahmed", "White", 2)
    print(car1.company)#jeep
    print(truck.company)#BMW
    car1.move()#the car has moved
    turck1.move()#the car has moved
    ```
    
- مفهوم Overriding
    - ينفع اضيف دالة في class الابن وهي موجوده بنفس الاسم والمدخل في class الاب مثل الاتي
    - واي استدعاء من الدالة في class Cat  يستخدم الدالة منها وليس من الاب
    
    ```python
    class Animal: 
    		def _init_(self, name, color):
    		
    		def run(speed):
    		
    			
    		def make_sound(self):
    				print("sound...")
    				
    				
    class Cat(Animal):
    		def make_sound(self):
    				print("mewo...")
    		
    cat1 = Cat("Lili","White")
    car1.make_sound()#mewo
    ```
    
- الوراثة متعدد المستويات
    - وتسمي ايضا multilevel inheritance
    - الوراثة من class يرث من class اخر
    - ex: Grandparent→ Parent(Grandparent)→ Child(Parent)
    - يقدر الكائن الموجود في الابن ان يرث الخصائص من كلا الجد والاب
    
    ```python
    class Grandparent: 
    		def g_display(self):
    				print("this is grandparent class")
    
    class Parent(Grandparent):
    		def p_display(self):
    				print("this is parent class")
    
    class Child(Parent): 
    		def c_display(self):
    				print("this is Child class")
    		
    
    child1 = Cild()
    chlid1 = c_display()# this is Child class
    chlid1 = p_display()# this is parent class
    chlid1 = g_display()# this is grandparent class
    ```
    
- الوراثة المتعددة
    - وتسمي ايضا multiple inheritance
    - قدرة class على الوراثة من اكثر من class واحد
    
    ```python
    class Polygon:
    		def p_display(self):
    				print("this is polygon class")
    				
    class Shape:
    		def sh_display(self):
    				print("this is Shape class")
    
    class Square(Polygon, Shape):
    		def s_display(self):
    				print("this is square class")
    				
    sq = square()
    sq = s_display()# this is square class
    sq = sh_display()# this is Shape class
    sq = p_display()# this is polygon class
    
    ```
    
- مفهوم MRO
    - عند وجود اكثر من داله في عدد من classes من اي class سيتم تنفيذها
    - في بايثون يتم عمل مبدأ depth - first اي يتم المرور على جميع الكلاسات الموجوده والبحث عن الداله فيها
    - ويتم البحث في اول كلاس تم كتابته في الاقواس وهو B
    - اي لو مش موجوده في d هيبحث في b لو مش موجوده هيبحث في اللى وارثه منه a لو مش موجوده هيبحث في الكلاس الثاني اللى وارث منه وهو c
    - اي الترتب D→B→ A→C
    - في حال كانت الوراثة مثل dimound shape اي وجود مثلا الكلاس b,c ييتشاركان الوراثة من الكلاس a فبدل ما الترتيب يكون كده D→B→ A→C→A
    - هنحذف اول تكرار ويكون هكذا D→B→ C→A
    
    ```python
    class A:
    		def do_this(self):
    		
    class B(A):
    		pass
    		
    class C:
    		def do_this(self):
    		
    class D(B,C):
    	pass
    	
    obj =D()
    obj.do_this()#
    ```
    
- تطبيق مفهوم MRO
    - 
    
    ```python
    class A:
    		def do_this(self):
    				print("class A")
    		
    class B(A):
    		pass
    		
    class C:
    		def do_this(self):
    				print("class C")
    		
    class D(B,C):
    	pass
    	
    obj =D()
    obj.do_this()#class A
    
    #dimound shape
    class C(A):
    		def do_this(self):
    				print("class C")
    obj =D()
    obj.do_this()#class C
    ```
    
- الدالة mro
    - تقوم بطباعة الترتيب
    
    ```python
    class A:
    		def do_this(self):
    				print("class A")
    		
    class B(A):
    		pass
    		
    class C:
    		def do_this(self):
    				print("class C")
    		
    class D(B,C):
    	pass
    	
    print(D.mro())
    #[<class '__main__. D'>, <class '__main__. B'>, <class '__main__. A'>, <class '__main__. C'>, <class 'object'>]
    
    #dimound shape
    class C(A):
    		def do_this(self):
    				print("class C")
    		
    print(D.mro())
    #[<class '__main__. D'>, <class '__main__. B'>, <class '__main__. C'>, <class '__main__. A'>, <class 'object'>]
    
    ```
    
- وراثة Consturctor
    - دالة init هي داله عادية فتورث كأي داله اخري وتختلف لو هناك اكثر من init في كلاسات اخري
    - لكي نهيئ الخصاصة العامة من class parson ونهيئ الخصائص الخاصة من class employee عند وجود دالتين init
    - نستدعي الدالة init عن طريق خاصية استدعاء الداله عن طريق الclass بشكل مباشر مثل المثال
    
    ```python
    class Person:
    		def _init_ (self, f_name, surname, tel):
    				self.f_name = f_name
    				seld.surname = surname
    				self.tel = tel
    				
    		del full_name(self):
    				return self.f_name + " " + self.surname
    				
    class Employee(Preson):
    		def _init_(self, f_name, surname, tel, salary):
    				Person._init_(self, f_name, surname, tel):
    				self.salary = salary
    	
    		def give_raise(self, amount):
    				self.salary = self.salary + amount
    ```
    
- الدالة Super
    - نفس الطريقة اللى فوق بس اسهل وعن طريق الدالة super ب
    - 
    
    ```python
    class Person:
    		def _init_ (self, f_name, surname, tel):
    				self.f_name = f_name
    				seld.surname = surname
    				self.tel = tel
    				
    		del full_name(self):
    				return self.f_name + " " + self.surname
    				
    class Employee(Preson):
    		def _init_(self, f_name, surname, tel, salary):
    				super()._init_(f_name, surname, tel)
    				self.salary = salary
    	
    		def give_raise(self, amount):
    				self.salary = self.salary + amount
    				
    emp1 = Employee(1700, "Eslam", "Ahmed", "010000")
    ```
    
- مفهوم Polymorphism
    - المعني الحرفي هو تعدد الاوجه
    - في الرمجة يدل على دالة تملك نفس الاسم ولكن هذا الاسم يتصرف باشكال متعددة
    - يتم مشاركة نفس الاسم في classes مختلفة ولكن implemetation  اكواد تختلاف في كل class لذلك هذا الاسم يتصرف باشكال متعددة
    - يتم تطبيقه عندما تتواجد دالة تقوم بشيء مشترك في اكثر من class
    - يتم كتابة نفس الاسم لو هينفس نفس الامر بأختلافات بسيطه في كل class
    
    ```python
    class Student:
    		def print_info(self):
    				print("code student")
    				
    class Teacher: 
    		def print_info(self):
    				print("code teacher")
    				
    student1 = Student()
    teacher1 = Teacher()
    
    student1.print_info()#code student
    teacher1.print_info()#code teacher
    ```
    
- تطبيق Polymorphism
    - نلاحظ ان اضافة صغيره، تغير في طريقة كتابة الكود
    - ومن هنا نستخدم طريقة polymorphism افضل ولا تغير في طريقة كتابة الكود عند اضافة اي اضافة
    
    ```python
    class Circle;
    		pass
    
    class Square:
    		pass
    
    circle1 = Circle()
    square1 = Square()
    
    Shapes = [circle1, square1]
    
    for sh in shapes:
    		if isinstance(sh, Circle):
    				print("draw circle")
    		else:
    				print("draw square")
    				
    # a لو اضفنا كمان سيتغير الكود الى 
    class Circle;
    		pass
    
    class Square:
    		pass
    
    class Triangle:
    		pass
    
    circle1 = Circle()
    square1 = Square()
    triangle1 = Triangle()
    
    Shapes = [circle1, square1, triangle1]
    
    for sh in shapes:
    		if isinstance(sh, Circle):
    				print("draw circle")
    		elif isinstance(sh, square):
    				print("draw square")
    		else:
    				print("draw triangle")
    				
    #### b الطرقة الافضل
    class Circle;
    		def draw(self):
    				print("draw circle")
    
    class Square:
    		def draw(self):
    				print("draw square")
    				
    class Triangle:
    		def draw(self):
    				print("draw triangle")
    
    circle1 = Circle()
    square1 = Square()
    triangle1 = Triangle()
    
    Shapes = [circle1, square1, triangle1]
    
    for sh in shapes:
    		sh.draw()
    #draw circle
    #draw square
    #draw triangle
    
    ```
    
- مميزات Polymorphism في Python
    - تقوم بأخذ اي كائن وتقوم بتنفيذ الداله عليه بدون التحقق من الكلاس التي يستقبله
    - تفترض ان الكائن يمكن ان يكون طالب او معلم قبل ان نوعه او كلاسه
    - وهو مفهوم اسمه duck typing وتفترض ان هذا الكائن يمتلك هذه الدالة
    - قراءة خصائص الكائن اولا بدلا من التحقق منه( والذي يكلم مزيدا من الوقت)
    - في حال عدم امتلاكها يعطي attrupite error
    
    ```python
    class Student:
    		def print_info(self):
    				print("code student")
    				
    class Teacher: 
    		def print_info(self):
    				print("code teacher")
    				
    student1 = Student()
    teacher1 = Teacher()
    
    #a 
    def func(obj):
    		obj.print_info()
    
    func(student1)#code student
    func(teacher1)#code teacher
    ```
    

### Project Python 103

- what is the project
    
    # مشروع الحساب البنكي
    
    ## بنهاية هذا المشروع سيكون الطالب قادرًا على:
    
    1. فهم نمط البرمجة كائنية التوجه.
    2. معرفة التعامل مع Class.
    3. معرفة التعامل مع Object.
    4. معرفة تطبيق مفاهيم Encapsulation و Polymorphism.
    
    ## المتطلبات Requirements
    
    قم بكتابة برنامج يمثل حساب المستخدم في البنك، بحيث يقوم بالتالي:
    
    - عندما يتم إنشاء مستخدم يقوم بتهيئة رصيده البنكي وإعطائه القيمة صفر.
    - يستطيع المستخدم إيداع نقوده عن طريق زيادة رصيده البنكي.
    - يستطيع المستخدم السحب عن طريق خصم رصيده البنكي.
    - يستطيع المستخدم الاستعلام عن رصيده عن طريق الوصول لقيمة الرصيد الحالي.
    - يتم إظهار جملة طباعة عند السحب أو الإيداع مع التاريخ والوقت عند حدوث تلك العملية.
    
    ### مثال:
    
    | العملية | المخرجات |
    | --- | --- |
    | إيداع 2000 ريال | تم إيداع 2000 ريال لرصيدك البنكي في يوم الخميس، ١٠ يونيو ٢٠٢١، الساعة 4:45am. |
    | خصم 150 ريال | تم خصم 150 ريال من رصيدك البنكي في يوم الثلاثاء، ٩ فبراير ٢٠٢١، الساعة 9:15pm. |
- my sulution
    
    ```python
    #a التواريخ والمكاتب
    import datatime
    #b. كلاس الاكون لكل عميل
    class Account:
    		#b.1 خصائص ثابته
    		balance = 0
    		def _init_(self, name, balance):
    				self.name = name 
    		#b.2 تقوم بحساب الرصيد المضاف		
    		def sd():
    		
    		#
    		 
    ```
    
