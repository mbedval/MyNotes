

##### Comments : 
```
# Anything which starts with # will be consisted as comment in python. This line will not be interpreted as code but just as information in the file. it is ignored
```
##### DocString
```
 """  The information provided inside block with 3 double quotes is called DocString and is considered as instruction for manual/help guide
 Intepreter do not ignore but use the information as publishing info about class or function.
```


#### Data Types

##### 1. Numbers
1.1 Integer
```
x=10
```
1.2 float 
```
10.234
```
1.3 Complex
```
x = 25j
```

##### 2. String
**Code**:
```
fname = 'Mukesh'
lname = "Bedval"

print(len(fname))
print(fname[0] , [name[0])
print(fname[0]+ [name[0])

mycityGreeting="Ahmedabad {} padharo".format( "is nice place")
print(mycityGreeting)

```
output	
	M B
	MB
	"Ahmedabad is nice place padharo"




##### 3. Booleans
	True/False

##### 4. List
**Description**: Collection of array which can be changed or re-ordered
```
Fruites = ['pineapple', 'mango', 'banana']
# List allow the list combination of different type of datavalues
MixList = ['pineapple', 'pasta', 1 , 5, True, 'Jan', 'Feb', False]
print(MixList[1:5])
MixList.append('Elephant')
MixList.append(4,'Lion')
print(MixList[1:5])
MixList.reverse()
print(MixList)
```

Output
	['pasta', 1, 5, True]	
	['pasta', 1, 5, 'Lion']
	['Elephant', False, 'Feb', 'Jan', True, 'Lion', 5, 1, 'pasta', 'pineapple']

##### 5. Dictionary 
Description: This is unordered list , Can be modified and cannot have duplicate entries . It is designed with {key: value}
```
##Example of Dictionary
myWeekDictionary = {1:"Sun", 2:"Mon", 3:"Tue", 4:"Wed", 5:"Thr" , 6:"Fri", 7:"Sat" }
print( myWeekDictionary)
print("Third Day of week is " , myWeekDictionary[3])
## Adding new item in the Dictionary
myWeekDictionary[8] = "Holiday"
print(myWeekDictionary)
del myWeekDictionary[8]
print(myWeekDictionary)
```

Output
	{1: 'Sun', 2: 'Mon', 3: 'Tue', 4: 'Wed', 5: 'Thr', 6: 'Fri', 7: 'Sat'}
	Third Day of week is  Tue
	{1: 'Sun', 2: 'Mon', 3: 'Tue', 4: 'Wed', 5: 'Thr', 6: 'Fri', 7: 'Sat', 8: 'Holiday'}

> List and Dictionary are mutable while string, float, integer & Boolean are non-immutable. this can be confirmed with `id(variable)` which will return new identifier when new value is set to existing value.


##### 6. TUPLE
Description: Ordered and unchangeable Collection.  Duplicate entries is allowed. #nonMutable
Tuple is immutable list
```
tupleAnimal = ('dog', 'cow', 'tiger', 'cow' )
print(tupleAnimal)
print(tupleAnimal[1])
print(tupleAnimal[1:3])
CountCow = tupleAnimal.count('cow')
print(CountCow)

```
output
	('dog', 'cow', 'tiger', 'cow')
	cow
	('cow', 'tiger')
	2


##### 7. SET
Description: Unordered collection, No Duplicate entries are present Collect
```
print(" =====================" , "Set")
mySet = {'dog', 'cow', 'tiger', 'cow' }
print(mySet)  # this will remove the duplicate value
print(mySet[1])  #this will throw error as it donot support index 
```
Output:
	{'dog', 'cow', 'tiger'}




==`Note: Lists, Dictionary, Tuples, Sets are collection datatypes because they are used to store collections of data.`==


#### Specialised Collection Data types:
##### **nametuple**(): Extension of tuple. 
Description: 
```
from collections importt namedtuple
myNamedTuple = namedtuple()
```
##### chainmap
Description:

```
from collections import ChainMap
a = {1: 'mukesh', 2:'manish'}
b = {3: 'bsc', 4:'bcom'}
al = ChainMap(a,b)
print(al)
```

Output:
	ChainMap({1: 'mukesh', 2: 'manish'}, {3: 'bsc', 4: 'bcom'})
##### deque
Description: 
```
from collections import deque
name = ['m','u','k','e','s','h']
dequedname = deque(name)
print(dequedname)
dequedname.append('Bedval')
dequedname.appendleft("Mr. ')
print(dequedname)
dequedname.pop()
dequedname.popleft()
print(dequedname)
```

Output
	deque(['m', 'u', 'k', 'e', 's', 'h'])
	deque(['m', 'u', 'k', 'e', 's', 'h', 'Bedval'])
	deque(['Mr. ', 'm', 'u', 'k', 'e', 's', 'h', 'Bedval'])
	deque(['m', 'u', 'k', 'e', 's', 'h'])


##### counter
Description: Counter is a dictionary subclass for counting hash-able objects.
```
from collections import Counter
a =[1,1,2,3,5,8,13]
cCounter = Counter(a)
print(cCounter)
print(cCounter.most_common()) #Gives the count of each item of appearance
subitem = {1:1}
cCounter.subtract(subitem)
print(cCounter.most_common())
```

