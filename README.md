# Uncommon HTML Error: Broken Image in innerHTML

This repository demonstrates an uncommon HTML error that arises from setting the `innerHTML` of an element with an image that has a broken `src` attribute.  This can lead to unexpected behavior and script errors in some browsers.  The solution showcases a safer approach using DOM manipulation.

## Bug

The `bug.html` file contains the erroneous code. It directly sets the `innerHTML` property using string concatenation including an image element that links to a non-existent image file. This may result in an error depending on browser's behavior and might silently fail on other browsers.

## Solution

The `bugSolution.html` file provides a more robust solution. Instead of directly using `innerHTML`, it uses `createElement` and `appendChild` to create and add the elements dynamically. This provides better control and reduces the chances of introducing errors. It also includes error handling to check if the image exists before appending it to the DOM.