```python runnable

print("List as a stack data structure")


stack = ["Apple", "Banana", "Grapes", "PineApple"]
print(stack) #print stack
stack.pop(1) # remove the value on 1 index which is 6
print(stack) #print stack
stack.append("Mango") # append Mango value in stack
print(stack) #print stack

```

```python runnable


print("Set Data Structure in Python")
sets = {123, 345, 678, 321}
# sets.clear()
# print(set)
sets.remove(123)
print(set)
sets.pop()
print(set)
sets.add(23)
print(set)
sets.update()
print(set)
# sets.issuperset()
# sets.issubset()

set1 = sets.copy()
print(set1)

print("Tuple data Structure in python")

values = ("Apple", "Banana", 334, 78,)
print(values)

print(values.count("apple"))

print(values.index(78))
```
```python runnable

from collections import deque
print("List as a queue data structure in python")

queue = deque(["apple", "Banana", "orange"])
print(queue)
queue.append("grapes")
print(queue)
queue.append("mango")
print(queue)
queue.popleft()
print(queue)
queue.pop()
print(queue)
```
```python runnable


class nodeClass:
    def __init__(self, values1):
        self.values1 = values1
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insertAtPosition(self, values1, position):
        newNode = nodeClass(values1)
        if position == 0:
            newNode.next = self.head
            self.head = newNode
            return

        current = self.head
        currentPosition = 0
        while current is not None and currentPosition < position - 1:
            current = current.next
            currentPosition += 1

        if current is None:
            print("Position out of range")
            return

        nextNode = current.next
        current.next = newNode
        newNode.next = nextNode

    def printList(self):
        temp = self.head
        while (temp):
            print(temp.values1)
            temp = temp.next

llist = LinkedList()
llist.insertAtPosition(3, 0)
llist.insertAtPosition(2, 0)
llist.insertAtPosition(1, 0)

# Inserting node with data=4 at position=2
llist.insertAtPosition(4, 2)
llist.insertAtPosition(7, 3)

llist.printList()
```

```python runnable


class Node:
    def __init__(self, value):
        self.value = value
        self.next = None

class Llist:
    def __int__(self):
        self.head = None

    def displayList(self):
        tempVariable = self.head
        while(tempVariable):
            print(tempVariable.value)
            tempVariable = tempVariable.next

list = Llist()
list.head = Node(1)
nextHead = Node(2)
nextHead1 = Node(3)

list.head.next = nextHead
nextHead.next = nextHead1

list.displayList()

```

```python runnable


print("Small Flight Management System using Python Dictionary")

class flightManagementSystem:
    passportNumber = {}
    nameAndAge = {}

    def addingNewUser(self, passportID, passportName, userName, userAge):
        if passportID in self.passportNumber.values():
            print("Already Exist, try different One")
        else:
            self.passportNumber[passportName] = passportID
            self. nameAndAge[userName] = userAge
            print("User Added Succefully")

    def displayList(self):
        print(self.passportNumber)
        print(self.nameAndAge)

        # TO Display Keys and Values
        # for PassportID And CNIC ID
        print(self.passportNumber.keys())
        print(self.passportNumber.values())

        # for USer Name and AGe
        print(self.nameAndAge.keys())
        print(self.nameAndAge.values())


flightmanagementsystem = flightManagementSystem()

# flightmanagementsystem.addingNewUser(12345678, "CNIC", "De Developer", 23)
# flightmanagementsystem.addingNewUser(12345978, "CNIC", "De Developer", 24)
# flightmanagementsystem.addingNewUser(123458, "CNIC", "De Developer", 24)
# flightmanagementsystem.addingNewUser(123458, "CNIC", "De Developer", 24)
flightmanagementsystem.addingNewUser(123458, "CNIC", "De Developer", 24)
flightmanagementsystem.addingNewUser(12334523428, "Passport", "De Shah", 64)
flightmanagementsystem.displayList()

```

