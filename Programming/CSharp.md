### Comments
`// Single-line comment`
`/*   Multi line comment  */`


> `// TODO: add comments to a task list in visual studio`

### Documentation Comments
`/// Single-line comment used for documentation`
`/** Multi line comment used for documentation **/`
### Datatypes

#### primitive data types

| Data types | Size             | Range                            |
| ---------- | ---------------- | -------------------------------- |
| int        | 4 bytes          | -2(power 31) to 2 (power 31)  -1 |
| long       | 8 bytes          | -2(power 63) to 2(power 63) -1   |
| float      | 4 bytes          | 6 to 7 decimal digits            |
| double     | 8 bytes          | 15 decimal digits                |
| decimal    | 16 bytes         | 28 to 29 decimal digits          |
| char       | 2 bytes          | 0 to 65535                       |
| bool       | 1 bit            | true/false                       |
| string     | 2 bytes per char | N/A                              |
|            |                  |                                  |
|            |                  |                                  |
#### ARRAY
```
char[] chars = new char[10];
chars[0] = 'a';
chars[1] = 'b';

string[] letters = {"A", "B", "C"};
int[] mylist = {100, 200};
bool[] answers = {true, false};

```

#### STRING
```
string fname = "Bukesh" ;
string lname = "Bedval"; 
string name = fname + " " + lname; 
// output is "Mukesh Bedval"

//String Interpolation
string name = $"{fname} {lname}"

// Methods of strings
name.length
name.Compare()
name.Contains()
name.Equals()
name.Format()
name.Trim()
name.Split()


```

### Condition
```
if (expression1){
	console.WriteLine("when expression1 is true);
}else if(expression2){
	Console.WriteLine("when expression2 is true);
}else
	Console.WriteLine("when both expression do not pass");
}
```
### Loops

```
int [] numbers = {2,4,6,8,10};
for (int i= 0 ; i  < numbers.Length; i++ ) {
	Console.WriteLine(numbers[i]);
}

or 
foreach (int num in numbers){
	Console.WriteLine(num);
}
```
### TYPE CASTING
```
int.TryParse()
```
