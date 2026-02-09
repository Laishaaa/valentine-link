<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You, With Love 💖</title>
<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #fbc2eb, #a6c1ee);
  text-align: center;
  color: #7a003c;
}
.container {
  margin-top: 80px;
}
input {
  padding: 12px;
  width: 260px;
  border-radius: 10px;
  border: none;
  margin: 10px;
  font-size: 16px;
}
button {
  padding: 12px 25px;
  border-radius: 25px;
  border: none;
  background: #ff4d6d;
  color: white;
  font-size: 16px;
  cursor: pointer;
}
.envelope {
  width: 260px;
  height: 160px;
  background: #ff6f91;
  margin: 40px auto;
  border-radius: 10px;
  display: none;
}
.message {
  display: none;
  background: white;
  padding: 25px;
  border-radius: 15px;
  margin: 20px auto;
  width: 300px;
  color: #ff4d6d;
}
</style>
</head>

<body>

<div class="container" id="form">
  <h1>Generate Your Valentine Message 💘</h1>
  <input id="toName" placeholder="Her / His Name"><br>
  <input id="fromName" placeholder="Your Name"><br>
  <button onclick="generate()">Generate 💝</button>
</div>

<div class="envelope" id="envelope" onclick="openMsg()"></div>

<div class="message" id="msg"></div>

<script>
function generate() {
  const to = document.getElementById("toName").value;
  const from = document.getElementById("fromName").value;
  if (!to || !from) {
    alert("Please enter both names ❤️");
    return;
  }
  document.getElementById("form").style.display = "none";
  document.getElementById("envelope").style.display = "block";
  document.getElementById("msg").innerHTML =
    "Dear " + to + " 💖<br><br>" +
    "You are the reason my heart smiles every day.<br>" +
    "Happy Valentine’s Day! 💌<br><br>" +
    "With love,<br>" + from + " ❤️";
}

function openMsg() {
  document.getElementById("envelope").style.display = "none";
  document.getElementById("msg").style.display = "block";
}
</script>

</body>
</html>
