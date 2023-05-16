---
title: "#Day1 of Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
seoTitle: "JavaScript Drum Kit"
seoDescription: "Mastering JavaScript Fundamentals: The Complete Guide to JavaScript30"
datePublished: Wed May 10 2023 17:41:34 GMT+0000 (Coordinated Universal Time)
cuid: clhhzm87x000408mnhi704rnn
slug: day1-of-mastering-javascript-fundamentals-the-complete-guide-to-javascript30
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683663476895/89ce8447-b9d7-4d61-90ae-3ffce8d1a38d.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683740323701/a21a6428-1b6e-49f8-a874-a6a78e23adf8.png
tags: programming-blogs, css, javascript, web-development, html5

---

# JavaScript Drum Kit

One of his well-known projects is the JavaScript Drum Kit, which is actually the first project in the JavaScript30 course. The JavaScript Drum Kit is a simple application that allows users to play a virtual drum kit using their computer keyboard.

The project is built using HTML, CSS, and JavaScript, and it demonstrates several key concepts, including DOM manipulation, event listeners, and audio playback. The JavaScript Drum Kit is a great introduction to JavaScript for beginners, and it's a fun project for more experienced developers as well.

## Some of the concepts used in making the JavaScript Drum Kit!

1. ### DOM manipulation
    
    The Document Object Model (DOM) is the programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. In the JavaScript Drum Kit, DOM manipulation is used to select elements on the page (e.g. the drum pads and the corresponding audio files), add and remove CSS classes to change their appearance, and trigger events when they are clicked or pressed.
    
2. ### Event listeners
    
    An event listener is a function that waits for a specific event to occur, such as a click or keypress, and then executes a block of code in response. In the JavaScript Drum Kit, event listeners are used to detect when the user clicks or presses a key on their keyboard, and then play the corresponding audio file and animate the drum pad.
    
3. ### Audio playback
    
    The Web Audio API is a powerful JavaScript API for controlling sound in the browser. In the JavaScript Drum Kit, the Web Audio API is used to load and play the audio files associated with each drum pad.
    
4. ### CSS transitions
    
    CSS transitions are a way to animate changes to CSS properties over time. In the JavaScript Drum Kit, CSS transitions are used to create visual feedback when the user clicks or presses a key on the drum pad.
    

Overall, the JavaScript Drum Kit is a great example of how these concepts can be used together to create a fun and interactive application in the browser.

## How to create a simple drum kit using JavaScript! Here's an example of how you could get started:

1. Create an HTML file with the drum pads and audio elements:
    

```xml
<!DOCTYPE html>
<html>
<head>
	<title>JavaScript Drum Kit</title>
	<link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
	<div class="keys">
		<div data-key="65" class="key">
			<div class="sound">clap</div>
		</div>
		<div data-key="83" class="key">
			<div class="sound">hihat</div>
		</div>
		<div data-key="68" class="key">
			<div class="sound">kick</div>
		</div>
		<div data-key="70" class="key">
			<div class="sound">openhat</div>
		</div>
		<div data-key="71" class="key">
			<div class="sound">boom</div>
		</div>
		<div data-key="72" class="key">
			<div class="sound">ride</div>
		</div>
		<div data-key="74" class="key">
			<div class="sound">snare</div>
		</div>
		<div data-key="75" class="key">
			<div class="sound">tom</div>
		</div>
		<div data-key="76" class="key">
			<div class="sound">tink</div>
		</div>
	</div>

	<audio data-key="65" src="sounds/clap.wav"></audio>
	<audio data-key="83" src="sounds/hihat.wav"></audio>
	<audio data-key="68" src="sounds/kick.wav"></audio>
	<audio data-key="70" src="sounds/openhat.wav"></audio>
	<audio data-key="71" src="sounds/boom.wav"></audio>
	<audio data-key="72" src="sounds/ride.wav"></audio>
	<audio data-key="74" src="sounds/snare.wav"></audio>
	<audio data-key="75" src="sounds/tom.wav"></audio>
	<audio data-key="76" src="sounds/tink.wav"></audio>

	<script src="main.js"></script>
</body>
</html>
```

In this example, we have nine drum pads with different data-key attributes, and we also have nine audio elements with the same data-key attributes that correspond to the drum pads.

1. Create a CSS file to style the drum pads:
    

```css
.keys {
	display: flex;
	flex-wrap: wrap;
	align-items: center;
	justify-content: center;
	min-height: 100vh;
}

.key {
	border: .4rem solid black;
	border-radius: .5rem;
	margin: 1rem;
	font-size: 1.5rem;
	padding: 1rem .5rem;
	transition: all .07s ease;
	width: 10rem;
	text-align: center;
	color: white;
	background: rgba(0,0,0,0.4);
	text-shadow: 0 0 .5rem black;
}

.playing {
	transform: scale(1.1);
	border-color: #ffc600;
	box-shadow: 0 0 1rem #ffc600;
}
```

