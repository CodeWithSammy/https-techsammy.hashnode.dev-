---
title: "#Day4  of Mastering JavaScript Fundamentals: 
The Complete Guide to JavaScript30"
seoTitle: "Array Methods"
seoDescription: "#Day4  of Mastering JavaScript Fundamentals: 
The Complete Guide to JavaScript30"
datePublished: Sat May 13 2023 07:34:43 GMT+0000 (Coordinated Universal Time)
cuid: clhlo9ds7023il9nvgfxf54m4
slug: day4-of-mastering-javascript-fundamentals-the-complete-guide-to-javascript30
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683960318352/7c417c05-c91f-4755-8d12-6cd2fe359d1d.png
tags: programming, javascript, web-development, beginners, hashnode

---

# Array Cardio Day 1

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683970459133/3c55a60e-59a4-455e-9469-31fe8b0528ec.png align="center")

In the first part of his "Array Cardio" tutorial series, Wes Bos covers some useful array methods in JavaScript. He demonstrates how to use these methods by manipulating an array of objects containing information about different people. The methods covered in this tutorial include filter(), map(), sort(), and reduce(). Bos provides real-life examples of how each of these methods can be used to manipulate and extract data from arrays efficiently. By the end of this tutorial, you'll have a better understanding of how to work with arrays in JavaScript and how these methods can help you write more effective code.

# Array Methods/Functions used

Here's a brief overview of the array methods used in the Array Cardio Day 1 project:

1. `filter()` method:
    
    This method creates a new array with all elements that pass the test implemented by the provided function.
    
2. `map()` method:
    
    This method creates a new array with the results of calling a provided function on every element in the calling array.
    
3. `sort()` method:
    
    This method sorts the elements of an array in place and returns the sorted array.
    
4. `reduce()` method:
    
    This method applies a function against an accumulator and each element in the array to reduce it to a single value.
    

By using these array methods, we can manipulate and transform arrays in various ways to obtain the desired results.

# Code Snippets

Here are some code snippets and explanations to get you started:

```html
 const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
      { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
      { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
      { first: 'Marie', last: 'Curie', year: 1867, passed: 1934 },
      { first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630 },
      { first: 'Nicolaus', last: 'Copernicus', year: 1473, passed: 1543 },
      { first: 'Max', last: 'Planck', year: 1858, passed: 1947 },
      { first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979 },
      { first: 'Ada', last: 'Lovelace', year: 1815, passed: 1852 },
      { first: 'Sarah E.', last: 'Goode', year: 1855, passed: 1905 },
      { first: 'Lise', last: 'Meitner', year: 1878, passed: 1968 },
      { first: 'Hanna', last: 'Hammarström', year: 1829, passed: 1909 }
    ];
```

* `Array.prototype.filter()`:
    

This method creates a new array with all elements that pass the test implemented by the provided function. In the project, we use this method to filter out data based on specific conditions. Here's an example code snippet:

```javascript
const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600));
```

* [`Array.prototype.map`](http://Array.prototype.map)`()`:
    

This method creates a new array populated with the results of calling a provided function on every element in the calling array. In the project, we use this method to transform data into a new format. Here's an example code snippet:

```javascript
const fullNames = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
```

* `Array.prototype.sort()`:
    

This method sorts the elements of an array in place and returns the sorted array. In the project, we use this method to sort data based on specific criteria. Here's an example code snippet:

```javascript
//Sort the inventors by birthdate, oldest to youngest
const ordered = inventors.sort((a, b) => a.year > b.year ? 1 : -1);

//for Sorting the inventors by years lived
const oldest = inventors.sort(function(a,b){
      const lastGuy = a.passed - a.year;
      const nextGuy = b.passed - b.year;
      return lastGuy > nextGuy ? -1 : 1;
    });
    console.table(oldest);
```

* `Array.prototype.reduce()`:
    

This method executes a reducer function on each element of the array, resulting in a single output value. In the project, we use this method to perform calculations on data. Here's an example code snippet:

```javascript
const totalYears = inventors.reduce((total, inventor) => {
  return total + (inventor.passed - inventor.year);
}, 0);
```

I hope these code snippets and explanations help you get started on creating the "Array Cardio Day 1" project!

# Summary

In this Blog, we covered how the "Array Cardio Day 1" tutorial series by Wes Bos covers several useful array methods in JavaScript, including filter(), map(), sort(), and reduce(). Bos provides real-life examples of how each of these methods can be used to manipulate and extract data from arrays efficiently, using an array of objects containing information about different people. By using these array methods, we can manipulate and transform arrays in various ways to obtain the desired results. The tutorial also includes code snippets that demonstrate the use of these array methods, such as filtering out data based on specific conditions, transforming data into a new format, sorting data based on specific criteria, and performing calculations on data.

# Other Reads

This blog provides a brief overview of the topics covered in the JavaScript30 course. For those looking for a quick review or to brush up on their JavaScript skills, this blog is a great resource. However, for a more comprehensive understanding of the topics covered, I highly recommend checking out the JavaScript30 course.

The JavaScript30 course covers a wide range of practical JavaScript projects that will help you build your skills and understanding of the language. The course is designed for anyone with a basic understanding of JavaScript and covers topics such as working with the DOM, manipulating CSS with JavaScript, making AJAX requests, and using ES6 features.

Overall, the JavaScript30 course is an excellent resource for anyone looking to improve their JavaScript skills and build practical projects. By following along with the course, you'll gain a solid understanding of the language and be able to apply your skills to real-world projects.

# Reference

* [JavaScript30 Course](https://javascript30.com/)
    
* Other [javascript30 Blogs](https://techsammy.hashnode.dev/series/javascript30) to follow along