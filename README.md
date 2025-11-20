<!DOCTYPE html>
text-shadow: 2px 2px 6px rgba(0,0,0,0.4);
}


.gallery {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
gap: 20px;
padding: 20px;
max-width: 1200px;
margin: auto;
}


.gallery img {
width: 100%;
height: 350px;
object-fit: cover;
border-radius: 15px;
box-shadow: 0 6px 15px rgba(0,0,0,0.3);
transition: transform 0.3s ease, box-shadow 0.3s ease;
}


.gallery img:hover {
transform: scale(1.05);
box-shadow: 0 10px 25px rgba(0,0,0,0.4);
}


button {
background: #ffffffaa;
border: none;
padding: 12px 25px;
font-size: 1.1rem;
border-radius: 10px;
cursor: pointer;
margin: 20px;
transition: background 0.3s;
}


button:hover {
background: #ffffffdd;
}
</style>
</head>
<body>
<header>🌸 Anime Girl Gallery 🌸</header>


<button onclick="addRandomImage()">Add Random Anime Girl</button>


<div class="gallery" id="gallery"></div>


<script>
const images = [
"https://i.imgur.com/u5F0yYB.jpeg",
"https://i.imgur.com/6adYdCP.jpeg",
"https://i.imgur.com/Qx6aJJA.jpeg",
"https://i.imgur.com/JqWQ2Y8.jpeg",
"https://i.imgur.com/OhlcN1w.jpeg"
];


const gallery = document.getElementById("gallery");


function addRandomImage() {
const img = document.createElement("img");
img.src = images[Math.floor(Math.random() * images.length)];
gallery.appendChild(img);
}


// Load 4 images on start
for (let i = 0; i < 4; i++) addRandomImage();
</script>
</body>
</html>
