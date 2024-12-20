<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>GitHub Wahyu</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<h1></h1>
<div class="jam"></div>
<script src="script.js"></script>
</body>
</html>
```

CSS (style.css)
```
body {
font-family: Arial, sans-serif;
background-color: #f0f0f0;
text-align: center;
}

h1 {
font-size: 36px;
margin-bottom: 20px;
}

.jam {
font-size: 64px;
font-weight: bold;
margin-top: 40px;
}
```

JavaScript (script.js)
```
const judul = document.querySelector('h1');
const jamElement = document.querySelector('.jam');

judul.textContent = '';

setInterval(() => {
const tanggal = new Date();
const jam = tanggal.getHours().toString().padStart(2, '0');
const menit = tanggal.getMinutes().toString().padStart(2, '0');
const detik = tanggal.getSeconds().toString().padStart(2, '0');

jamElement.textContent = `${jam}:${menit}:${detik}`;
}, 1000);
```