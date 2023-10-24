# JavaScript-Series
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="styles.css">
  <style>
    *{
    padding: 0;
    margin: 0;
}
.calculator{
    display: flex;
    /* align-items: center; */
    margin-top: 8%;
    justify-content: space-around;
}
.calculator-border{
    border: none;
    height: auto;
    
    padding: 15px;
    
}
.white{
    background-color: rgb(247, 242, 242);
    box-shadow: 1px 1px 5px 3px rgb(151, 135, 135);

}
.black{
    background-color: black;
    /* float: right; */
}
.calculator-content{
    margin: 15px;
    /* display: flex;
    justify-content: space-between; */
}
.calculator-screen input{
    border: none;
    width: 100%;
    height: 15vh;
    font-size: 25px;
    position: relative;
}
.first-line-btn-white, .second-line-btn-white, .third-line-btn-white, .fourth-line-btn-white, .fifth-line-btn-white{
    display: flex;
    justify-content: space-evenly;
    margin: 15px auto ;
}
.first-line-btn-white button, .second-line-btn-white button, .third-line-btn-white button, .fourth-line-btn-white button, .fifth-line-btn-white button{
    border: none;
    background-color: white;
    color: black;
    font-size: 20px;
    width: 22%;
    border-radius: 8px;
    height: 6vh;
    box-shadow: 1px 1px 3px 3px rgb(151, 135, 135);
}


  </style>
</head>

<body>
    <div class="calculator">
        <div class="calculator-border white">
            <div class="calculator-content ">
                <div class="calculator-screen">
                    <input type="number">
                </div>
                <div class="calculator-btn">
                    <div class="first-line-btn-white">
                        <button>AC</button>
                        <button>+/-</button>
                        <button>%</button>
                        <button id="÷" style="background-color: rgb(255, 69, 0);">÷</button>
                    </div>
                    <div class="second-line-btn-white">
                        <button>7</button>
                        <button>8</button>
                        <button>9</button>
                        <button id="X" style="background-color: rgb(255, 69, 0);">X</button>
                    </div>
                    <div class="third-line-btn-white">
                        <button>4</button>
                        <button>5</button>
                        <button>6</button>
                        <button id="-" style="background-color: rgb(255, 69, 0);">-</button>
                    </div>
                    <div class="fourth-line-btn-white">
                        <button>1</button>
                        <button>2</button>
                        <button>3</button>
                        <button id="+" style="background-color: rgb(255, 69, 0);">+</button>
                    </div>
                    <div class="fifth-line-btn-white">
                        <button class="zero" style="width: 47%;">0</button>
                        <button>,</button>
                        <button id="=" style="background-color: rgb(255, 69, 0);">=</button>
                    </div>

                </div>
            </div>
        </div>
        <!-- <div class="calculator-border black">
            <div class="calculator-content">
                <div class="calculator-screen">
                    <input type="number">
                </div>
                <div class="calculator-btn">

                </div>
            </div>
        </div> -->
    </div>
</body>

</html>
