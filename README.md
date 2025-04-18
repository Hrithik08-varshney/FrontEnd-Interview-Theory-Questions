# FrontEnd-Interview-Theory-Questions

1. **Difference between HTML and HTML5?**
<details>
  <summary>Answer</summary>
  <table border="1" cellspacing="0" cellpadding="10">
  <thead>
    <tr>
      <th>Feature</th>
      <th>HTML</th>
      <th>HTML5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Version</strong></td>
      <td>Earlier versions (e.g., HTML 4.01, XHTML)</td>
      <td>Latest standard of HTML</td>
    </tr>
    <tr>
      <td><strong>Multimedia Support</strong></td>
      <td>Limited; relies on plugins like Flash</td>
      <td>Built-in <code>&lt;audio&gt;</code> and <code>&lt;video&gt;</code> tags</td>
    </tr>
    <tr>
      <td><strong>Semantics</strong></td>
      <td>Lacks semantic tags (e.g., uses <code>&lt;div&gt;</code>)</td>
      <td>Semantic tags like <code>&lt;article&gt;</code>, <code>&lt;section&gt;</code>, <code>&lt;nav&gt;</code></td>
    </tr>
    <tr>
      <td><strong>Forms</strong></td>
      <td>Basic input types</td>
      <td>Advanced input types (<code>date</code>, <code>email</code>, etc.) and attributes (<code>required</code>, <code>placeholder</code>)</td>
    </tr>
    <tr>
      <td><strong>Graphics</strong></td>
      <td>No native support for canvas or SVG</td>
      <td>Native support for <code>&lt;canvas&gt;</code> and SVG</td>
    </tr>
    <tr>
      <td><strong>Storage</strong></td>
      <td>Relies on cookies</td>
      <td>Supports <code>localStorage</code> and <code>sessionStorage</code></td>
    </tr>
  </tbody>
</table>

</details>

---

2. **What is Box Model?**
<details>
  <summary>Answer</summary>
<p>The <strong>box model</strong> is a fundamental concept in web development used to describe the structure of elements in CSS. It defines how the size of an element is calculated and how its spacing works.</p>
    <h2>Components of the Box Model</h2>
    <ol>
        <li>
            <strong>Content</strong>: 
            <p>The actual content inside the element, such as text, images, or other elements. Its size is controlled by <code>width</code> and <code>height</code>.</p>
        </li>
        <li>
            <strong>Padding</strong>: 
            <p>The space between the content and the border. Padding is transparent and can be controlled using <code>padding</code> properties (e.g., <code>padding-top</code>, <code>padding-right</code>).</p>
        </li>
        <li>
            <strong>Border</strong>: 
            <p>The edge surrounding the padding. The size and style of the border are controlled using properties like <code>border-width</code>, <code>border-style</code>, and <code>border-color</code>.</p>
        </li>
        <li>
            <strong>Margin</strong>: 
            <p>The space outside the border, creating distance between the element and other elements. It is controlled using <code>margin</code> properties (e.g., <code>margin-top</code>, <code>margin-bottom</code>).</p>
        </li>
    </ol>
    <h2>Box Model Formula</h2>
    <p>By default (<code>box-sizing: content-box</code>):</p>
    <pre>
Total Width = Content Width + Padding (left + right) + Border (left + right) + Margin (left + right)
Total Height = Content Height + Padding (top + bottom) + Border (top + bottom) + Margin (top + bottom)
    </pre>
    <p>Alternatively, with <code>box-sizing: border-box</code>, padding and border are included in the specified width and height, simplifying size calculations.</p>
    <p>Understanding the box model is crucial for designing layouts and managing spacing effectively in web design.</p>

</details>

---

3. **Difference between id and class? Which have high priority?**
<details>
  <summary>Answer</summary>
    <h1>Difference Between <code>id</code> and <code>class</code></h1>
    <table border="1" cellspacing="0" cellpadding="5">
        <thead>
            <tr>
                <th>Aspect</th>
                <th><code>id</code></th>
                <th><code>class</code></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Uniqueness</td>
                <td>Must be unique within a document.</td>
                <td>Can be shared by multiple elements.</td>
            </tr>
            <tr>
                <td>Selector</td>
                <td>Represented as <code>#id</code>.</td>
                <td>Represented as <code>.class</code>.</td>
            </tr>
            <tr>
                <td>Purpose</td>
                <td>Used for uniquely identifying an element.</td>
                <td>Used for grouping multiple elements.</td>
            </tr>
            <tr>
                <td>Reusability</td>
                <td>Not reusable within the same document.</td>
                <td>Reusable for multiple elements.</td>
            </tr>
            <tr>
                <td>Specificity</td>
                <td>Higher specificity in CSS.</td>
                <td>Lower specificity compared to <code>id</code>.</td>
            </tr>
        </tbody>
    </table>
 <h1>CSS Priority Specificity</h1>
    <ol>
        <li><strong>Inline Styles:</strong> Highest priority (e.g., <code>style="color: orange;"</code>)</li>
        <li><strong>ID Selector:</strong> Higher specificity than class or element selectors (e.g., <code>#example-id</code>)</li>
        <li><strong>Class Selector:</strong> Lower specificity than ID but higher than element selectors (e.g., <code>.example-class</code>)</li>
        <li><strong>Element Selector:</strong> Lowest specificity (e.g., <code>p</code>)</li>
    </ol>

    <h2>Example</h2>
    <p id="example-id" class="example-class" style="color: orange;">
        This text demonstrates specificity in CSS. The color is set to orange because inline styles have the highest priority.
    </p>

</details>

---

4. **Difference between let, var and const ?**
<details>
  <summary>Answer</summary>
    <table border="1" cellpadding="10">
  <thead>
    <tr>
      <th>Feature</th>
      <th>var</th>
      <th>let</th>
      <th>const</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Scope</td>
      <td>Function-scoped</td>
      <td>Block-scoped</td>
      <td>Block-scoped</td>
    </tr>
    <tr>
      <td>Hoisting</td>
      <td>Hoisted, initialized to <code>undefined</code></td>
      <td>Hoisted, not initialized (throws error if accessed before declaration)</td>
      <td>Hoisted, not initialized (throws error if accessed before declaration)</td>
    </tr>
    <tr>
      <td>Re-declaration</td>
      <td>Allowed in the same scope</td>
      <td>Not allowed in the same scope</td>
      <td>Not allowed in the same scope</td>
    </tr>
    <tr>
      <td>Reassignment</td>
      <td>Allowed</td>
      <td>Allowed</td>
      <td>Not allowed</td>
    </tr>
    <tr>
      <td>Use Case</td>
      <td>Avoid in modern JavaScript</td>
      <td>Use for variables that may change</td>
      <td>Use for constants that should not change</td>
    </tr>
  </tbody>
</table>
</details>

---

5. **What is media query in CSS ?**
<details>
  <summary>Answer</summary>
<p>
    A <strong>media query</strong> in CSS is a technique used to apply styles conditionally based on specific device 
    characteristics, such as screen size, resolution, orientation, or aspect ratio. Media queries allow websites to 
    be responsive, adapting their layout and design to different devices.
  </p>
  <h2>Syntax</h2>
  <pre>
    <code>
@media (condition) {
  /* CSS rules */
}
    </code>
  </pre>
  <h2>Example</h2>
  <pre>
    <code>
/* Styles for screens smaller than 768px */
@media (max-width: 768px) {
  body {
    background-color: lightblue;
  }
}

/* Styles for screens larger than 768px */
@media (min-width: 769px) {
  body {
    background-color: lightgreen;
  }
}
    </code>
  </pre>
  <h2>Common Use Cases</h2>
  <ul>
    <li>Making layouts responsive across different screen sizes.</li>
    <li>Changing font sizes, margins, or padding based on screen width.</li>
    <li>Adjusting images or navigation bars for mobile, tablet, or desktop views.</li>
  </ul>
  <p>Resize your browser window to see the background color change based on the screen size.</p>
</details>

---

6. **Difference between margin and padding?**
<details>
  <summary>Answer</summary>
 <table>
    <thead>
      <tr>
        <th>Aspect</th>
        <th>Margin</th>
        <th>Padding</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Definition</td>
        <td>Space outside the element, separating it from other elements.</td>
        <td>Space inside the element, between its content and border.</td>
      </tr>
      <tr>
        <td>Purpose</td>
        <td>Creates external spacing between elements.</td>
        <td>Creates internal spacing around the content.</td>
      </tr>
      <tr>
        <td>Placement</td>
        <td>Outside the border of the element.</td>
        <td>Inside the border of the element.</td>
      </tr>
      <tr>
        <td>Effect on Element Size</td>
        <td>Does not increase the element's size.</td>
        <td>Increases the element's size.</td>
      </tr>
    </tbody>
  </table>
</details>

---

7. **What is callback function ? What is use of it?**
<details>
  <summary>Answer</summary>
 <p>
    A <strong>callback function</strong> in JavaScript is a function that is passed as an argument to another function 
    and is executed after some operation is completed. It allows you to execute code asynchronously or in response 
    to certain events.
  </p>

  <h2>Example:</h2>
  <pre>
<code>
function greet(name, callback) {
    console.log(`Hello, ${name}`);
    callback();
}

function sayGoodbye() {
    console.log('Goodbye!');
}

greet('Alice', sayGoodbye);
</code>
  </pre>
  <p><strong>Output:</strong></p>
  <pre>
Hello, Alice
Goodbye!
  </pre>

  <h2>Use of Callback Functions:</h2>
  <ul>
    <li>
      <strong>Asynchronous Operations:</strong>
      <p>Used in handling tasks like API calls, file reading, or timers without blocking code execution.</p>
      <pre>
<code>
setTimeout(() => {
    console.log('This runs after 2 seconds');
}, 2000);
</code>
      </pre>
    </li>
    <li>
      <strong>Event Handling:</strong>
      <p>Used in DOM event listeners.</p>
      <pre>
<code>
document.getElementById('btn').addEventListener('click', () => {
    console.log('Button clicked!');
});
</code>
      </pre>
    </li>
    <li>
      <strong>Control Flow:</strong>
      <p>To maintain a sequence of operations where one function depends on another's result.</p>
    </li>
    <li>
      <strong>Reusability:</strong>
      <p>
        You can pass different callback functions for different behaviors without modifying the core function.
      </p>
    </li>
  </ul>

  <h2>Modern Alternatives:</h2>
  <p>
    In modern JavaScript, <strong>Promises</strong> and <strong>async/await</strong> are often preferred for better 
    readability and handling asynchronous code, but callbacks remain fundamental.
  </p>
</details>

---

8. **What is Promises ?**
<details>
  <summary>Answer</summary>
  <p>
    In JavaScript, <strong>promises</strong> are objects that represent the eventual completion (or failure) 
    of an asynchronous operation and its resulting value. They help manage asynchronous tasks effectively, 
    avoiding the "callback hell."
  </p>

  <h2>Promise States</h2>
  <ul>
    <li><strong>Pending:</strong> The initial state, neither fulfilled nor rejected.</li>
    <li><strong>Fulfilled:</strong> The operation completed successfully, and a result is available.</li>
    <li><strong>Rejected:</strong> The operation failed, and a reason (error) is available.</li>
  </ul>

  <h2>Syntax</h2>
  <pre>
<code>
const promise = new Promise((resolve, reject) => {
  // Perform an asynchronous operation
  if (/* success condition */) {
    resolve('Success!'); // Fulfill the promise
  } else {
    reject('Error!'); // Reject the promise
  }
});
</code>
  </pre>

  <h2>Using Promises</h2>
  <p>You can handle a promise's result using <code>.then()</code>, <code>.catch()</code>, and <code>.finally()</code>:</p>
  <pre>
<code>
promise
  .then((result) => {
    console.log('Fulfilled:', result); // Handle success
  })
  .catch((error) => {
    console.log('Rejected:', error); // Handle error
  })
  .finally(() => {
    console.log('Done'); // Executes regardless of success or failure
  });
</code>
  </pre>

  <h2>Example</h2>
  <p>Fetching data with a promise:</p>
  <pre>
<code>
fetch('https://api.example.com/data')
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error('Error:', error));
</code>
  </pre>

  <h2>Key Advantage</h2>
  <p>Promises make asynchronous code easier to read and manage, especially when combined with <code>async/await</code>.</p>
