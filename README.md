# ODD23-24-WT-JavaScript
# AIM : To create the following programs using javascript
## Objective 1 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electricity Bill Calculator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 20px;
            text-align: center;
        }

        h2 {
            color: #4CAF50;
        }

        form {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 400px;
            margin: auto;
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
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #result {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>

    <h2>Electricity Bill Calculator</h2>

    <form id="electricityForm">
        <label for="units">Enter Units Consumed: (in kwph)</label>
        <input type="number" id="units" name="units" placeholder="Enter units" required>

        <label for="rate">Rate per Unit: (in rupees)</label>
        <input type="number" id="rate" name="rate" placeholder="Enter rate" required>

        <button type="button" onclick="calculateBill()">Calculate Bill</button>

        <label for="result">Electricity Bill:</label>
        <input type="text" id="result" name="result" readonly>
    </form>

    <script>
        function calculateBill() {
            // Get input values
            var units = parseFloat(document.getElementById('units').value);
            var rate = parseFloat(document.getElementById('rate').value);

            // Calculate bill
            var billAmount = units * rate;

            // Display result
            document.getElementById('result').value = billAmount.toFixed(2);
        }
    </script>

</body>
</html>
```
## Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/7f85f2a9-00c9-4761-a7f4-dea3b01bc0c8)

# Objective 2 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Factorial Calculator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 20px;
            text-align: center;
        }

        h2 {
            color: #4CAF50;
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
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #result {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            padding: 8px;
        }
    </style>
</head>
<body>

    <h2>Factorial Calculator</h2>

    <label for="number">Enter a Number:</label>
    <input type="number" id="number" placeholder="Enter a number" required>

    <button type="button" onclick="calculateFactorial()">Calculate Factorial</button>

    <label for="result">Factorial:</label>
    <div id="result"></div>

    <script>
        function calculateFactorial() {
            // Get input value
            var number = parseInt(document.getElementById('number').value);

            // Check if the input is a non-negative integer
            if (Number.isInteger(number) && number >= 0) {
                var factorial = 1;

                // Calculate factorial
                for (var i = 2; i <= number; i++) {
                    factorial *= i;
                }

                // Display result
                document.getElementById('result').innerText = `The factorial of ${number} is: ${factorial}`;
            } else {
                // Display error for invalid input
                document.getElementById('result').innerText = 'Please enter a non-negative integer.';
            }
        }
    </script>

</body>
</html>
```
# Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/f3986977-7b96-4bf4-a1ca-a2c992cbdc27)

# Objective 3 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prime Number Generator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 20px;
            text-align: center;
        }

        h2 {
            color: #4CAF50;
        }

        form {
            background-color: #fff;
            border: 2px solid #3498db; /* Blue border */
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 400px;
            margin: auto;
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
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #result {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            padding: 8px;
            margin-top: 16px;
        }
    </style>
</head>
<body>

    <h2>Prime Number Generator</h2>

    <form id="primeForm">
        <label for="count">Enter the number of primes (N):</label>
        <input type="number" id="count" placeholder="Enter N" required>

        <button type="button" onclick="generatePrimes()">Generate Primes</button>

        <label for="result">Prime Numbers:</label>
        <div id="result"></div>
    </form>

    <script>
        function isPrime(num) {
            for (var i = 2; i < num; i++) {
                if (num % i === 0) {
                    return false;
                }
            }
            return num > 1;
        }

        function generatePrimes() {
            var count = parseInt(document.getElementById('count').value);
            var primeNumbers = [];

            if (count > 0) {
                var num = 2; // Start with the first prime number

                while (primeNumbers.length < count) {
                    if (isPrime(num)) {
                        primeNumbers.push(num);
                    }
                    num++;
                }

                document.getElementById('result').innerText = primeNumbers.join(', ');
            } else {
                document.getElementById('result').innerText = 'Please enter a valid count.';
            }
        }
    </script>

</body>
</html>
```
# Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/275fd43c-db59-40b2-bfb0-5db464c6bb76)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/1bcbdc54-c795-4130-a8d7-601d64ab7e67)


# Objective 4 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #282c35; /* Dark background color */
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        form {
            background-color: #444;
            border: 2px solid #3498db;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            padding: 20px;
            max-width: 400px;
            width: 100%;
            text-align: center;
        }

        h2 {
            color: #3498db; /* Blue color for the heading */
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #fff;
        }

        input, select {
            width: calc(100% - 16px);
            padding: 8px;
            margin-bottom: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: #333; /* Dark input background */
            color: #fff;
        }

        button {
            background-color: #3498db; /* Blue color for the button */
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #2071a8; /* Darker shade of blue on hover */
        }

        #result {
            background-color: #333;
            border: 1px solid #3498db;
            padding: 8px;
            margin-top: 16px;
            font-weight: bold;
            color: #fff;
        }
    </style>
</head>
<body>

    <form id="calculatorForm">
        <h2>Simple Calculator</h2>

        <label for="num1">Enter number 1:</label>
        <input type="number" id="num1" placeholder="Enter number 1" required>

        <label for="operator">Select operator:</label>
        <select id="operator" required>
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>

        <label for="num2">Enter number 2:</label>
        <input type="number" id="num2" placeholder="Enter number 2" required>

        <button type="button" onclick="calculate()">Calculate</button>

        <div id="result"></div>
    </form>

    <script>
        function calculate() {
            var num1 = parseFloat(document.getElementById('num1').value);
            var num2 = parseFloat(document.getElementById('num2').value);
            var operator = document.getElementById('operator').value;

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
                    if (num2 !== 0) {
                        result = num1 / num2;
                    } else {
                        document.getElementById('result').innerText = 'Cannot divide by zero.';
                        return;
                    }
                    break;
                default:
                    document.getElementById('result').innerText = 'Invalid operator.';
                    return;
            }

            document.getElementById('result').innerText = `Result: ${result}`;
        }
    </script>

</body>
</html>
```
# Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/65f3c487-1500-4f4d-8df4-27181db307db)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/bb8be043-d181-4262-9497-21e742873315)