```python runnable


# Create an empty stack
stack = []

# Push items onto the stack
stack.append(1)
stack.append(2)
stack.append(3)

# Pop items off the stack
print(stack.pop())  # Output: 3
print(stack.pop())  # Output: 2
print(stack.pop())  # Output: 1



                            # In this example, we create an empty list and use
                            # the append() method toadd items onto the stack.
                            # We then use the pop() method to remove items
                            # from the stack in last-in, first-out (LIFO)
                            # order. The output of the pop()method is the
                            # last item that was added to the stack


```

```python runnable


print("Example on Dictionary DSA using Python")
class carsClass:

    carsList = {"Toyota": 20000}
    def addingNewCar(self, name, price):
        if name in self.carsList.keys():
            print("Car Name Already exist")
        else:
            self.carsList[name] = price
    def displayList(self):
        print(self.carsList)

carsclass = carsClass()
# carsclass.addingNewCar("Toyota", 200000)
# carsclass.addingNewCar("Toyota1", 200000)
# carsclass.addingNewCar("Toyota", 200000)
# print(carsclass.addingNewCar("Toyota", 200000))
carsclass.addingNewCar("Toyota1", 200000)
carsclass.displayList()

```

```python runnable

print("Dictionary in Python")

dictt = {"apple": 2, "grapes": 4, "Banana": 5}
print(dictt)
print(dictt["apple"])
print(dictt)
print(sorted(dictt))
print(dictt)
del (dictt["grapes"])
print(dictt)

```

```python runnable


class user:
    messageDict = {}
    isLogin = False # True
    def __init__(self, userName, pinCode):
        self.userName = userName
        self.pinCode = pinCode


    def isAuthintic(self):
        if self.userName == "de" and self.pinCode == 1234:
            self.isLogin=True

    def login(self):
        self.userName = input("Enter Your Name: ")
        self.pinCode = int(input("Enter Your PinCode: "))
        self.isAuthintic()



    def inputFromUSer(self):
        if self.isLogin == True:
            print("login Success")
            self.name = input("Enter Name of the Person: ")
            self.message = input("Type Your Message: ")
            self.messageDict[self.name] = self.message
            choice = input("type y for more messages and n for exit")
            if choice == "y":
                self.inputFromUSer()
            else:
                return
        else:
            print("Invalid Arguments: please Try Again")
            self.login()


    def outPutForUser(self):
        print(self.messageDict)


user1 = user("de Developer", 1234)
user1.login()
user1.inputFromUSer()
user1.outPutForUser()

```

```python runnable


print("Small Student Management System using Dictionary in Python")

class teacherData:
    teacherList = {}
    studentList = {}

    def addingNewTeacher(self, name, salary, ID, age, phoneNumber):
        if ID in self.teacherList.values():
            print("Teacher Already Exist with spacific ID, try deferent one")
        else:
            self.teacherList["name"] = name
            self.teacherList["phoneNumber"] = phoneNumber
            self.teacherList["age"] = age
            self.teacherList['salary'] = salary
            self.teacherList["ID"] = ID

            print("Teacher Added Successfully")


    def DIsplayListOfTeachers(self):
        print(self.teacherList)


class studentData(teacherData):
    def addingNewSTudent(self, name, rollNumber, age, phoneNumber):
        if rollNumber in self.teacherList.values():
            print("Student Already Exist with spacific Roll Number, try deferent one")
        else:
            self.studentList["name"] = name
            self.studentList["phoneNumber"] = phoneNumber
            self.studentList["age"] = age
            self.studentList["rollNumber"] = rollNumber

            print("Student Added Successfully")


    def DIsplayListOfStudent(self):
        print(self.studentList)


# Adding New Teacher
teacherdata = teacherData()
teacherdata.addingNewTeacher("MR. Shah", 45000, 1, 45, 9823423222)
teacherdata.DIsplayListOfTeachers()


# adding New Student
studentdata = studentData()
studentdata.addingNewSTudent("MR. Developer", 206274, 35,923469745939)
studentdata.DIsplayListOfStudent()

```

