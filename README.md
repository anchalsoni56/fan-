# fan-
A rotating fan 
html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="container">
        <br><br>
        <form>
            <input type="radio" id="stop" name="fan">
            <label for="stop" id="stop_active">Stop</label>

            <input type="radio" id="low" name="fan">
            <label for="low" id="low_active">Low</label>

            <input type="radio" id="second" name="fan">
            <label for="second" id="high_active">Medium</label>

            <input type="radio" id="third" name="fan">
            <label for="third" id="high_active">Fast</label>

            <div class="svg">
                <img class="wings"
                    src="https://tse1.mm.bing.net/th?id=OIP.CSgajfPUh6JEQUmU7qKbkgHaHb&pid=Api&P=0&h=220">
            </div>


        </form>
    </div>

</body>

</html>
CSS
body {
    font-family: "Poppins", sans-serif;
    background: white;

}

.conatiner {
    width: 100%;
    text-align: center;
    align-items: center;

}

.svg {
    width: 90%;
    margin: 0 auto;
    overflow: hidden;
    margin-top: 40px;
}

img {
    width: 450px;
    height: 450px;

}

input[type=radio] {
    width: 20px;
    height: 20px;
    cursor: pointer;
    margin-left: 10px;
    display: none;

}

label {
    padding: 10px 20px;
    border-radius: 5px;
    font-weight: 900;
    margin-left: 20px;
    cursor: pointer;
    box-shadow: 5px 5px 13px #b6b7b7, -5px -5px 13px #e8e9e9;

}

label:hover {
    box-shadow: inset 5px 5px 13px #b6b7b7, -5px -5px 13px #e8e9e9;
}

.wings {
    animation-iteration-count: infinite;
    animation-timing-function: linear;

}

#stop:checked~.svg>.wings {
    transform: rotate(0);
}

#low:checked~.svg>.wings {
    animation-name: slow;
    animation-duration: 1s;

}

@keyframes slow {
    100% {
        transform: rotate(360deg);
    }
}

#second:checked~.svg>.wings {
    animation-name: mdm;
    animation-duration: .5s;

}

@keyframes mdm {
    100% {
        transform: rotate(360deg);
    }
}


#third:checked~.svg>.wings {
    animation-name: fast;
    animation-duration: .1s;

}

@keyframes fast {
    100% {
        transform: rotate(360deg);
    }
}
