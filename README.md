# JavaScript-DOM-Basics

// Select the element or group of elements
// Decide the effect we want to apply to selection

document.body.style.backgroundColor = 'blue';
document.getElementById('btn').style.color = 'red';

// assign to a variable
const element = document.getElementById('element');

// do something
document.querySelector('element');

### getElementById

const h1 = document.getElementById('title');
h1.style.color = 'red';

document.getElementById('btn').style.backgroundColor = 'blue';

### getElementByTagName

const headings = document.getElementsByTagName('h2');
console.log(headings.length);
