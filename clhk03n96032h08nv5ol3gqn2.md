---
title: "#Day3  of Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
seoTitle: "CSS Variables"
seoDescription: "Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
datePublished: Fri May 12 2023 03:30:39 GMT+0000 (Coordinated Universal Time)
cuid: clhk03n96032h08nv5ol3gqn2
slug: day3-of-mastering-javascript-fundamentals-the-complete-guide-to-javascript30
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683833608061/1f7d9476-91be-436b-b878-138fef8b2c75.png
tags: css, programming, javascript, web-development, hashnode

---

# CSS Variables

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683834654426/1164e68c-7a0d-45b4-90be-45733d4ad716.png align="center")

Working with CSS Variables and how to manipulate them dynamically using JavaScript. In this project, you'll learn how to create and use CSS variables to easily update styles across your web page, without having to modify the CSS file directly.

The project involves creating a web page with a few different inputs, such as sliders and color pickers, that dynamically update the CSS variables that control the page's color scheme and layout. The goal is to create a live preview of how the changes will look on the page in real-time.

Throughout the project, Wes Bos provides step-by-step instructions on how to manipulate the CSS variables using JavaScript, as well as tips and best practices for using CSS variables effectively in your projects.

# Concepts We'll Use in Making this Project

The CSS Variables project in Wes Bos's JavaScript30 course utilizes several key concepts, including:

1. ### CSS Variables
    
    This project demonstrates the power and usefulness of CSS Variables, which allow you to define values that can be reused throughout your stylesheet.
    
2. ### Manipulating CSS with JavaScript
    
    The project uses JavaScript to dynamically update CSS properties, allowing you to change things like color, spacing, and blur effects in real-time.
    
3. ### Event Listeners
    
    The project uses event listeners to detect when the user interacts with the page (e.g., when they move a slider or click a checkbox), and then triggers corresponding JavaScript functions to update the CSS.
    
4. ### Data Attributes
    
    The project uses data attributes to store additional information about HTML elements, such as the value of a slider or the name of a color.
    

Overall, the project demonstrates how CSS and JavaScript can work together to create dynamic and interactive web pages, and how you can use modern web development techniques to create powerful user experiences.

# Creating the Project...

First, let's create a basic HTML structure for our project:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>CSS Variables</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h2>Update CSS Variables with <span class='hl'>JS</span></h2>
  <div class="controls">
    <label for="spacing">Spacing:</label>
    <input type="range" name="spacing" min="10" max="200" value="10" data-sizing="px">

    <label for="blur">Blur:</label>
    <input type="range" name="blur" min="0" max="25" value="0" data-sizing="px">

    <label for="base">Base Color</label>
    <input type="color" name="base" value="#ffc600">
  </div>

  <img src="https://source.unsplash.com/7bwQXzbF6KE/800x500">

  <script src="main.js"></script>
</body>
</html>
```

In the above code, we have included the necessary HTML elements like a `div` container for the controls, `input` elements to capture the user inputs for spacing, blur, and color, and an image element to apply the styles.

Next, let's create a CSS file `style.css` and apply some basic styles to the elements:

```css
:root {
  --base-color: #ffc600;
  --spacing: 10px;
  --blur: 0px;
}

img {
  padding: var(--spacing);
  background: var(--base-color);
  filter: blur(var(--blur));
}
```

In the above code, we have defined three CSS variables in the `:root` selector, which will hold the values for `--base-color`, `--spacing`, and `--blur`. We have also applied these CSS variables to the `img` element's `padding`, `background`, and `filter` properties.

Now, let's write the JavaScript code in `main.js` to update the CSS variables based on user input:

```javascript
const inputs = document.querySelectorAll('.controls input');

function handleUpdate() {
  const suffix = this.dataset.sizing || '';
  document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
}

inputs.forEach(input => input.addEventListener('change', handleUpdate));
inputs.forEach(input => input.addEventListener('mousemove', handleUpdate));
```

In the above code, we have selected all the `input` elements with the class `controls` using the `querySelectorAll()` method. We have also defined a function `handleUpdate()` to update the CSS variables based on the user input. The `suffix` variable holds the units (like px or em) of the input value, which is stored in the `data-sizing` attribute of each `input` element. We have used the `setProperty()` method to update the CSS variables with the new values.

Finally, we have added two event listeners to each `input` element, one for the `change` event and another for the `mousemove` event. This way, the CSS variables will update in real-time as the user moves the range slider.

That's it! We have successfully created the "CSS Variables" project with HTML, CSS, and JavaScript.

# JavaScript is Simplified

First, we are selecting the inputs that control the CSS variables using the `querySelectorAll` method. This method selects all elements that match the provided CSS selector, in this case, all inputs with a `data-sizing` attribute.

Next, we are setting up event listeners on each of these inputs using a `forEach` loop. This loop iterates over each input element and attaches a `change` event listener to it.

When one of these input elements changes, the event listener function is called. Inside this function, we are updating the CSS variable associated with that input element by setting its value equal to the value of the input. We are using the `dataset` property of the input element to get the value of the `data-sizing` attribute, which we use to append the appropriate unit to the CSS variable value.

Finally, we are updating the preview element to reflect the changes made to the CSS variables. We are using the `setProperty` method to update the CSS values for the `--base`, `--spacing`, and `--blur` variables, based on the values of the corresponding input elements.

# Summary

The third project in the Javascript30 course by Wes Bos focuses on the creation and manipulation of CSS variables using JavaScript. Through this project, the user learns how to create and apply CSS variables that control the styling and layout of a web page, without the need to modify the CSS file.

The web page created in this project contains various inputs that update the CSS variables dynamically, giving the user a live preview of the changes made in real-time. The project demonstrates the effective use of CSS variables, JavaScript, event listeners, and data attributes to create interactive web pages.

I hope this explanation helps! Let me know if you have any further questions.

# Other Reads

This blog provides a brief overview of the topics covered in the JavaScript30 course. For those looking for a quick review or to brush up on their JavaScript skills, this blog is a great resource. However, for a more comprehensive understanding of the topics covered, I highly recommend checking out the JavaScript30 course.

The JavaScript30 course covers a wide range of practical JavaScript projects that will help you build your skills and understanding of the language. The course is designed for anyone with a basic understanding of JavaScript and covers topics such as working with the DOM, manipulating CSS with JavaScript, making AJAX requests, and using ES6 features.

Overall, the JavaScript30 course is an excellent resource for anyone looking to improve their JavaScript skills and build practical projects. By following along with the course, you'll gain a solid understanding of the language and be able to apply your skills to real-world projects.

# Reference

* [JavaScript30 Course](https://javascript30.com/)
    
* Other [javascript30 Blogs](https://techsammy.hashnode.dev/series/javascript30) to follow along