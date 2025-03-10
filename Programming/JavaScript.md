- JavaScript is a high-level, dynamic, interpreted programming language that is well-suited to object-oriented and functional programming styles 
- JavaScript’s variables are untyped
- ES6 was released in 2015 and added major new features including class and module syntax that changed Javascript from scripting language into a serious, general purpose language suitable for large-scale software engineering. 
- ECMAScript specification has moved to a yearly release cadence and versions of the language {ES2016, ES2017, ES2018, ES2019, ES2020} and now identified by year of release.
- '**Use Strict**' directive can be used to correct the legacy flaws pre-ES5. For example if you use the ES6 class keyword or create ES6 module, then all the code within the class or module is automatically strict and flawed features are not available in those contexts.
- The core Javascript language defines a minimal API for working with numbers, texts arrays, set, maps and so on.
- The Original host environment for JavaScript was a web browser, and this is still common execution environment. This web browser environment allows Javascript code to obtain input from the user's mouse and keyboard and by making HTTP requests. And it allows JavaScript code to display output to the user with HTML and CSS
- Node is another environment available since 2010 for JavaScript allowing access to the entire operating system, allowing to read and write files, send and receive data over the network, and make and serve HTTP requests. It is poplular choice for implementing web servers and also a convenient tool for writing simple utility scripts as a alternative to shell scripts.
- JavaScript is case-sensitive language.
- JavaScript ignores spaces that appear between tokens in programs. There are some exceptions in this. spaces and lines breaks can be used to format and indent your programs
- Along with regular space '\u0020', there are few more characters like Tab, assorted ASCII control characters and various characters which are considered as white-space.
- // is used for single line comment
-  /* multiple line comment is placed in such a block \*/ 
- Literals are the data values that appears directly in a program.
- A Javascript identified must begin with a letter an underscore(_) or a dollar sign($). Digits are not allowed as first characters
- Note: let can't fully reserved in order to retain backward compatibility with older programs. and so the rule is "let can be used as a variable name if declared with var outside of class, but not if declared inside a class or with const"
- There are various keywords which are reserved or restricted to use , it might not be keyword but might be used in future { as, async, while, await, break, yield, case, catch, class, const, continue, debugger, default, delete, do, else, export, extends , false, finally, for, from, function, get, if, import, in, instanceof, new, null, of , return, set, static, super, switch, target, this, throw, true, try, typeof, var, void, with} - 
- versions. {enum, implements, interface, package, private, protected, public}
- we can use unicode characters in strings and comments. for portability and ease of editing , it is common to use only ASCII letters and digits in identifiers. but this is programming convention and not restriction so JavaScript allows `unicode` letters, digits and ideographs in identifiers. we can use Pi symbol as identifier. 
- Some computer hardware and software cannot display, input or correctly process the full set of unicode characters, to support this JavaScript defines escape sequence that allow us to write Unicode characters using only ASCII characters. This Unicode escapes begin with the characters '\u' and are either followed by exactly four hexadecimal digits enclosed within curly braces.
- null is a language keyword that represent value i absent. `typeof` operator on null returns "object". == operator treat null and undefined as equal, `neither` null nor `undefined` have any property or methods. 

  variable is symbolic name of a value
```
  let x = 0; 
  x = 0.007;
  x = "Hello world"  
  x = false
  x = null
  x = undefined
  x = 'namate duniya'
```
  here x is variable name which contains value 0. value can be assigned by operator '='


- J
```
let café  =1;

caf\u00e9'  
// retrieving value of variable café

caf\u{E9}   // alternate way to retrieving value of variable café
```
- While using Unicode characters in your JavaScript Programs, you should ensure that your editor or some other tools perform unicode normalization of your source source code to prevent your from ending up with different but visually indistinguishable identifier

example
```
"caf\u{e9}"
"cafe\u{301}"
// both variable identifier would look same in editor as 'café' 

```
Semicolon is optional two statements are written in different line

```
return
true;
// Note : this code is interpreted as return; true; 
```
So we need to consider few exception involved in #return, #throw #yield #break #continue


### Types Values and Variable

JavaScript types can be divided into two categories 
	1. Primitive Types: includes number, string and boolean, null and booleans are also primitive types. Any Javascript value that is not number, a string, a boolean a symbol, null, or undefined is an object.
	2. Object Types: An object is collection of properties where each property has name and value. Functions are classes are specialized kin of object. An ordinary Javascript object is an unordered collection of named values. Array is special kind of object that represents an ordered collection of numbered values. Javascript's object types are mutable and its primitive types are immutable. 
