<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Update Notifier</title>
    <style>
        #updateTimer {
            font-size: 1.2em;
        }
    </style>
</head>
<body>
    <h1>Website Update Notifier</h1>
    
    <p>Last update: <span id="lastUpdate"></span></p>
    <p id="updateTimer"></p>
    
    <script>
        // Display last update time
        function displayLastUpdate() {
            var lastUpdateElement = document.getElementById('lastUpdate');
            var lastUpdate = localStorage.getItem('lastUpdate');
            if (lastUpdate) {
                lastUpdateElement.textContent = new Date(lastUpdate).toLocaleString();
            } else {
                lastUpdateElement.textContent = 'Never';
            }
        }
        
        // Update timer
        function updateTimer() {
            var updateTimerElement = document.getElementById('updateTimer');
            var lastUpdate = localStorage.getItem('lastUpdate');
            if (lastUpdate) {
                var elapsedTime = new Date() - new Date(lastUpdate);
                var seconds = Math.floor(elapsedTime / 1000);
                var minutes = Math.floor(seconds / 60);
                var hours = Math.floor(minutes / 60);
                var days = Math.floor(hours / 24);
                seconds %= 60;
                minutes %= 60;
                hours %= 24;
                updateTimerElement.textContent = days + 'd ' + hours + 'h ' + minutes + 'm ' + seconds + 's';
            } else {
                updateTimerElement.textContent = '';
            }
        }
        
        // Check if service workers are supported
        if ('serviceWorker' in navigator) {
            // Register the service worker
            navigator.serviceWorker.register('service-worker.js')
            .then(registration => {
                console.log('Service Worker registered successfully:', registration);
                // Display last update time and start update timer
                displayLastUpdate();
                updateTimer();
                setInterval(updateTimer, 1000); // Update timer every second
            })
            .catch(error => {
                console.error('Service Worker registration failed:', error);
            });
        } else {
            console.log('Service workers are not supported.');
        }
    </script>
</body>
</html>
