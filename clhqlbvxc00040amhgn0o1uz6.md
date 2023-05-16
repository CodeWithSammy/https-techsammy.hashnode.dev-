---
title: "#Day7  of Mastering JavaScript Fundamentals: 
The Complete Guide to JavaScript30"
seoTitle: "Array Cardio"
seoDescription: "#Day7  of Mastering JavaScript Fundamentals: 
The Complete Guide to JavaScript30"
datePublished: Tue May 16 2023 18:11:32 GMT+0000 (Coordinated Universal Time)
cuid: clhqlbvxc00040amhgn0o1uz6
slug: day7-of-mastering-javascript-fundamentals-the-complete-guide-to-javascript30
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684260030037/350f7905-83db-468f-ad08-c7472b2d8ad1.png
tags: programming-blogs, programming, javascript, web-development, array-methods

---

# Array Cardio Day2

In Day 7 of the JavaScript30 course by Wes Bos, the focus is on further exploring and practicing array methods through the "Array Cardio Day 2" project. This project builds upon the concepts covered in Day 4's "Array Cardio Day 1" project. The main goal is to gain proficiency in using advanced array methods such as some(), every(), findIndex(), and splice().

Throughout the project, Wes Bos provides a set of real-world coding challenges that involve manipulating arrays and extracting specific data. By working through these challenges, participants learn how to leverage the power of array methods to efficiently solve common programming problems. The project emphasizes the importance of understanding array methods and their capabilities, enabling developers to write clean and concise code while working with arrays.

By completing "Array Cardio Day 2," participants strengthen their array manipulation skills, expand their understanding of advanced array methods, and gain confidence in using these methods to solve complex coding tasks.

# "Array Cardio Day 2" key concepts

**Related to array manipulation and advanced array methods are covered. Here are the key concepts used in this project:**

1. Array methods:
    
    The project focuses on advanced array methods such as some(), every(), findIndex(), and splice(). These methods allow for efficient array manipulation and data extraction.
    
2. Data filtering:
    
    The project demonstrates how to filter arrays based on specific criteria using methods like some() and every(). These methods test the elements of an array against a condition and return a Boolean value.
    
3. Data searching:
    
    The project explores methods like findIndex() to search for specific elements in an array. findIndex() returns the index of the first element that satisfies a given condition.
    
4. Array mutation:
    
    The project introduces the splice() method, which allows for in-place modification of an array by adding, removing, or replacing elements.
    
5. Arrow functions:
    
    The project utilizes arrow function syntax to write concise and readable code. Arrow functions provide a shorthand way of defining functions.
    

By understanding and applying these key concepts, developers can effectively manipulate arrays, filter data, search for elements, and modify arrays using advanced array methods in JavaScript.

# Explaining the concepts with Code snippets

Here's a step-by-step walkthrough along with code snippets:

1. Start by creating an array of inventors:
    

```javascript
const inventors = [
  { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
  { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
  { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
  // Add more inventors here...
];
```

1. Implement the following functionalities:
    

* Use the `some()` method to check if at least one inventor was born in the 19th century:
    

```javascript
const nineteenthCenturyInventor = inventors.some(
  inventor => inventor.year >= 1800 && inventor.year < 1900
);
console.log(nineteenthCenturyInventor);
```

* Use the `every()` method to check if all inventors lived at least until the age of 80:
    

```javascript
const allInventorsLivedLong = inventors.every(
  inventor => inventor.passed - inventor.year >= 80
);
console.log(allInventorsLivedLong);
```

* Use the `findIndex()` method to find the index of the inventor with the last name "Galilei":
    

```javascript
const galileiIndex = inventors.findIndex(
  inventor => inventor.last === 'Galilei'
);
console.log(galileiIndex);
```

* Use the `splice()` method to remove the inventor with the last name "Galilei" from the array:
    

```javascript
inventors.splice(galileiIndex, 1);
console.log(inventors);
```

1. Finally, you can experiment with other array methods like `map()`, `sort()`, `reduce()`, etc., to further manipulate and explore the `inventors` array.
    

By following these steps and using the provided code snippets, you'll be able to create the "Array Cardio Day 2" project and gain hands-on experience with advanced array methods in JavaScript.

# Summary

Array Cardio Day 2 is part of the JavaScript30 course by Wes Bos, focusing on advanced array methods. The project builds upon concepts from Day 4 and aims to strengthen array manipulation skills. Key concepts include advanced array methods (some(), every(), findIndex(), splice()), data filtering, searching, array mutation, and arrow functions. Participants solve real-world coding challenges by leveraging these methods. Code snippets are provided to demonstrate how to create an array of inventors, filter data, check conditions, find indexes, and modify arrays. By completing the project, participants enhance their understanding of advanced array methods and improve their array manipulation abilities in JavaScript.

# Other Reads

This blog provides a brief overview of the topics covered in the JavaScript30 course. For those looking for a quick review or to brush up on their JavaScript skills, this blog is a great resource. However, for a more comprehensive understanding of the topics covered, I highly recommend checking out the JavaScript30 course.

The JavaScript30 course covers a wide range of practical JavaScript projects that will help you build your skills and understanding of the language. The course is designed for anyone with a basic understanding of JavaScript and covers topics such as working with the DOM, manipulating CSS with JavaScript, making AJAX requests, and using ES6 features.

Overall, the JavaScript30 course is an excellent resource for anyone looking to improve their JavaScript skills and build practical projects. By following along with the course, you'll gain a solid understanding of the language and be able to apply your skills to real-world projects.

# Reference

* [JavaScript30 Course](https://javascript30.com/)
    
* Other [javascript30 Blogs](https://techsammy.hashnode.dev/series/javascript30) to follow along