> A Value of mutable type can change. By this it means program can change the values of object properties and array elements. Number, boolean, Symbols, null and undefined are immutable. 
#### 1. Number Type
- Number is used to represent integers and to approximate real numbers. It use 64-bit floating point format defined by IEEE 754 std. So it can represent 
- Larger than allowed value, may lose precision in the trailing digits.
 
``` 
	let rating = 5	// numerical literal value which is base-10 integer
	let marks1 = 0xff // value is represented in Hexadecimal digits
	let marks2 = 0o377 // value is reperented in Octal (base 8)
	let marks3 = 0b10101 // value is representated in binary (base 2)
	let price1 = 2345.6789 // this is floating point literal value
	let price2 = 6.02e24 //  this represents (6.02 x 10^23)
	
	//example of separators in numeric literal allowed in javascript
	let billion = 1_000_000_000
	let bytes = 0x89_AB_CD_EF // bytes separator
	let bits = 0b0001_1101_0111 // as a nibble separator
	let fraction = 0.123_456_789 / works in fractional part also.


```

>  Arithmetic operators (+, -, * , / , % ) are available to work with numeric value. for complex mathematical operations there are set of functions and constants available with `Math` object

##### MATH Object
```
Math.pow(2, 4) // output: 16
Math.round(.6) // output 1.0
Math.ceil (.6) // output 1.0
Math.abs(-5)   // output 5
Math.max(2,5,3) // output 5
Math.min(2,5,3) // output 2
Math.random()   //pseduo-random number x where 0 <= x
Math.log(10) // output 
Math.log(512) // output

Since ES6 have more functions 
Math.cbrt(27) // cube root of 27 = 3
Math.hypot(3,4) // square root of sum of squears of all
Math.imul(2,3) // optimized muliplication of 32-bit
Math.truc(3.9) //truncate the decimal value and return integer value

Number.Max_value * 2  // result is infinity value 
1/0  //is also infinity
-Numer.Max_value * 2 // is negative Infinity
0/0 // is the NaN

Number.isNaN( 0/0) // result true .

// rounding error : impact
let x = .3 - .2 
let y = .2 - .1
x === y  /// false and value of x and y are not same this is due to rounding error
x === .1 // false : as output is not .1
y === .1 // true : as output is .1

```

> numeric operation results Infinity or Negative Infinity when there is overflow or underflow or division by zero. In JavaScript `division by zero` is not an error.  It simply result NaN (Not a Number)

> ES2020 : three is new numeric type knows as BigInt and is already implemented in chrome, Firefox, edge and node. It will allow 64-bit integers. It is represented as `12345n` . it cannot be mixed with other types in any arithmetic operator but can work fine with comparison operators. None of Math object accept BigInt Operands.



#### 2 . String Type
- Strings are immutable.
- JavaScript liberally converts values from one type to another. \``===`\` operator perform strict equality, it don't perform any type conversion.
``` 
	let bookname = "Life is owesome"
	
	let euro = "€";
	let love = "❤";
	euro.length 
	// => 1: this character has one 16-bit element
	love.length
	// => 2: UTF-16 encoding of ❤ is "\ud83d\udc99"

	
```

##### 2.1 escape sequence
```
	\0  // the NULL character  "\u0000"
	\b  // Backspace "\u0008"
	\t  // Horizontal-tab "\u0009"
	\n  // Newline "\u000A"
	\v  // Vertical-tab  "\u000B" 
	\f  // form feed "\u000C )"
	\r  // Carriage return "\u0022" 
	\"  // Double quote "\u0022"
	\'  // Apostrophe or single quote "u0027"
	\\  // Backslash "\u005C"
	\Xnn //The unicode character specified by the two hexadecimal digits nn
	\unnnn  //The unicode character specified by the four hexadecimal digits nnnn
	\u{n}  // The Unicode character specified by the codepoint n, where n is one to six hexadecimal digits between 0 and 10FFFF (ES6)

