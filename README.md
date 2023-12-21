# ODD23-24-WT-JavaScript
# AIM : To create the following programs using javascript
## Objective 1 :
# Aim :
To Create a form with java script code to calculate electricity bill.
### Procedure :
#### Step 1 :
Create an HTML File:

Open a text editor (e.g., Notepad, VS Code) and copy the provided HTML code.
Paste the code into the text editor.
Save the file with a ".html" extension, such as "electricity_bill.html".
#### Step 2 :
Save and Store:

Save the file in a location where you can easily access it.
#### Step 3 :
Open in Web Browser:

Double-click on the saved HTML file. This will open the Electricity Bill Calculator in your default web browser.
#### Step 4 :
Integration (Optional)

If desired, you can customize the HTML or CSS further based on your project requirements.
Integrate the code into your project by copying and pasting the relevant sections.
## Code :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Electricity Bill Calculator</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
    }
    h1 {
      text-align: center;
      color: #333;
      margin-bottom: 20px;
      padding: 20px 0;
      background-color: #0d0dd2;
      color: #fff;
      margin: 0;
    }
    form {
      padding: 20px;
    }
    label {
      display: block;
      margin-bottom: 8px;
      color: #555;
    }
    input {
      width: calc(100% - 16px);
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: 100%;
      box-sizing: border-box;
    }
    button:hover {
      background-color: #2828e7;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      text-align: center;
      color: #0f09c1;
    }
  </style>
</head>
<body>

  <div id="container">
    <h1>Electricity Bill Calculator</h1>
    <form id="electricityForm">
      <label for="units">Enter Units Consumed (in kwph):</label>
      <input type="number" id="units" name="units" required>

      <label for="rate">Rate per Unit (in rupees):</label>
      <input type="number" id="rate" name="rate" step="0.01" required>

      <button type="button" onclick="calculateBill()">Calculate Bill</button>
    </form>
    <div id="result"></div>
  </div>
  <script>
    function calculateBill() {
      // Get input values
      var units = parseFloat(document.getElementById("units").value);
      var rate = parseFloat(document.getElementById("rate").value);
      // Validate input
      if (isNaN(units) || isNaN(rate)) {
        alert("Please enter valid numbers for units and rate.");
        return;
      }
      // Calculate total bill
      var totalBill = units * rate;
      // Display result
      var resultElement = document.getElementById("result");
      resultElement.textContent = "Total Bill: ₹" + totalBill.toFixed(2);
    }
  </script>
</body>
</html>
```
## Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/fb7bb721-5d46-4460-bde3-fc11dd5305f3)


# Objective 2 :
# Aim :
To Develop a JavaScript program to compute the factorial of a given number without recursion.
# Procedure :
## Step 1 :
Create an HTML File:

Open a text editor (e.g., Notepad, VS Code) and copy the provided HTML code.
Paste the code into the text editor.
Save the file with a ".html" extension, such as "factorial_calculator.html".
## Step 2 :
Save and Store:

Save the file in a location where you can easily access it.
## Step 3 :
Open in Web Browser:

Double-click on the saved HTML file. This will open the Factorial Calculator in your default web browser.
## Step 4 :
Enter a Number:

In the opened web page, you will see an input field labeled "Enter a Number".
Type a non-negative integer into the input field.
## Step 5 :
Calculate Factorial:

Click the "Calculate Factorial" button.
The factorial of the entered number will be displayed below the button.
## Step 6 :
Error Handling:

If an invalid input (e.g., not a non-negative integer) is entered, an error message will be displayed.

# Code :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Factorial Calculator</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to right, #1abc9c, #3498db); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      padding: 20px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #333;
    }

    input {
      width: calc(100% - 16px);
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: calc(100% - 16px);
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #0f09c1;
    }
  </style>
  <script>
    function calculateFactorial() {
      // Get the input value
      var number = parseInt(document.getElementById("number").value);

      // Validate input
      if (isNaN(number) || number < 0) {
        alert("Please enter a non-negative integer.");
        return;
      }

      // Calculate factorial using a loop
      var factorial = 1;
      for (var i = 2; i <= number; i++) {
        factorial *= i;
      }

      // Display the result
      var resultElement = document.getElementById("result");
      resultElement.textContent = "Factorial of " + number + " is: " + factorial;
    }
  </script>
</head>
<body>

  <div id="container">
    <h1>Factorial Calculator</h1>
    <label for="number">Enter a non-negative integer:</label>
    <input type="number" id="number" required>
    <button type="button" onclick="calculateFactorial()">Calculate Factorial</button>
    <div id="result"></div>
  </div>

</body>
</html>
```
# Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/db6c004a-ace9-4cd0-a604-2a0a95540464)


