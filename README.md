# Uncommon HTML Bug: Accessing Element Before DOM Load

This repository demonstrates a common yet often overlooked HTML bug: attempting to manipulate a DOM element before it has been fully loaded by the browser. The bug occurs when JavaScript code tries to access and modify an element's properties (like `innerHTML`) before that element exists in the Document Object Model (DOM). 

## The Bug
The `bug.html` file contains a simple HTML page with a div element. A script tries to modify its innerHTML.  However, if the script runs *before* the element is parsed, a runtime error will occur because `getElementById` will return `null`.

## The Solution
The `bugSolution.html` file demonstrates a correct approach.  It uses the `DOMContentLoaded` event listener to ensure that the script runs only after the entire HTML document has been parsed and the DOM is ready.