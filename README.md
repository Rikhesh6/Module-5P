## Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program
```
class Student:
    def __init__(self):
        self.a=input()
    def show(self):
        print("This is non-parameterized constructor")
        print("Welcome",self.a)
obj=Student()
obj.show()
```

## Output
<img width="442" height="235" alt="image" src="https://github.com/user-attachments/assets/5c1a9fb2-65e5-440b-be24-30219f633d1d" />

## Result
Thus the program to demonstrate a non-parameterized constructor has been executed successfully.
The student name is accepted and displayed with a welcome message.

# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
```
class Demo:
    def __init__(self):
        self.status="Alive"
        print(self.status)
    def __del__(self):
        print("Object is being destroyed")
obj=Demo()
del obj
```
## 🧪 Output
<img width="423" height="198" alt="image" src="https://github.com/user-attachments/assets/f25d5e81-8bd1-444a-a287-239cfbdb0a14" />

## Result
Thus the program to demonstrate constructor and destructor has been executed successfully.
The object is created and destroyed with corresponding messages displayed.

# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
class Details:
    def __init__(self,name,age):
        self.name=name
        self.age=age
    def getName(self):
        return self.name
    def getAge(self):
        return self.age
class Employee(Details):
    def __init__(self,name,age,employee_id,department):
        super().__init__(name,age)
        self.employee_id=employee_id
        self.department=department
    def getEmployeeDetails(self):
        print(self.name,self.age,self.employee_id,self.department)
class Patient(Details):
    def __init__(self,name,age,patient_id,disease):
        super().__init__(name,age)
        self.patient_id=patient_id
        self.disease=disease
    def getPatientDetails(self):
        print(self.name,self.age,self.patient_id,self.disease)
ename=input()
eage=int(input())
eid=input()
dept=input()
pname=input()
page=int(input())
pid=input()
disease=input()
e=Employee(ename,eage,eid,dept)
p=Patient(pname,page,pid,disease)
e.getEmployeeDetails()
p.getPatientDetails()
```

## Sample Output
<img width="414" height="413" alt="image" src="https://github.com/user-attachments/assets/d1c901df-0c09-4f0e-bd11-968bec9b93e8" />

## Result
Thus the program demonstrating inheritance using base and derived classes has been executed successfully.
The employee and patient details are accepted and displayed.

# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```
class Parent:
    def __init__(self,name):
        self.name=name
    def getName(self):
        return self.name
class Child(Parent):
    def __init__(self,name,age):
        super().__init__(name)
        self.age=age
    def getAge(self):
        return self.age
class Grandchild(Child):
    def __init__(self,name,age,location):
        super().__init__(name,age)
        self.location=location
    def getLocation(self):
        return self.location
name=input()
age=int(input())
location=input()
obj=Grandchild(name,age,location)
print(obj.getName(),obj.getAge(),obj.getLocation())
```

## Sample Output
<img width="403" height="246" alt="image" src="https://github.com/user-attachments/assets/9b767d06-6d0d-427f-8393-ba27f8e18a44" />


# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:
    def Summation(self,a,b):
        return a+b
class Calculation2:
    def Subtraction(self,a,b):
        return a-b
class Derived(Calculation1,Calculation2):
    def Division(self,a,b):
        return a/b
a=float(input())
b=float(input())
obj=Derived()
print(obj.Summation(a,b))
print(obj.Subtraction(a,b))
print(obj.Division(a,b))
```
## Output Example
<img width="444" height="276" alt="image" src="https://github.com/user-attachments/assets/0a99029c-4f86-48d9-9f15-46ebb9380f53" />
