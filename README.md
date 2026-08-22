# simple_calci
# Ex04 Simple Calculator - React Project
## Date: 22.8.26

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
css
```
body{
background:#f4f4f4;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
font-family:Arial;
}

.calculator{
background:white;
padding:25px;
border-radius:10px;
box-shadow:0 5px 15px rgba(0,0,0,0.2);
text-align:center;
width:260px;
}

.display{
width:100%;
height:40px;
margin-bottom:15px;
font-size:18px;
text-align:right;
padding:5px;
}

.buttons{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:10px;
}

button{
padding:12px;
font-size:16px;
border:none;
background:#007bff;
color:white;
cursor:pointer;
border-radius:5px;
}

button:hover{
background:#0056b3;
}
```

js
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {

  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearDisplay = () => {
    setInput("");
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">

      <h2>Simple Calculator</h2>

      <input type="text" value={input} readOnly className="display" />

      <div className="buttons">

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("/")}>/</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("*")}>*</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={clearDisplay}>C</button>
        <button onClick={calculateResult}>=</button>
        <button onClick={() => handleClick("+")}>+</button>

      </div>

    </div>
  );
}

export default Calculator;
```
## OUTPUT

<img width="1234" height="778" alt="Screenshot 2026-08-22 105951" src="https://github.com/user-attachments/assets/aa849a2e-64cb-41dc-b573-034679ca57e3" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