This CSS code sets up the layout and styling for the drum pads and also defines a CSS transition for the .playing class that we will add with JavaScript later.

Create a JavaScript:

Here's an example of how you could use JavaScript to create the drum kit and make it interactive:

```javascript
// Get all the drum pads and audio elements
const keys = Array.from(document.querySelectorAll('.key'));
const audioElements = Array.from(document.querySelectorAll('audio'));

// Add an event listener to each drum pad
keys.forEach(key => {
  key.addEventListener('click', () => playSound(key));
});

// Add an event listener to the document to detect keypresses
document.addEventListener('keydown', (event) => {
  const key = document.querySelector(`.key[data-key="${event.keyCode}"]`);
  playSound(key);
});

// Define the playSound function
function playSound(key) {
  // If there is no corresponding audio element, return
  if (!key || !key.classList.contains('key')) return;
  
  // Get the audio element with the same data-key as the drum pad
  const audio = document.querySelector(`audio[data-key="${key.dataset.key}"]`);
  
  // If there is no corresponding audio element, return
  if (!audio) return;
  
  // Add the .playing class to the drum pad and play the audio
  key.classList.add('playing');
  audio.currentTime = 0;
  audio.play();
  
  // Remove the .playing class from the drum pad after the transition has ended
  setTimeout(() => key.classList.remove('playing'), 70);
}
```

This JavaScript code does a few things:

1. It selects all the drum pads and audio elements on the page using the querySelectorAll method.
    
2. It adds an event listener to each drum pad that triggers the playSound function when the drum pad is clicked.
    
3. It adds an event listener to the document that triggers the playSound function when a key is pressed.
    
4. The playSound function takes a drum pad element as its argument and plays the corresponding audio element, adds the .playing class to the drum pad to trigger the CSS transition, and then removes the .playing class after the transition has ended.
    

With this JavaScript code, you should be able to create a simple drum kit that responds to both mouse clicks and key presses!

### A little about `data-key`

`data-key` is a custom attribute that can be added to HTML elements to store additional information about that element. It is prefixed with the word "data" and followed by any name you choose (e.g. `data-keyboard-key`, `data-color`, `data-product-id`, etc.).

In the HTML code for the drum kit, each drum pad element has a `data-key` attribute set to a specific value that corresponds to a key code (for example, the 'A' key is 65 in ASCII code, so the `data-key` attribute for the 'A' drum pad is set to 65).

In the JavaScript code, the `data-key` attribute is used to select the corresponding audio element to play when the drum pad is clicked or the corresponding key is pressed. For example, in the `playSound` function, the line `const audio = document.querySelector(`audio\[data-key="${key.dataset.key}"\]`);` selects the audio element with the `data-key` attribute that matches the `data-key` attribute of the drum pad that was clicked or the corresponding key that was pressed.

In summary, `data-key` is a custom attribute used to store data associated with an HTML element that can be accessed and used by scripts and programs. In the drum kit example, it is used to associate each drum pad element with a specific key code and audio clip.

# Summary

The JavaScript Drum Kit is a fun, interactive application that allows users to play a virtual drum kit using their computer keyboard. This project is built using HTML, CSS, and JavaScript and is a great introduction to JavaScript for beginners. It demonstrates key concepts such as DOM manipulation, event listeners, and audio playback. CSS transitions are also used to create visual feedback. This article provides an example of how to create a simple drum kit using JavaScript, HTML, and CSS.

# Other Reads

This blog provides a brief overview of the topics covered in the JavaScript30 course. For those looking for a quick review or to brush up on their JavaScript skills, this blog is a great resource. However, for a more comprehensive understanding of the topics covered, I highly recommend checking out the JavaScript30 course.

The JavaScript30 course covers a wide range of practical JavaScript projects that will help you build your skills and understanding of the language. The course is designed for anyone with a basic understanding of JavaScript and covers topics such as working with the DOM, manipulating CSS with JavaScript, making AJAX requests, and using ES6 features.

Overall, the JavaScript30 course is an excellent resource for anyone looking to improve their JavaScript skills and build practical projects. By following along with the course, you'll gain a solid understanding of the language and be able to apply your skills to real-world projects.

# Reference

* [JavaScript30 Course](https://javascript30.com/)
    
* Other [javascript30 Blogs](https://techsammy.hashnode.dev/series/javascript30) to follow along
    
* [keycode.info](http://keycode.info) : to see a specific value that corresponds to a key code (for example, the 'A' key is 65 in ASCII code