# Panel-x
<p>© 2026 Panel X - Free Fire | Creado por [Tu Nombre]</p>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Panel Free Fire - Dashboard</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* HEADER */
        header {
            background: linear-gradient(135deg, #ff6b00 0%, #ff8c00 100%);
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 8px 32px rgba(255, 107, 0, 0.3);
        }

        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1.1em;
            opacity: 0.9;
        }

        /* STATS GRID */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: rgba(255, 107, 0, 0.1);
            border: 2px solid #ff6b00;
            padding: 25px;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 107, 0, 0.2);
            box-shadow: 0 8px 32px rgba(255, 107, 0, 0.3);
        }

        .stat-card h3 {
            color: #ff6b00;
            margin-bottom: 10px;
            text-transform: uppercase;
            font-size: 0.9em;
            letter-spacing: 1px;
        }

        .stat-card .value {
            font-size: 2.5em;
            font-weight: bold;
            color: #fff;
        }

        .stat-card .unit {
            font-size: 0.8em;
            color: #888;
            margin-top: 5px;
        }

        /* PROFILE SECTION */
        .profile-section {
            background: rgba(255, 107, 0, 0.05);
            border: 2px solid #ff6b00;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .profile-header {
            display: flex;
            gap: 20px;
            align-items: center;
            margin-bottom: 20px;
        }

        .profile-avatar {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, #ff6b00, #ff8c00);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3em;
        }

        .profile-info h2 {
            font-size: 1.8em;
            margin-bottom: 5px;
        }

        .profile-info p {
            color: #888;
            margin-bottom: 3px;
        }

        /* INPUT SECTION */
        .input-section {
            background: rgba(255, 107, 0, 0.05);
            border: 2px solid #ff6b00;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .input-section h3 {
            color: #ff6b00;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .input-group {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }

        input, select {
            padding: 12px;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid #ff6b00;
            color: #fff;
            border-radius: 5px;
            font-size: 1em;
        }

        input::placeholder {
            color: #888;
        }

        input:focus, select:focus {
            outline: none;
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 0 10px rgba(255, 107, 0, 0.5);
        }

        /* BUTTONS */
        .button-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        button {
            padding: 12px 30px;
            background: linear-gradient(135deg, #ff6b00, #ff8c00);
            border: none;
            color: white;
            font-size: 1em;
            border-radius: 5px;
            cursor: pointer;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 1px;
            transition: all 0.3s ease;
        }

        button:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 32px rgba(255, 107, 0, 0.5);
        }

        button:active {
            transform: scale(0.95);
        }

        /* ACHIEVEMENTS SECTION */
        .achievements {
            background: rgba(255, 107, 0, 0.05);
            border: 2px solid #ff6b00;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .achievements h3 {
            color: #ff6b00;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .achievement-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
        }

        .achievement-item {
            background: rgba(255, 107, 0, 0.1);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #ff6b00;
        }

        .achievement-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        /* FOOTER */
        footer {
            text-align: center;
            padding: 20px;
            color: #888;
            border-top: 2px solid #ff6b00;
            margin-top: 40px;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8em;
            }

            .profile-header {
                flex-direction: column;
                align-items: flex-start;
            }

            .stats-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- HEADER -->
        <header>
            <h1>🔥 Panel Free Fire</h1>
            <p>Dashboard de Estadísticas y Gestión</p>
        </header>

        <!-- PROFILE SECTION -->
        <div class="profile-section">
            <div class="profile-header">
                <div class="profile-avatar">🎮</div>
                <div class="profile-info">
                    <h2 id="username">Jugador</h2>
                    <p>ID: <span id="userid">0000000</span></p>
                    <p>Nivel: <span id="userlevel">1</span></p>
                </div>
            </div>
        </div>

        <!-- STATS GRID -->
        <div class="stats-grid">
            <div class="stat-card">
                <h3>Victorias</h3>
                <div class="value" id="wins">0</div>
                <div class="unit">Partidas Ganadas</div>
            </div>
            <div class="stat-card">
                <h3>Eliminaciones</h3>
                <div class="value" id="kills">0</div>
                <div class="unit">Total de Kills</div>
            </div>
            <div class="stat-card">
                <h3>Muertes</h3>
                <div class="value" id="deaths">0</div>
                <div class="unit">Total de Muertes</div>
            </div>
            <div class="stat-card">
                <h3>K/D Ratio</h3>
                <div class="value" id="kdratio">0.00</div>
                <div class="unit">Proporción Kill/Death</div>
            </div>
            <div class="stat-card">
                <h3>Partidas Jugadas</h3>
                <div class="value" id="matches">0</div>
                <div class="unit">Total de Partidas</div>
            </div>
            <div class="stat-card">
                <h3>Tasa de Victoria</h3>
                <div class="value" id="winrate">0%</div>
                <div class="unit">% de Victorias</div>
            </div>
        </div>

        <!-- INPUT SECTION -->
        <div class="input-section">
            <h3>📊 Actualizar Estadísticas</h3>
            <div class="input-group">
                <input type="text" id="nameInput" placeholder="Nombre de Usuario">
                <input type="text" id="idInput" placeholder="ID del Jugador">
                <input type="number" id="levelInput" placeholder="Nivel" value="1">
            </div>
            <div class="input-group">
                <input type="number" id="winsInput" placeholder="Victorias" value="0">
                <input type="number" id="killsInput" placeholder="Eliminaciones" value="0">
                <input type="number" id="deathsInput" placeholder="Muertes" value="0">
                <input type="number" id="matchesInput" placeholder="Partidas" value="0">
            </div>
            <div class="button-group">
                <button onclick="updateStats()">💾 Guardar Estadísticas</button>
                <button onclick="resetStats()">🔄 Limpiar</button>
                <button onclick="loadExample()">📌 Datos de Ejemplo</button>
            </div>
        </div>

        <!-- ACHIEVEMENTS SECTION -->
        <div class="achievements">
            <h3>🏆 Logros</h3>
            <div class="achievement-list">
                <div class="achievement-item">
                    <div class="achievement-icon">🎯</div>
                    <p>Primera Victora</p>
                </div>
                <div class="achievement-item">
                    <div class="achievement-icon">⚡</div>
                    <p>10 Kills</p>
                </div>
                <div class="achievement-item">
                    <div class="achievement-icon">🔥</div>
                    <p>100 Kills</p>
                </div>
                <div class="achievement-item">
                    <div class="achievement-icon">👑</div>
                    <p>Top 10</p>
                </div>
                <div class="achievement-item">
                    <div class="achievement-icon">💎</div>
                    <p>Nivel 50</p>
                </div>
                <div class="achievement-item">
                    <div class="achievement-icon">⭐</div>
                    <p>Campeón</p>
                </div>
            </div>
        </div>

        <!-- FOOTER -->
        <footer>
            <p>© 2026 Panel Free Fire - Dashboard Profesional | Creado por Tu Nombre</p>
        </footer>
    </div>

    <script>
        // Cargar datos del localStorage al abrir la página
        window.addEventListener('load', function() {
            loadStats();
        });

        // Función para actualizar estadísticas
        function updateStats() {
            const stats = {
                username: document.getElementById('nameInput').value || 'Jugador',
                userid: document.getElementById('idInput').value || '0000000',
                level: document.getElementById('levelInput').value || '1',
                wins: parseInt(document.getElementById('winsInput').value) || 0,
                kills: parseInt(document.getElementById('killsInput').value) || 0,
                deaths: parseInt(document.getElementById('deathsInput').value) || 0,
                matches: parseInt(document.getElementById('matchesInput').value) || 0
            };

            // Guardar en localStorage
            localStorage.setItem('freeFireStats', JSON.stringify(stats));

            // Actualizar el panel
            displayStats(stats);
            
            alert('✅ Estadísticas guardadas correctamente');
        }

        // Función para mostrar estadísticas
        function displayStats(stats) {
            document.getElementById('username').textContent = stats.username;
            document.getElementById('userid').textContent = stats.userid;
            document.getElementById('userlevel').textContent = stats.level;
            document.getElementById('wins').textContent = stats.wins;
            document.getElementById('kills').textContent = stats.kills;
            document.getElementById('deaths').textContent = stats.deaths;
            document.getElementById('matches').textContent = stats.matches;

            // Calcular K/D Ratio
            const kdratio = stats.deaths > 0 ? (stats.kills / stats.deaths).toFixed(2) : stats.kills;
            document.getElementById('kdratio').textContent = kdratio;

            // Calcular tasa de victoria
            const winrate = stats.matches > 0 ? ((stats.wins / stats.matches) * 100).toFixed(1) : 0;
            document.getElementById('winrate').textContent = winrate + '%';
        }

        // Función para cargar datos guardados
        function loadStats() {
            const saved = localStorage.getItem('freeFireStats');
            if (saved) {
                const stats = JSON.parse(saved);
                displayStats(stats);
                // Llenar los inputs
                document.getElementById('nameInput').value = stats.username;
                document.getElementById('idInput').value = stats.userid;
                document.getElementById('levelInput').value = stats.level;
                document.getElementById('winsInput').value = stats.wins;
                document.getElementById('killsInput').value = stats.kills;
                document.getElementById('deathsInput').value = stats.deaths;
                document.getElementById('matchesInput').value = stats.matches;
            }
        }

        // Función para limpiar datos
        function resetStats() {
            document.getElementById('nameInput').value = '';
            document.getElementById('idInput').value = '';
            document.getElementById('levelInput').value = '1';
            document.getElementById('winsInput').value = '0';
            document.getElementById('killsInput').value = '0';
            document.getElementById('deathsInput').value = '0';
            document.getElementById('matchesInput').value = '0';
            localStorage.removeItem('freeFireStats');
            location.reload();
        }

        // Función para cargar datos de ejemplo
        function loadExample() {
            const example = {
                username: 'MiJugador123',
                userid: '1234567',
                level: '35',
                wins: 45,
                kills: 823,
                deaths: 312,
                matches: 156
            };
            
            document.getElementById('nameInput').value = example.username;
            document.getElementById('idInput').value = example.userid;
            document.getElementById('levelInput').value = example.level;
            document.getElementById('winsInput').value = example.wins;
            document.getElementById('killsInput').value = example.kills;
            document.getElementById('deathsInput').value = example.deaths;
            document.getElementById('matchesInput').value = example.matches;

            displayStats(example);
            alert('📌 Datos de ejemplo cargados');
        }
    </script>
</body>
</html>
