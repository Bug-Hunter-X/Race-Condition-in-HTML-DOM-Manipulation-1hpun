# Race Condition in HTML DOM Manipulation

This repository demonstrates a subtle race condition that can occur when JavaScript attempts to manipulate the DOM before the HTML parser has completed. This is an uncommon error that can be hard to track down.

## Bug Description

The `bug.html` file contains a simple HTML document with a div element. A JavaScript script tries to change the innerHTML of this div. However, if the script executes *before* the browser has finished parsing the HTML, it might not find the div element, resulting in an error (or unexpected behavior). This race condition is dependent on the browser's parsing speed and the order of execution.