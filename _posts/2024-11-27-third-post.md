---
title: clock html
date: 2024-11-26 16:00:00 -0400
categories: jekyll update
---

<!DOCTYPE html>
<html lang="en">



<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Current US Time</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #f3f4f6;
            margin: 0;
        }

        .time-container {
            text-align: center;
        }

        h1 {
            font-size: 2rem;
        }

        .time {
            font-size: 3rem;
            color: #333;
        }
    </style>
</head>

<body>
    <div class="time-container">
        <h1>Current Time in USA (Eastern Time Zone)</h1>
        <div class="time" id="us-time"></div>
    </div>

    <script>
        function updateTime() {
            const options = { timeZone: 'America/New_York', hour: '2-digit', minute: '2-digit', second: '2-digit' };
            const currentTime = new Date().toLocaleTimeString('en-US', options);
            document.getElementById('us-time').textContent = currentTime;
        }
        setInterval(updateTime, 1000);
        updateTime();
    </script>
</body>

</html>