# Objective 5 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Text Editor</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to right, #3498db, #6c5b7b, #bcb8b1);
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        h2 {
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        textarea {
            width: 80%;
            height: 150px;
            padding: 12px;
            margin-bottom: 16px;
            border: 2px solid #3498db;
            border-radius: 8px;
            resize: none;
            font-size: 16px;
            color: #333;
            background-color: #fff;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 8px;
            margin-bottom: 8px; /* Added margin for spacing */
            font-size: 16px;
        }

        #output {
            background-color: #fff;
            border: 2px solid #3498db;
            padding: 12px;
            text-align: left;
            border-radius: 8px;
            width: 80%;
            font-size: 16px;
            color: #333;
        }
    </style>
</head>
<body>

    <h2>Simple Text Editor</h2>

    <textarea id="inputText" placeholder="Type your text here..."></textarea>

    <div>
        <button onclick="capitalizeText()">Capitalize</button>
        <button onclick="makeUppercase()">Uppercase</button>
        <button onclick="makeLowercase()">Lowercase</button>
        <button onclick="reverseText()">Reverse</button>
        <button onclick="clearText()">Clear</button>
    </div>

    <div id="output"></div>

    <script>
        function capitalizeText() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            var capitalizedText = inputText.replace(/\b\w/g, function (char) {
                return char.toUpperCase();
            });

            outputDiv.innerText = capitalizedText;
        }

        function makeUppercase() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.toUpperCase();
        }

        function makeLowercase() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.toLowerCase();
        }

        function reverseText() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.split('').reverse().join('');
        }

        function clearText() {
            document.getElementById('inputText').value = '';
            document.getElementById('output').innerText = '';
        }
    </script>

</body>
</html>
```
# Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/49b130a8-dc60-4d72-a3a2-b5a6d5673c96)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/8658f197-7f2d-4ee2-a72b-bcdd0cd35250)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/38e4bb2e-8ede-4ec6-ae3d-93cd4cb24d98)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/99c21685-2231-4f74-85c9-8c9eb8036563)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/ff1bc5b2-4cf3-4cf4-aed4-0cdbd7f27494)
# Objective 6 :
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
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to right, #3498db, #1abc9c);
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        h2 {
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
        }

        form {
            width: 80%;
            max-width: 400px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
        }

        input {
            width: calc(100% - 16px);
            padding: 12px;
            margin-bottom: 16px;
            border: 2px solid #3498db;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 16px;
            color: #333;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049;
        }

        .error-message {
            color: red;
            margin-top: -8px;
            margin-bottom: 16px;
            text-align: left;
        }
    </style>
</head>
<body>

    <h2>Form Validation</h2>

    <form id="myForm" onsubmit="validateForm(); return false;">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name">
        <div id="nameError" class="error-message"></div>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email">
        <div id="emailError" class="error-message"></div>

        <button type="submit">Submit</button>
    </form>

    <script>
        function validateForm() {
            // Reset error messages
            document.getElementById('nameError').innerText = '';
            document.getElementById('emailError').innerText = '';

            // Get form values
            var name = document.getElementById('name').value;
            var email = document.getElementById('email').value;

            // Validate name
            if (name.trim() === '') {
                document.getElementById('nameError').innerText = 'Name is required.';
            }

            // Validate email
            if (email.trim() === '') {
                document.getElementById('emailError').innerText = 'Email is required.';
            } else if (!isValidEmail(email)) {
                document.getElementById('emailError').innerText = 'Invalid email format.';
            }
        }

        function isValidEmail(email) {
            // Basic email validation regex
            var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailRegex.test(email);
        }
    </script>

</body>
</html>
```
# Output :
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/4266f4c4-dfa9-4f62-90e7-8e0cd89cd26e)
<br>
<br>
![image](https://github.com/SANTHAN-2006/ODD23-24-WT-JavaScript/assets/80164014/ae0b8c9f-37ed-47b8-8790-b7cc38d98903)
