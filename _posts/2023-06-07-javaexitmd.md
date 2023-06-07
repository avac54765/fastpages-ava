---
title: Javascript MD
description: Seeing if I can run this here.
permalink: /java/md
categories: [week 36]
---

<html>
  <head>
    <style>
      input {
        margin-bottom: 10px;
      }
    </style>
  </head>
  <body>
    <h2>Length Unit Converter</h2>
    <label for="metersInput">Meters:</label>
    <input type="number" id="metersInput" step="0.01" />
    <br />
    <label for="feetInput">Feet:</label>
    <input type="number" id="feetInput" step="0.01" />
    <br />
    <button onclick="convertMetersToFeet()">Convert Meters to Feet</button>
    <button onclick="convertFeetToMeters()">Convert Feet to Meters</button>
    <script>
      // Conversion constants
      const METERS_TO_FEET = 3.28084;
      const FEET_TO_METERS = 0.3048;
      // Conversion functions
      function convertMetersToFeet() {
        const metersInput = document.getElementById("metersInput");
        const feetInput = document.getElementById("feetInput");
        const meters = parseFloat(metersInput.value);
        const feet = meters * METERS_TO_FEET;
        feetInput.value = feet.toFixed(2);
      }
      function convertFeetToMeters() {
        const feetInput = document.getElementById("feetInput");
        const metersInput = document.getElementById("metersInput");
        const feet = parseFloat(feetInput.value);
        const meters = feet * FEET_TO_METERS;
        metersInput.value = meters.toFixed(2);
      }
    </script>
  </body>
</html>