Output
	[(1, 2), (2, 1), (3, 1), (5, 1), (8, 1), (13, 1)] 
	[(1, 1), (2, 1), (3, 1), (5, 1), (8, 1), (13, 1)]  # one count is reduce for item 1 which was appearing twice in input list
	
##### orderedDict
Description: orderedDict is dictionary subclass which remembers the order in which the entries were done
```

from collections import OrderedDict
od = OrderedDict()
od[1]= 'c#'
od[3]= 'Python'
od[1]= 'JavaScript'
print(od.keys())
print(od.items())
```

Output:
	odict_keys([1, 3])
	odict_items([(1, 'JavaScript'), (3, 'Python')])
##### defaultdict

Description: defaultdict is a dictionary subclass which calls a factory function to supply missing values. Handle and return 0 if there is no item specified with specified key

```
from collections import defaultdict
varDefaultDict = defaultdict(int)
varDefaultDict[1] = "c#"
varDefaultDict[2] = "python"
print(varDefaultDict[1])
print(varDefaultDict[2])
print(varDefaultDict[3])
```

Output:
	c#
	python
	0

##### UserDict
Description: Is wrapped around dictionary objects for easier dictionary sub-classing
##### UserList
Description: Is wrapper list object for easier List sub-classing

##### UserString
Description: Is a wrapper around string objects for easier string sub-classing

#### Array:
An Array is basically a data-structure which can hold more than one value at a time. It is a collection or ordered series of elements of the same types.
Array: can store data type of same type, while list can store data of different data type.
```
print(" =====================" , "Array")
import array
iArrayVar = array.array('i',[1,2,3,4,5,6])
print(iArrayVar)
dArrayVar = array.array('d',[1,2,3,4,5])
print(dArrayVar)
dArrayVar.append(6)
print(dArrayVar)
dArrayVar.extend([8,9,10])
print(dArrayVar)
dArrayVar.insert(6,7)
print(dArrayVar)

```
	Output:
	array('i', [1, 2, 3, 4, 5, 6])
	array('d', [1.0, 2.0, 3.0, 4.0, 5.0])
	array('d', [1.0, 2.0, 3.0, 4.0, 5.0, 6.0])
	array('d', [1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 8.0, 9.0, 10.0])
	array('d', [1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0])
#### Type Conversion

int()
float()
tuple()
list()
set()
dict()

### If Block

```
age=input("Enter your age")
if (int(age)>16 and int(age)<18):
    print("You are teen")
elif (int(age)>=18 and int(age)<=60):
    print("You are adult")
else:
    print("You are free birds")
```

### While Block
```
while (i<5)
	print("hello {} time ".format(i))
```

### For Block
```
for i in range(10);
	print(i)
```

#### lambda
```
op1= lambda x:x**2

print(op1(4))
print(op1(12))

# //output
# 16
# 144
```

#### Reading File and Exception Handling
```
def SampleTryException():
    try:
        ReadFile=open("tes1.txt","r")
        for line in ReadFile:
            print(line)
        ReadFile.close()
    except IOError:
        print("File not found")
    print("App is closed successfully")
 

SampleTryException()

# //output
# File not found
# App is closed successfully
```

#### Writing file and Exception Handling


#### Class

static method
- If method is not having 'self' as argument. Self is the conventional variable to refer to the class instance.
- classname can be used to call the method. it is common to all instance of object.
- class childclass(Dog) : here childclass is inheriting Dog attributes and method.
-  isinstance(n1,newspaper) = results true if n1 is instance of newspaper class.
- Instance method is a method that can be called on a specific instance of a class
- Instance attribute that holds data specific to an instance of a class.
- The key difference between class variable and instance variables is "Class variables are shared among all instances of the class, while instance variables are unique to each instance".
- super() is used to get an instance of the the parent class.
```
- super().append() #will allow to modify the method append in parent class
- super().__init__() #will make sure parent constructor is class first.
```



#### MAP Method


#### Filter Function
l




- This declaration will import method goodMorning from the library (module) name greeting 
 - Instead of greeting you can specify complete path of the library package like src.lib.greeting 
#### Error Handling
- The name of class can help users
- They can extend any python exception class
- They can print messages in a stack trace.
- But it is false to say they are very large with lots of business logic

#### Importing method(s) from the modules  

from <greeting>  import <goodMorning> 
import Src
import Src.Lib as aliaslib
import Src.Lib.Module


- This declaration will import method goodMorning from the library (module) name greeting 
- Instead of greeting you can specify complete path of the library package like src.lib.greeting 
- If * is used instead of method name all method are imported.  
- Instead you can use comma separated list of methods to be imported from module 


###### Packaging of modules. 
- __init__.py should exist in all the package folder  
- It should import the sub module package by syntax [ from . import Food]  in the


environment setup #spyder
```
pip install spyder-kernels==2.4.*
```



#### Decorators
- Decorators can modify the arguments of a function
- Decorators can tear down and after a function runs
- Decorators can modify the return value of a function.
- But Decorators cannot Change the name of a function.
@staticMethod

temp


'''  '''