</details>

---

9. **What is Event Loop ?**
<details>
  <summary>Answer</summary>
<p>The <strong>Event Loop</strong> is a mechanism in JavaScript that handles asynchronous operations and ensures non-blocking execution. It continuously checks the <strong>Call Stack</strong> and the <strong>Callback Queue</strong>, executing tasks accordingly.</p>
    <h2>How It Works:</h2>
    <ul>
        <li><strong>Call Stack:</strong> Executes synchronous code line by line.</li>
        <li><strong>Web APIs:</strong> Handles asynchronous operations (e.g., setTimeout, fetch, event listeners).</li>
        <li><strong>Callback Queue:</strong> Stores callbacks of completed async tasks.</li>
        <li><strong>Microtask Queue:</strong> Stores promises and <code>queueMicrotask()</code> callbacks (executed before the callback queue).</li>
        <li><strong>Event Loop:</strong> Moves tasks from the Microtask/Callback Queue to the Call Stack when it's empty.</li>
    </ul>
    <h2>Example:</h2>
    <pre><code>console.log("Start");
setTimeout(() => {
    console.log("Timeout");
}, 0);
Promise.resolve().then(() => {
    console.log("Promise");
});
console.log("End");</code></pre>
    <h2>Expected Output:</h2>
    <pre><code>Start
End
Promise
Timeout</code></pre>
    <p>The <strong>Promise</strong> executes before <strong>setTimeout</strong> due to the Microtask Queue priority.</p>
</details>

---

10. **What is CSS Preprocessor ?**
<details>
  <summary>Answer</summary>
<p>A <strong>CSS Preprocessor</strong> is a scripting language that extends CSS by adding features like variables, nested rules, mixins, functions, and more. It compiles into standard CSS that browsers can understand.</p>

<h2>Popular CSS Preprocessors:</h2>
<ul>
    <li><strong>SASS (SCSS):</strong> Most widely used, supports variables, nesting, mixins, and functions.</li>
    <li><strong>LESS:</strong> Similar to SASS but uses JavaScript-like syntax.</li>
    <li><strong>Stylus:</strong> More flexible syntax with optional semicolons and brackets.</li>
</ul>

<h2>Benefits:</h2>
<ul>
    <li><strong>Code Reusability:</strong> Variables, mixins.</li>
    <li><strong>Better Maintainability:</strong> Structured nesting.</li>
    <li><strong>Improved Readability:</strong> Modular approach.</li>
    <li><strong>Enhanced Functionality:</strong> Math operations, functions.</li>
</ul>

<h2>Example (SASS):</h2>
<pre><code>
// SCSS Syntax
$primary-color: blue;

button {
  background: $primary-color;
  color: white;
}
</code></pre>
</details>

---

10. **Can our browser directly understand SASS code ?**
<details>
  <summary>Answer</summary>
<p>No, browsers cannot directly understand SASS code. SASS (Syntactically Awesome Stylesheets) is a preprocessor that needs to be compiled into standard CSS before a browser can render it.</p>
    <p>You must use a SASS compiler (like Dart Sass, node-sass, or a build tool like Webpack) to convert <code>.scss</code> or <code>.sass</code> files into <code>.css</code>.</p>
</details>

---

11. **What is AJAX ?**
<details>
  <summary>Answer</summary>
<p><strong>AJAX (Asynchronous JavaScript and XML)</strong> is a technique used in web development to send and receive data from a server asynchronously without reloading the page. It allows dynamic updates of web content without refreshing the entire page.</p>

    <h2>Key Aspects of AJAX:</h2>
    <ul>
        <li>Uses <code>XMLHttpRequest</code> or <code>fetch API</code> to communicate with the server.</li>
        <li>Can send and receive data in formats like JSON, XML, or plain text.</li>
        <li>Improves user experience by making web applications faster and more responsive.</li>
    </ul>

    <h2>Example (Using Fetch API in JavaScript):</h2>
    <pre>
        <code>
        fetch('https://api.example.com/data')
          .then(response => response.json())
          .then(data => console.log(data))
          .catch(error => console.error('Error:', error));
        </code>
    </pre>

    <h2>Live Example:</h2>
    <button onclick="fetchData()">Fetch Data</button>
    <pre id="output"></pre>

    <script>
        function fetchData() {
            fetch('https://jsonplaceholder.typicode.com/todos/1')
                .then(response => response.json())
                .then(data => {
                    document.getElementById('output').textContent = JSON.stringify(data, null, 2);
                })
                .catch(error => console.error('Error:', error));
        }
    </script>
</details>

---

12. **Some git commands you used in your project?**
<details>
  <summary>Answer</summary>
 <ul>
   <li><b>git checkout -b branchname</b></li>
   <li><b>git push</b></li>
   <li><b>git rebase --continue</b></li>
   <li><b>git pull origin branchname</b></li>
   <li><b>git rebase --abort</b></li>
   <li><b>git add .</b></li>
   <li><b>git commit -m "commit message"</b></li>
   <li><b>git stash</b></li>
 </ul>
</details>

---

13. **Difference between null and undefined?**
<details>
  <summary>Answer</summary>
<table>
        <tr>
            <th>Feature</th>
            <th><code>null</code></th>
            <th><code>undefined</code></th>
        </tr>
        <tr>
            <td><strong>Type</strong></td>
            <td>Object</td>
            <td>Undefined</td>
        </tr>
        <tr>
            <td><strong>Meaning</strong></td>
            <td>Intentional absence of a value</td>
            <td>Variable declared but not assigned a value</td>
        </tr>
        <tr>
            <td><strong>Usage</strong></td>
            <td>Explicitly assigned to indicate "no value"</td>
            <td>Default value for uninitialized variables</td>
        </tr>
        <tr>
            <td><strong>Comparison</strong></td>
            <td><code>null == undefined</code> → <code>true</code> (loose equality)</td>
            <td><code>null === undefined</code> → <code>false</code> (strict equality)</td>
        </tr>
        <tr>
            <td><strong>Typeof</strong></td>
            <td><code>typeof null</code> → <code>"object"</code> (JS bug)</td>
            <td><code>typeof undefined</code> → <code>"undefined"</code></td>
        </tr>
    </table>
<h3>Example:</h3>
    <pre>
<code>
let a = null;
console.log(a); // null
let b;
console.log(b); // undefined
</code>
    </pre>
</details>

---

13. **New Features in ES6?**
<details>
  <summary>Answer</summary>
<ul>
        <li><strong>let & const</strong> – Block-scoped variable declarations.</li>
        <li><strong>Arrow Functions</strong> – Shorter syntax for functions (<code>const add = (a, b) => a + b</code>).</li>
        <li><strong>Template Literals</strong> – String interpolation using backticks (<code>`Hello, ${name}`</code>).</li>
        <li><strong>Default Parameters</strong> – Function parameters with default values (<code>function greet(name = "User") {}</code>).</li>
        <li><strong>Destructuring Assignment</strong> – Extract values from arrays/objects (<code>const { name, age } = user</code>).</li>
        <li><strong>Spread & Rest Operators</strong> – (<code>...</code> for array spreading and function arguments).</li>
        <li><strong>Modules (import/export)</strong> – Native ES6 module support.</li>
        <li><strong>Promises</strong> – Built-in promise handling for async operations.</li>
        <li><strong>Classes</strong> – Syntactic sugar for prototype-based inheritance (<code>class Person {}</code>).</li>
        <li><strong>Enhanced Object Literals</strong> – Shorter syntax for defining methods/properties.</li>
        <li><strong>for...of Loop</strong> – Iterates over iterable objects (<code>for (const item of array) {}</code>).</li>
        <li><strong>Map & Set</strong> – New data structures for key-value pairs and unique values.</li>
        <li><strong>Symbols</strong> – Unique and immutable primitive data type.</li>
        <li><strong>Generators</strong> – Functions that can pause and resume execution (<code>function* generator() {}</code>).</li>
        <li><strong>WeakMap & WeakSet</strong> – Collection types that do not prevent garbage collection.</li>
    </ul>
</details>

---

14. **Difference between Arrow Function and Normal Function?**
<details>
  <summary>Answer</summary>
<table>
        <tr>
            <th>Feature</th>
            <th>Arrow Function (<code>=&gt;</code>)</th>
            <th>Normal Function (<code>function</code>)</th>
        </tr>
        <tr>
            <td><strong><code>this</code> Binding</strong></td>
            <td>Lexically binds <code>this</code> (inherits from surrounding scope).</td>
            <td>Dynamically binds <code>this</code> (depends on how function is called).</td>
        </tr>
        <tr>
            <td><strong>Usage as Constructor</strong></td>
            <td>❌ Cannot be used as a constructor (<code>new</code> keyword will throw an error).</td>
            <td>✅ Can be used as a constructor (<code>new</code> keyword works).</td>
        </tr>
        <tr>
            <td><strong>Arguments Object</strong></td>
            <td>❌ Does not have its own <code>arguments</code> object.</td>
            <td>✅ Has its own <code>arguments</code> object.</td>
        </tr>
        <tr>
            <td><strong>Implicit Return</strong></td>
            <td>✅ Can return a value implicitly (if single expression, no <code>{}</code> needed).</td>
            <td>❌ Requires explicit <code>return</code> statement.</td>
        </tr>
        <tr>
            <td><strong>Hoisting</strong></td>
            <td>❌ Not hoisted like function declarations. Must be defined before use.</td>
            <td>✅ Function declarations are hoisted.</td>
        </tr>
        <tr>
            <td><strong>Methods in Objects</strong></td>
            <td>❌ Not suitable as object methods (due to <code>this</code> binding issue).</td>
            <td>✅ Works correctly as object methods.</td>
        </tr>
    </table>
<h3>Example:</h3>
    <h4>Arrow Function:</h4>
    <pre>
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
    </pre>
    
    <h4>Normal Function:</h4>
    <pre>
function add(a, b) {
  return a + b;
}
console.log(add(2, 3)); // 5
    </pre>
</details>

---

13. **New Features in ES6?**
<details>
  <summary>Answer</summary>
