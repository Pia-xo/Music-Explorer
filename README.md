# Music-Explorer
Hackathon Teilnahme. Start 05/10/25 (8:10). Status 0

JS:8
HTML:56
CSS:97

addEventListener('load', function(e) {
  document.querySelector('#test').innerHTML = 'Music Explorer';
});

# 1. Clone this repo
git clone <your-fork-url>
cd global-hackathon-v1

# 2. Create timestamp (REQUIRED for anti-cheating)
date > .hackathon-start
git add .hackathon-start
git commit -m "Starting hackathon - $(date)"
git push

# 3. Build your project here

// Liste der Songs (nur lizenzfreie Titel!)
const songs = [
  { title: "Acoustic Breeze – Bensound", file: "songs/song1.mp3" },
  { title: "Creative Minds – Bensound", file: "songs/song2.mp3" },
  { title: "Sunny – KODOMOi", file: "songs/song3.mp3" }
];

const songList = document.getElementById("song-list");
const audioPlayer = document.getElementById("audio-player");
const songTitle = document.getElementById("song-title");

// Songs in die Liste einfügen
songs.forEach((song, index) => {
  const li = document.createElement("li");
  li.textContent = song.title;
  li.addEventListener("click", () => playSong(index));
  songList.appendChild(li);
});

// Funktion zum Abspielen
function playSong(index) {
  const song = songs[index];
  songTitle.textContent = song.title;
  audioPlayer.src = song.file;
  audioPlayer.play();
}

# 4. Commit regularly (minimum 5 commits)




<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width" />
  <title>hackahon</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>hackahon</h1>
  <div id="test"></div>

  <script src="script.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>🎧 Meine Musik Streaming App</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>🎶 Meine Musik Streaming App</h1>

  <div id="player">
    <h2 id="song-title">Wähle einen Song</h2>
    <audio id="audio-player" controls></audio>
  </div>

  <h3>Verfügbare Songs:</h3>
  <ul id="song-list"></ul>

  <script src="script.js"></script>
</body>
</html>




#test {
  color: gray;
}

body {
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #74ABE2, #5563DE);
  color: white;
  text-align: center;
  padding: 40px;
}

#player {
  margin: 30px auto;
  background: rgba(255, 255, 255, 0.1);
  padding: 20px;
  border-radius: 12px;
  width: 300px;
}

audio {
  width: 100%;
  margin-top: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background: rgba(255, 255, 255, 0.15);
  margin: 5px auto;
  width: 300px;
  padding: 10px;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.2s;
}

li:hover {
  background: rgba(255, 255, 255, 0.3);
}