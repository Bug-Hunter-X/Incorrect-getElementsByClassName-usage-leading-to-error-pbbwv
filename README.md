# Uncommon HTML Bug: Incorrect getElementsByClassName Usage

This repository demonstrates an uncommon error that can occur when using `getElementsByClassName` in HTML/JavaScript. The bug arises from incorrectly assuming that `getElementsByClassName` returns a single element when it actually returns a collection of elements.  Attempting to access an element by index before checking if the collection is empty results in a runtime error.

## Bug Description:
The `bug.html` file contains a JavaScript snippet that attempts to access an element using `getElementsByClassName`. The targeted class ('nonExistentClass') does not exist in the HTML, leading to an empty `HTMLCollection` being returned.  The code then proceeds to access `elements[0]`, which throws a `TypeError: Cannot read properties of undefined (reading 'innerHTML')` error because there's no element at index 0.

## Solution:
The `bugSolution.html` file demonstrates the correct approach to accessing elements obtained using `getElementsByClassName`. It includes error handling to check if the collection is empty before attempting to access any elements.