<ul>
        <li><strong>let & const</strong> – Block-scoped variable declarations.</li>
        <li><strong>Arrow Functions</strong> – Shorter syntax for functions (<code>const add = (a, b) => a + b</code>).</li>
        <li><strong>Template Literals</strong> – String interpolation using backticks (<code>`Hello, ${name}`</code>).</li>
        <li><strong>Default Parameters</strong> – Function parameters with default values (<code>function greet(name = "User") {}</code>).</li>
        <li><strong>Destructuring Assignment</strong> – Extract values from arrays/objects (<code>const { name, age } = user</code>).</li>
        <li><strong>Spread & Rest Operators</strong> – (<code>...</code> for array spreading and function arguments).</li>
        <li><strong>Modules (import/export)</strong> – Native ES6 module support.</li>
        <li><strong>Promises</strong> – Built-in promise handling for async operations.</li>
        <li><strong>Classes</strong> – Syntactic sugar for prototype-based inheritance (<code>class Person {}</code>).</li>
        <li><strong>Enhanced Object Literals</strong> – Shorter syntax for defining methods/properties.</li>
        <li><strong>for...of Loop</strong> – Iterates over iterable objects (<code>for (const item of array) {}</code>).</li>
        <li><strong>Map & Set</strong> – New data structures for key-value pairs and unique values.</li>
        <li><strong>Symbols</strong> – Unique and immutable primitive data type.</li>
        <li><strong>Generators</strong> – Functions that can pause and resume execution (<code>function* generator() {}</code>).</li>
        <li><strong>WeakMap & WeakSet</strong> – Collection types that do not prevent garbage collection.</li>
    </ul>
</details>

---

14. **Arrow function will be hoisted or not?**
<details>
  <summary>Answer</summary>
<p>No, arrow functions are <strong>not hoisted</strong>. Only the variable declaration is hoisted, not the function definition.</p>
    <h3>Example:</h3>
    <p>The following code will throw an error:</p>
    <code>
console.log(sum(2, 3)); // ❌ ReferenceError: Cannot access 'sum' before initialization
const sum = (a, b) => a + b;
    </code>
    <p>To ensure hoisting, use a function declaration instead:</p>
    <code>
console.log(sum(2, 3)); // ✅ Works fine
function sum(a, b) {
  return a + b;
}
    </code>
</details>

---

15. **What is Closure?**
<details>
  <summary>Answer</summary>
 <p>A <strong>closure</strong> in JavaScript is a function that <em>remembers</em> the variables from its <em>outer scope</em> even after the outer function has finished executing.</p>
    <h3>Example:</h3>
    <pre>
        <code>
function outerFunction(outerVariable) {
    return function innerFunction(innerVariable) {
        console.log(`Outer: ${outerVariable}, Inner: ${innerVariable}`);
    };
}
const newFunction = outerFunction("Hello");
newFunction("World"); // Output: Outer: Hello, Inner: World
        </code>
    </pre>
    <h3>Use Cases:</h3>
    <ul>
        <li>Data encapsulation (private variables)</li>
        <li>Function factories</li>
        <li>Event handlers and callbacks</li>
    </ul>
</details>

---

16. **What is 'this' keyword?**
<details>
  <summary>Answer</summary>
<h3>1. Global Context</h3>
    <p>In browsers, <code>this</code> refers to the <code>window</code> object. In strict mode, it is <code>undefined</code>.</p>
    <pre><code>console.log(this); // window (in browsers)</code></pre>
    <h3>2. Object Method Context</h3>
    <p><code>this</code> refers to the object that owns the method.</p>
    <pre><code>const obj = {
  name: "Task",
  show() {
    console.log(this.name);
  }
};
obj.show(); // "Task"</code></pre>
    <h3>3. Constructor Function Context</h3>
    <p><code>this</code> refers to the newly created object.</p>
    <pre><code>function Person(name) {
  this.name = name;
}
const p = new Person("John");
console.log(p.name); // "John"</code></pre> 
    <h3>4. Arrow Function Context</h3>
    <p>Arrow functions inherit <code>this</code> from their surrounding scope.</p>
    <pre><code>const obj2 = {
  name: "React",
  show: () => {
    console.log(this.name);
  }
};
obj2.show(); // undefined</code></pre>
    <h3>5. Explicit Binding (call, apply, bind)</h3>
    <p>You can manually set <code>this</code> using <code>call</code>, <code>apply</code>, or <code>bind</code>.</p>
    <pre><code>function greet() {
  console.log(this.name);
}
const user = { name: "Dev" };
greet.call(user); // "Dev"</code></pre>
    <h3>6. Event Listener Context</h3>
    <p>In event handlers, <code>this</code> refers to the element that triggered the event.</p>
    <button id="btn">Click Me</button>
    <pre><code>document.getElementById("btn").addEventListener("click", function () {
  console.log(this); // refers to the clicked button
});</code></pre>
    <script>
        document.getElementById("btn").addEventListener("click", function () {
            console.log(this); // refers to button
        });
    </script>
</details>

---

17. **What is React JS ?**
<details>
  <summary>Answer</summary>
 <p><strong>ReactJS</strong> is a <strong>JavaScript library</strong> used for building <strong>user interfaces</strong>, mainly for <strong>single-page applications (SPAs)</strong>.</p>
<h2>Key Features:</h2>
    <ul>
        <li><strong>Component-Based</strong>: UI is divided into reusable components.</li>
        <li><strong>Virtual DOM</strong>: Efficient updates for better performance.</li>
        <li><strong>Declarative</strong>: Simplifies UI updates by describing the desired state.</li>
        <li><strong>JSX</strong>: Combines JavaScript and HTML-like syntax for easier development.</li>
        <li><strong>State Management</strong>: Handles dynamic data changes efficiently.</li>
    </ul>
<h2>Example:</h2>
    <pre>
        <code>
import React from "react";
function App() {
  return &lt;h1&gt;Hello, React!&lt;/h1&gt;;
}
export default App;
        </code>
    </pre>
</details>

---

18. **What is JSX ?**
<details>
  <summary>Answer</summary>
<p><strong>JSX (JavaScript XML)</strong> is a syntax extension for JavaScript used in React. It allows you to write HTML-like code within JavaScript, making it easier to define UI components. JSX is transpiled by Babel into standard JavaScript (e.g., <code>React.createElement</code> calls).</p> 
    <h3>Example:</h3>
    <pre><code>const element = &lt;h1&gt;Hello, World!&lt;/h1&gt;;</code></pre> 
    <p>JSX improves readability and maintainability but requires a build step to convert it into JavaScript.</p>
</details>

---

19. **Can our browser directly understand JSX ?**
<details>
  <summary>Answer</summary>
<p><strong>No</strong>, browsers cannot directly understand JSX because it is not valid JavaScript.</p>
    <p>JSX is a syntax extension for JavaScript used in React to write UI components in a more declarative way.</p>
    <p>Before it can run in the browser, JSX needs to be <strong>transpiled</strong> into standard JavaScript using tools like <strong>Babel</strong> or <strong>TypeScript</strong>.</p>
    <p>This process converts JSX into <code>React.createElement()</code> calls or modern React's <strong>JSX runtime</strong> functions.</p>
</details>

---

20. **What is Webpacks?**
<details>
  <summary>Answer</summary>
<p>Webpack is a <strong>module bundler</strong> for JavaScript applications. It takes modules with dependencies (JS, CSS, images, etc.) and bundles them into static assets for efficient loading.</p>
    <h3>Key Features:</h3>
    <ul>
        <li><strong>Code Splitting:</strong> Loads only necessary code, improving performance.</li>
        <li><strong>Loaders:</strong> Transforms files (e.g., Babel for JS, SCSS to CSS).</li>
        <li><strong>Plugins:</strong> Enhances functionality (e.g., minification, environment variables).</li>
        <li><strong>Tree Shaking:</strong> Removes unused code to reduce bundle size.</li>
    </ul>
    <p>It's commonly used in React, Vue, and other modern JS frameworks. 🚀</p>
</details>

---

21. **Life cycle methods in React JS?**
<details>
  <summary>Answer</summary>
<h2>1. Mounting (Component Creation)</h2>
    <p>Methods invoked when the component is first created:</p>
    <ul>
        <li><strong>constructor(props)</strong>: Initializes state and binds methods.</li>
        <li><strong>static getDerivedStateFromProps(props, state)</strong>: Updates state based on props before rendering.</li>
        <li><strong>render()</strong>: Returns JSX to render the UI.</li>
        <li><strong>componentDidMount()</strong>: Runs after the component is mounted (useful for API calls).</li>
    </ul>
<h2>2. Updating (Component Re-rendering)</h2>
    <p>Triggered when props or state change:</p>
    <ul>
        <li><strong>static getDerivedStateFromProps(props, state)</strong>: Updates state before re-render.</li>
        <li><strong>shouldComponentUpdate(nextProps, nextState)</strong>: Controls whether to re-render.</li>
        <li><strong>render()</strong>: Re-renders the UI.</li>
        <li><strong>getSnapshotBeforeUpdate(prevProps, prevState)</strong>: Captures state before the update.</li>
        <li><strong>componentDidUpdate(prevProps, prevState)</strong>: Runs after re-render (useful for DOM updates or API calls).</li>
    </ul>
<h2>3. Unmounting (Component Removal)</h2>
    <p>Method called before removing the component:</p>
    <ul>
        <li><strong>componentWillUnmount()</strong>: Cleanup (e.g., remove event listeners, cancel API calls).</li>
    </ul>
<h2>React Hooks Alternative (For Functional Components)</h2>
    <ul>
        <li><strong>useEffect(() => { ... }, [])</strong> → Equivalent to <code>componentDidMount</code>.</li>
        <li><strong>useEffect(() => { ... }, [dependencies])</strong> → Runs on state/props updates (<code>componentDidUpdate</code>).</li>
        <li><strong>useEffect(() => { return () => { ... } }, [])</strong> → Equivalent to <code>componentWillUnmount</code>.</li>
    </ul>
<p>In modern React, functional components with hooks (<code>useState</code>, <code>useEffect</code>) are preferred over class components.</p>
</body>
</details>

---

22. **What is useRef?**
<details>
  <summary>Answer</summary>
<p><code>useRef</code> is a React hook that creates a mutable object (<code>ref</code>) that persists across renders without causing re-renders when updated. It is commonly used for:</p>
    <h2>1. Accessing DOM Elements</h2>
    <pre><code>
    function FocusInput() {
      const inputRef = useRef(null);
      return (
        &lt;div&gt;
          &lt;input ref={inputRef} /&gt;
          &lt;button onClick={() => inputRef.current.focus()}&gt;Focus Input&lt;/button&gt;
        &lt;/div&gt;
      );
    }
    </code></pre>
    <h2>2. Storing Mutable Values Without Re-renders</h2>
    <pre><code>
    function Timer() {
      const count = useRef(0);
      useEffect(() => {
        setInterval(() => {
          count.current += 1;
          console.log(count.current); // Updates but doesn't re-render
        }, 1000);
      }, []);
      return &lt;p&gt;Check console&lt;/p&gt;;
    }
    </code></pre>
    <h2>3. Keeping References Between Renders</h2>
    <pre><code>
    function Counter() {
      const renderCount = useRef(0);
      useEffect(() => {
        renderCount.current += 1;
      });
      return &lt;p&gt;Renders: {renderCount.current}&lt;/p&gt;;
    }
    </code></pre>
    <p>It does <strong>not</strong> trigger re-renders when its value changes, unlike <code>useState</code>.</p>
</details>

---

23. **What is Controlled and Uncontrolled Components?**
<details>
  <summary>Answer</summary>
<h2>Controlled Component</h2>
    <p>A component where React <strong>controls the form elements</strong> via state. The component’s state dictates the input value.</p>
    <h3>Example:</h3>
    <code>
