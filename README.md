# Build-an-Analog-Clock-in-JavaScript-

index.html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Analog Clock</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>

        <div class="clock">
            <div id="seconds-hand"></div>
            <div id="minites-hand"></div>
            <div id="hours-hand"></div>
            <div>id_center</div>
        </div>

        <script src="app.js"></script>
    </body>
    </html>
    
    
    App.js
    const secondsHand = document.getElementById('seconds-hand')
const minutesHand = document.getElementById('minutes-hand')
const hoursHand = document.getElementById('hours-hand')

function getTime() {
    const now = new Data()
    const seconds = now.getSeconds()
    const minutes = now.getMinutes()
    const hours = now.getHours()
    const timeInterval = 6 

    
    console.log(seconds)
    secondsHand.style.transform = 'rotate(' + (seconds * timeInterval) + deg')'
    minutesHand.style.transform = 'rotate(' + (minutes * timeInterval + seconds / 10 ) + deg')'
    hoursHand.style.transform = 'rotate(' + (hours * 30 + minutes / 2) + deg')'
}


setInterval(getTime, 100)


styles.css
body{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: rgb(43,43,43);
}

.clock {
    height: 300px;
    width: 300px; 
    border-radius: 150px;
    border: solid 5px rgb(252,255,55)
    position: absolute;

}

#second-hand{
    position: absolute;
    height: 130px;
    width: 2px;
    background-color: rgb(70,255,255);
    left: 149px;
    bottom: 149px;
    opacity: 50%;
    transform-origin: 0% 100%;
    
}

#minutes-hand {
    height: 100PX;
    width: 2px;
    background-color: rgb(253,120,227);
    position: absolute;
    left: 149px;
    bottom: 149px;
    transform-origin: 0% 100%;
}

#hours-hand {
    height: 80px;
    width: 4px;
    background-color: rgb(205,112,255);
    position: absolute;
    left: 148px;
    bottom: 148px;
    transform-origin: 0% 100%;
}

#center {
    height: 10px;
    width: 10px;
    border-radius: 5px;
    background-color: rgb(252,255,55);
    position: absolute;
    left: 145px;
    bottom: 145px;

}

