<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            font-weight: bolder;
            background: linear-gradient(to right, rgba(238, 130, 238, 0.388), rgba(0, 0, 255, 0.418));
            margin-top: 50px;
            align-items: center;
            font-family: Arial, sans-serif;
        }
        #input{
            text-align: center;
            display: inline;
            margin-left: 470px;
            background-color: rgb(235, 233, 233);
            height: 90px;
            width:370px;
            font-size: 50px;
            text-align: right;
        }
        button{
            width: 90px;
            height: 90px;
            margin: 2px;
            font-size: 50px;
        }
        button:hover {
            transform: scale(1.05);
            cursor: pointer;
        }
        main div{
            display: flex;
            flex-basis: auto auto auto auto;
        }
        main{
            margin-left: 470px;
        }
        div button:nth-child(1){
            background-color:rgb(196, 139, 245)  ;
        }
        div button:nth-child(2){
            background-color:rgb(196, 139, 245)  ;
        }
        div button:nth-child(3){
            background-color:rgb(196, 139, 245) ;
        }
        div button:nth-child(4){
            background-color:rgba(255, 166, 0, 0.931) ;
        }
        #equ{
            background-color: rgba(0, 128, 87, 0.876);
            width:370px;
        }
</style>
</head>
<body>
    <input id="input" readonly>
    <br><br>
    <main>
        <div>
        <button onclick="press('7')">7</button>
        <button onclick="press('8')">8</button>
        <button onclick="press('9')">9</button> 
        <button onclick="press('+')">+</button>
        </div>
        <div>
        <button onclick="press('4')">4</button>
        <button onclick="press('5')">5</button>
        <button onclick="press('6')">6</button>
        <button onclick="press('-')">-</button>
        </div>
        <div>
        <button onclick="press('1')">1</button>
        <button onclick="press('2')">2</button>
        <button onclick="press('3')">3</button>
        <button onclick="press('*')">*</button>
        </div>
        <div>
        <button onclick="press('0')">0</button>
        <button onclick="press('.')">.</button>
        <button style="background-color: rgba(255, 0, 0, 0.432);" onclick="clears()">C</button>
        <button onclick="press('/')">÷</button>
        </div>
        <button id="equ" onclick="equals()">=</button>
</main>
<script>
    function press(val){
        document.getElementById("input").value+=val
    }
    function equals(){
    try{
        let inputVal = document.getElementById("input").value;
        let result = eval(inputVal);
        document.getElementById("input").value = result;
    }
    catch{
        document.getElementById("input").value = "error";
        document.getElementById("description").innerText = "Invalid input. Please try again.";
    }
    }
    function clears(){
        document.getElementById("input").value=""
    }
</script>
</body>
</html>
