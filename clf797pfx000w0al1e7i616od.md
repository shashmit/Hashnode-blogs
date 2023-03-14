---
title: "the equal problem"
datePublished: Mon Mar 13 2023 20:05:20 GMT+0000 (Coordinated Universal Time)
cuid: clf797pfx000w0al1e7i616od
slug: the-equal-problem
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678737854535/8286fd86-6edf-4f79-89b0-ee3f1c2917ad.jpeg
tags: java, javascript, equality-operator-in-javascript

---

In general, we understand what the equal sign represents but in the language of programming, it is understood in different manners. Here, I will talk about two of the language that I'm learning right now.

One is the most talked about language on the internet JAVASCRIPT second guess it's very simple people assume these two are related to each other if you didn't guess it is none other than JAVA itself. God-tier language with a hard-to-remember syntax but simple ways to do the hard task with an amazing library and one of the biggest helping communities if you get stuck somewhere.

After gaining enough knowledge I can talk about the problem that I faced the problem is not that big and it kinda talked about a lot on the Internet. **THE DOUBLE EQUAL('==') PROBLEM**. Both have their way to deal with it but it's very confusing to let's talk about it.

**JAVA**

talking about java is always fun to me as it has so much to offer still it doesn't offer as much as C++, but you see from many perspectives but depends on you, do you like the syntax or not.

We will be talking in terms of the string first.

Talking about the difference in java the two:

* That is `.equals()` is a method while `==` is an operator.
    
* `==` operators for reference comparison **address comparison** and `.equals()` method for **content comparison**.
    

```java
//code 1.0 
String name = "Shashmit";
String blame = "Shashmit";
System.out.println(name == blame);//true
```

In the &lt;code 1.0&gt; there is no separate space allocated to the blame as it contains the same value it points at the same address as the name.

```java
//code 1.1
String name = "Shashmit";
String blame = new string ("Shashmit");
System.out.println(name == blame);//false
```

In the &lt;code 1.1&gt; the `==` operator checks again if the memory of both the Strings is at the same place as it checks only for the same memory space. As it gets a false from the memory. It produces a false over the statement that is being asked. It doesn't check for the value inside the memory.

Talking about the `.equal()` method in java to compare the inside data in a string.

```java
code 1.2 
String name = "shashmit";
        String blame = new String("shashmit");
        System.out.println(name.equals(blame));//true
```

In the code &lt;1.2&gt; as you can see the result that is produced is true in this case the method treats data inside the variable as the important key and compares the data rather than comparing the addresses.

Few Points about Equals():

* Cannot be used for primitive type
    
* To compare the content in a string it is used.
    
* Equals() can be overridden.
    

Woosh and we are done with java lets go to one of the most amazing languages for a new learner that is javascript.

**JAVASCRIPT**

If you think java was nothing when we talk about `==` in javascript we just not used two equals we use three to compare..yes it's kind of weird as it has it set of rules that we will talk about in the coming lines.

* `===` - Strictly Equal
    
* `==` - Equal
    

**Strictly Equal**`===`

The `===` operators follow **the Strictly equality comparison algorithm**, i.e., it doesn't do the type conversion of the operands before comparing their values and returns false even if the data type of the operands aren't the same.

The `===` operator compares operands and returns *true* if both operands are of the same data type and have some value, otherwise, it returns *false*.

```javascript
Code 2.0
const a = 10;
const b = '10';
const c = 10;
console.log(a === c);//true
console.log(a===b);//false
```

In this &lt;code 2.0&gt; the first statement compares the two datatypes and concludes the overall statement.

While in the other states, the data types are different..hence the conclusion is false.

```javascript
Code 2.1
const a = 'shashmit';
const b = new String('shashmit');
console.log(a==b);//true
console.log(a===b);//false
```

In this &lt;code 2.1&gt; the first statement compares the two data types by changing one type to the other and comparing it...hence it gives a true result.

while in the other states the conversion is not taking place and hence two different types produce false.

```javascript
Code 2.2
const a = new String('shashmit');
const b = new String('shashmit');
console.log(a===b);//false
console.log(a==b);//true
```

In this &lt;code 2.2&gt;, the first comparison is comparing two array-type strings without the array index which compares the address index of the two variables.

While in the next statement, compares the array as it is by comparing it.

**Equal**`==`

The `==` operator returns *true* if both operands are of the same data type and have the same value or if both are of different data types, but either of them can be converted to the data type of the other operand and have the same value. If both operands have different values, then it returns *false*.

*What is type conversion?*

The `==` operators *loosely* compare two operands, i.e., while comparing two operands, if both operands aren't of the same data type, then the operator tends to convert either of them into another operand's type and then compares their values.

```javascript
Code 2.5
const n = 10;
const p = '10;
console.log(n == p);//will be true
```

In the &lt;code 2.5&gt; here the p operand has been converted to the data type of n and then checked with the n value. As both of them are the same output is true.

```javascript
Code 2.6
let str1 = 'ShashmitKumar';
let str2 = 'Shashmitkumar';
let str3 = 'Shashmitkumar';
console.log(str1 == str2);
//output: false
console.log(str2 == str3);
//output: true
```

In the &lt;code 2.6&gt; here the two strings have been compared to each other and checked with each other.

References :

[Mozilla Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String).

[GFG](https://www.geeksforgeeks.org/difference-between-and-equals-method-in-java/)

[W3 Schools](https://www.w3schools.com/java/ref_string_equals.asp)

Thank you for following the whole process.

See you in the next blog related to something new, something that I’m also doing.

Follow me On [Twitter](https://twitter.com/Shaashmit)