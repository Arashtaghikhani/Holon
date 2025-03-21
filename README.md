# Holon
Holon Ecosystem 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HOLON - 40 Weeks Countdown</title>
    <style>
        /* Global Styles */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #1c1c1c;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }
        .container {
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            padding: 40px;
            width: 100%;
            max-width: 600px;
            box-shadow: 0 0 20px rgba(0, 255, 204, 0.6);
        }
        h1 {
            font-size: 36px;
            color: #00ffcc;
            margin-bottom: 20px;
            font-weight: bold;
        }
        #timer {
            font-size: 48px;
            color: #ffcc00;
            font-weight: bold;
            letter-spacing: 2px;
            margin-top: 30px;
            transition: color 0.5s ease;
        }
        #timer span {
            display: inline-block;
            margin: 0 10px;
        }
        .socials a {
            color: #ffcc00;
            text-decoration: none;
            margin: 10px;
            display: inline-block;
            font-size: 18px;
            padding: 10px 20px;
            border: 2px solid #ffcc00;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        .socials a:hover {
            color: #00ffcc;
            background-color: #ffcc00;
            transform: scale(1.05);
        }
    </style>
    <script>
        function countdown() {
            // Set target date to 40 weeks from now
            let targetDate = new Date();
            targetDate.setDate(targetDate.getDate() + (40 * 7)); // 40 weeks later

            let timer = setInterval(function() {
                let now = new Date().getTime();
                let timeLeft = targetDate - now;

                if (timeLeft < 0) {
                    clearInterval(timer);
                    document.getElementById("timer").innerHTML = "HOLON has launched!";
                    return;
                }

                let weeks = Math.floor(timeLeft / (1000 * 60 * 60 * 24 * 7)); // weeks
                let days = Math.floor((timeLeft % (1000 * 60 * 60 * 24 * 7)) / (1000 * 60 * 60 * 24)); // days
                let hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)); // hours
                let minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60)); // minutes
                let seconds = Math.floor((timeLeft % (1000 * 60)) / 1000); // seconds

                // Display the result
                document.getElementById("timer").innerHTML = 
                    `<span>${weeks} Weeks</span> <span>${days} Days</span> <span>${hours} Hours</span> <span>${minutes} Minutes</span> <span>${seconds} Seconds</span>`;
            }, 1000);
        }
    </script>
</head>
<body onload="countdown()">
    <div class="container">
        <h1>HOLON Countdown: 40 Weeks</h1>
        <div id="timer"></div>
        <div class="socials">
            <a href="https://twitter.com/holon" target="_blank">Twitter</a>
            <a href="https://discord.gg/holon" target="_blank">Discord</a>
            <a href="https://holon.io" target="_blank">Website</a>
        </div>
    </div>
</body>
</html>