function ControlledInput() {<br>
&nbsp;&nbsp;const [text, setText] = useState("");<br><br>
&nbsp;&nbsp;return &lt;input value={text} onChange={(e) => setText(e.target.value)} /&gt;;<br>
}
    </code>
    <h3>Key Points:</h3>
    <ul>
        <li>✅ React manages the state.</li>
        <li>✅ Useful for real-time validation & dynamic behavior.</li>
        <li>❌ More re-renders, requires state management.</li>
    </ul>
</div>
<div class="container">
    <h2>Uncontrolled Component</h2>
    <p>A component where the <strong>DOM itself manages the input state</strong> instead of React. You access the value using <code>ref</code>.</p>
    <h3>Example:</h3>
    <code>
function UncontrolledInput() {<br>
&nbsp;&nbsp;const inputRef = useRef();<br><br>
&nbsp;&nbsp;return (<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;form onSubmit={(e) => {<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e.preventDefault();<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;alert(inputRef.current.value);<br>
&nbsp;&nbsp;&nbsp;&nbsp;}}&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;input ref={inputRef} /&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;button type="submit"&gt;Submit&lt;/button&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/form&gt;<br>
&nbsp;&nbsp;);<br>
}
    </code>
    <h3>Key Points:</h3>
    <ul>
        <li>✅ Less re-rendering, good for performance.</li>
        <li>✅ Useful for integrating with non-React code.</li>
        <li>❌ Harder to track and manipulate state dynamically.</li>
    </ul>
</div>
<div class="container">
    <h2>Which One to Use?</h2>
    <ul>
        <li>Use <strong>controlled components</strong> for forms requiring validation, live updates, or complex UI logic.</li>
        <li>Use <strong>uncontrolled components</strong> for simple inputs, non-critical forms, or when interacting with third-party libraries.</li>
    </ul>
</div>
</details>

---

24. **What is High Order Functions?**
<details>
  <summary>Answer</summary>
 <p>High Order Functions (HOFs) are functions that either:</p>
    <ul>
        <li>Take one or more functions as arguments, or</li>
        <li>Return a function as their result.</li>
    </ul>
    <p>They enable functional programming patterns like <strong>map, filter, and reduce</strong> in JavaScript.</p>
    <h3>Examples:</h3>
    <h4>1. Using a HOF (map):</h4>
    <pre>
        <code>
const numbers = [1, 2, 3, 4];
const squared = numbers.map(num => num * num);
console.log(squared); // [1, 4, 9, 16]
        </code>
    </pre>
    <h4>2. Returning a function:</h4>
    <pre>
        <code>
function multiplier(factor) {
    return function (num) {
        return num * factor;
    };
}
const double = multiplier(2);
console.log(double(5)); // 10
        </code>
    </pre>
    <p>HOFs help in code reusability and cleaner logic.</p>
</details>

---

25. **What is Map, Filter and Reduce Methods?**
<details>
  <summary>Answer</summary>
<h2>1. Map Method (<code>map()</code>)</h2>
    <p>Transforms each element in an array and returns a <strong>new array</strong> with modified elements.</p>
    <code>
        const numbers = [1, 2, 3, 4]; <br>
        const squared = numbers.map(num => num * num); <br>
        console.log(squared); // [1, 4, 9, 16]
    </code>
    <h2>2. Filter Method (<code>filter()</code>)</h2>
    <p>Filters elements based on a condition and returns a <strong>new array</strong> with elements that pass the condition.</p>
    <code>
        const numbers = [1, 2, 3, 4, 5]; <br>
        const evenNumbers = numbers.filter(num => num % 2 === 0); <br>
        console.log(evenNumbers); // [2, 4]
    </code>
    <h2>3. Reduce Method (<code>reduce()</code>)</h2>
    <p>Reduces an array to a single value using an <strong>accumulator</strong> and <strong>current value</strong>.</p>
    <code>
        const numbers = [1, 2, 3, 4, 5]; <br>
        const sum = numbers.reduce((acc, num) => acc + num, 0); <br>
        console.log(sum); // 15
    </code>
    <h2>Key Differences:</h2>
    <table>
        <tr>
            <th>Method</th>
            <th>Purpose</th>
            <th>Returns</th>
        </tr>
        <tr>
            <td><code>map()</code></td>
            <td>Transforms elements</td>
            <td>New array</td>
        </tr>
        <tr>
            <td><code>filter()</code></td>
            <td>Filters elements</td>
            <td>New array</td>
        </tr>
        <tr>
            <td><code>reduce()</code></td>
            <td>Reduces array to a value</td>
            <td>Single value</td>
        </tr>
    </table>

</details>

---

26. **Difference between state and props?**
<details>
  <summary>Answer</summary>
<h2>State</h2>
    <ul>
        <li>Managed <strong>internally</strong> by the component.</li>
        <li>Can be <strong>modified</strong> using <code>useState</code> or <code>setState</code> in class components.</li>
        <li>Used for <strong>dynamic data</strong> that changes over time (e.g., user input, UI updates).</li>
    </ul>
    <h3>Example:</h3>
    <code>
        function Counter() {<br>
        &nbsp;&nbsp;const [count, setCount] = useState(0);<br>
        &nbsp;&nbsp;return &lt;button onClick={() => setCount(count + 1)}&gt;Count: {count}&lt;/button&gt;;<br>
        }
    </code>
    <h2>Props</h2>
    <ul>
        <li>Passed <strong>externally</strong> from a parent component.</li>
        <li><strong>Immutable</strong> (cannot be modified inside the component).</li>
        <li>Used to <strong>pass data</strong> and event handlers to child components.</li>
    </ul>
    <h3>Example:</h3>
    <code>
        function Greeting({ name }) {<br>
        &nbsp;&nbsp;return &lt;h1&gt;Hello, {name}!&lt;/h1&gt;;<br>
        }<br><br>
        function App() {<br>
        &nbsp;&nbsp;return &lt;Greeting name="John" /&gt;;<br>
        }
    </code>
    <h2>Key Differences</h2>
    <table>
        <tr>
            <th>Feature</th>
            <th>State</th>
            <th>Props</th>
        </tr>
        <tr>
            <td><strong>Mutability</strong></td>
            <td>Mutable</td>
            <td>Immutable</td>
        </tr>
        <tr>
            <td><strong>Scope</strong></td>
            <td>Local to component</td>
            <td>Passed from parent</td>
        </tr>
        <tr>
            <td><strong>Usage</strong></td>
            <td>Stores component data</td>
            <td>Passes data to child</td>
        </tr>
        <tr>
            <td><strong>Changes</strong></td>
            <td>Updated via <code>setState</code></td>
            <td>Cannot be changed by child</td>
        </tr>
    </table>
    <p>In short, <strong>state</strong> is for managing component-specific data, while <strong>props</strong> are for passing data between components. 🚀</p>

</details>

---

28. **What is Server Side Rendering?**
<details>
  <summary>Answer</summary>
<p><strong>Server-Side Rendering (SSR)</strong> is a technique where a webpage is rendered on the server instead of the client’s browser. The server processes the request, generates the full HTML page, and sends it to the client. This improves performance, SEO, and initial load time.</p>
    <h2>Benefits of SSR:</h2>
    <ul>
        <li><strong>Faster First Contentful Paint (FCP)</strong>: Users see content sooner.</li>
        <li><strong>Better SEO</strong>: Search engines can index pre-rendered HTML.</li>
        <li><strong>Improved Performance</strong>: Reduces the workload on the client.</li>
    </ul>
    <h2>Downsides:</h2>
    <ul>
        <li><strong>Increased Server Load</strong>: The server processes each request.</li>
        <li><strong>Slower Time-to-Interactive</strong>: Since JS needs to hydrate the app after rendering.</li>
    </ul>
    <h2>SSR in React:</h2>
    <p>Next.js makes SSR easy with <code>getServerSideProps</code> for fetching data at request time.</p>
</details>

---

29. **How to optimise performance of web application?**
<details>
  <summary>Answer</summary>
 <h2>Frontend Optimization</h2>
    <ul>
        <li><strong>Code Splitting & Lazy Loading:</strong> Use React’s <code>React.lazy</code> and <code>Suspense</code> to load components only when needed.</li>
        <li><strong>Reduce Bundle Size:</strong> Use Webpack’s <code>Tree Shaking</code>, remove unused libraries, and enable gzip/Brotli compression.</li>
        <li><strong>Optimize Images:</strong> Use WebP format, lazy loading (<code>loading="lazy"</code>), and responsive images (<code>srcset</code>).</li>
        <li><strong>Minify & Compress Assets:</strong> Use tools like Terser, UglifyJS, and CSS minification to reduce file sizes.</li>
        <li><strong>Use a CDN:</strong> Deliver static assets via CDN for faster global access.</li>
        <li><strong>Efficient State Management:</strong> Use React Context or lightweight libraries like Zustand over Redux where applicable.</li>
        <li><strong>Avoid Unnecessary Re-renders:</strong> Use <code>React.memo</code>, <code>useCallback</code>, and <code>useMemo</code> to optimize rendering.</li>
    </ul>
    <h2>Backend Optimization</h2>
    <ul>
        <li><strong>Use Efficient Database Queries:</strong> Optimize indexes, avoid N+1 queries, and use caching (Redis, Memcached).</li>
        <li><strong>Enable HTTP Caching:</strong> Use <code>Cache-Control</code>, <code>ETag</code>, and <code>Expires</code> headers to reduce redundant requests.</li>
        <li><strong>Optimize API Responses:</strong> Compress JSON responses and paginate large datasets.</li>
        <li><strong>Use Load Balancing:</strong> Distribute traffic across multiple servers to handle higher loads.</li>
    </ul>
    <h2>Network Optimization</h2>
    <ul>
        <li><strong>Reduce HTTP Requests:</strong> Combine CSS/JS files and use HTTP/2 or HTTP/3 for multiplexing.</li>
        <li><strong>Use WebSockets for Real-Time Data:</strong> Avoid frequent API polling by implementing WebSockets.</li>
        <li><strong>Prefetch & Preload:</strong> Use <code>rel="preload"</code> and <code>rel="prefetch"</code> for faster navigation.</li>
    </ul>
    <h2>Monitoring & Profiling</h2>
    <ul>
        <li><strong>Use Lighthouse & Web Vitals:</strong> Regularly check performance metrics.</li>
        <li><strong>Monitor with APM Tools:</strong> Use New Relic, Datadog, or Google Analytics for real-time insights.</li>
    </ul>
</details>

---

30. **What is FlexBox?**
<details>
  <summary>Answer</summary>
<p>Flexbox (Flexible Box Layout) is a CSS layout model designed for efficient arrangement, alignment, and distribution of elements inside a container, even when their sizes are dynamic. It is particularly useful for creating responsive designs.</p>
    <h2>Key Features:</h2>
    <ul>
        <li><strong>Main Axis & Cross Axis:</strong> Items are laid out along a main axis (<code>row</code> or <code>column</code>), with a cross axis perpendicular to it.</li>
        <li><strong>Flexible Sizing:</strong> Elements can grow, shrink, or stay fixed as needed.</li>
        <li><strong>Alignment & Distribution:</strong> Easy centering, spacing, and alignment using properties like <code>justify-content</code> (main axis) and <code>align-items</code> (cross axis).</li>
        <li><strong>Reordering:</strong> Items can be reordered without changing the HTML structure (<code>order</code> property).</li>
    </ul>
    <h2>Basic Properties:</h2>
    <h3>For the flex container:</h3>
    <div class="container">
        <div class="code">display: flex;</div>
        <div class="code">flex-direction: row | column;</div>
        <div class="code">justify-content: flex-start | center | space-between;</div>
        <div class="code">align-items: flex-start | center | stretch;</div>
        <div class="code">flex-wrap: nowrap | wrap;</div>
    </div>