# Objective 3 :
# Aim :
To Construct a JavaScript code to generate ‘N’ prime numbers.

# Procedure :
## Step 1 :
Create an HTML File:

Open a text editor (e.g., Notepad, VS Code) and copy the provided HTML code.
Paste the code into the text editor.
Save the file with a ".html" extension, such as "prime_number_generator.html".
## Step 2 :
Save and Store:

Save the file in a location where you can easily access it.
## Step 3 :
Open in Web Browser:

Double-click on the saved HTML file. This will open the Prime Number Generator in your default web browser.
## Step 4 :
Enter the Number of Primes (N):

In the opened web page, you will see a form labeled "Enter the number of primes (N)" with an input field.
Type a positive integer into the input field.
## Step 5 :
Generate Primes:

Click the "Generate Primes" button.
The first 'N' prime numbers will be displayed below the button.
## Step 6 :
Error Handling:

If an invalid input (e.g., not a positive integer) is entered, an error message will be displayed.

# Code : 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prime Number Generator</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #ffcccc, #ff9999); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      padding: 20px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #333;
    }

    input {
      width: calc(100% - 16px);
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: calc(100% - 16px);
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #0f09c1;
    }
  </style>
  <script>
    function generatePrimes() {
      var count = parseInt(document.getElementById("count").value);

      if (isNaN(count) || count <= 0) {
        alert("Please enter a positive integer.");
        return;
      }

      var primes = [];
      var num = 2;

      while (primes.length < count) {
        if (isPrime(num)) {
          primes.push(num);
        }
        num++;
      }

      var resultElement = document.getElementById("result");
      resultElement.textContent = "First " + count + " prime numbers: " + primes.join(", ");
    }

    function isPrime(num) {
      for (var i = 2; i < num; i++) {
        if (num % i === 0) {
          return false;
        }
      }
      return num > 1;
    }
  </script>
</head>
<body>

  <div id="container">
    <h1>Prime Number Generator</h1>
    <label for="count">Enter the count of prime numbers:</label>
    <input type="number" id="count" required>
    <button type="button" onclick="generatePrimes()">Generate Primes</button>
    <div id="result"></div>
  </div>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prime Number Generator</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #54d811, #ff9999); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      padding: 20px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #333;
    }

    input {
      width: calc(100% - 16px);
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: calc(100% - 16px);
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #0f09c1;
    }
  </style>
  <script>
    function generatePrimes() {
      var count = parseInt(document.getElementById("count").value);

      if (isNaN(count) || count <= 0) {
        alert("Please enter a positive integer.");
        return;
      }

      var primes = [];
      var num = 2;

      while (primes.length < count) {
        if (isPrime(num)) {
          primes.push(num);
        }
        num++;
      }

      var resultElement = document.getElementById("result");
      resultElement.textContent = "First " + count + " prime numbers: " + primes.join(", ");
    }

    function isPrime(num) {
      for (var i = 2; i < num; i++) {
        if (num % i === 0) {
          return false;
        }
      }
      return num > 1;
    }
  </script>
