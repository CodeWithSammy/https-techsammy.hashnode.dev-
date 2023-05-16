---
title: "#Day2  of Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
seoTitle: "JS and CSS Clock"
seoDescription: "Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
datePublished: Thu May 11 2023 17:43:27 GMT+0000 (Coordinated Universal Time)
cuid: clhjf4ibq000h09mn4koz1doe
slug: day2-of-mastering-javascript-fundamentals-the-complete-guide-to-javascript30
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683825680386/d08bc31e-aa1e-491c-bc7b-9d32ec675d0a.png
tags: css, programming, javascript, technology, web-development

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683825866454/e720f0c7-dbd5-4a68-a5c4-9d96ef40b9a5.png align="center")

# JS and CSS Clock

One of the projects in the JavaScript30 course is the "CSS + JS Clock," which is a digital clock that displays the current time using both CSS and JavaScript. The clock is built using HTML, CSS, and JavaScript, and uses CSS animations to create the ticking effect.

If you're interested in learning more about the CSS + JS Clock project, you can check out the JavaScript30 course on Wes Bos's website, or search for tutorials and examples online.

## Some of the concepts used in making the (JS +CSS Clock)

1. ### CSS transforms
    
    The clock hands are rotated using CSS transforms. The `transform` property is used to rotate the hands by a certain number of degrees.
    
2. ### JavaScript Date object
    
    The current time is obtained using the JavaScript `Date` object. The `getHours()`, `getMinutes()`, and `getSeconds()` methods are used to get the current hour, minute, and second respectively.
    
3. ### setInterval() function
    
    The `setInterval()` function is used to update the clock every second. This function calls a specified function repeatedly at a specified time interval.
    
4. ### CSS transitions
    
    The smooth animation of the clock hands is achieved using CSS transitions. The `transition` property is used to specify the duration and easing function for the transition.
    
5. ### CSS variables
    
    CSS variables are used to store common values such as color and font size. This allows for easy customization of the clock appearance by simply changing the values of the variables.
    
6. ### Flexbox layout
    
    The clock is positioned using a flexbox layout, which allows for easy centering and positioning of the clock hands.
    

These are just a few of the concepts used in making the JS and CSS clock.

# Let's Create a similar version of The Clock

Here's a step-by-step guide on how to create a JavaScript and CSS clock:

1. First, we need to create a basic HTML structure for our clock. This will include a container div and three child divs for the hour, minute, and second hands.
    

```html
<div class="clock">
  <div class="hour-hand"></div>
  <div class="minute-hand"></div>
  <div class="second-hand"></div>
</div>
```

1. Next, we'll use CSS to style the clock and its hands. We'll set the width, height, and border-radius of the container div, and position the hands in the center of the clock face.
    

```css
.clock {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  position: relative;
  margin: 50px auto;
  box-shadow: inset 0 0 0 4px rgba(0,0,0,0.1), 
              0 0 0 8px rgba(0,0,0,0.2), 
              0 0 0 16px rgba(0,0,0,0.1);
}

.hand {
  position: absolute;
  top: 50%;
  width: 50%;
  height: 6px;
  transform-origin: 100%;
  transform: rotate(90deg);
  transition: all 0.05s;
  transition-timing-function: cubic-bezier(0.1, 2.7, 0.58, 1);
}
.hour-hand {
  height: 10%;
}
.minute-hand {
  height: 20%;
}
.second-hand {
  height: 30%;
  background-color: #ff4136;
}
```

Here we've set up the `clock` container to have a width and height of 300px, a border-radius of 50%, and a box-shadow to give it a nice 3D effect. We've also created a `.hand` class to position the hands, set their width and height, and rotate them 90 degrees so they're pointing straight up. We've also added a transition effect and a cubic-bezier timing function to make the hands move smoothly.

1. Now, we'll use JavaScript to get the current time and rotate the hands accordingly. We'll use the `Date()` object to get the current hour, minute, and second, and then use some simple math to calculate the degrees that each hand needs to rotate.
    

```javascript
const secondHand = document.querySelector('.second-hand');
const minuteHand = document.querySelector('.minute-hand');
const hourHand = document.querySelector('.hour-hand');

function setDate() {
  const now = new Date();

  const seconds = now.getSeconds();
  const secondsDegrees = ((seconds / 60) * 360) + 90;
  secondHand.style.transform = `rotate(${secondsDegrees}deg)`;

  const minutes = now.getMinutes();
  const minutesDegrees = ((minutes / 60) * 360) + ((seconds/60)*6) + 90;
  minuteHand.style.transform = `rotate(${minutesDegrees}deg)`;

  const hours = now.getHours();
  const hoursDegrees = ((hours / 12) * 360) + ((minutes/60)*30) + 90;
  hourHand.style.transform = `rotate(${hoursDegrees}deg)`;
}

setInterval(setDate, 1000);
```

Here we've defined three variables to hold references to the hour, minute, and second hands, and created a `setDate()` function that uses the `Date()` object to get the current time. We then use some simple math

## A simpler explanation of the javascript code

First, the `setDate()` function is used to get the current date and time. This is done by creating a new `Date` object and storing it in the `now` variable.

Next, the `getSeconds()`, `getMinutes()`, and `getHours()` methods are used to get the current seconds, minutes, and hours from the `now` object, respectively. These values are then used to calculate the degree of rotation for the second, minute, and hour hands of the clock.

The degree of rotation is calculated by multiplying the current value (seconds, minutes, or hours) by a factor that represents how many degrees of rotation are needed for each unit of time (60 for seconds and minutes, and 12 for hours).

For example, to calculate the degree of rotation for the second hand, we take the current seconds value and multiply it by 6 (since there are 60 seconds in a minute, and 360 degrees in a full rotation, 360/60 = 6).

The same process is applied to the minute and hour hands, using their respective factors of 6 and 30 (since there are 60 minutes in an hour, and 12 hours in a day).

Finally, the `style.transform` property is used to rotate each of the hands to their appropriate degree of rotation, using the `rotate()` function in CSS

# Summary

The JS and CSS Clock project by Wes Bos is a digital clock that shows the current time using both CSS and JavaScript. The clock is built using HTML, CSS, and JavaScript, and uses CSS animations to create the ticking effect. The concepts used in the project include CSS transforms, JavaScript Date object, setInterval() function, CSS transitions, CSS variables, Math functions, and Flexbox layout. To create a similar clock, you can follow a step-by-step guide that includes creating a basic HTML structure for the clock, styling it using CSS, and rotating the hands using JavaScript.

I hope this helps! Let me know if you have any further questions in the comment section, I'll be happy to answer.

# Other Reads

This blog provides a brief overview of the topics covered in the JavaScript30 course. For those looking for a quick review or to brush up on their JavaScript skills, this blog is a great resource. However, for a more comprehensive understanding of the topics covered, I highly recommend checking out the JavaScript30 course.

The JavaScript30 course covers a wide range of practical JavaScript projects that will help you build your skills and understanding of the language. The course is designed for anyone with a basic understanding of JavaScript and covers topics such as working with the DOM, manipulating CSS with JavaScript, making AJAX requests, and using ES6 features.

Overall, the JavaScript30 course is an excellent resource for anyone looking to improve their JavaScript skills and build practical projects. By following along with the course, you'll gain a solid understanding of the language and be able to apply your skills to real-world projects.

# Reference

* [JavaScript30 Course](https://javascript30.com/)
    
* Other [javascript30 Blogs](https://techsammy.hashnode.dev/series/javascript30) to follow along