<html>
    <head>
        

        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
        <style>
            body {
                /* display: flex;
                justify-content: center; */
                text-align: center;
                background-color: black;

            }
            button {
            background-color: #ffffff; 
            color: rgb(0, 0, 0);
            padding: 25px 47px;
            text-align: center;
            display: inline-block;
            font-size: 26px;
            transition-duration: 0.4s;
            cursor: pointer;
            border-radius: 15% ;
            border: 2px solid #ffffff ;
            margin: 50px;
            }

            button:hover {
            background-color: #000000;
            color: rgb(255, 255, 255);
            border :rgb(0, 0, 0)
            }
        </style>
        <title>anomaly</title>
    </head>
    <body>
        <p style="color: #ffffff; font-size: 22px;">انتخاب کنید که به چه کسی اعتماد میکنید، توجه کنید در پایان راه بازگشتی نخواهید داشت</p>
        <div id="safeTimer" class="divdiv">
            <p id="safeTimerDisplay" style="color: #ffffff;">00:30</p>
        </div>

        <div>
            <button>ناجی</button> <button>سرپرست</button>
        </div>
        <script>
            var myVar = setInterval(function(){ myTimer() }, 1000);
            var secondlimit = 30;
            
            function myTimer() {
            if(secondlimit == 0)
            {
                myStopFunction();
            }
            
            document.getElementById("safeTimerDisplay").innerHTML = '00:' + zeroPad(secondlimit,2);
            secondlimit = secondlimit  - 1;
            
            }
            
            function myStopFunction() {
                clearInterval(myVar);
            }
            
            function zeroPad(num, places) {
              var zero = places - num.toString().length + 1;
              return Array(+(zero > 0 && zero)).join("0") + num;
            }
            
            </script>
    </body>
</html>
