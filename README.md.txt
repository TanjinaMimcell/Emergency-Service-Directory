1.What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Answer: 

Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll----
getElementById("id")--> A single element with the given id.	Returns null if not found and it is the fastest method.
getElementsByClassName("class")--> HTMLCollection of elements with the given class.	Live collection of auto-updates if DOM changes.
querySelector("selector")--> The first element matching any CSS selector. It can use id (#id), class (.class), tags, or combinations.
querySelectorAll("selector")--> NodeList of all elements matching the CSS selector.	It is a static collection and it does not auto-update.


2.How do you create and insert a new element into the DOM?

Answer: 

// 1. Create an element
const newDiv = document.createElement("div");

// 2. Add content or attributes
newDiv.textContent = "Hello World!";
newDiv.className = "my-div";

// 3. Choose parent element
const parent = document.getElementById("parentContainer");

// 4. Insert into DOM
parent.appendChild(newDiv); // adds as the last child
// OR
parent.insertBefore(newDiv, parent.firstChild); // inserts at the beginning


3.What is Event Bubbling and how does it work?

Answer: 

Event Bubbling: When an event occurs on a DOM element, it first runs on the target element and then “bubbles up” through its parent elements up to the document root.


4. What is Event Delegation and why is it useful?

Answer: 

Event Delegation: Instead of adding event listeners to many child elements, you add one listener to a common parent and check which child triggered the event using event.target.


It is useful for fewer event listeners → better performance and works for dynamically added elements (added after page load).


5. What is the difference between preventDefault() and stopPropagation() methods?

Answer: 

Method	Purpose
preventDefault() method	prevents the default action of an element (e.g., link navigation, form submission).
stopPropagation() method stops the event from bubbling (or capturing) further up/down the DOM tree.




