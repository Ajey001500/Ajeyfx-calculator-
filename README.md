<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Forex Position Size Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      margin: 0;
      background: #f2f2f2;
    }
    .container {
      background: #fff;
      padding: 20px;
      max-width: 100%;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
    }
    label {
      margin-top: 10px;
      font-weight: bold;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      width: 100%;
      padding: 12px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Forex Position Size Calculator</h2>

    <label>Account Balance ($):</label>
    <input type="number" id="accountBalance" />

    <label>Risk Per Trade (%):</label>
    <input type="number" id="riskPercent" />

    <label>Stop Loss (pips):</label>
    <input type="number" id="stopLossPips" />

    <label>Pip Value per Lot ($):</label>
    <input type="number" id="pipValue" value="10" />

    <button onclick="calculatePositionSize()">Calculate</button>

    <div id="result"></div>
  </div>

  <script>
    function calculatePositionSize() {
      const accountBalance = parseFloat(document.getElementById("accountBalance").value);
      const riskPercent = parseFloat(document.getElementById("riskPercent").value);
      const stopLossPips = parseFloat(document.getElementById("stopLossPips").value);
      const pipValue = parseFloat(document.getElementById("pipValue").value);

      if (isNaN(accountBalance) || isNaN(riskPercent) || isNaN(stopLossPips) || isNaN(pipValue)) {
        document.getElementById("result").innerText = "Please fill out all fields correctly.";
        return;
      }

      const riskAmount = accountBalance * (riskPercent / 100);
      const riskPerLot = stopLossPips * pipValue;
      const positionSize = riskAmount / riskPerLot;

      document.getElementById("result").innerText =
        "Recommended Position Size: " + positionSize.toFixed(2) + " standard lots";
    }
  </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Forex Position Size Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      margin: 0;
      background: #f2f2f2;
    }
    .container {
      background: #fff;
      padding: 20px;
      max-width: 100%;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
    }
    label {
      margin-top: 10px;
      font-weight: bold;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      width: 100%;
      padding: 12px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Forex Position Size Calculator</h2>

    <label>Account Balance ($):</label>
    <input type="number" id="accountBalance" />

    <label>Risk Per Trade (%):</label>
    <input type="number" id="riskPercent" />

    <label>Stop Loss (pips):</label>
    <input type="number" id="stopLossPips" />

    <label>Pip Value per Lot ($):</label>
    <input type="number" id="pipValue" value="10" />

    <button onclick="calculatePositionSize()">Calculate</button>

    <div id="result"></div>
  </div>

  <script>
    function calculatePositionSize() {
      const accountBalance = parseFloat(document.getElementById("accountBalance").value);
      const riskPercent = parseFloat(document.getElementById("riskPercent").value);
      const stopLossPips = parseFloat(document.getElementById("stopLossPips").value);
      const pipValue = parseFloat(document.getElementById("pipValue").value);

      if (isNaN(accountBalance) || isNaN(riskPercent) || isNaN(stopLossPips) || isNaN(pipValue)) {
        document.getElementById("result").innerText = "Please fill out all fields correctly.";
        return;
      }

      const riskAmount = accountBalance * (riskPercent / 100);
      const riskPerLot = stopLossPips * pipValue;
      const positionSize = riskAmount / riskPerLot;

      document.getElementById("result").innerText =
        "Recommended Position Size: " + positionSize.toFixed(2) + " standard lots";
    }
  </script>
</body>
</html># Ajeyfx-calculator-
