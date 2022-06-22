# JavaScript-DOM-Basics

### Selectors

// Select the element or group of elements\
// Decide the effect we want to apply to selection

document.body.style.backgroundColor = 'blue';\
document.getElementById('btn').style.color = 'red';

// assign to a variable\
const element = document.getElementById('element');

// do something\
document.querySelector('element');

### getElementById

const h1 = document.getElementById('title');\
h1.style.color = 'red';

document.getElementById('btn').style.backgroundColor = 'blue';

### getElementByTagName

const headings = document.getElementsByTagName('h2');\
console.log(headings.length);

### getElementsByClassName

const list = document.getElementsByClassName('special');\
console.log(list);

### querySelector('any css'); - selects single

### querySelector('any css'); - selects all

const result = document.querySelector('#result');\
result.style.backgroundColor = 'blue';

const list = document.querySelectorAll('.special');\
console.log(list);

### Traverse the DOM Tree

// childNodes\
// children, firstChild, lastChild

const result = document.querySelector('#result');\
const children = result.children;\
console.log(children);\
console.log(result.firstChild);\
console.log(result.lastChild);

// parent Element

const heading = document.querySelector('h2');\
console.log(heading.parentElement);

// previousSibling\
// nextSibling\
// return whitespace

const first = document.querySelector('.first');\
const second = first.nextSibling.nextSibling;\
console.log(second);

// previousElementSibling\
//nextElementSibling

const first = document.querySelector('.first');\
first.nextElementSibling.style.color = 'red';

// nodeValue\
// textContent

const item = document.getElementById('special');\
const value = item.firstChild.nodeValue;

const easyValue = item.textContent;

### getAttribute & setAttribute

const first = document.querySelector('.first');
const classValue = first.getAttribute('class');

const link = document.getElementById('link');
const last = link.nextElementSibling;
last.setAttribute('class', 'first');
last.textContent = 'i also have a class of first';

const links = document.querySelectorAll('.first');

### className & classList

const first = document.getElementById('first');
const second = document.getElementById('second');
const third = document.getElementById('third');

// check class name
const classValue = first.className;
console.log(classValue);

// adding class
second.className = 'colors';

// adds classes without overriding
third.classList.add('colors', 'text');
third.classList.remove('text');

// checks to see if we have class
let result = third.classList.contains('colors');
if(result){
console.log("Yes we have colors class");
} else {
console.log('No we do not have colors class');
}

### createElement('element')

### createTextNode('text content')

### element.appendChild(childElement)

// create empty element\
const bodyDiv = document.createElement('div');

// create text node\
const text = document.createTextNode('a simple body div');

// add text to bodyDiv, then add bodyDiv to body\
bodyDiv.appendChild(text);\
document.body.appendChild(bodyDiv);

### innerHTML

const heading2 = document.createElement('h2');
heading2.innerHTML = '<h2>Heading 2</h2>';
document.body.appendChild(heading2);
