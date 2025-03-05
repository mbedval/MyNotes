- JavaScript is a high-level, dynamic, interpreted programming language that is well-suited to object-oriented and functional programming styles 
- JavaScript’s variables are untyped
- ES6 was released in 2015 and added major new features including class and module syntax that changed Javascript from scripting language into a serious, general purpose language suitable for large-scale software engineering. 
- ECMAScript specification has moved to a yearly release cadence and versions of the language {ES2016, ES2017, ES2018, ES2019, ES2020} and now identified by year of release.
- '**Use Strict**' directive can be used to correct the legacy flaws pre-ES5. For example if you use the ES6 class keyword or create ES6 module, then all the code within the class or module is automatically strict and flawed features are not available in those contexts.
- The core Javascript language defines a minimal API for working with numbers, texts arrays, set, maps and so on.
- The Original host environment for JavaScript was a web browser, and this is still common execution environment. This web browser environment allows Javascript code to obtain input from the user's mouse and keyboard and by making HTTP requests. And it allows JavaScript code to display output to the user with HTML and CSS
- Node is another environment available since 2010 for JavaScript allowing access to the entire operating system, allowing to read and write files, send and receive data over the network, and make and serve HTTP requests. It is poplular choice for implementing web servers and also a convenient tool for writing simple utility scripts as a alternative to shell scripts.

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


- JavaScript is case-sensitive language.
- JavaScript ignores spaces that appear between tokens in programs. There are some exceptions in this. spaces and lines breaks can be used to format and indent your programs
- Along with regular space '\u0020', there are few more characters like Tab, assorted ASCII control characters and various characters which are considered as white-space.
- // is used for single line comment
-  /* multiple line comment is placed in such a block \*/ 
- Literals are the data values that appears directly in a program.
- A Javascript identified must begin with a letter an underscore(_) or a dollar sign($). Digits are not allowed as first characters
- Note: let can't fully reserved in order to retain backward compatibility with older programs. and so the rule is "let can be used as a variable name if declared with var outside of class, but not if declared inside a class or with const"
- There are various keywords which are reserved or restricted to use , it might not be keyword but might be used in future { as, async, while, await, break, yield, case, catch, class, const, continue, debugger, default, delete, do, else, export, extends , false, finally, for, from, function, get, if, import, in, instanceof, new, null, of , return, set, static, super, switch, target, this, throw, true, try, typeof, var, void, with} 
- 
- versions. {enum, implements, interface, package, private, protected, public}
- we can use unicode characters in strings and comments. for portability and ease of editing , it is common to use only ASCII letters and digits in identifiers. but this is programming convention and not restriction so Javascript allows unicode letters, digits and ideagraphs in identifiers. we can use Pi symbol as identifier. 
- Some computer hardware and software cannot display, input or correctly process the full set of unicode characters, to support this JavaScript defines escape sequence that allow us to write Unicode characters using only ASCII characters. This Unicode escapes begin with the characters '\u' and are either followed by exactly four hexadecimal digits enclosed within curly braces.
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
	1. Primitive Types: includes number, string and boolean, null and booleans are also primitive types
	2. Object Types: An object is collection of properties where each property has name and value. Functions are classes are specialized kin of object
- Strings are immutable.
- Booleans, symbols, null and undefined are immutable. 
- JavaScript liberally converts values from one type to another. `===` operator perform stric equality, it donot perform any type conversion.
- JavaScript represents 64-bit floating point format defined by IEEE 754 standard. it allow all integer between 2 ^53 - and 2^53
- The certains operations in JavaScript such as array indexing and the bitwise operators are performed with 33-bit integers
- JavaScript recognizes base-10 (decimal) and base-16 (hexadecimals) values. hexadecimals literal begins with 0x or 0X  followed by hexadecimal digits. {0-9-A-F}
- In ES6 and later , you can express integers in binary (base2) or octal (base 8) using the prefixes 0b and 0o (0B and 0O)
- BigInt is new numeric type defined in ES2020 . It has been implemented in various browser and node. BigInt values can have thousands or even millions of digits . but as it donot attempt to prevent timing attacks, it cannot be used for cryptography. (i.e. 1234n is small but BigInt Literal example)
- BigInt(Number.MAX_SAFE_INTEGER) can be used to convert regular JavaScript numbers to BigInt Values. Arithmetic works in similar way of numbler but division drops any remainder and rounds down to zero
#### String type
```
let euro = "€";
let love = "❤";
euro.length 
// => 1: this character has one 16-bit element
love.length
// => 2: UTF-16 encoding of ❤ is "\ud83d\udc99"
```
- 


Tools:
	Cypress
	