</details>

---

31. **What is the difference between Virtual and Real DOM?**
<details>
  <summary>Answer</summary>
<table>
        <tr>
            <th>Feature</th>
            <th>Virtual DOM</th>
            <th>Real DOM</th>
        </tr>
        <tr>
            <td><strong>Definition</strong></td>
            <td>A lightweight copy of the Real DOM that updates efficiently.</td>
            <td>The actual structure of HTML elements in the browser.</td>
        </tr>
        <tr>
            <td><strong>Update Speed</strong></td>
            <td>Faster updates due to diffing and batching.</td>
            <td>Slower updates as it re-renders the entire affected tree.</td>
        </tr>
        <tr>
            <td><strong>Re-rendering</strong></td>
            <td>Only updates the changed parts (diffing algorithm).</td>
            <td>Updates the entire UI, even for small changes.</td>
        </tr>
        <tr>
            <td><strong>Performance</strong></td>
            <td>More efficient and optimized.</td>
            <td>Less efficient due to direct manipulation.</td>
        </tr>
        <tr>
            <td><strong>Usage</strong></td>
            <td>Used in frameworks like React for better UI updates.</td>
            <td>Used natively by browsers.</td>
        </tr>
    </table>
    <h3>How Virtual DOM Works in React?</h3>
    <ul>
        <li>A copy of the Real DOM is created (Virtual DOM).</li>
        <li>When the state changes, a new Virtual DOM is generated.</li>
        <li>React compares the new Virtual DOM with the previous one (diffing).</li>
        <li>Only the changed elements are updated in the Real DOM (reconciliation).</li>
    </ul>
</details>

---

32. **What is Function Currying?**
<details>
  <summary>Answer</summary>
<p><strong>Function currying</strong> is a technique in functional programming where a function is transformed into a sequence of functions, each taking a single argument. Instead of calling a function with multiple arguments at once, you call a series of functions, each taking one argument and returning another function until all arguments are provided.</p>   
    <h2>Example in JavaScript:</h2>
    <code>
        function curryFunction(a) {<br>
        &nbsp;&nbsp;return function (b) {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;return function (c) {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return a + b + c;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;};<br>
        &nbsp;&nbsp;};<br>
        }<br><br>
        console.log(curryFunction(1)(2)(3)); // Output: 6
    </code>
    <h2>Why Use Currying?</h2>
    <ul>
        <li><strong>Reusability:</strong> You can create specialized functions by passing only some arguments.</li>
        <li><strong>Code Readability:</strong> Helps break down complex functions into smaller, manageable ones.</li>
        <li><strong>Functional Programming:</strong> Encourages immutability and pure functions.</li>
    </ul>
</details>

---

33. **What is Redux?**
<details>
  <summary>Answer</summary>
 <p>Redux is a state management library for JavaScript applications, commonly used with React. It helps manage application state in a predictable way using a single global store.</p>
    <h2>Key Concepts:</h2>
    <ul>
        <li><strong>Store:</strong> Centralized state container.</li>
        <li><strong>Actions:</strong> Objects describing state changes.</li>
        <li><strong>Reducers:</strong> Pure functions that update the state based on actions.</li>
        <li><strong>Dispatch:</strong> Method to send actions to the store.</li>
        <li><strong>Selectors:</strong> Functions to extract specific data from the store.</li>
    </ul>
    <h2>Why Use Redux?</h2>
    <ul>
        <li>Centralized state management.</li>
        <li>Predictable state updates.</li>
        <li>Easier debugging with time-travel debugging.</li>
        <li>Works well for complex applications with shared state.</li>
    </ul>
    <p>For smaller projects, React's built-in state (<code>useState</code>, <code>useReducer</code>, <code>Context API</code>) may be enough.</p>
</details>

---

34. **Difference between Call, Apply and Bind?**
<details>
  <summary>Answer</summary>
 <p>All three methods are used to invoke a function with a specified <code>this</code> value, but they differ in how they handle arguments.</p>
    <table>
        <tr>
            <th>Method</th>
            <th>Execution</th>
            <th>Arguments Passing</th>
            <th>Returns</th>
        </tr>
        <tr>
            <td><code>call()</code></td>
            <td>Invokes the function immediately</td>
            <td>Arguments are passed individually</td>
            <td>Function’s result</td>
        </tr>
        <tr>
            <td><code>apply()</code></td>
            <td>Invokes the function immediately</td>
            <td>Arguments are passed as an array</td>
            <td>Function’s result</td>
        </tr>
        <tr>
            <td><code>bind()</code></td>
            <td>Returns a new function (does NOT execute immediately)</td>
            <td>Arguments are passed individually</td>
            <td>New function with bound <code>this</code></td>
        </tr>
    </table>
    <h2>Examples</h2>
    <h3>1. <code>call()</code></h3>
    <pre><code>
function greet(city) {
    console.log(`Hello, my name is ${this.name} and I'm from ${city}`);
}
const person = { name: "John" };
greet.call(person, "New York"); // "Hello, my name is John and I'm from New York"
    </code></pre>
    <h3>2. <code>apply()</code></h3>
    <pre><code>
greet.apply(person, ["Los Angeles"]); // "Hello, my name is John and I'm from Los Angeles"
    </code></pre>
    <h3>3. <code>bind()</code></h3>
    <pre><code>
const boundGreet = greet.bind(person, "Chicago");
boundGreet(); // "Hello, my name is John and I'm from Chicago"
    </code></pre>
    <h2>Key Takeaways</h2>
    <ul>
        <li>Use <code>call()</code> when you know the arguments in advance.</li>
        <li>Use <code>apply()</code> when arguments are in an array.</li>
        <li>Use <code>bind()</code> when you want to create a function with a fixed <code>this</code> value for later execution.</li>
    </ul>
</details>

---

35. **What is Debouncing?**
<details>
  <summary>Answer</summary>
  <p>Debouncing is a programming technique used to limit the number of times a function executes, especially in response to events like keystrokes, clicks, or window resizing. It ensures that the function runs only after a specified delay has passed since the last event trigger.</p>
    <h3>Example (JavaScript):</h3>
    <pre>
<code>
function debounce(func, delay) {
    let timer;
    return function (...args) {
        clearTimeout(timer);
        timer = setTimeout(() => func.apply(this, args), delay);
    };
}
// Usage: Debounced search input
const searchInput = document.getElementById("search");
searchInput.addEventListener("input", debounce((e) => {
    console.log("Searching for:", e.target.value);
}, 300));
</code>
    </pre>
    <h3>Live Demo:</h3>
  <pre>
    <input type="text" id="search" placeholder="Type to search...">
    <script>
        function debounce(func, delay) {
            let timer;
            return function (...args) {
                clearTimeout(timer);
                timer = setTimeout(() => func.apply(this, args), delay);
            };
        }
        // Debounced input example
        const searchInput = document.getElementById("search");
        searchInput.addEventListener("input", debounce((e) => {
            console.log("Searching for:", e.target.value);
        }, 300));
    </script>
  </pre>
</details>

---

36. **What is Shallow and Deep Copy?**
<details>
  <summary>Answer</summary>
<h1>Shallow Copy vs Deep Copy</h1>
    <h2>1. Shallow Copy</h2>
    <ul>
        <li>Copies only the reference of nested objects, not the actual objects themselves.</li>
        <li>If the original object is modified, the changes reflect in the copied object as well (for nested objects).</li>
        <li>In JavaScript, you can create a shallow copy using:</li>
        <ul>
            <li><code>Object.assign({}, obj)</code></li>
            <li>Spread operator: <code>{ ...obj }</code></li>
            <li><code>Array.prototype.slice()</code> or <code>Array.prototype.concat()</code> for arrays</li>
        </ul>
    </ul>
    <h2>2. Deep Copy</h2>
    <ul>
        <li>Creates a completely independent copy, including nested objects.</li>
        <li>Changes in the original object do not affect the copied object.</li>
        <li>In JavaScript, deep copies can be made using:</li>
        <ul>
            <li><code>JSON.parse(JSON.stringify(obj))</code> (loses functions & special objects like Date, Map)</li>
            <li><strong>Lodash:</strong> <code>_.cloneDeep(obj)</code></li>
            <li>Manually using recursion for complex structures</li>
        </ul>
    </ul>
    <h2>Example in JavaScript</h2>
    <pre>
let obj1 = { a: 1, b: { c: 2 } };
let shallowCopy = { ...obj1 }; // Shallow copy
shallowCopy.b.c = 42;
console.log(obj1.b.c); // 42 (Changes reflected in the original)
let deepCopy = JSON.parse(JSON.stringify(obj1)); // Deep copy
deepCopy.b.c = 99;
console.log(obj1.b.c); // Still 42 (No changes in the original)
    </pre>
</details>

---

37. **What is Throttling?**
<details>
  <summary>Answer</summary>
    <p>Throttling is a technique used in JavaScript to limit the execution of a function to a fixed interval. This is useful for optimizing performance in events like scrolling, resizing, or keypresses.</p>
    <h2>Example: Throttling with <code>setTimeout</code></h2>
    <pre class="code">
function throttle(func, limit) {
    let inThrottle;
    return function() {
        const args = arguments;
        const context = this;
        if (!inThrottle) {
            func.apply(context, args);
            inThrottle = true;
            setTimeout(() => (inThrottle = false), limit);
        }
    };
}
    </pre>
    <h2>Usage Example</h2>
    <p>The example below demonstrates throttling on a scroll event. The text updates only once per second while scrolling.</p>
    <p id="status">Waiting for scroll...</p>
    <div class="scroll-box">
        <h2>Scroll down to see throttling in action</h2>
    </div>
    <pre>
    <script>
        function throttle(func, limit) {
            let inThrottle;
            return function() {
                const args = arguments;
                const context = this;
                if (!inThrottle) {
                    func.apply(context, args);
                    inThrottle = true;
                    setTimeout(() => (inThrottle = false), limit);
                }
            };
        }
        const updateStatus = () => {
            document.getElementById("status").textContent = "Scroll event triggered at " + new Date().toLocaleTimeString();
        };
        window.addEventListener("scroll", throttle(updateStatus, 1000));
    </script>
    </pre>
</details>

---

38. **Difference between position Fixed and Absolute?**
<details>
  <summary>Answer</summary>
      <table>
        <tr>
            <th>Feature</th>
            <th>position: absolute</th>
            <th>position: fixed</th>
        </tr>
        <tr>
            <td><strong>Reference</strong></td>
            <td>Nearest positioned (non-static) ancestor or <code>&lt;html&gt;</code> if none</td>
            <td>Viewport (browser window)</td>
        </tr>
        <tr>
            <td><strong>Scrolling</strong></td>
            <td>Moves with page scroll</td>
            <td>Stays fixed, does not move with scroll</td>
        </tr>
        <tr>
            <td><strong>Parent Dependence</strong></td>
            <td>Positioned inside a specific container if an ancestor is positioned</td>
            <td>Independent of any container</td>
        </tr>
        <tr>
            <td><strong>Common Use Cases</strong></td>
            <td>Tooltips, dropdowns, overlays inside a container</td>
            <td>Sticky headers, floating buttons, fixed navbars</td>
        </tr>
        <tr>
            <td><strong>Example CSS</strong></td>
            <td><code>position: absolute; top: 20px; left: 20px;</code></td>
            <td><code>position: fixed; top: 20px; left: 20px;</code></td>
        </tr>
    </table>