```

##### 2.2 String manipulation
There are various method to manipulate , retrieve full or partial info on string
```
var s = "mukesh is Automation Architect"
s.substring(1,4) // return value 'ukes'
s.slic(1,4) // also return value "ukes"
s.split(" ")  // returns array ['mukesh', 'is', 'Automation', 'Architect'] 
s.indexOf("A") // return value 10 as A first occurence is as 11th character
s.indexOf("A",11) // return value 21 as A first occurencs is as 22nd character
s.lastIndexOf("A") //return value 21 as this is last occurance of A
s.startsWith("mukes") //return true
s.endsWith("mukesh)") //return false
s.endWith("tect") // returns true
s.includes("Automation") //returns true
s.includes("automation") //returns false, as it is case sensitive
s.replace("Automation" , "Test Automation") //returns 'mukesh is Test Automation Architect'
s.toUpperCase() // return string in uppercase
s.normalize
s.charAt(10) //return 'A' as a is located at index value 10
s[10]  // also return 'A' this is retrieval witho
s.charCode(10) //return 65, it is 16-bit number at the specified position
s.codePointAt(10) //ES6 for > 16 bits
s.padStart(3) // add spaces on the left to the lenght of 3
s.padEnd(3)  // add spaces on the right to a lenght of 3

s.trim // remove spaces at start and end
s.trimStart() //remove spaces on left
s.trimEnd() // removes spaces on Right

s.concat (". He is also good tester") // return concatenated string 'mukesh is Automation Architect. He is also good tester'

"--".repeat(10) // returns the displayed string with '--' repeated 10 times
```
> Remember that strings are immutable in JavaScript. Methods like replace() and toUpperCase() returns new strings. they do not modify the string on which they are are invoked. So Strings can be also treated like read-only arrays. and you can access invidual characters (16-bit values) from string using square brackets instead of charAt() method:

> Template literals : is string like syntax allowing arbitrary JavaScript expressions

```
let name = "Mukesh"
let greeting = `Hello ${name} how are you`  //returns string value after update name 

`\n`.lenght returns 1 becuase string has single new line character
String.raw`\n`.length // return 2 as string raw function returns the text within backticks without any processing of backslash escapes.


```

##### 2.3 Regular expression or pattern matching
```
/^HTML/ // try to match string with H or T or M or L at first possible
/[0-9[0-9]*/ Matches string for starting with nonzero digit followed by any digits
/\bjavascript\b/i Matches "Javascript" as word without case sensitivity
```
>RegExp objects define a number of useful methods and strings also have methods that accepts RegExp arguments.

```
let text = "testing: 1, 2, 3"
let pattern /\d+/g
pattern.test(text) // returns true
text.search(pattern) // 9 position of first match
test.match(pattern) //["1", "2", "3"] array is returned for all matches
text.replacee(pattern, "#") // returns 'testing, #, #, #'
text.split(/\D+/)  // split on nondigit so return is ["", "1","2", "3"]



```
#### 3 . Boolean Type

#### 4 . Array 

#### 5 . Date
Dates are objects but they also have numeric representation as a timestamp that specifies the number of elapsed milliseconds (since 1 Jan 1970)
```
let timestamp =date.now()
let now = new Date()
let ms = now.getTime()
let iso = now.toISOString() // Convert to string in standard format

```
#### 6. Set Object represents a set of values
```
let dynObj = {}
let monthname = "jan"
dynObj[monthname] = "1"
dynObj[monthname] //returns 1
dynObj["jan")] //returns 1
typeof(strname) // return is "string"

let symname = Symbol("Propname") // use symbol to use as a property name
typeof(symname) // return is "symbol"
dynObj[symname] = 2
dynObj[symname] //return 2

```

> There is global Symbol registry to prevent any case of conflict. 

```
let s = Symbol.for("shared")
let t = Symbol.for("shared")
s === t  // return true
s.tostring() // return 'Symbol(shared)'
Symbol.keyFor(t)  //return "shared"
```

#### 7 . GLOBAL Objects
When JavaScript interpreter starts (or whenever a web browser loads a new page) it create a new global object and gives it an initial set of properties that defines:
	- Global constants like undefined , infinity and `NaN`.
	- Global functions like i`sNaN(), parseInt() and eval()`
	- Constructor functions like Date(), `RegExp`(), String(), Object() and Array() 
	- Global objects like Math and `JSON`.
> The initial properties of the global object are not reserved words, but deserve to be treated a if they are .
> In Node : global object has property named global whose value is the global object iteself so you can always refer to the global object. 
> In Web Browser: global object is served by Window object, and contained in the browser window it represents. Window Object defines core global properties and other global that are specific to web browsers and clien-side JavaScript. Web worker threads have different global object than the Window with which they are associated.


> ES2020 final defines `globalThis` as the standard way to refer to the global object in any context.  

Objects are different than primitives, Firstly they are mutuable their values can change:

```
	let o = :x: 1}
	o.x = 2   // mutate it by changing the value of a property
	9.y = 3  // mutate it by adding new property.
	let a = [1,2,3] : Arrays are also mutable
	a[0] = 0
	a[3] = 4
		
