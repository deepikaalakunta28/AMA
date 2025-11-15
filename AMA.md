## 1. **Inheritance**
Inheritance allows a class (child/subclass) to acquire the properties and methods of another class (parent/superclass). It helps in code reusability.

```python
class Parent:
    def greet(self):
        print("Hello from Parent")

class Child(Parent):
    pass

c = Child()
c.greet()  # Output: Hello from Parent
```

## 2. **Abstraction**
Abstraction hides complex implementation details and shows only essential features to the user. In Python, abstraction can be achieved using abstract classes and abstract
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Square(Shape):
    def __init__(self, side):
        self.side = side
    def area(self):
        return self.side * self.side

s = Square(4)
print(s.area())  # Output: 16


## 3. Difference Between List and Tuple
| Feature    | List            | Tuple         |
| ---------- | --------------- | ------------- |
| Mutability | Mutable         | Immutable     |
| Syntax     | `[1, 2, 3]`     | `(1, 2, 3)`   |
| Methods    | More methods    | Fewer methods |
| Use Case   | Changeable data | Fixed data    |

my_list = [1, 2, 3]

my_tuple = (1, 2, 3)

my_list.append(4)  # Works

my_tuple.append(4)  

Error: tuple has no append
## 4.Difference Between Single and Multiple Inheritance
| Type                 | Description                                     | Example                          |
| -------------------- | ----------------------------------------------- | -------------------------------- |
| Single Inheritance   | Child inherits from **one** parent class        | `class Child(Parent):`           |
| Multiple Inheritance | Child inherits from **multiple** parent classes | `class Child(Parent1, Parent2):` |

### single Inheritance
```
class Animal:
    """The Parent class (Superclass)."""
    def eat(self):
        print("Animal is eating.")

class Dog(Animal):
    """The Child class (Subclass) inheriting from Animal."""
    def bark(self):
        print("Dog barks 'Woof!'")
### multiple inheritance 

class Mother:
    def skills(self):
        print("Cooking and Painting")
class Father:
    def skills(self):
        print("Programming and Gardening")
class Child(Mother, Father):
    def show_skills(self):
        print("Child's Skills:")
        super().skills()  
c = Child()
c.show_skills()  
Mother.skills(c)  # Output: Cooking and
my_dog = Dog()
my_dog.bark()  # Output: Dog barks 'Woof!'
```

## 5. Constructor
A constructor is a special method __init__() used to initialize an object when it is created.
```
class Person:
    def __init__(self, name):
        self.name = name
p = Person("Alice")
print(p.name)  # Output: Alice
```
## 6. Use of self Keyword
self represents the instance of the class and is used to access class variables and methods.
```
class Person:
    def __init__(self, name):
        self.name = name
    def greet(self):
        print("Hello,", self.name)
p = Person("Bob")
p.greet()  # Output: Hello, Bob
```

## 7. Polymorphism
Polymorphism allows objects of different classes to be treated the same way. Methods can have the same name but behave differently.
```
class Cat:
    def speak(self):
        print("Meow")
class Dog:
    def speak(self):
        print("Woof")
def animal_sound(animal):
    animal.speak()
animal_sound(Cat())  # Output: Meow
animal_sound(Dog())  # Output: Woof
```
## 8. Encapsulation
Encapsulation restricts direct access to class variables and methods, usually using private (__) attributes.
```
class Bank:
    def __init__(self):
        self.__balance = 0  # Private variable
    def deposit(self, amount):
        self.__balance += amount
    def get_balance(self):
        return self.__balance
b = Bank()
b.deposit(100)
print(b.get_balance())  # Output: 100
print(b.__balance)  # Error: Private variable
```

## 9. enumerate Keyword
enumerate() adds a counter to an iterable and returns it as an enumerate object.
```
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(index, fruit)
# Output:
0 apple
1 banana
2 cherry
```
## 10. List Comprehension
A concise way to create lists using a single line.
```
squares = [x*x for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

## 11. Difference Between break and continue
| Keyword    | Description                                        | Example                                |
| ---------- | -------------------------------------------------- | -------------------------------------- |
| `break`    | Stops the loop completely                          | `for i in range(5): if i==3: break`    |
| `continue` | Skips the current iteration and moves to next loop | `for i in range(5): if i==3: continue` |
```

for i in range(5):
    if i == 3:
        continue
    print(i)
 Output: 0 1 2 4
```

## 12. Open/Closed Principle (SOLID)
A class should be open for extension but closed for modification. You should be able to extend its behavior without changing its source code.
```
class Shape:
    def area(self):
        pass
class Square(Shape):
    def __init__(self, side):
        self.side = side
    def area(self):
        return self.side * self.side
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    def area(self):
        return 3.14 * self.radius * self.radius
```

