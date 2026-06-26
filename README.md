<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<title>Grow a Smurf</title>

<style>
body{
    background:#6cc8ff;
    text-align:center;
    font-family:Arial;
}

h1{
    color:white;
}

#smurf{
    font-size:120px;
    cursor:pointer;
    transition:.1s;
    user-select:none;
}

#smurf:active{
    transform:scale(1.1);
}

button{
    padding:12px 25px;
    font-size:20px;
    margin-top:20px;
    border:none;
    border-radius:10px;
    cursor:pointer;
}
</style>

</head>
<body>

<h1>Grow a Smurf</h1>

<h2>💰 돈 : <span id="money">0</span></h2>
<h2>📏 키 : <span id="height">1</span> cm</h2>

<div id="smurf">🔵</div>

<button onclick="sell()">스머프 팔기</button>

<script>

let money=0;
let height=1;

const moneyText=document.getElementById("money");
const heightText=document.getElementById("height");
const smurf=document.getElementById("smurf");

smurf.onclick=function(){

height++;

heightText.innerText=height;

let size=120+height/2;

if(size>300) size=300;

smurf.style.fontSize=size+"px";

}

function sell(){

money+=height;

moneyText.innerText=money;

height=1;

heightText.innerText=1;

smurf.style.fontSize="120px";

}

</script>

</body>
</html># -