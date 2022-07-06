# Digit-clock
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clock</title>
    <style>
        body{
            /* background-color: grey; */
        }
        #clock {
            font-size: 100px;
            margin-left: 400px;
            margin-top: 200px;
            background-color: black;
            border: 2px solid yellow;
            width: 540px;
            color: white;
            position: relative;

        }

        h1 {
            position: absolute;
            left: 416px;
            top: 109px;
            font-size: 45px;
            color: red;
        }
        h1 .one{
            color: Black;
        }
        h1 .two{
            color: red;
        }
        h1 .three{
            color: rgb(255, 217, 4);
        }
    </style>
</head>

<body>
    <h1> <span class="one"> Standard</span>  <span class="two">Time</span> <span class="three"> Germany</span></h1>

    <div id="clock"></div>

    <script>
        setInterval(Digitclock, 1000);
        function Digitclock() {
            var time = new Date();
            var hrs = time.getHours();
            var min = time.getMinutes();
            var sec = time.getSeconds();
            var en = 'AM';
            if (hrs > 12) {
                en = 'PM';
            }

            if (hrs > 12) {
                hrs = hrs - 12;
            }
            if (hrs == 0) {
                hrs = 12;
            }
            if (hrs < 10) {
                hrs = '0' + hrs;
            }
            if (min < 10) {
                min = '0' + min;
            }
            if (sec < 10) {
                sec = '0' + sec;
            }


            document.getElementById('clock').innerHTML = hrs + ':' + min + ':' + sec + ' ' + en;



        }
    </script>

</body>



</html>
