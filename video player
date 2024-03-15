<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Media Player</title>
</head>
<body>
    <h1>Media Player</h1>
    
    <!-- Audio Player -->
    <audio controls id="audioPlayer">
        <source src="" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <!-- Playlist -->
    <ul id="playlist">
        <li><a href="#" onclick="playAudio('audio_file_1.mp3')">Audio File 1</a></li>
        <li><a href="#" onclick="playAudio('audio_file_2.mp3')">Audio File 2</a></li>
        <!-- Add more audio files here -->
    </ul>

    <script>
        function playAudio(audioSrc) {
            var audioPlayer = document.getElementById('audioPlayer');
            audioPlayer.src = audioSrc;
            audioPlayer.play();
        }
    </script>
</body>
</html>
