# Web Development Question Bank CAE-2

<iframe src="https://drive.google.com/file/d/15gl6diuYMrl1btfyIE8X8FSJKNHxPaOr/preview" width="800px" height="800px"></iframe>

## Questions

1. [Describe the process of styling the background and text of an HTML element using CSS. Provide an example of how to set a background color and change the text color of a paragraph element.](#ans1) [CO3]

2. [Explain the role of CSS selectors in applying styles.](#ans2) [CO3]

3. [What is JavaScript, and what are its main advantages in web development? Provide at least 5 key features or applications of using JavaScript.](#ans3) [CO4]

4. [Explain the purpose and usage of JavaScript popup boxes. Provide an example of each type of popup box and describe when you might use them in a web application.](#ans4) [CO4]

5. [Describe the CSS Box Model and its components. Explain how padding, margin, and border affect the layout of an HTML element. Additionally, provide an example of an advanced CSS technique or property used to create a responsive web design layout.](#ans5) [CO4]

6. [Explain the concept of Cascading Style Sheets (CSS) and provide at least three CSS properties commonly used in web design. Briefly describe how each property affects the styling of a web page.](#ans6) [CO3]

7. [Design & implement all types of popup boxes using JavaScript code for password validation.](#ans7) [CO4]

8. [Display the current Date and Time using JavaScript.](#ans8) [CO4]

9. [Difference between `<span>` and `<p>` tag.](#ans9) [CO3]

10. [What makes JavaScript a dynamically typed language?](#ans10) [CO4]

11. [Show how Let, Var, and Const differ from one another.](#ans11) [CO3]

12. [Design a basic navigation bar with HTML and CSS.](#ans12) [CO3]

13. [Design a Search bar using CSS and HTML.](#ans13) [CO3]

14. [What are the input types for form validation in HTML? Explain with an example how to style the input fields.](#ans14) [CO3]

15. [How do we create a hyperlink in an HTML page and what are the ways to style the different states of hyperlinks?](#ans15) [CO3]

16. [Design a feedback form using HTML and CSS.](#ans16) [CO3]

17. [Write complete HTML code that will print an unordered list containing the following elements: Array, Link List, Stack, Queues, Stack, Graphs.](#ans17) [CO3]

18. [Write HTML and CSS code to design the following form: Name (Textbox), Address (Textbox), Mobile No (Textbox), Class (dropdown containing FY, SY, TY, BTECH), Division (Dropdown containing A, B, C), Percentage (Textbox). All elements should have a border of Blue color with a width of 200 pixels.](#ans18) [CO3]

19. [Why is JavaScript a cross-platform language? Explain the advantages of JavaScript.](#ans19) [CO4]

20. [Explain the following terms with suitable examples: Hyperlink, Types of Lists, Table tags.](#ans20)

## Answers

## Question 1: Describe the process of styling the background and text of an HTML element using CSS. Provide an example of how to set a background color and change the text color of a paragraph element

###### Ans1

To style the background and text of an HTML element using CSS, you can use CSS properties. Let's consider a <p> (paragraph) element as an example and demonstrate how to set a background color and change the text color:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS code to style the paragraph element */
      p {
        background-color: lightblue; /* Set the background color */
        color: darkred; /* Change the text color */
        padding: 20px; /* Add padding for better readability */
      }
    </style>
  </head>
  <body>
    <p>
      This is a styled paragraph with a custom background color and text color.
    </p>
  </body>
</html>
```

In the above code:

- We use the `<style>` element within the `<head>` section to embed our CSS styles.
- We target the `<p>` element using the p selector.
- To set the background color, we use the background-color property and specify a color value (e.g., lightblue).
- To change the text color, we use the color property and specify a different color value (e.g., darkred).
- We also added padding to the paragraph for better spacing and readability using the padding property.

You can customize the background color, text color, and other CSS properties as needed to achieve the desired styling for your HTML elements.

## Question 2: Explain the role of CSS selectors in applying styles

###### Ans2

CSS selectors play a crucial role in applying styles to HTML elements. They allow you to target specific elements or groups of elements and apply styling rules to them. Here are some key aspects of CSS selectors:

- Element Selectors: These selectors target specific HTML elements by their tag names. For example, p selects all `<p>` elements, and h1 selects all `<h1>` elements.

- Class Selectors: Class selectors allow you to target elements with a specific class attribute. For example, .btn selects all elements with the class "btn."

- ID Selectors: ID selectors target a single unique element based on its id attribute. For example, #header selects the element with the ID "header."

- Descendant Selectors: These selectors target elements that are descendants of another element. For instance, ul li selects all `<li>` elements within `<ul>` elements.

- Pseudo-classes: Pseudo-classes allow you to target elements based on their state or position. For example, a:hover selects all anchor `<a>` elements when hovered.

- Attribute Selectors: Attribute selectors target elements based on their attributes. For instance, `[type="text"]` selects all elements with a type attribute set to "text."

- Combination Selectors: You can combine multiple selectors to target specific elements more precisely. For example, ul.nav li selects `<li>` elements within a `<ul>` element with the class "nav."

CSS selectors are powerful tools that enable you to apply styles selectively to HTML elements, making it possible to create visually appealing and well-structured web pages.

## Question 3: What is JavaScript, and what are its main advantages in web development? Provide at least 5 key features or applications of using JavaScript

###### Ans3

JavaScript is a versatile and widely used programming language primarily employed in web development. Here are five key features and applications of JavaScript in web development:

- Interactivity: JavaScript enables the creation of interactive web pages. You can respond to user actions like clicks, mouse movements, and keyboard input, enhancing user engagement and providing a dynamic user experience.

- Client-Side Scripting: JavaScript is executed on the client's browser, reducing server load and improving website performance. It allows for client-side validation, form handling, and real-time updates without requiring page reloads.

- Cross-Browser Compatibility: JavaScript libraries and frameworks (e.g., jQuery, React, Angular) address browser compatibility issues, ensuring that web applications work consistently across different browsers and platforms.

- Asynchronous Programming: JavaScript supports asynchronous programming through callbacks, Promises, and async/await, making it efficient for handling tasks like fetching data from APIs without blocking the main thread.

- DOM Manipulation: JavaScript can dynamically manipulate the Document Object Model (DOM), allowing you to add, remove, or modify elements and content on a web page. This feature is crucial for building responsive and interactive user interfaces.

- Rich Ecosystem: JavaScript has a vast ecosystem of libraries and frameworks for various purposes, such as front-end development (React, Vue.js), back-end development (Node.js), data visualization (D3.js), and more.

- Server-Side Development: With Node.js, JavaScript can also be used for server-side development, enabling full-stack development using a single programming language.

JavaScript's versatility and widespread adoption make it a fundamental tool in modern web development, allowing developers to create dynamic, responsive, and feature-rich web applications.

## Question 4: Explain the purpose and usage of JavaScript popup boxes. Provide an example of each type of popup box and describe when you might use them in a web application

###### Ans4

JavaScript popup boxes are used to interact with users and provide information or gather input. There are three main types of popup boxes: alert, confirm, and prompt. Let's explore each type and when you might use them in a web application:

Alert Box:

- Purpose: To display a message to the user.
- Usage: You can use alert to provide informational messages or notifications. For example, alerting users about a successful action, reminding them of important information, or displaying error messages.

```javascript
alert("This is an alert message!");
```

Confirm Box:

- Purpose: To confirm an action with the user.
- Usage: confirm is used when you want the user to confirm or cancel an action. It returns true if the user clicks "OK" and false if they click "Cancel." For example, confirming before deleting a record.

```javascript
if (confirm("Do you want to delete this item?")) {
  // Delete the item
} else {
  // Cancel the action
}
```

Prompt Box:

- Purpose: To gather input from the user.
- Usage: prompt allows you to request input from the user. It displays a text input field along with a message. For example, you can use it to collect user names or values for further processing.

```javascript
const userInput = prompt("Please enter your name:");
if (userInput !== null) {
  // Process the user input
}
```

These popup boxes are useful for enhancing the user experience and ensuring that users are aware of critical actions or providing a means for user interaction. However, it's essential to use them judiciously to avoid interrupting the user's flow excessively.

## Question 5: Describe the CSS Box Model and its components. Explain how padding, margin, and border affect the layout of an HTML element. Additionally, provide an example of an advanced CSS technique or property used to create a responsive web design layout

###### Ans5

The CSS Box Model is a fundamental concept in web design that defines how the layout of an HTML element is calculated. It consists of several components: content, padding, border, and margin. Let's describe each component and how they affect the layout of an HTML element:

- Content: The content area is the innermost part of the box and holds the actual content of the element, such as text, images, or other HTML elements. Its size is determined by the element's width and height properties.

- Padding: Padding is the space between the content and the element's border. It can be added using the padding property. Padding provides spacing within the element and affects the element's overall size.

```css
.box {
  padding: 20px; /* Adds 20px of padding on all sides of the content */
}
```

Border: The border surrounds the padding and content area, creating a visible boundary for the element. You can set the border's width, style, and color using the border property.

```css
.box {
  border: 2px solid #333; /* 2px solid border with color #333 */
}
```

Margin: Margin is the space outside the element's border, separating it from other elements. It can be added using the margin property. Margins are used to control the spacing between elements on a web page.

```css
.box {
  margin: 10px; /* Adds 10px of margin around the element */
}
```

These components collectively determine the total space occupied by an HTML element. For example, if you set the width of an element to 200px, and it has 10px of padding, a 2px border, and 20px of margin, the total width of the box would be 232px (200px + 2 _10px + 2_ 2px + 2 \* 20px).

To create responsive web designs, CSS provides advanced techniques and properties, such as media queries and flexbox. Media queries allow you to apply different styles based on the screen size or device, making your website adapt to various devices and screen resolutions. Flexbox is a layout model that simplifies the creation of flexible and responsive layouts, making it easier to align and distribute elements within a container.

Here's an example of using media queries to adjust styles based on screen size:

```css
/* Styles for screens with a width less than 600px */
@media (max-width: 600px) {
  .box {
    width: 100%; /* Make the element occupy the full width */
  }
}
```

In this example, when the screen width is 600px or less, the .box element will take up the full width of its container.

These advanced CSS techniques help you create responsive and adaptable web layouts, ensuring a consistent user experience across different devices and screen sizes.

## Question 6: Explain the concept of Cascading Style Sheets (CSS) and provide at least three CSS properties commonly used in web design. Briefly describe how each property affects the styling of a web page

###### Ans6

Cascading Style Sheets (CSS) is a stylesheet language used in web development to control the presentation and styling of HTML elements on a web page. CSS allows web designers and developers to define how web content should be displayed, including aspects like layout, colors, fonts, spacing, and responsiveness. Here are three commonly used CSS properties in web design and how each property affects the styling of a web page:

color Property:

- Description: The color property is used to define the text color of an element.

Example:

```css
    p {
        color: blue;
    }

    Effect: This sets the text color of all <p> elements to blue. It affects the foreground color of the text content within the element.

font-size Property:

    Description: The font-size property determines the size of the font used for text within an element.
    Example:

    css

    h1 {
        font-size: 24px;
    }

    Effect: This increases the font size of all <h1> headings to 24 pixels, making the text larger and more prominent.

margin Property:

    Description: The margin property defines the space outside the element's border, creating separation between elements.
    Example:

    css

        .container {
            margin: 10px;
        }
```

Effect: Adds a margin of 10 pixels around all elements with the class "container." This provides spacing between adjacent elements.

These CSS properties are just a small sample of the many properties available in CSS. They allow designers and developers to precisely control the appearance and layout of web pages, making it possible to create visually appealing and well-structured websites.

## Question 7: Design & implement all types of popup boxes using JavaScript code for password validation. (CO4)

###### Ans7

To implement JavaScript popup boxes for password validation, you can use the prompt function to collect user input and the alert function to provide feedback. Here's an example of how you can do this:

```javascript
// Function to validate a password
function validatePassword() {
  // Prompt the user for a password
  const userPassword = prompt("Please enter your password:");

  // Check if the password meets the criteria
  if (userPassword === null) {
    alert("Password validation canceled.");
  } else if (userPassword.length < 8) {
    alert("Password must be at least 8 characters long.");
  } else {
    alert("Password is valid!");
  }
}

// Call the validation function when needed, e.g., on a button click
```

In this example:

- We define a function validatePassword that uses the prompt function to collect a password from the user.
- We check the password against criteria, such as minimum length (8 characters in this case).
- Depending on the outcome, we use the alert function to display a message to the user, indicating whether the password is valid or not.

You can trigger this password validation function in response to user actions, such as clicking a button or submitting a form.

## Question 8: Display current Date and Time using JavaScript. (CO4)

###### Ans8

To display the current date and time using JavaScript, you can use the Date object. Here's an example:

```javascript
// Create a new Date object
const currentDate = new Date();

// Get the current date and time components
const date = currentDate.toLocaleDateString(); // Get the date in a readable format
const time = currentDate.toLocaleTimeString(); // Get the time in a readable format

// Display the date and time
console.log("Current Date:", date);
console.log("Current Time:", time);
```

In this example:

- We create a new Date object, which represents the current date and time.
- We use the toLocaleDateString and toLocaleTimeString methods to format the date and time components in a human-readable format.
- Finally, we display the current date and time using console.log, but you can display it in an HTML element or any other desired way.

This JavaScript code will dynamically show the current date and time whenever it is executed.

## Question 9: Difference between `<span>` and`<p>` tag. (CO3)

###### Ans9

The `<span>` and `<p>` tags are both HTML elements, but they serve different purposes and have distinct characteristics:

`<span>` Tag:

- Inline Element: `<span>` is an inline HTML element. It does not create a line break before or after its content.
- No Paragraph Formatting: It does not add any paragraph-level formatting (e.g., margins or line spacing).
- Use for Styling:`<span>` is often used to apply styling, such as CSS styles or inline styles, to a specific portion of text within a block-level element.
- No Default Styling: It does not provide any default styling to its content.
- Examples: Used within text to apply styles or highlight specific words or phrases.

`<p>` Tag:

- Block-Level Element: `<p>` is a block-level HTML element. It creates a line break before and after its content, effectively starting a new paragraph.
- Paragraph Formatting: It adds paragraph-level formatting, including margins and line spacing, to its content.
- Structural Element: `<p>` is used to structure content into paragraphs and is typically used for text that forms complete paragraphs or blocks of content.
- Default Styling: It may have default styling applied by web browsers, such as margin spacing.
- Examples: Used to separate and structure textual content into paragraphs.

In summary, `<span>` is typically used for applying styling or targeting specific parts of text within other elements, while `<p>` is used for structuring content into paragraphs with paragraph-level formatting. The choice between them depends on your specific needs and the structure of your web page.

## Question 10: What makes JavaScript a dynamically typed language? (CO4)

###### Ans10

JavaScript is considered a dynamically typed language, which means that variable types are determined at runtime rather than explicitly declared in the code. Here are some characteristics of JavaScript's dynamic typing:

- Variable Type Inference: In JavaScript, you can create variables without specifying their types. The type of a variable is determined based on the value it holds at runtime.

- Dynamic Type Changes: Variables in JavaScript can change their types during their lifetime. For example, a variable initially holding a number can later hold a string or an object.

- No Type Annotations: JavaScript does not require type annotations or explicit type declarations in variable declarations. You can simply assign values to variables.

- Type Coercion: JavaScript performs type coercion, which means it automatically converts values from one type to another when necessary. For example, concatenating a string and a number will result in a string.

- Flexibility and Expressiveness: Dynamic typing provides flexibility and expressiveness, allowing developers to write code more quickly and adapt to changing requirements.

While dynamic typing offers flexibility, it can also lead to runtime errors if not used carefully. Developers need to be mindful of variable types and handle type-related issues to ensure robust code.

## Question 11: Show how let, var, and const differ from one another. (CO3)

###### Ans11

In JavaScript, let, var, and const are used to declare variables, but they have distinct characteristics and scoping rules:

let:

- Block Scope: Variables declared with let have block scope. They are only accessible within the block (enclosed by curly braces) in which they are declared.
- Reassignment: let variables can be reassigned to new values after declaration.
- Hoisting: Like var, let variables are hoisted to the top of their containing block, but they are not initialized until the declaration is encountered in the code.

var:

- Function Scope: Variables declared with var have function scope, which means they are accessible throughout the function in which they are declared (or globally if declared outside any function).
- Reassignment: var variables can be reassigned to new values after declaration.
- Hoisting: var variables are hoisted to the top of their containing function or global scope and are initialized with undefined by default.

const:

- Block Scope: Variables declared with const have block scope, similar to let.

- Immutable: const variables cannot be reassigned after declaration. However, for objects and arrays declared with const, their properties or elements can still be modified.

Here's a brief example illustrating the differences:

```javascript
function example() {
  if (true) {
    var varVariable = "I'm a var"; // Function-scoped
    let letVariable = "I'm a let"; // Block-scoped
    const constVariable = "I'm a const"; // Block-scoped
  }
  console.log(varVariable); // Accessible
  console.log(letVariable); // ReferenceError: not defined outside the block
  console.log(constVariable); // ReferenceError: not defined outside the block
}

example();
```

In this example:

- varVariable is accessible throughout the function because it's declared with var.
- letVariable and constVariable are block-scoped and not accessible outside the if block.

Use const for variables that should not be reassigned, let for variables that can be reassigned, and be cautious when using var due to its function scope behavior. let and const are typically preferred in modern JavaScript for better scoping and error prevention.

## Question 12: Design a basic navigation bar with HTML and CSS. (CO3)

###### Ans12

To design a basic navigation bar with HTML and CSS, you can use HTML's `<nav>` element for the container and `<ul>` and `<li>` elements for the list of navigation links. Here's a simple example:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS for the navigation bar */
      nav {
        background-color: #333;
        color: #fff;
        padding: 10px;
      }

      ul {
        list-style-type: none;
        padding: 0;
      }

      li {
        display: inline;
        margin-right: 20px;
      }

      a {
        text-decoration: none;
        color: #fff;
      }

      /* Style the navigation links on hover */
      a:hover {
        text-decoration: underline;
      }
    </style>
  </head>
  <body>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </body>
</html>
```

In this example:

- We create a `<nav>` element to contain the navigation bar.
- Inside the `<nav>`, we use an unordered list `<ul>` for the list of navigation links.
- Each navigation link is represented as a list item `<li>`.
- We apply CSS styles to the navigation bar, links, and their hover states.

The background-color, color, and padding properties are used to style the navigation bar. The list-style-type, display, and margin properties are used to format the list items as inline elements.

The text-decoration property is used to remove the underline from the links (text-decoration: none), and color is set to white. We also use the :hover pseudo-class to style the links differently when hovered over, adding an underline to indicate interactivity.

## Question 13: Design a Search bar using CSS and HTML. (CO3)

###### Ans13

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS for the search bar */
      .search-container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 50px;
      }

      .search-input {
        width: 300px;
        padding: 10px;
        border: 2px solid #333;
        border-radius: 5px;
        font-size: 16px;
        outline: none;
      }

      .search-button {
        background-color: #333;
        color: #fff;
        border: none;
        border-radius: 5px;
        padding: 10px 20px;
        margin-left: 10px;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <div class="search-container">
      <input class="search-input" type="text" placeholder="Search..." />
      <button class="search-button">Search</button>
    </div>
  </body>
</html>
```

In this example:

- We create a container `<div>` with the class search-container to hold the search bar elements.

- Inside the container, we have an `<input>` element with the class search-input for the text input.

- We style the input with properties such as width, padding, border, border-radius, font-size, and outline to give it a simple and clean appearance.

- Next, we have a `<button>` element with the class search-button for the search button. We style the button with background color, text color, padding, border-radius, and a cursor style.

This creates a basic search bar with an input field and a search button that can be customized further to fit the design of your web page.

## Question 14: What are the input types for form validation in HTML? Explain with an example how to style the input fields. (CO3)

###### Ans14

HTML provides various input types for form validation. Some common input types include:

- Text Input (type="text"): Allows users to enter text. Example:

```html
<input type="text" name="username" required />
```

Email Input (type="email"): Ensures that the entered text follows an email format. Example:

```html
<input type="email" name="email" required />
```

Password Input (type="password"): Masks the entered text for password fields. Example:

```html
<input type="password" name="password" required />
```

Number Input (type="number"): Allows users to enter numeric values. Example:

```html
<input type="number" name="quantity" min="1" max="100" />
```

Checkbox (type="checkbox"): Represents a binary choice. Example:

```html
<input type="checkbox" name="subscribe" value="yes" /> Subscribe to newsletter
```

Radio (type="radio"): Represents a set of mutually exclusive options. Example:

```html
<input type="radio" name="gender" value="male" /> Male
<input type="radio" name="gender" value="female" /> Female
```

File Input (type="file"): Allows users to upload files. Example:

```html
<input type="file" name="file-upload" />
```

To style input fields, you can use CSS. Here's an example of styling text and email input fields:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS for input fields */
      input[type="text"],
      input[type="email"] {
        width: 100%;
        padding: 10px;
        margin: 5px 0;
        border: 2px solid #333;
        border-radius: 5px;
        font-size: 16px;
        outline: none;
      }

      input[type="text"]:focus,
      input[type="email"]:focus {
        border-color: #007bff; /* Change border color on focus */
      }
    </style>
  </head>
  <body>
    <form>
      <label for="username">Username:</label>
      <input type="text" id="username" name="username" required />

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required />
    </form>
  </body>
</html>
```

In this example, we use CSS to style text and email input fields by specifying their type attributes in the CSS selector. We set properties like width, padding, margin, border, border-radius, font-size, and outline to control the appearance.

Additionally, we change the border color to blue (#007bff) when the input fields are in focus using the :focus pseudo-class, providing visual feedback to users.

## Question 15: How do we create hyperlinks in an HTML page, and what are the ways to style the different states of hyperlinks? (CO3)

###### Ans15

To create hyperlinks in an HTML page, you can use the `<a>` (anchor) element. Hyperlinks are used to navigate to other web pages or resources. Here's how to create a hyperlink:

````html
<a href="https://www.example.com">Visit Example.com</a>``` In this example, the
href attribute specifies the destination URL, and the link text is "Visit
Example.com." You can style different states of hyperlinks using CSS. Common
states include: - Normal State (a): The default appearance of a link. - Hover
State (a:hover): The appearance when the mouse pointer is over the link. -
Visited State (a:visited): The appearance of a link that has been visited by the
user. - Active State (a:active): The appearance when the link is being clicked.
Here's an example of styling different states of hyperlinks: ```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* Normal state */
      a {
        color: #007bff; /* Blue color for links */
        text-decoration: none; /* Remove underlines */
      }

      /* Hover state */
      a:hover {
        text-decoration: underline; /* Add underline on hover */
      }

      /* Visited state */
      a:visited {
        color: #purple; /* Change color for visited links */
      }

      /* Active state */
      a:active {
        color: #ff0000; /* Change color when clicked */
      }
    </style>
  </head>
  <body>
    <p><a href="https://www.example.com">Visit Example.com</a></p>
  </body>
</html>
````

In this example, we use CSS to style links in different states:

- In the normal state (a), links are styled with blue color and no underlines.
- In the hover state (a:hover), links have underlines added when the mouse hovers over them.
- In the visited state (a:visited), links change to a purple color after being visited.
- In the active state (a:active), links turn red when clicked.

These styles enhance the visual feedback and user experience when interacting with hyperlinks on a web page. You can customize the styles to match your website's design.

## Question 16: Design a feedback form using HTML and CSS. (CO3)

###### Ans16

To design a feedback form using HTML and CSS, you can create a simple form with input fields, labels, and a submit button. Here's an example:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS for the feedback form */
      .feedback-form {
        max-width: 400px;
        margin: 0 auto;
        padding: 20px;
        border: 2px solid #007bff; /* Blue border */
        border-radius: 10px;
      }

      .form-group {
        margin-bottom: 15px;
      }

      label {
        display: block;
        font-weight: bold;
      }

      input[type="text"],
      select {
        width: 100%;
        padding: 10px;
        border: 2px solid #007bff;
        border-radius: 5px;
      }

      select {
        height: 35px;
      }

      input[type="submit"] {
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 5px;
        padding: 10px 20px;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <div class="feedback-form">
      <h2>Feedback Form</h2>
      <form>
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" name="name" required />
        </div>

        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" name="email" required />
        </div>

        <div class="form-group">
          <label for="feedback">Feedback:</label>
          <textarea id="feedback" name="feedback" rows="4" required></textarea>
        </div>

        <div class="form-group">
          <input type="submit" value="Submit" />
        </div>
      </form>
    </div>
  </body>
</html>
```

In this example:

- We create a div with the class feedback-form to style the form container.
- Inside the form container, we have a form element with various form elements such as text inputs, a textarea for feedback, and a submit button.
- CSS is used to style the form elements, including setting their widths, padding, borders, and border-radius to create a visually appealing form.
- The form includes labels for each input field to provide context for users.

This example provides a basic structure for a feedback form that you can further customize to meet your specific requirements.

## Question 17: Write complete HTML code that will print an unordered list containing the following elements: Array, Link List, Stack, Queues, Stack, Graphs. (CO3)

###### Ans17

Here's the HTML code that prints an unordered list containing the given elements:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Unordered List Example</title>
  </head>
  <body>
    <ul>
      <li>Array</li>
      <li>Link List</li>
      <li>Stack</li>
      <li>Queues</li>
      <li>Stack</li>
      <!-- Note: "Stack" is repeated in the provided list -->
      <li>Graphs</li>
    </ul>
  </body>
</html>
```

In this HTML code:

- We use the `<ul>` (unordered list) element to create an unordered list.
- Each list item is represented by the `<li>` (list item) element.
- We list the given elements within the `<li>` elements to create the unordered list.

## Question 18: Write code in HTML CSS to design the following form

- Name: Textbox
- Address: Textbox
- Mobile No: Textbox
- Class: Dropdown containing FY, SY, TY, BTECH
- Division: Dropdown containing A, B, C
- Percentage: Textbox
- Above elements should have a border of Blue color with a width of200 pixels. (CO3)

###### Ans18

Here's the HTML and CSS code to design a form with specified elements and styles:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* CSS for the form */
      .custom-form {
        max-width: 400px;
        margin: 0 auto;
        padding: 20px;
        border: 2px solid #007bff; /* Blue border */
        border-radius: 10px;
      }

      .form-group {
        margin-bottom: 15px;
      }

      label {
        display: block;
        font-weight: bold;
      }

      input[type="text"],
      select {
        width: 200px; /* Set width to 200px as specified */
        padding: 10px;
        border: 2px solid #007bff; /* Blue border */
        border-radius: 5px;
      }

      select {
        height: 35px;
      }
    </style>
  </head>
  <body>
    <div class="custom-form">
      <h2>Student Information</h2>
      <form>
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" name="name" required />
        </div>

        <div class="form-group">
          <label for="address">Address:</label>
          <input type="text" id="address" name="address" required />
        </div>

        <div class="form-group">
          <label for="mobile">Mobile No:</label>
          <input type="text" id="mobile" name="mobile" required />
        </div>

        <div class="form-group">
          <label for="class">Class:</label>
          <select id="class" name="class">
            <option value="FY">FY</option>
            <option value="SY">SY</option>
            <option value="TY">TY</option>
            <option value="BTECH">BTECH</option>
          </select>
        </div>

        <div class="form-group">
          <label for="division">Division:</label>
          <select id="division" name="division">
            <option value="A">A</option>
            <option value="B">B</option>
            <option value="C">C</option>
          </select>
        </div>

        <div class="form-group">
          <label for="percentage">Percentage:</label>
          <input type="text" id="percentage" name="percentage" required />
        </div>

        <div class="form-group">
          <input type="submit" value="Submit" />
        </div>
      </form>
    </div>
  </body>
</html>
```

In this code:

- We create a form with various form elements including text inputs, select (dropdown) elements, and a submit button.
- CSS styles are applied to set the width, padding, borders, and border-radius of the form elements, giving them a consistent appearance with blue borders as specified.
- Labels are provided for each input field to provide context for users.

## Question 19: Why is JavaScript a cross-platform language? Explain the advantages of JavaScript. (CO4)

###### Ans19

**JavaScript is considered a cross-platform language due to several key factors:**

- Browser Compatibility: JavaScript is supported by all major web browsers, including Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, and others. This cross-browser compatibility allows JavaScript code to run consistently across different browsers and platforms.

- Platform Independence: JavaScript code is executed by the web browser's JavaScript engine, making it independent of the underlying operating system (OS). This means that JavaScript functions the same way on Windows, macOS, Linux, and other operating systems.

- Client-Side Language: JavaScript primarily runs on the client side, within the user's web browser. As a result, it does not rely on server-specific configurations or dependencies, making it platform-agnostic.

- Web Standards: JavaScript is based on web standards defined by organizations like the World Wide Web Consortium (W3C). These standards ensure that JavaScript code is interoperable across various platforms and adheres to consistent rules.

**Advantages of JavaScript in Web Development:**

- Interactivity: JavaScript enables the creation of dynamic and interactive web applications. It allows developers to respond to user actions, validate form data, and update content without requiring a page reload.

- Client-Side Validation: JavaScript can perform client-side form validation, reducing the need for server-side validation and improving user experience.

- Cross-Browser Compatibility: JavaScript libraries and frameworks, such as jQuery and React, help streamline development and ensure compatibility with different browsers.

- Rich Web Applications: JavaScript is essential for building modern web applications, including single-page applications (SPAs) that offer a responsive and seamless user experience.

- Asynchronous Operations: JavaScript supports asynchronous programming, allowing developers to fetch data from servers, perform background tasks, and update the user interface without blocking the main thread.

- Community and Ecosystem: JavaScript has a vast and active developer community, with numerous libraries, frameworks, and tools available. This ecosystem contributes to its versatility and cross-platform capabilities.

## Question 20:Explain the following terms with suitable examples: Hyperlink, Types of Lists, Table Tags

###### Ans20

### Hyperlink

A hyperlink, commonly referred to as a link, is a clickable element on a web page that allows users to navigate to another web page, document, or resource. Hyperlinks are an essential part of web content and are used to connect web pages, provide references, and enable navigation within websites. They are typically created using the `<a>` (anchor) element in HTML.

Example of a Hyperlink:

```html
<a href="https://www.example.com">Visit Example.com</a>
```

In this example, the `<a>` element creates a hyperlink that, when clicked, takes the user to the "<https://www.example.com>" website.
Types of Lists:

HTML provides various types of lists to organize and structure content. Three common types of lists are:

- Ordered List (`<ol>`): An ordered list is used to represent a list of items in a specific order, typically with sequential numbers or letters (e.g., 1., 2., 3.).

Example:

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```

Unordered List (`<ul>`): An unordered list is used to represent a list of items without a specific order. Bullets or other symbols are commonly used to mark list items.

Example:

```html
<ul>
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
</ul>
```

Definition List (`<dl`>): A definition list is used to display a list of terms (dt) and their corresponding definitions (dd).

Example:

```html
<dl>
  <dt>Term 1</dt>
  <dd>Definition 1</dd>
  <dt>Term 2</dt>
  <dd>Definition 2</dd>
</dl>
```