</details>

---

39. **Difference between inline and block element?**
<details>
  <summary>Answer</summary>
   <h2>Block Elements</h2>
    <ul>
        <li>Take up the full width available (span the entire width of their parent container).</li>
        <li>Always start on a new line.</li>
        <li>Can contain both block and inline elements.</li>
        <li>Examples: <code>&lt;div&gt;</code>, <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code> to <code>&lt;h6&gt;</code>, 
            <code>&lt;section&gt;</code>, <code>&lt;article&gt;</code>, <code>&lt;header&gt;</code>, <code>&lt;footer&gt;</code>, <code>&lt;ul&gt;</code>, <code>&lt;li&gt;</code>.
        </li>
    </ul>
    <h2>Inline Elements</h2>
    <ul>
        <li>Take up only as much width as necessary.</li>
        <li>Do not start on a new line; they appear alongside other elements.</li>
        <li>Cannot contain block elements.</li>
        <li>Examples: <code>&lt;span&gt;</code>, <code>&lt;a&gt;</code>, <code>&lt;strong&gt;</code>, <code>&lt;em&gt;</code>, <code>&lt;img&gt;</code>, <code>&lt;label&gt;</code>, <code>&lt;b&gt;</code>, <code>&lt;i&gt;</code>.
        </li>
    </ul>
    <h2>Example:</h2>
    <p>This is a block element:</p>
    <div style="border: 1px solid black; padding: 10px;">Block Element (div)</div>
    <p>This is an inline element inside a block element:</p>
    <p>Text with a <span style="color: red; border: 1px solid red; padding: 2px;">inline span</span> inside.</p>
</details>

---

40. **Difference between if and ternary?**
<details>
  <summary>Answer</summary>
  <h2>1. <code>if</code> Statement</h2>
    <ul>
        <li>Used for multi-line conditional logic.</li>
        <li>Can execute multiple statements.</li>
        <li>More readable for complex conditions.</li>
    </ul>
    <pre>
let num = 10;
if (num > 0) {
    console.log("Positive");
} else {
    console.log("Non-positive");
}
    </pre>  
    <h2>2. Ternary Operator (<code>? :</code>)</h2>
    <ul>
        <li>A compact, single-line alternative to <code>if-else</code>.</li>
        <li>Returns a value (expression-based).</li>
        <li>Best for simple conditions.</li>
    </ul>
    <pre>
let num = 10;
let result = num > 0 ? "Positive" : "Non-positive";
console.log(result);
    </pre> 
    <h2>3. When to Use?</h2>
    <ul>
        <li>Use <code>if</code> for complex logic.</li>
        <li>Use the ternary operator for simple, concise conditions.</li>
    </ul>
</details>

---

41. **Why we add DOCTYPE in HTML?**
<details>
  <summary>Answer</summary>
 <p><code>&lt;!DOCTYPE html&gt;</code> is used in HTML to declare the document type and version of HTML being used.</p>
    <p>It ensures that the browser renders the page in <strong>standards mode</strong> instead of <strong>quirks mode</strong>. This helps maintain consistent rendering across different browsers.</p>
    <p>For modern web development, <code>&lt;!DOCTYPE html&gt;</code> is used for <strong>HTML5</strong>.</p>
</body>
</details>

---

42. **What is the purpose of Head Tag in html?**
<details>
  <summary>Answer</summary>
 <p>
        The <code>&lt;head&gt;</code> tag in HTML contains metadata and links to external resources 
        that are essential for the webpage but are not displayed directly to users. It typically includes:
    </p>
    <ul>
        <li><strong>&lt;title&gt;</strong> – Sets the page title (shown in the browser tab).</li>
        <li><strong>&lt;meta&gt;</strong> – Defines metadata like character encoding, viewport settings, and SEO descriptions.</li>
        <li><strong>&lt;link&gt;</strong> – Links external stylesheets (CSS).</li>
        <li><strong>&lt;script&gt;</strong> – Includes JavaScript files or inline scripts.</li>
        <li><strong>&lt;style&gt;</strong> – Contains internal CSS.</li>
        <li><strong>&lt;base&gt;</strong> – Sets the base URL for relative links.</li>
    </ul>
    <p>
        These elements help structure, style, and enhance the functionality of the webpage.
    </p>
</body>
</details>

---

43. **What is the use of deffer keyword in script tag?**
<details>
  <summary>Answer</summary>
<h1>Understanding the defer Attribute in &lt;script&gt; Tag</h1>
    <h2>Key Benefits:</h2>
    <ul>
        <li><strong>Non-blocking Execution:</strong> The script is downloaded in the background while the HTML continues parsing.</li>
        <li><strong>Maintains Execution Order:</strong> If multiple scripts have <code>defer</code>, they execute in the order they appear in the document.</li>
        <li><strong>Runs After DOM Parsing:</strong> Ensures that the entire HTML document is parsed before executing the script.</li>
    </ul>
    <h2>Example:</h2>
    <pre>
        &lt;!DOCTYPE html&gt;
        &lt;html lang="en"&gt;
        &lt;head&gt;
            &lt;script src="script1.js" defer&gt;&lt;/script&gt;
            &lt;script src="script2.js" defer&gt;&lt;/script&gt;
        &lt;/head&gt;
        &lt;body&gt;
            &lt;h1&gt;Hello World&lt;/h1&gt;
        &lt;/body&gt;
        &lt;/html&gt;
    </pre>
    <h2>Explanation:</h2>
    <ul>
        <li><code>script1.js</code> loads and executes before <code>script2.js</code> (even if <code>script2.js</code> loads first).</li>
        <li>The scripts run <strong>only after</strong> the HTML is fully parsed.</li>
    </ul>
    <h2>When to Use?</h2>
    <p>Use <code>defer</code> when:</p>
    <ul>
        <li>The script doesn't need to execute immediately.</li>
        <li>You need scripts to execute in order.</li>
        <li>The script interacts with the DOM.</li>
    </ul>
</details>

---

44. **What is the use of async keyword in script tag?**
<details>
  <summary>Answer</summary>
<h2>Use of <code>async</code> in Script Tag</h2>
    <p>The <code>async</code> keyword in the <code>&lt;script&gt;</code> tag is used to load and execute an external JavaScript file asynchronously. It allows the script to download in parallel with HTML parsing and execute as soon as it’s ready, without blocking the rendering of the page.</p>
    <h3>Example:</h3>
    <pre>
        <code>
        &lt;script async src="script.js"&gt;&lt;/script&gt;
        </code>
    </pre>
    <h3>Behavior:</h3>
    <ul>
        <li>The script is fetched in parallel with the HTML parsing.</li>
        <li>Once downloaded, it executes immediately, possibly before the HTML is fully loaded.</li>
        <li>It does <strong>not</strong> guarantee execution order if multiple async scripts are present.</li>
    </ul>
    <h3>When to Use:</h3>
    <p>Use <code>async</code> for scripts that don’t depend on other scripts or DOM elements (e.g., analytics, ads, tracking scripts).</p>
    <p>For scripts that rely on execution order, use <code>defer</code> instead.</p>
</details>

---

45. **What are DataTypes in JS?**
<details>
  <summary>Answer</summary>
 <ul>
            <li><strong>Number:</strong> Represents numeric values. Example: <code>let num = 42;</code></li>
            <li><strong>String:</strong> Represents text. Example: <code>let str = "Hello";</code></li>
            <li><strong>Boolean:</strong> Represents <code>true</code> or <code>false</code>. Example: <code>let isActive = true;</code></li>
            <li><strong>Undefined:</strong> A variable declared but not assigned a value. Example: <code>let x; console.log(x); // undefined</code></li>
            <li><strong>Null:</strong> Represents an intentional absence of value. Example: <code>let y = null;</code></li>
            <li><strong>BigInt:</strong> Used for very large integers. Example: <code>let bigNum = 12345678901234567890n;</code></li>
            <li><strong>Symbol:</strong> Used to create unique identifiers. Example: <code>let sym = Symbol("unique");</code></li>
        </ul>
        <h2>Non-Primitive (Reference) Data Type</h2>
        <ul>
            <li><strong>Object:</strong> Collection of key-value pairs (includes arrays, functions, and objects). Example: <code>let obj = { name: "John", age: 30 };</code></li>
        </ul>
        <p>All primitive types are immutable, whereas objects are mutable and stored by reference.</p>
</details>

---

46. **What is type of a Class?**
<details>
  <summary>Answer</summary>
<p>In JavaScript, a <strong>class</strong> is a special type of function.</p>
    <h3>Checking the Type of a Class:</h3>
    <pre><code>
class MyClass {}
console.log(typeof MyClass); // "function"
    </code></pre>
    <h3>Explanation:</h3>
    <ul>
        <li>In JavaScript, <strong>classes are syntactic sugar</strong> over constructor functions.</li>
        <li>A class itself is a <strong>function</strong>, specifically a constructor function.</li>
    </ul>
    <p>Even though classes look different from traditional functions, under the hood, they are still <strong>special functions</strong> in JavaScript.</p>
</details>

---

47. **Why do we use Semantic Tags in HTML?**
<details>
  <summary>Answer</summary>
 <section>
        <p>Semantic tags in HTML provide meaning to the content, making it easier for both developers and search engines to understand the structure of a webpage.</p>
    </section>
    <section>
        <h2>Benefits of Semantic Tags</h2>
        <ul>
            <li><strong>Readability:</strong> Makes code easier to read and understand.</li>
            <li><strong>SEO:</strong> Helps search engines better index the webpage.</li>
            <li><strong>Accessibility:</strong> Enhances usability for assistive technologies.</li>
            <li><strong>Maintainability:</strong> Simplifies code management and updates.</li>
        </ul>
</details>

---

48. **What is difference between Div and Span Tag?**
<details>
  <summary>Answer</summary>
 <section>
  <h3>1. Block vs Inline</h3>
    <p><strong>&lt;div&gt;</strong> is a <b>block-level</b> element → Takes up the full width and starts on a new line.</p>
    <p><strong>&lt;span&gt;</strong> is an <b>inline</b> element → Only takes up as much width as its content.</p>

    <h3>2. Usage</h3>
    <p><strong>&lt;div&gt;</strong> is used for <b>structuring layouts</b> and grouping elements.</p>
    <p><strong>&lt;span&gt;</strong> is used for <b>styling or modifying specific text</b> within a block.</p>

    <h3>Example:</h3>
    <div class="div-box">This is a div (block-level element)</div>
    <p>This is a <span class="span-text">span</span> (inline element inside a paragraph).</p>
</details>

---

