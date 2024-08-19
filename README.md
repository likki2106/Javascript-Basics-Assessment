# Javascript-Basics-Assessment
#Simple Calculator

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Array Sum</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            max-width: 300px;
            margin: 0 auto;
        }
        input, button {
            margin: 5px 0;
            padding: 10px;
            font-size: 16px;
            width: 100%;
            box-sizing: border-box;
        }
        .result {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Sum of Even Numbers</h2>
        <input type="text" id="arrayInput" placeholder="Enter numbers separated by commas">
        <button onclick="calculateSum()">Calculate Sum</button>
        <div class="result" id="sumResult"></div>
    </div>

    <script>
        function calculateSum() {
            const arrayInput = document.getElementById('arrayInput').value;
            const numbers = arrayInput.split(',').map(Number);
            let sum = 0;

            for (let i = 0; i < numbers.length; i++) {
                if (numbers[i] % 2 === 0) {
                    sum += numbers[i];
                }
            }

            document.getElementById('sumResult').innerText = `Sum of even numbers: ${sum}`;
        }
    </script>
</body>
</html>


#Sum of even numbers

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Object Manipulation with User Input</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
        }
        input, button {
            margin: 5px 0;
            padding: 10px;
            font-size: 16px;
            width: 100%;
            box-sizing: border-box;
        }
        .result {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Person Object</h2>
        <input type="text" id="firstNameInput" placeholder="Enter first name">
        <input type="text" id="lastNameInput" placeholder="Enter last name">
        <input type="number" id="ageInput" placeholder="Enter age">
        <button onclick="createPerson()">Create Person</button>
        <button onclick="showPersonInfo()">Show Person Info</button>
        <button onclick="incrementAge()">Increment Age</button>
        <div class="result" id="personResult"></div>
    </div>

    <script>
        let Person = null; // Initialize Person as null

        function createPerson() {
            const firstName = document.getElementById('firstNameInput').value;
            const lastName = document.getElementById('lastNameInput').value;
            const age = parseInt(document.getElementById('ageInput').value, 10);

            if (firstName && lastName && !isNaN(age)) {
                Person = {
                    firstName: firstName,
                    lastName: lastName,
                    age: age,
                    getFullName: function() {
                        return `${this.firstName} ${this.lastName}`;
                    },
                    incrementAge: function() {
                        this.age += 1;
                    }
                };
                document.getElementById('personResult').innerText = `Person created: ${Person.getFullName()}, Age: ${Person.age}`;
            } else {
                document.getElementById('personResult').innerText = 'Error: Please provide valid inputs for all fields.';
            }
        }

        function showPersonInfo() {
            if (Person) {
                document.getElementById('personResult').innerText = `Full Name: ${Person.getFullName()}, Age: ${Person.age}`;
            } else {
                document.getElementById('personResult').innerText = 'Error: Person object not created yet.';
            }
        }

        function incrementAge() {
            if (Person) {
                Person.incrementAge();
                showPersonInfo();
            } else {
                document.getElementById('personResult').innerText = 'Error: Person object not created yet.';
            }
        }
    </script>
</body>
</html>


#Person object

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Object Manipulation with User Input</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
        }
        input, button {
            margin: 5px 0;
            padding: 10px;
            font-size: 16px;
            width: 100%;
            box-sizing: border-box;
        }
        .result {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Person Object</h2>
        <input type="text" id="firstNameInput" placeholder="Enter first name">
        <input type="text" id="lastNameInput" placeholder="Enter last name">
        <input type="number" id="ageInput" placeholder="Enter age">
        <button onclick="createPerson()">Create Person</button>
        <button onclick="showPersonInfo()">Show Person Info</button>
        <button onclick="incrementAge()">Increment Age</button>
        <div class="result" id="personResult"></div>
    </div>

    <script>
        let Person = null; // Initialize Person as null

        function createPerson() {
            const firstName = document.getElementById('firstNameInput').value;
            const lastName = document.getElementById('lastNameInput').value;
            const age = parseInt(document.getElementById('ageInput').value, 10);

            if (firstName && lastName && !isNaN(age)) {
                Person = {
                    firstName: firstName,
                    lastName: lastName,
                    age: age,
                    getFullName: function() {
                        return `${this.firstName} ${this.lastName}`;
                    },
                    incrementAge: function() {
                        this.age += 1;
                    }
                };
                document.getElementById('personResult').innerText = `Person created: ${Person.getFullName()}, Age: ${Person.age}`;
            } else {
                document.getElementById('personResult').innerText = 'Error: Please provide valid inputs for all fields.';
            }
        }

        function showPersonInfo() {
            if (Person) {
                document.getElementById('personResult').innerText = `Full Name: ${Person.getFullName()}, Age: ${Person.age}`;
            } else {
                document.getElementById('personResult').innerText = 'Error: Person object not created yet.';
            }
        }

        function incrementAge() {
            if (Person) {
                Person.incrementAge();
                showPersonInfo();
            } else {
                document.getElementById('personResult').innerText = 'Error: Person object not created yet.';
            }
        }
    </script>
</body>
</html>
