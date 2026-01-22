# Hicham-FUT
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hicham FUT</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: #0b0f14;
    color: #ffffff;
}

header {
    background: linear-gradient(90deg, #0a7c4a, #0d3b66);
    padding: 20px;
    text-align: center;
    font-size: 2.2em;
    font-weight: bold;
}

.menu {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin: 30px;
}

.menu button {
    background: #161b22;
    color: white;
    border: 1px solid #2ea043;
    padding: 15px 35px;
    font-size: 1.1em;
    border-radius: 8px;
    cursor: pointer;
}

.menu button:hover {
    background: #2ea043;
}

.section {
    display: none;
    padding: 20px;
    text-align: center;
}

.card {
    background: #161b22;
    margin: 15px auto;
    padding: 15px;
    max-width: 400px;
    border-radius: 10px;
    border: 1px solid #30363d;
}

.card a {
    color: #2ea043;
    text-decoration: none;
    font-weight: bold;
}

.card a:hover {
    text-decoration: underline;
}

.country-btn {
    background: #21262d;
    color: white;
    border: none;
    padding: 12px;
    margin: 8px;
    border-radius: 6px;
    cursor: pointer;
}

.country-btn:hover {
    background: #0d3b66;
}
</style>
</head>

<body>

<header>⚽ Hicham FUT</header>

<div class="menu">
    <button onclick="showSection('fut')">FUT</button>
    <button onclick="showSection('tv')">TV EN DIRECTO</button>
</div>

<!-- FUT -->
<div id="fut" class="section">
    <h2>Partidos de Fútbol</h2>

    <div class="card">Real Madrid 🆚 FC Barcelona<br>LaLiga</div>
    <div class="card">PSG 🆚 Marseille<br>Ligue 1</div>
    <div class="card">Manchester City 🆚 Arsenal<br>Premier League</div>

    <p style="opacity:0.7">Resultados, horarios y enlaces oficiales</p>
</div>

<!-- TV -->
<div id="tv" class="section">
    <h2>Canales en Directo (Oficiales)</h2>

    <h3>Europa</h3>
    <button class="country-btn" onclick="showCountry('espana')">🇪🇸 España</button>
    <button class="country-btn" onclick="showCountry('francia')">🇫🇷 Francia</button>

    <h3>Norte de África</h3>
    <button class="country-btn" onclick="showCountry('marruecos')">🇲🇦 Marruecos</button>
    <button class="country-btn" onclick="showCountry('argelia')">🇩🇿 Argelia</button>

    <!-- ESPAÑA -->
    <div id="espana" class="section">
        <div class="card"><a href="https://www.rtve.es/play/" target="_blank">RTVE La 1 / La 2</a></div>
        <div class="card"><a href="https://www.atresplayer.com/" target="_blank">Antena 3 / La Sexta</a></div>
    </div>

    <!-- FRANCIA -->
    <div id="francia" class="section">
        <div class="card"><a href="https://www.france.tv/" target="_blank">France TV</a></div>
    </div>

    <!-- MARRUECOS -->
    <div id="marruecos" class="section">
        <div class="card"><a href="https://www.snrt.ma/" target="_blank">Al Aoula</a></div>
        <div class="card"><a href="https://arryadia.snrt.ma/" target="_blank">Arryadia</a></div>
        <div class="card"><a href="https://2m.ma/" target="_blank">2M</a></div>
    </div>

    <!-- ARGELIA -->
    <div id="argelia" class="section">
        <div class="card"><a href="https://www.entv.dz/" target="_blank">ENTV</a></div>
    </div>
</div>

<script>
function showSection(id) {
    document.querySelectorAll('.section').forEach(s => s.style.display = 'none');
    document.getElementById(id).style.display = 'block';
}

function showCountry(id) {
    document.querySelectorAll('#tv .section').forEach(s => s.style.display = 'none');
    document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>