</head>
</html>
```
# Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/a6d8df12-6148-4eb2-b91b-cb4b1f06095e)

# Objective 4 :
# Aim :
To Construct a JavaScript program to implement a simple calculator.

# Procedure :
## Step 1 :
Create an HTML File:

Open a text editor (e.g., Notepad, VS Code) and copy the provided HTML code for the Simple Calculator.
Paste the code into the text editor.
Save the file with a ".html" extension, such as "simple_calculator.html".
## Step 2 :
Save and Store:

Save the file in a location where you can easily access it.
## Step 3 :
Open in Web Browser:

Double-click on the saved HTML file. This will open the Simple Calculator in your default web browser.
## Step 4 :
Enter Numbers and Operator:

In the opened web page, you will see input fields for two numbers and a dropdown to select an operator (+, -, *, /).
Enter numeric values in the input fields and select an operator.
## Step 5 :
Perform Calculation:

Click the "Calculate" button.
The result of the calculation will be displayed below the button.
## Step 6 :
Error Handling:

If an invalid input (e.g., non-numeric values) or division by zero occurs, an error message will be displayed.
# Code :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #ef11e1, #4860e6); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
      padding: 20px 0;
      background-color: #f2f2f2;
    }

    input {
      width: calc(100% - 16px);
      padding: 10px;
      margin: 10px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 18px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: calc(50% - 16px);
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #0f09c1;
      font-size: 20px;
    }
  </style>
  <script>
    function calculate() {
      var num1 = parseFloat(document.getElementById("num1").value);
      var num2 = parseFloat(document.getElementById("num2").value);
      var operator = document.getElementById("operator").value;

      if (isNaN(num1) || isNaN(num2)) {
        alert("Please enter valid numbers.");
        return;
      }

      var result;
      switch (operator) {
        case '+':
          result = num1 + num2;
          break;
        case '-':
          result = num1 - num2;
          break;
        case '*':
          result = num1 * num2;
          break;
        case '/':
          if (num2 === 0) {
            alert("Cannot divide by zero.");
            return;
          }
          result = num1 / num2;
          break;
        default:
          alert("Invalid operator.");
          return;
      }

      document.getElementById("result").textContent = "Result: " + result;
    }
  </script>
</head>
<body>
  <div id="container">
    <h1>Simple Calculator</h1>
    <input type="number" id="num1" placeholder="Enter number" required>
    <select id="operator">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
    <input type="number" id="num2" placeholder="Enter number" required>
    <button type="button" onclick="calculate()">Calculate</button>
    <div id="result"></div>
  </div>
</body>
</html>
```
# Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/3c7351c9-47fd-4e8d-b738-aa80d9d27452)

# Objective 5 :
# Aim :
To Design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

# Procedure :
## Step 1 :
Create an HTML File:

Open a text editor (e.g., Notepad, VS Code) and copy the provided HTML code for the Simple Text Editor.
Paste the code into the text editor.
Save the file with a ".html" extension, such as "simple_text_editor.html".
## Step 2 :
Save and Store:

Save the file in a location where you can easily access it.
## Step 3 :
Open in Web Browser:

Double-click on the saved HTML file. This will open the Simple Text Editor in your default web browser.
## Step 4 :
Type Text:

In the opened web page, you will see a textarea where you can type or paste text.
## Step 5 :
Text Operations:

Click on the provided buttons (Capitalize, Uppercase, Lowercase, Reverse, Clear) to perform different text operations.
## Step 6 :
View Result:

The result of the text operation will be displayed in a separate div on the page.
# Code :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Text Editor</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #ffcccc, #ff9999); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 400px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
      padding: 20px 0;
      background-color: #f2f2f2;
    }

    textarea {
      width: calc(100% - 20px);
      padding: 10px;
      margin: 10px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 16px;
      height: 150px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      margin: 10px;
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #0f09c1;
      font-size: 16px;
    }
  </style>
  <script>
    function capitalizeText() {
      var input = document.getElementById("textArea");
      input.value = input.value.toUpperCase();
    }

    function toLowerCase() {
      var input = document.getElementById("textArea");
      input.value = input.value.toLowerCase();
    }

    function alternateCase() {
      var input = document.getElementById("textArea");
      var result = "";
      for (var i = 0; i < input.value.length; i++) {
        result += i % 2 === 0 ? input.value[i].toUpperCase() : input.value[i].toLowerCase();
      }
      input.value = result;
    }

    function reverseText() {
      var input = document.getElementById("textArea");
      input.value = input.value.split('').reverse().join('');
    }

    function clearText() {
      document.getElementById("textArea").value = '';
    }

    function countCharacters() {
      var input = document.getElementById("textArea");
      var count = input.value.length;
      document.getElementById("result").textContent = "Character Count: " + count;
    }
  </script>