```

> Objects are not compared by values: even if it have equal same properties and values|. Objects are sometime called reference types and object values are references.  

```
let 0 = :x:1}, p = {x:1}
o === p  // returns false distinct objects are never equal.
let a = [] , b =[]
a === b  // returns false as distinct objects are never equal.
```

>  two objects will be referred as same if they refer to the same underlying object.
```
let a = []
let b = a
b[0] = 1;
a[0]   //returns as change is visible through variable a.
a === b // returns true as they refer to same object (or array))


```
#### Explicit Conversions

##### Primitive Type Conversion
The simplest way to perform an explicit type conversion by using global functions  
- Boolean()
- Number() : it works on base-10 and does not allow trailing characters that are not literals.
- `parseInt`() and `parseFloat`() are more flexible. if string has `"0x or 0X"` than all white-space are ignore and if the first non space character is not part of a valid numberic literal then return `NaN`
- String() 

Any value other than null or undefined has a `toString`() method, and the result of this method is usually the same as that returned by string() function
```
 let n = 17
 let binary = "ob" + n.toString(2);   // return "0b10001"
 let octal = "0o") + n.toString(8)  // return  == "0x21"
 let dex = "0x" + n.toString(16) // return "0x11"
```

> To work with financial data, the Number class defines three methods for these kinds of number-to-string conversions.

```
	let n = 123456.789;
	n.toFixed(0) //return "123457"
	n.toFixed(2) //return "123456.79"
	n.toFixed(5) // return "123456.78600"
	n.toExpotential(1) // return 1.2e+5
	n.toExponential(3) // return 1.235e+5"
	n.toPrecision(4)   // return 1.235e+5"
	n.toPrecision(7)   // return 123456.8"
	n.toPrecision(10)  // return 123456.7890"
```

##### Object to Primitive Conversions.
JavaScript specifications defines three fundamental algorithms for converting objects to primitive
1. Prefer-string: returns a primitive value if conversion to string is possible
2. Prefer-string: returns a primitive value if conversion to number is possible
3. no-preference: do not have preference of primitive value of desired. All except Date implement prefer-number, since date class implement prefer-string.

> All Objects inherit two conversion methods that are used by object-to-primitive conversions. and before we can explain the prefer-string, prefer-number and no-preference conversion algorithms. `toString()` and `valueOf()`
> 

#### 7. MAP objects represents a mapping from keys to values. And allow operations on arrays of bytes and other binary data.






### Popular Framework 
#### Popular Testing Framework
1. #JEST it is testing framework which can work with babel, typescript, node, react, angular vue. Supports #TDD 
2. #Mocha : framework that runs on Nodejs. and in the browser making asynchronous testing simple and fun. Allow flexible and accurate reporting, while mapping uncaught exception to correct test cases. Supports both BDD and TDD 
3. #Chai : chai is BDD/ TDD assertion library for node and the browser tht can be delightfully paired with any JavaScript framework
4. #Jasmine : is framework for testing JavaScript code. It does not depends on any other JavaScript framework. it runs in browser an in node.js. primarily supports BDD
5. #k6  is open-source tools and cloud service that makes load testing easy for developers and QA engineers
6. #Webdriver.io : allows you to test in actual browser or mobile devices. Allow to perform e2e , unit and component testing in the browser. It has automatic waits for elements to appear before interacting with them.
7. #nightwatchjs : framework with a powerful set of tools to write , run and debug your tests across web and native mobile applications.




#### Useful in Popluar Development Framework
1.  #Nextjs enables to create high-quality web applications with the power of react components .[URL](https://nextjs.org/)
2.  #Nuxt is Open source framework that makes web development intuitive and powerful. Create performant and production -grade full-stack web apps and website with confidence



Tools:
	Cypress

