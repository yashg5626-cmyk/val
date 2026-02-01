<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Will you be my Valentine?</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="card">
    <div class="emoji">🐱</div>
    <h1><span id="name">madhuri</span> will you be my valentine?</h1>

    <div class="btns">
      <button id="yes">Yes</button>
      <button id="no">No</button>
    </div>

    <p id="msg"></p>
  </div>

  <script src="script.js"></script>
</body>
</html>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  background:#f7c8d4;
  font-family: Arial, sans-serif;
}

.card{
  background:#fff;
  padding:40px 30px;
  border-radius:18px;
  text-align:center;
  width:380px;
  box-shadow:0 10px 30px rgba(0,0,0,.2);
}

.emoji{
  font-size:60px;
  margin-bottom:10px;
}

h1{
  font-size:26px;
  margin:0 0 25px;
}

.btns{
  position:relative;
  height:80px;
}

button{
  padding:12px 25px;
  border:none;
  border-radius:25px;
  font-size:18px;
  cursor:pointer;
}

#yes{
  background:#ff4d79;
  color:white;
}

#no{
  background:#eee;
  position:absolute;
  left:170px;
  top:0px;
}
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");
const msg = document.getElementById("msg");

noBtn.addEventListener("mouseover", () => {
  const x = Math.random() * 250;
  const y = Math.random() * 40;
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", () => {
  msg.innerHTML = "Yayyy 😍 I love you ❤️";
  msg.style.fontSize = "20px";
});