</head>
<body>

  <div id="container">
    <h1>Simple Text Editor</h1>
    <textarea id="textArea" placeholder="Enter text..."></textarea>
    <br>
    <button onclick="capitalizeText()">Capitalize</button>
    <button onclick="toLowerCase()">Lowercase</button>
    <button onclick="alternateCase()">Alternate Case</button>
    <button onclick="reverseText()">Reverse</button>
    <button onclick="clearText()">Clear</button>
    <br>
    <button onclick="countCharacters()">Count Characters</button>
    <div id="result"></div>
  </div>

</body>
</html>

```
# Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/abcd114f-5968-467d-bdea-8c36654da044)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/2d408fd4-b9a8-436f-ad86-6beef7849cbe)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/4a4cbfe7-c0d2-49ca-a658-616ef78d1161)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/c45c5d8d-4948-490c-bd3b-803f4e7118d0)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/1980699a-ecee-4f8a-beb0-6a74c2d64e94)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/d0e2a52d-0a3a-4a42-a1b5-2b8d57950825)

# Objective 6 :
# Aim :
To Design a JavaScript program which displays error messages when a field in form is entered incorrectly.
# Procedure :
## Step 1 :
HTML Structure:

Start with a well-structured HTML file containing form elements like <form>, <input>, and <button>.
## Step 2 :
JavaScript Validation:

Write JavaScript functions to validate form inputs. Include checks for required fields, email format, or any custom validation.
## Step 3 :
CSS Styling (Optional):

Enhance the form's visual appeal by applying CSS styles. Customize colors, fonts, and layouts to create an attractive user interface.
## Step 4 :
Testing and Debugging:

Test the form by entering values and submitting. Debug any issues with the validation logic or styling.
## Step 5 :
Refinement and Deployment:

Iterate on the code, refining validation, styling, and functionality as needed.
Deploy the form on a web server or integrate it into your project.
# Code :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Form with JavaScript Validation</title>
  <style>
    body {
      font-family: 'Verdana', sans-serif;
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #ee0c0c, #2fddf1); /* Adjust colors as needed */
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #container {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      text-align: center;
    }

    h1 {
      color: #0d0dd2;
      margin-bottom: 20px;
      padding: 20px 0;
      background-color: #f2f2f2;
    }

    form {
      padding: 20px;
      box-sizing: border-box;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #333;
    }

    input {
      width: calc(100% - 16px);
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #079020;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      width: 100%;
      box-sizing: border-box;
    }

    button:hover {
      background-color: #2828e7;
    }

    .error {
      color: red;
      margin-top: -10px;
      margin-bottom: 10px;
    }
  </style>
  <script>
    function validateForm() {
      var name = document.getElementById("name").value;
      var email = document.getElementById("email").value;

      var nameError = document.getElementById("nameError");
      var emailError = document.getElementById("emailError");

      nameError.textContent = "";
      emailError.textContent = "";

      var isValid = true;

      if (name.trim() === "") {
        nameError.textContent = "Name is required";
        isValid = false;
      }

      if (email.trim() === "") {
        emailError.textContent = "Email is required";
        isValid = false;
      } else if (!isValidEmail(email)) {
        emailError.textContent = "Invalid email format";
        isValid = false;
      }

      return isValid;
    }

    function isValidEmail(email) {
      // Basic email validation, you can enhance it as needed
      var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return emailRegex.test(email);
    }
  </script>
</head>
<body>
  <div id="container">
    <h1>Form with JavaScript Validation</h1>
    <form onsubmit="return validateForm()">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>
      <div class="error" id="nameError"></div>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>
      <div class="error" id="emailError"></div>

      <button type="submit">Submit</button>
    </form>
  </div>
</body>
</html>
```
# Output :
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/6066d002-8b53-42f8-8326-13a82d57176a)
<br>
<br>
![image](https://github.com/Madhavareddy09/ODD23-24-WT-JavaScript/assets/145742470/99e65662-8cbf-49fd-99eb-f49ab45a31e3)

