 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Temperature Converter</title>
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="converter">
            <input type="number" id="celsius" placeholder="Enter Celsius">
            <button id="convert">Convert</button>
            <p id="result"></p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
//css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
}

.container {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

h1 {
    color: #333;
}

.converter {
    margin-top: 20px;
}

input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    padding: 10px 20px;
    background-color: #007bff;
    border: none;
    color: #fff;
    border-radius: 5px;
    cursor: pointer;
}

#result {
    margin-top: 10px;
}
//js
const convertButton = document.getElementById("convert");
const celsiusInput = document.getElementById("celsius");
const resultText = document.getElementById("result");

convertButton.addEventListener("click", () => {
    const celsius = parseFloat(celsiusInput.value);
    if (!isNaN(celsius)) {
        const fahrenheit = (celsius * 9/5) + 32;
        resultText.textContent = `${celsius.toFixed(2)}°C is ${fahrenheit.toFixed(2)}°F`;
    } else {
        resultText.textContent = "Invalid input. Please enter a valid temperature in Celsius.";
    }
});
