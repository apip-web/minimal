---
layout: default
title: Kalkulator Skala Crop
---

  <style>
    body {
  font-family: 'Orbitron', sans-serif;
  padding: 30px;
  max-width: 450px;
  margin: auto;
  background-color: #0f0f0f;
  color: #e0e0e0;
  min-height: 100vh;
  box-sizing: border-box;
}

h2 {
  color: #ff0000; /* Radical Red */
  text-align: center;
  margin-bottom: 30px;
  text-shadow: 0 0 8px rgba(255, 0, 0, 0.5);
  letter-spacing: 3px;
  font-weight: 700;
  font-size: 28px;
}

label {
  display: block;
  margin-bottom: 8px;
  color: #cccccc;
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 1px;
}

input[type="number"] {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  background-color: #1a1a1a;
  border: 1px solid #333333;
  color: #ffffff;
  font-size: 16px;
  box-sizing: border-box;
  transition: border-color 0.3s ease;
  font-family: 'Orbitron', sans-serif;
  font-weight: 500;
}

input[type="number"]:focus {
  outline: none;
  border-color: #ff0000; /* Radical Red accent */
  box-shadow: 0 0 10px rgba(255, 0, 0, 0.3);
}

button {
  display: block;
  width: 100%;
  padding: 12px;
  background-color: #ff0000; /* Radical Red */
  color: #000000;
  font-weight: 700;
  font-size: 18px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
  margin-top: 10px;
  font-family: 'Orbitron', sans-serif;
  letter-spacing: 2px;
}

button:hover {
  background-color: #ff3333;
  transform: scale(1.02);
}

button:active {
  background-color: #cc0000;
}

.result {
  margin-top: 30px;
  padding: 15px;
  background-color: #1a1a1a;
  border: 1px solid #333333;
  font-weight: 700;
  color: #ff0000; /* Radical Red for results */
  white-space: pre-wrap;
  font-size: 18px;
  text-align: center;
  min-height: 60px;
  font-family: 'Orbitron', sans-serif;
  letter-spacing: 1px;
}
  </style>
  
  <h2>Kalkulator Skala Crop</h2>
  <label>Height gambar lama:</label>
  <input type="number" id="heightLama" value="1204">

  <label>Height gambar baru:</label>
  <input type="number" id="heightBaru" value="1350">

  <label>Top lama (px):</label>
  <input type="number" id="topLama" value="35">

  <label>Crop height lama (px):</label>
  <input type="number" id="cropLama" value="155">

  <button onclick="hitung()">Hitung</button>

  <div class="result" id="output"></div>

  <script>
    function hitung() {
      const hLama = parseFloat(document.getElementById('heightLama').value);
      const hBaru = parseFloat(document.getElementById('heightBaru').value);
      const topLama = parseFloat(document.getElementById('topLama').value);
      const cropLama = parseFloat(document.getElementById('cropLama').value);

      const skala = hBaru / hLama;
      const topBaru = Math.round(topLama * skala);
      const cropBaru = Math.round(cropLama * skala);

      document.getElementById('output').innerText = 
        `Top baru: ${topBaru}px\nHeight crop baru: ${cropBaru}px`;
    }
  </script>
