👋 Welcome to `stack.js`!

**Status : Beta**
`stack.js` is a lightweight JavaScript framework for building web applications. It provides a set of helpful functions for handling common tasks such as rendering, event listeners, element manipulation, lazy loading, and more.

## 📦 Installation

you can include the `stack.js` script directly in your HTML file:

    <script src="stack.js"></script>
## 🚀 Getting Started

To start using `stack.js`, simply include the script in your HTML file, and start using its functions. Here's an example of how to render data to an element using `stack.js`:

    stk.render('my-element', 'Hello, World!');

Stack is a lightweight JavaScript framework for building web applications. It includes several functions that make it easy to manipulate the DOM, interact with data, and manage application state. This documentation will cover each of these functions in detail, including examples of how to use them in your own projects.

## stk.getData

    stk.getData(url, successCallback, errorCallback, type);
The `stk.getData` function makes an AJAX request to the specified URL and returns the response. It takes four arguments:

-   `url`: The URL to request.
-   `successCallback`: A function to call if the request is successful. This function should take one argument, which will be the response from the server.
-   `errorCallback`: A function to call if the request fails. This function should take one argument, which will be an error message.
-   `type`: The type of request to make (e.g. "GET" or "POST").

Example usage:

    stk.getData("https://jsonplaceholder.typicode.com/posts", function(response) {
      console.log(response);
    }, function(error) {
      console.error(error);
    }, "GET");
## stk.render

    stk.render(id, data);
The `stk.render` function updates the HTML content of an element with the specified ID. It takes two arguments:

-   `id`: The ID of the element to update.
-   `data`: The HTML content to insert into the element.

Example usage:

    stk.render("content", "<h1>Hello, World!</h1>");
## stk.navigateTo

    stk.navigateTo(url);
The `stk.navigateTo` function redirects the user to the specified URL. It takes one argument:

-   `url`: The URL to navigate to.

Example usage:

    stk.navigateTo("https://example.com");
## stk.listener

    stk.listener(id, event, func, usecapture);
The `stk.listener` function attaches an event listener to the element with the specified ID. It takes four arguments:

-   `id`: The ID of the element to attach the event listener to.
-   `event`: The name of the event to listen for (e.g. "click").
-   `func`: The function to call when the event is triggered.
-   `usecapture`: Whether to use event capture. Defaults to `false`.

Example usage:

    stk.listener("button", "click", function() {
      console.log("Button clicked!");
    });
## stk.createElement

    stk.createElement(tagName, attributes, content);
The `stk.createElement` function creates a new HTML element with the specified tag name, attributes, and content. It takes three arguments:

-   `tagName`: The name of the HTML tag to create (e.g. "div").
-   `attributes`: An object containing the attributes to set on the new element.
-   `content`: The HTML content to insert into the new element.

Example usage:

    var div = stk.createElement("div", { "class": "container" }, "<h1>Hello, World!</h1>");
    stk.appendElement(document.body, div);
## stk.appendElement

    stk.appendElement(parentElement, childElement);
The `stk.appendElement` function appends a child element to a parent element. It takes two arguments:

-   `parentElement`: The element to append the child element to.
-   `childElement`: The element to append.

Example usage:

    var parent = document.getElementById("container");
    var child = document.createElement("div");
    stk.appendElement(parent, child);
## stk.removeElement

The `stk.removeElement(element)`

Removes an element from the DOM.

Parameters:

-   `element` (required): The element to remove.

Example Usage:

        <div id="myDiv">
      <p>Hello, world!</p>
    </div>
    <button onclick="removeMyDiv()">Remove</button>
    
    <script>
    function removeMyDiv() {
      var myDiv = document.getElementById("myDiv");
      stk.removeElement(myDiv);
    }
    </script>


## stk.addClass

The` stk.addClass(element, className)`

Adds a class to an element.

Parameters:

-   `element` (required): The element to add the class to.
-   `className` (required): The name of the class to add.

Example Usage:

    <div id="myDiv">
      <p>Hello, world!</p>
    </div>
    <button onclick="addClassToMyDiv()">Add class</button>
    
    <script>
    function addClassToMyDiv() {
      var myDiv = document.getElementById("myDiv");
      stk.addClass(myDiv, "highlight");
    }
    </script>

## stk.removeClass
The `stk.removeClass(element, className)`

Removes a class from an element.

Parameters:

-   `element` (required): The element to remove the class from.
-   `className` (required): The name of the class to remove.

Example Usage:

    <div id="myDiv" class="highlight">
      <p>Hello, world!</p>
    </div>
    <button onclick="removeClassFromMyDiv()">Remove class</button>
    
    <script>
    function removeClassFromMyDiv() {
      var myDiv = document.getElementById("myDiv");
      stk.removeClass(myDiv, "highlight");
    }
    </script>
    /* CSS code */
    .highlight {
      background-color: yellow;
    }
## stk.setStyle

The `stk.setStyle(element, styleName, styleValue)`

Sets a style for an element.

Parameters:

-   `element` (required): The element to set the style for.
-   `styleName` (required): The name of the style to set.
-   `styleValue` (required): The value of the style to set.

Example Usage:

    <div id="myDiv">
      <p>Hello, world!</p>
    </div>
    <button onclick="setStyleForMyDiv()">Set style</button>
    
    <script>
    function setStyleForMyDiv() {
      var myDiv = document.getElementById("myDiv");
      stk.setStyle(myDiv, "background-color", "yellow");
    }
    </script>
    
    /* CSS code */
    #myDiv {
      background-color: yellow;
    }
## stk.getComputedStyle
The `stk.getComputedStyle(element, styleName)`

Gets the computed style of an element.

Parameters:

-   `element` (required): The element to get the computed style of.
-   `styleName` (required): The name of the style to get.

Returns:

-   The computed style of the element.

Example Usage:

    <div id="myDiv" style="background-color: yellow;">
      <p>Hello, world!</p>
    </div>
    <button onclick="getComputedStyleOfMyDiv()">Get computed style</button>
    
    <script>
    function getComputedStyleOfMyDiv() {
      var myDiv = document.getElementById("myDiv");
      var backgroundColor = stk.getComputedStyle(myDiv, "background-color");
      alert("Background color is: " + backgroundColor);
    }
    </script>
    /* CSS code */
    #myDiv {
      background-color: yellow;
    }

