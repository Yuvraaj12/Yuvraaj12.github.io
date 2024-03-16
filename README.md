<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Video Player</title>
    <style>
        body {
            background-color: #f0f0f0; /* Set background color */
            font-family: Arial, sans-serif; /* Set font family */
            text-align: center; /* Center text horizontally */
            margin-top: 50px; /* Add top margin for spacing */
        }
        .blue-text {
            color: blue; /* Set text color to blue */
        }
        video {
            max-width: 100%; /* Ensure the video fits within the viewport */
        }
    </style>
</head>
<body>
    <h1 class="blue-text">Hi</h1>
    
    <!-- Video Player -->
    <video controls>
        <source id="videoSource" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <!-- Form to input video file path -->
    <form id="videoForm" onsubmit="return loadVideo()">
        <label for="videoFile">Video File:</label><br>
        <input type="text" id="videoFile" name="videoFile" placeholder="Enter video file path"><br>
        <button type="submit">Load Video</button>
    </form>

    <script>
        function loadVideo() {
            var videoFile = document.getElementById("videoFile").value;
            var videoSource = document.getElementById("videoSource");
            videoSource.src = videoFile;
            return false; // Prevent form submission
        }
    </script>
</body>
</html>
