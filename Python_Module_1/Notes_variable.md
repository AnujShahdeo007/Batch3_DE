What is Variables:
A variable is a name (identifier) used to store a value in memory.

a = 10
a → variable name
10 → value (object in memory)
Internal Working (VERY IMPORTANT)

Python does not store value in variable directly

It works like this:

a ───▶ [10]
10 is stored in memory
a is just a reference (pointer) to that object

2. Why Variables are Needed
Store data
Reuse values
Improve readability
Easy updates
Handle dynamic data (important in AWS, pipelines)
3. Rules for Naming Variables

Rule 1: Start with letter or _
name = "Raj"
_age = 25

Invalid:

1name = "Raj"
Rule 2: Only allowed characters
a–z, A–Z
0–9
_

Invalid:

salary$ = 50000
user-name = "Anuj"


Rule 3: Case Sensitive
name = "Anuj"
Name = "Rahul"

Different variables

Rule 4: Cannot use Keywords

Examples:

if, for, while, class

Invalid:

if = 10
Rule 5: No spaces


user name = "Anuj"


user_name = "Anuj"

Rule 6: Meaningful names (Best Practice)
x = 50000      # 
salary = 50000 # 

4. Variable Assignment

Basic Assignment
a = 10
Multiple Assignment
a, b, c = 10, 20, 30

Same Value Assignment
a = b = 10

Both point to same object

5. id() Function (Memory Concept)

Returns memory address of object

a = 10
print(id(a))
Example
a = 10
b = 10

print(id(a), id(b))

Same memory (due to optimization)

6. Python Memory Optimization

Integer Caching
Python caches numbers from -5 to 256
a = 100
b = 100

print(a is b)  # True
String Interning
a = "hello"
b = "hello"

print(a is b)  # True
7. is vs ==
 == → value comparison
 is → memory comparison
a = [1,2,3]
b = [1,2,3]

print(a == b)  # True
print(a is b)  # False
8. Mutable vs Immutable (Core Concept)
Immutable (Cannot change)
int
float
string
tuple
a = 10
a = 20  # new object created
Mutable (Can change)
list
dict
set
a = [1,2,3]
a.append(4)  # same object modified

9. Reference Behavior
Same Reference
a = [1,2,3]
b = a

Both point to same memory

Copy (Shallow Copy)
b = a.copy()

New object created

10. Important Tricky Concepts

1. List Reference
a = [1,2,3]
b = a

b.append(4)
print(a)

[1,2,3,4]

2. Reassignment
a = [1,2,3]
b = a

a = [4,5,6]
print(b)

[1,2,3]

3. Function Behavior
def modify(x):
    x.append(4)

a = [1,2,3]
modify(a)

Changes original list

4. Immutable Behavior
a = 10
b = a

a = 20
print(b)

10

5. Mutable inside Immutable

a = (1,2,[3,4])
a[2].append(5)

Tuple unchanged, list changed

11. Copy Types (Advanced)

Shallow Copy
import copy
b = copy.copy(a)

Nested objects still shared

Deep Copy
b = copy.deepcopy(a)

Fully independent

12. Variable Scope (Intro)

Local Variable
def test():
    x = 10
Global Variable
x = 10

13. Real Data Engineering Example
bucket = "my-data-bucket"
file_name = "orders_2026.csv"

s3_path = f"s3://{bucket}/{file_name}"

Dynamic and reusable

14. Common Mistakes

Using same reference unintentionally
Confusing is and ==
Not understanding mutable behavior
Overwriting variables

15. Interview Summary

“In Python, variables are references to objects stored in memory. Assignment creates a reference, not a copy. Mutable objects can be modified in place, while immutable objects create new objects on modification.”

16. Quick Revision Table
Concept	Meaning
Variable	Reference to object
id()	Memory address
=	Assignment
is	Same memory
==	Same value
Mutable	Can change
Immutable	Cannot change



Rules:1 : Variable must start with a letter or _ 

name="Raj" # valid 
_name="Raj" # Valid 

1name="Raj" # Invalid 

Rule 2: Cannot use special charcters 

salary=50000 # Valid 

salary$=50000 #Invalid 
user-name="A" # Invalid 

Only allowed :

Letters (a-z,A-Z)
Numbers(0-9)
Underscore (_)

Rule:3 Variable name are case senstitive 

name="Raj"
Name="Raj"

name != Name


Rule:4 : Cannot use Python Keywords 

if 
for 
while 

if=10 # Invalid 


Rule 5: Use meaningful names 
x=500000
salary =50000 



Rule 6:No spaecs allowed 

user name ="Raj" # invalid 


