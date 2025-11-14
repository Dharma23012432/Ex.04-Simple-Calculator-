# Ex04 Simple Calculator - React Project

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Calculator</title>
    <link href="style.css" rel="stylesheet" />
  </head>
  <body>
    <div class="calculator">

      <input id="display" type="text" disabled/><br />
    
    <div class="btn">
<button onclick="appendValue('1')">1</button>
<button onclick="appendValue('2')">2</button>
<button onclick="appendValue('3')">3</button>
<button onclick="appendValue('+')">+</button>

<button onclick="appendValue('4')">4</button>
<button onclick="appendValue('5')">5</button>
<button onclick="appendValue('6')">6</button>
<button onclick="appendValue('-')">-</button>

<button onclick="appendValue('7')">7</button>
<button onclick="appendValue('8')">8</button>
<button onclick="appendValue('9')">9</button>
<button onclick="appendValue('*')">*</button>

<button onclick="appendValue('.')">.</button>
<button onclick="appendValue('0')">0</button>
<button onclick="clearDisplay()">C</button>
<button onclick="appendValue('/')">/</button>
<button onclick="calculateResult('=')">=</button>
    </div>
    </div>
        <script src="script.js"></script>

  </body>
</html>
```
style.css
```
body{
    margin: 0;
    padding: 0;
    justify-content: center;
    align-items: center;
    display: flex;
    min-height: 100vh;
    background-color: aqua;
}
#display{
     width: 100%;
  height: 50px;
  font-size: 24px;
  margin-bottom: 10px;
  padding: 30px;
  text-align: right;
  border: 2px solid #000000;
  border-radius: 20px;
  box-sizing: border-box;
  background-color: white;
  
}
.calculator{
    padding: 20px;
    border: 2px solid rgb(12, 9, 9);
    border-radius: 30px;
    background: linear-gradient(to top,violet,green);
    box-shadow: 10px 10px 15px rgba(113, 2, 2, 0.6);
}    

.btn{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 10px;
}
button{
    padding: 25px;
    border-radius: 30px;
    background-color: rgb(255, 150, 0);
    font-weight: bold;
    font-size: large;
    cursor: pointer;
    transition: 0.2s;
    border: none;
}
button:hover{
    background-color: rgb(53, 52, 13);
}
.Operator{
    background-color: rgb(36, 35, 35);
    color: white;
    font-size: 100%;
}
.Operator:hover{
    background-color: rgb(67, 66, 66);
}

```
script.js
```
function appendValue(value) {
  document.getElementById("display").value += value;
}

function clearDisplay() {
  document.getElementById("display").value = "";
}

function deleteLast() {
  let current = document.getElementById("display").value;
  document.getElementById("display").value = current.slice(0, -1);
}

function calculateResult() {
  try {
    let result = eval(document.getElementById("display").value);
    document.getElementById("display").value = result;
  } catch {
    document.getElementById("display").value = "Error";
  }
}

```

## OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0d059c60-2bef-489d-a874-b51052002977" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
