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