49. **What is Specificity in CSS?**
<details>
  <summary>Answer</summary>
 <p>Specificity in CSS determines which rule takes precedence when multiple rules target the same element. It is calculated based on the types of selectors used:</p>
    <ul>
        <li><strong>Inline styles</strong> (<code>style</code> attribute) → Highest specificity <code>(1,0,0,0)</code></li>
        <li><strong>IDs</strong> (<code>#id</code>) → High specificity <code>(0,1,0,0)</code></li>
        <li><strong>Classes, attributes, and pseudo-classes</strong> (<code>.class</code>, <code>[attr]</code>, <code>:hover</code>) → Medium specificity <code>(0,0,1,0)</code></li>
        <li><strong>Elements and pseudo-elements</strong> (<code>div</code>, <code>h1</code>, <code>::before</code>) → Low specificity <code>(0,0,0,1)</code></li>
    </ul>
    <p>If two selectors have the same specificity, the one that appears later in the CSS file wins.</p>
    <h3>Example:</h3>
    <pre>
    /* Specificity: (0,0,1,0) */
    .button { color: blue; }  
    /* Specificity: (0,1,0,0) - Higher priority */
    #submit { color: red; }  
    /* Specificity: (1,0,0,0) - Highest priority */
    </pre>
    <button class="button" id="submit" style="color: green;">Click Me</button>
    <p>Here, the button text will be <strong style="color: green;">green</strong> due to the inline style.</p>
</details>

---

50. **What is Hoisting?**
<details>
  <summary>Answer</summary>
  <p>Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase, before the code is executed.</p>
    <h2>Key Points:</h2>
    <h3>1. Function Declarations</h3>
    <p>Function declarations are fully hoisted and can be called before they appear in the code.</p>
    <code>
        greet(); // Works fine
        function greet() {
            console.log("Hello!");
        }
    </code>
    <h3>2. Var Declarations</h3>
    <p>Var declarations are hoisted but initialized as <code>undefined</code>, so accessing them before declaration gives <code>undefined</code>.</p>
    <code>
        console.log(a); // undefined
        var a = 10;
    </code>
    <h3>3. Let and Const</h3>
    <p>Let and Const are hoisted but do not get initialized, leading to a <strong>Temporal Dead Zone (TDZ)</strong> until the declaration is encountered.</p>
    <code>
        console.log(b); // ReferenceError
        let b = 20;
    </code>
    <h2>Conclusion:</h2>
    <p>Hoisting allows function and variable declarations to be used before their actual declaration, but <code>var</code> initializes with <code>undefined</code>, while <code>let</code> and <code>const</code> remain in the TDZ.</p>
</body>
</html>
</details>

---

51. **How async operation is handled in JS?**
<details>
  <summary>Answer</summary>
  <h3>1. Callbacks (Old Approach)</h3>
    <p>A function is passed as an argument and executed once the async task is done.</p>
    <pre><code>
function fetchData(callback) {
    setTimeout(() => {
        callback("Data fetched");
    }, 1000);
}
fetchData((data) => console.log(data)); // Output after 1s: Data fetched
    </code></pre>
    <p><strong>Downside:</strong> Leads to callback hell if multiple async operations are nested.</p>
    <h3>2. Promises (Modern Approach)</h3>
    <p>A <code>Promise</code> represents a future value. It can be in pending, resolved, or rejected state.</p>
    <pre>
    <code>
function fetchData() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Data fetched");
        }, 1000);
    });
}
  fetchData().then((data) => console.log(data)); // Output after 1s: Data fetched
    </code>
    </pre>
    <p><strong>Advantage:</strong> Avoids callback hell using <code>.then()</code> chaining.</p>
    <h3>3. Async/Await (Recommended)</h3>
    <p>A cleaner and more readable way to handle async code.</p>
    <pre><code>
async function fetchData() {
    return "Data fetched";
}
async function getData() {
    const data = await fetchData();
    console.log(data);
}
getData(); // Output: Data fetched
    </code></pre>
    <p><strong>Advantage:</strong> Reads like synchronous code while being non-blocking.</p>
</details>

---

52. **What is Higher Order Components?**
<details>
  <summary>Answer</summary>
<p>Higher-Order Components (HOC) in React are functions that take a component as input and return an enhanced component. HOCs allow you to reuse component logic, manage state, and add extra functionalities without modifying the original component.</p>
    <h2>Example:</h2>
    <code>
        const withLogger = (WrappedComponent) => {  
            return (props) => {  
                console.log("Rendered with props:", props);  
                return &lt;WrappedComponent {...props} /&gt;;  
            };  
        };  
        const Button = (props) => &lt;button&gt;{props.label}&lt;/button&gt;;  
        const EnhancedButton = withLogger(Button);  
        // Usage  
        &lt;EnhancedButton label="Click Me" /&gt;;
    </code>
    <h2>Key Points:</h2>
    <ul>
        <li>HOCs <strong>don’t modify</strong> the original component; they wrap it.</li>
        <li>They are <strong>pure functions</strong> (they don't affect the original component).</li>
        <li>Useful for <strong>code reusability</strong> (e.g., authentication checks, logging, theming).</li>
    </ul>
    <p>Since React hooks (introduced in v16.8), HOCs are used less frequently, as hooks provide similar functionality in a more readable way.</p>
</details>

---

53. **What is Prop Drilling?**
<details>
  <summary>Answer</summary>
    <p>Prop Drilling is the process of passing data (props) from a parent component to deeply nested child components, even if some intermediate components don’t need that data. This can make the code harder to manage and maintain.</p>
    <h3>Example:</h3>
    <code>
        const Parent = () => {<br>
        &nbsp;&nbsp;const message = "Hello from Parent!";<br>
        &nbsp;&nbsp;return &lt;Child message={message} /&gt;;<br>
        };<br><br>
        const Child = ({ message }) => {<br>
        &nbsp;&nbsp;return &lt;GrandChild message={message} /&gt;;<br>
        };<br><br>
        const GrandChild = ({ message }) => {<br>
        &nbsp;&nbsp;return &lt;p&gt;{message}&lt;/p&gt;;<br>
        };
    </code>
    <h3>Solution:</h3>
    <p>To avoid prop drilling, you can use:</p>
    <ul>
        <li><strong>Context API</strong> (<code>useContext</code>)</li>
        <li><strong>State Management Libraries</strong> (Redux, Zustand, Jotai, etc.)</li>
    </ul>
</details>

---

54. **What is Lazy Loading?**
<details>
  <summary>Answer</summary>
 <p>
        Lazy loading is a technique that delays loading resources (like images, components, or data) until they are needed. 
        This improves performance by reducing initial load time and saving bandwidth.
    </p>
    <h2>Lazy Loading in React</h2>
    <p>
        In <strong>React</strong>, lazy loading is often implemented using <code>React.lazy</code> for component-based code splitting:
    </p>
    <code>
        const MyComponent = React.lazy(() => import('./MyComponent'));<br><br>
        function App() {<br>
        &nbsp;&nbsp;return (<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&lt;Suspense fallback=&lt;div&gt;Loading...&lt;/div&gt;&gt;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;MyComponent /&gt;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&lt;/Suspense&gt;<br>
        &nbsp;&nbsp;);<br>
        }
    </code>
    <p>
        Here, <code>MyComponent</code> is loaded only when it's needed, reducing the initial JavaScript bundle size.
    </p>
</details>

---

55. **What is Virtual DOM?**
<details>
  <summary>Answer</summary>
 <p>The <strong>Virtual DOM (VDOM)</strong> is a lightweight JavaScript representation of the actual DOM. It helps improve performance by minimizing direct manipulations of the real DOM.</p>
    <h2>How it Works:</h2>
    <ol>
        <li><strong>Render:</strong> React creates a virtual DOM tree based on the UI structure.</li>
        <li><strong>Diffing:</strong> When state changes, React compares (diffs) the new VDOM with the previous one.</li>
        <li><strong>Reconciliation:</strong> React updates only the changed parts in the real DOM instead of re-rendering everything.</li>
    </ol>
    <h2>Benefits:</h2>
    <ul>
        <li>Faster updates by reducing unnecessary DOM operations.</li>
        <li>Improved performance with efficient UI rendering.</li>
        <li>Better user experience with smooth updates.</li>
    </ul>
</details>

---

56. **Difference between Server Side Rendering and Client Side Rendering?**
<details>
  <summary>Answer</summary>
 <table>
        <tr>
            <th>Feature</th>
            <th>Server-Side Rendering (SSR)</th>
            <th>Client-Side Rendering (CSR)</th>
        </tr>
        <tr>
            <td><strong>Rendering Location</strong></td>
            <td>On the server before sending to the client</td>
            <td>On the client (browser) after receiving raw data</td>
        </tr>
        <tr>
            <td><strong>Initial Load Time</strong></td>
            <td>Faster (pre-rendered HTML sent)</td>
            <td>Slower (JS needs to load and execute)</td>
        </tr>
        <tr>
            <td><strong>SEO</strong></td>
            <td>Better (content is available on page load)</td>
            <td>Worse (content loads dynamically via JS)</td>
        </tr>
        <tr>
            <td><strong>Performance</strong></td>
            <td>Faster initial load, but slower navigation</td>
            <td>Slower initial load, but faster navigation after load</td>
        </tr>
        <tr>
            <td><strong>Interactivity</strong></td>
            <td>Needs hydration to become interactive</td>
            <td>Directly interactive after JS loads</td>
        </tr>
        <tr>
            <td><strong>Use Case</strong></td>
            <td>Good for SEO-heavy and content-based sites (e.g., blogs, e-commerce)</td>
            <td>Good for web apps with dynamic interactions (e.g., dashboards, SPAs)</td>
        </tr>
    </table>
    <h3>Examples:</h3>
    <ul>
        <li><strong>SSR:</strong> Next.js (with <code>getServerSideProps</code>)</li>
        <li><strong>CSR:</strong> React (default), Angular, Vue (without SSR)</li>
    </ul>
</details>

---

57. **What is Routing in React?**
<details>
  <summary>Answer</summary>
<p>Routing in React refers to the process of navigating between different components or pages in a React application without reloading the page.</p>
  <p>It's usually handled by a library like <strong>React Router</strong>.</p>
  <h2>Key Concepts:</h2>
  <ul>
    <li><strong>&lt;BrowserRouter&gt;</strong>: Wraps your app and enables routing.</li>
    <li><strong>&lt;Routes&gt;</strong>: Contains all your route definitions.</li>
    <li><strong>&lt;Route&gt;</strong>: Defines a path and the component to render.</li>
    <li><strong>useNavigate()</strong>: Programmatically navigate to a route.</li>
    <li><strong>useParams()</strong>: Access route parameters (e.g., /user/:id).</li>
  </ul>
  <h2>Example:</h2>
  <pre>
<code>
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Home from "./Home";
import About from "./About";
function App() {
  return (
    &lt;BrowserRouter&gt;
      &lt;Routes&gt;
        &lt;Route path="/" element={&lt;Home /&gt;} /&gt;
        &lt;Route path="/about" element={&lt;About /&gt;} /&gt;
      &lt;/Routes&gt;
    &lt;/BrowserRouter&gt;
  );
}
</code>
  </pre>
</details>

---

58. **What is IIFE in React?**
<details>
  <summary>Answer</summary>
  <p>
    In React, an <strong>IIFE (Immediately Invoked Function Expression)</strong> is a JavaScript function that runs as soon as it's defined. It's not React-specific but is sometimes used in React code to:
  </p>
  <ul>
    <li>Execute code immediately inside a component.</li>
    <li>Avoid polluting the main JSX return with complex logic.</li>
  </ul>
  <h2>Syntax:</h2>
  <pre><code>
(() => {
  // code here
})();
  </code></pre>
  <h2>Example in React:</h2>
  <pre><code>
const MyComponent = () =&gt; {
  const value = 10;
  return (
    &lt;div&gt;
      {
        (() =&gt; {
          if (value &gt; 5) return &lt;p&gt;Value is high&lt;/p&gt;;
          else return &lt;p&gt;Value is low&lt;/p&gt;;
        })()
      }
    &lt;/div&gt;
  );
};
  </code></pre>
</details>

---

59. **JS Object can have integer as a key?**
<details>
  <summary>Answer</summary>
 <p>In JavaScript, <strong>object keys are always strings (or symbols)</strong>. Even if you use an integer as a key, JavaScript automatically converts it to a string.</p>
  <h3>Example:</h3>
  <pre>
<code>
const obj = {
  1: "one",
  2: "two"
};
console.log(obj);         // { '1': 'one', '2': 'two' }
console.log(obj[1]);      // 'one'
console.log(obj["1"]);    // 'one'
</code>
  </pre>
  <p>So yes, you <strong>can</strong> use integers as keys when defining an object, but they will be stored as <strong>string keys</strong>.</p>
</details>

---

60. **Unique features of key in object?**
<details>
  <summary>Answer</summary>
<ol>
    <li>
      <strong>String or Symbol Only:</strong>  
      <p>Keys are always either strings or symbols — even if you use a number or boolean, it will be converted to a string.</p>
      <pre><code>const obj = { 1: "a", true: "b" };
console.log(Object.keys(obj)); // ["1", "true"]</code></pre>
    </li>
    <li>
      <strong>No Duplicate Keys:</strong>  
      <p>If you define a key more than once, the last one overrides the previous.</p>
      <pre><code>const obj = { a: 1, a: 2 };
console.log(obj.a); // 2</code></pre>
    </li>
    <li>
      <strong>Key Order (Mostly Predictable):</strong>
      <ul>
        <li>Integer-like keys come first in ascending order.</li>
        <li>Other string keys follow in insertion order.</li>
        <li>Symbol keys maintain their own insertion order.</li>
      </ul>
    </li>
    <li>
      <strong>Dynamic Key Names:</strong>  
      <p>You can use computed property names with <code>[]</code>.</p>
      <pre><code>const key = "name";
const obj = { [key]: "John" };</code></pre>
    </li>
    <li>
      <strong>Symbols as Unique Keys:</strong>  
      <p>Symbols create keys that won’t conflict with other string keys.</p>
      <pre><code>const sym = Symbol("id");
const obj = { [sym]: 123 };</code></pre>
    </li>
    <li>
      <strong>Not Accessible via Dot Notation (for non-string/safe keys):</strong>  
      <p>You must use bracket notation for keys with spaces or symbols.</p>
      <pre><code>const obj = { "full name": "John Doe" };
console.log(obj["full name"]); // valid</code></pre>
    </li>
  </ol>
</details>

---

61. **What is useCallback?**
<details>
  <summary>Answer</summary>
 <p><code>useCallback</code> is a React Hook that <strong>memoizes a function</strong>, so it doesn't get recreated on every render unless its dependencies change.</p>
  <h2>Syntax:</h2>
  <pre><code>const memoizedFn = useCallback(() =&gt; {
  // function code
}, [dependencies]);</code></pre>
  <h2>Why use it?</h2>
  <p>To <strong>avoid unnecessary re-renders or re-creations</strong> of functions, especially when passing them to child components or using them in <code>useEffect</code>.</p>
  <h2>Example:</h2>
  <pre><code>import { useState, useCallback } from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  const increment = useCallback(() =&gt; {
    setCount(c =&gt; c + 1);
  }, []); // `increment` won't be recreated on every render
  return &lt;button onClick={increment}&gt;Count: {count}&lt;/button&gt;;
}</code></pre>
  <p>Without <code>useCallback</code>, <code>increment</code> would be a <strong>new function on every render</strong>, which can cause issues if passed to memoized child components.</p>
