# Lab13-

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,
initial-scale=1.0"> <title>Document</title>
</head>
<body>
<h1> STUDENT REG FORM</h1>
<form id="studentForm" onsubmit="return validateMyform()">
Enrollment Number: <br>
<input type="text" id="enrollment"><br><br>
Name: <br>
<input type="text" id="name"><br><br>
Email ID: <br>
<input type="email" id="email"><br><br>
Password: <br>
<input type="password" id="password"><br><br>
Confirm Password: <br>
<input type="password" id="confirmPassword"><br><br>
Phone Number: <br>
<input type="text" id="phone"><br><br>
Address: <br>
<textarea id="address" rows="3" cols="30"></textarea><br><br>
Gender: <br>
<input type="radio" name="gender" value="Male"> Male
<input type="radio" name="gender" value="Female">
Female
<br><br>
Branch: <br>
<select id="branch">
<option value="">--Select Branch--</option>
<option value="Computer Engineering">Computer
Engineering</option> <option value="IT Engineering">IT
Engineering</option>
<option value="Electronics">Electronics</option>
<option value="Mechanical">Mechanical</option>
<option value="Civil">Civil</option>
</select><br><br>
<input type="submit" value="Submit">
</form>
<script>
function validateMyform() {
let enrollment = document.getElementById("enrollment").value;
let name = document.getElementById("name").value;
let email = document.getElementById("email").value;
let password = document.getElementById("password").value;
let confirmPassword = document.getElementById("confirmPassword").value;
let phone = document.getElementById("phone").value;
let address = document.getElementById("address").value;
let gender =
document.querySelector('input[name="gender"]:checked'); let branch
= document.getElementById("branch").value;
if (enrollment === "" || name === "" || email === "" || password === "" || 
confirmPassword === "" || phone === "" || address === "" || !gender || branch === "") {
alert("please fill out all deatils");
return false;
}
emailpattern = /^[a-z]+\.{1}[a-z]+[0-9]{6}@marwadiuniversity\.ac\.in$/
if (!email.match(emailpattern)) {
alert("Invalid email address");
return false;
}
if (password !== confirmPassword) {
alert("password and confirm password not match");
return false;
}
if (password.length < 6 ) {
alert("Password must be at least 6 characters long!");
return false;
}
phonepattern = /^[0-9]{10}$/
if (!phone.match(phonepattern)) {
alert("Invalid phone number");
return false;
}
alert("Form Submitted Successfully!");
return true;
}
</script>
</body>
</html>
Parthil Mehta(92500103043)
