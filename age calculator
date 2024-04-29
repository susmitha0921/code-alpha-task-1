<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Age Calculator</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
    }
    input[type="number"] {
        width: 50px;
    }
</style>
</head>
<body>
<h1>Age Calculator</h1>
<form id="ageCalculatorForm">
    <label for="dobDay">Day:</label>
    <input type="number" id="dobDay" min="1" max="31" required>
    <label for="dobMonth">Month:</label>
    <input type="number" id="dobMonth" min="1" max="12" required>
    <label for="dobYear">Year:</label>
    <input type="number" id="dobYear" min="1900" max="2024" required>
    <button type="submit">Calculate Age</button>
</form>
<div id="ageResult"></div>
<script>
document.getElementById("ageCalculatorForm").addEventListener("submit", function(event) {
    event.preventDefault();
    var dobDay = parseInt(document.getElementById("dobDay").value);
    var dobMonth = parseInt(document.getElementById("dobMonth").value);
    var dobYear = parseInt(document.getElementById("dobYear").value);

    var dob = new Date(dobYear, dobMonth - 1, dobDay); // month is 0-based

    var today = new Date();
    var age = today.getFullYear() - dob.getFullYear();
    var monthDiff = today.getMonth() - dob.getMonth();
    if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < dob.getDate())) {
        age--;
    }

    document.getElementById("ageResult").innerText = "You are " + age + " years old.";
});
</script>
</body>
</html>