</details>

---

62. **What is useMemo?**
<details>
  <summary>Answer</summary>
<p><code>useMemo</code> is a React Hook that <strong>memoizes the result of a computation</strong>, so it's only recalculated when its dependencies change. It helps optimize performance by avoiding unnecessary recalculations.</p>
  <h3>Syntax:</h3>
  <pre><code>const memoizedValue = useMemo(() =&gt; computeExpensiveValue(a, b), [a, b]);</code></pre>
  <h3>Use Case:</h3>
  <p>When you have a <strong>computationally expensive function</strong> or want to avoid re-running logic unless dependencies change.</p>
  <h3>Example:</h3>
  <pre><code>const sortedList = useMemo(() =&gt; {
  return list.sort((a, b) =&gt; a - b);
}, [list]);</code></pre>
  <p>This ensures <code>sortedList</code> is only recalculated when <code>list</code> changes.</p>
</details>

---

63. **What is Pure Components?**
<details>
  <summary>Answer</summary>
<p>In React, <strong>Pure Components</strong> are components that do a shallow comparison of props and state to determine if a re-render is necessary.</p>
  <h3>Key Points:</h3>
  <ul>
    <li>A <strong>PureComponent</strong> only re-renders when props or state actually change.</li>
    <li>It implements <code>shouldComponentUpdate()</code> with a <strong>shallow</strong> prop and state comparison.</li>
    <li>Used to optimize performance and avoid unnecessary re-renders.</li>
  </ul>
  <h3>Syntax:</h3>
  <pre><code>
import React, { PureComponent } from 'react';
class MyComponent extends PureComponent {
  render() {
    return &lt;div&gt;{this.props.name}&lt;/div&gt;;
  }
}
  </code></pre>
  <h3>Difference from <code>Component</code>:</h3>
  <ul>
    <li><code>Component</code> always re-renders by default.</li>
    <li><code>PureComponent</code> skips re-render if nothing changed (shallow check).</li>
  </ul>
  <h3>Note:</h3>
  <p>Use PureComponent only when:</p>
  <ul>
    <li>Props and state are <strong>immutable</strong> or <strong>simple objects</strong>.</li>
    <li>You want to boost performance in large lists or complex UIs.</li>
  </ul>
</details>

---

64. **How to improve react application performance?**
<details>
  <summary>Answer</summary>
<h2>🔁 1. Avoid Unnecessary Re-renders</h2>
  <ul>
    <li>Use <code>React.memo</code> for functional components.</li>
    <li>Use <code>PureComponent</code> for class components.</li>
    <li>Use <code>useMemo</code> and <code>useCallback</code> to memoize expensive computations and functions.</li>
  </ul>
  <h2>⚛️ 2. Code Splitting</h2>
  <ul>
    <li>Use <code>React.lazy</code> with <code>Suspense</code> for dynamic imports.</li>
    <li>Implement route-based code splitting with React Router.</li>
  </ul>
  <h2>🧹 3. Optimize State Management</h2>
  <ul>
    <li>Lift state only when needed.</li>
    <li>Use local state instead of global where possible.</li>
    <li>Avoid excessive re-renders from frequent state updates.</li>
  </ul>
  <h2>🧮 4. Virtualize Long Lists</h2>
  <ul>
    <li>Use <a href="https://react-window.vercel.app/" target="_blank">react-window</a> or <code>react-virtualized</code>.</li>
    <li>Only render visible items in large lists.</li>
  </ul>
  <h2>📦 5. Bundle Optimization</h2>
  <ul>
    <li>Use tools like Webpack Bundle Analyzer.</li>
    <li>Remove unused packages and dead code.</li>
    <li>Use tree-shakable libraries (ES modules).</li>
  </ul>

  <h2>🎨 6. Lazy Load Images and Components</h2>
  <ul>
    <li>Use libraries like <code>react-lazyload</code> or native <code>&lt;img loading="lazy" /&gt;</code>.</li>
    <li>Only load components/images when needed.</li>
  </ul>
  <h2>🌐 7. Use CDN and Caching</h2>
  <ul>
    <li>Host static assets (images, fonts) on a CDN.</li>
    <li>Enable proper HTTP caching headers.</li>
  </ul>
  <h2>⚙️ 8. Use Production Build</h2>
  <ul>
    <li>Deploy the <code>npm run build</code> production version for better performance and minification.</li>
  </ul>
  <h2>📉 9. Monitor and Profile</h2>
  <ul>
    <li>Use React DevTools Profiler.</li>
    <li>Use Chrome DevTools Performance tab to find bottlenecks.</li>
  </ul>
  <h2>🚀 10. Avoid Anonymous Functions in JSX</h2>
  <pre><code>// bad
&lt;MyComponent onClick={() =&gt; doSomething()} /&gt;
// good
const handleClick = useCallback(() =&gt; doSomething(), []);
&lt;MyComponent onClick={handleClick} /&gt;
</code></pre>
</details>

---

65. **What are Interceptors?**
<details>
  <summary>Answer</summary>
<p><strong>Interceptors</strong> are functions or classes used in many frameworks (like Angular, Axios in JavaScript, etc.) to <strong>intercept and modify HTTP requests or responses</strong> before they are handled by the application or sent to the server.</p>
  <h3>In simple terms:</h3>
  <p>They <strong>"catch"</strong> the request or response and let you:</p>
  <ul>
    <li>Modify headers</li>
    <li>Add auth tokens</li>
    <li>Handle errors globally</li>
    <li>Log or transform data</li>
  </ul>
  <h3>🧠 Example (Axios - JavaScript):</h3>
  <pre><code>axios.interceptors.request.use((config) =&gt; {
  config.headers.Authorization = `Bearer token`;
  return config;
});
axios.interceptors.response.use(
  (response) =&gt; response,
  (error) =&gt; {
    // Handle error globally
    return Promise.reject(error);
  }
);</code></pre>
  <h3>⚙️ Common Use Cases:</h3>
  <ul>
    <li>Adding authentication tokens</li>
    <li>Logging requests/responses</li>
    <li>Global error handling</li>
    <li>Showing loaders/spinners</li>
  </ul>
</details>

---

66. **What is Tanstack Query?**
<details>
  <summary>Answer</summary>
<p><strong>TanStack Query</strong> (formerly known as React Query) is a powerful data-fetching and state management library for <strong>React</strong>, <strong>Vue</strong>, <strong>Solid</strong>, and <strong>Svelte</strong>. It's mainly used for managing <strong>server state</strong> in frontend apps.</p>
  <h2>Key Features:</h2>
  <ul>
    <li>Fetch, cache, sync, and update server data with ease</li>
    <li>Automatic caching and background refetching</li>
    <li>Pagination & infinite queries</li>
    <li>Mutations (for POST/PUT/DELETE)</li>
    <li>Query invalidation and refetch control</li>
    <li>Devtools support</li>
  </ul>
  <h2>Common Use Case:</h2>
  <pre><code>
import { useQuery } from '@tanstack/react-query';
const fetchUser = async () => {
  const res = await fetch('/api/user');
  return res.json();
};
const Component = () => {
  const { data, isLoading, error } = useQuery({
    queryKey: ['user'],
    queryFn: fetchUser,
  });
  if (isLoading) return 'Loading...';
  if (error) return 'Error!';
  return &lt;div&gt;{data.name}&lt;/div&gt;;
};
  </code></pre>
  <p><strong>In short:</strong> <em>TanStack Query simplifies async data logic</em>, handles loading/error/caching states automatically, and improves UX without writing a lot of boilerplate.</p>
</details>

---

