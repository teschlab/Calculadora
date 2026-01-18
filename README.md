6


Las notificaciones de mensajes están desactivadas. Activar
2
11:25
11:02
1
10:46
2
9:00
Ayer
Ayer
1
Ayer
viernes
viernes
jueves
jueves
jueves
jueves
jueves
miércoles
miércoles
miércoles
miércoles
miércoles
martes
11/1/2026
10/1/2026
3
9/1/2026
6/1/2026
3/1/2026
1/1/2026
26/12/2025
21/12/2025
12/12/2025
12/12/2025
8/12/2025
6/12/2025
26/11/2025
30/12/2025
6/11/2025
6/11/2025
5/11/2025
22/10/2025
21/10/2025
15:38
15/10/2025
miércoles
22/11/2025
17/10/2025
4/10/2025
30/9/2025
30/10/2025
22/9/2025
16/9/2025
30/10/2025
13/9/2025
16/10/2025
2/9/2025
15:38
26/9/2025
20/8/2025
3/1/2026
21/10/2025
11/7/2025
10/7/2025
30/6/2025
26/10/2025
7/12/2025
28/6/2025
Envía mensajes a este mismo número.
martes
miércoles
Ayer
Hoy
github.com
https://github.com/teschlab/Tesch.git
github.com
https://github.com/teschlab/Tesch.git
16:23
github.com
https://github.com/teschlab/Calculadora.git
github.com
https://github.com/teschlab/Calculadora.git
16:26
Para que tu sitio sea accesible desde cualquier lugar (teléfono, tablet o cualquier computadora) y tenga todas las funciones que hemos diseñado, el proceso tiene dos partes: el código final mejorado y el paso a paso para publicarlo gratis.
El Código Maestro (LabCalc Professional)
He integrado la calculadora de molaridad, diluciones, porcentajes, la tabla de reactivos y el bloc de notas en un solo archivo optimizado para móviles.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LabCalc Professional - Acceso Remoto</title>
    <style>
        :root {
            --primary: #1a252f;
            --accent: #27ae60;
            --blue: #2980b9;
            --or…Leer más
16:27
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LabCalc Professional - Acceso Remoto</title>
    <style>
        :root {
            --primary: #1a252f;
            --accent: #27ae60;
            --blue: #2980b9;
            --orange: #e67e22;
            --bg: #f4f4f9;
        }

        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); margin: 0; padding: 10px; color: #333; }
        header { background: var(--primary); color: white; padding: 20px; text-align: center; border-radius: 10px; margin-bottom: 20px; }
        
        .grid-container { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); 
            gap: 20px; 
            max-width: 1200px; 
            margin: auto; 
        }

        .card { 
            background: white; 
            padding: 20px; 
            border-radius: 15px; 
            box-shadow: 0 4px 12px rgba(0,0,0,0.1); 
            border-top: 6px solid var(--blue);
        }

        .card.dilution { border-top-color: var(--accent); }
        .card.percent { border-top-color: var(--orange); }

        h2 { font-size: 1.2rem; margin-bottom: 15px; display: flex; align-items: center; gap: 10px; }
        label { display: block; font-size: 0.85rem; margin-top: 10px; font-weight: bold; }
        
        input, textarea { 
            width: 100%; padding: 12px; margin-top: 5px; 
            border: 1px solid #ccc; border-radius: 8px; box-sizing: border-box; 
            font-size: 1rem;
        }

        .result-box { 
            margin-top: 15px; padding: 15px; background: #f0f7ff; 
            border-radius: 8px; font-weight: bold; text-align: center; color: var(--blue);
            border: 1px dashed var(--blue);
        }

        table { width: 100%; border-collapse: collapse; margin-top: 10px; font-size: 0.9rem; }
        th, td { padding: 10px; border-bottom: 1px solid #eee; text-align: left; }
        .btn-use { 
            background: var(--accent); color: white; border: none; 
            padding: 6px 12px; border-radius: 5px; cursor: pointer; 
        }

        footer { text-align: center; padding: 20px; color: #7f8c8d; font-size: 0.8rem; }
    </style>
</head>
<body>

<header>
    <h1>🧪 LabCalc Cloud</h1>
    <p>Herramientas de Precisión de Laboratorio</p>
</header>

<div class="grid-container">
    
    <div class="card">
        <h2>⚖️ Molaridad a Masa</h2>
        <label>Molaridad (M)</label>
        <input type="number" id="m1" placeholder="Ej: 0.5" oninput="calcMolar()">
        <label>Volumen (mL)</label>
        <input type="number" id="v1" placeholder="Ej: 250" oninput="calcMolar()">
        <label>Peso Molecular (g/mol)</label>
        <input type="number" id="pm1" placeholder="Ej: 58.44" oninput="calcMolar()">
        <div class="result-box" id="resMolar">Masa necesaria: -</div>
    </div>

    <div class="card dilution">
        <h2>💧 Dilución (C1V1 = C2V2)</h2>
        <label>Concentración Stock (C1)</label>
        <input type="number" id="c1" placeholder="Stock" oninput="calcDil()">
        <label>Concentración Final (C2)</label>
        <input type="number" id="c2" placeholder="Deseada" oninput="calcDil()">
        <label>Volumen Final (V2) mL</label>
        <input type="number" id="v2" placeholder="Volumen final" oninput="calcDil()">
        <div class="result-box" id="resDil" style="color:var(--accent); border-color:var(--accent); background:#f0f9f4;">V1 a tomar: -</div>
    </div>

    <div class="card percent">
        <h2>📊 Porcentaje (% w/v)</h2>
        <label>Porcentaje (%)</label>
        <input type="number" id="p_val" placeholder="Ej: 1" oninput="calcPerc()">
        <label>Volumen Final (mL)</label>
        <input type="number" id="p_vol" placeholder="Ej: 100" oninput="calcPerc()">
        <div class="result-box" id="resPerc" style="color:var(--orange); border-color:var(--orange); background:#fffaf5;">Pesar Soluto: -</div>
    </div>

    <div class="card">
        <h2>📚 Reactivos Comunes</h2>
        <table>
            <thead><tr><th>Reactivo</th><th>PM</th><th></th></tr></thead>
            <tbody>
                <tr><td>NaCl</td><td>58.44</td><td><button class="btn-use" onclick="fillPM(58.44)">Usar</button></td></tr>
                <tr><td>NaOH</td><td>40.00</td><td><button class="btn-use" onclick="fillPM(40.00)">Usar</button></td></tr>
                <tr><td>KCl</td><td>74.55</td><td><button class="btn-use" onclick="fillPM(74.55)">Usar</button></td></tr>
                <tr><td>Tris</td><td>121.14</td><td><button class="btn-use" onclick="fillPM(121.14)">Usar</button></td></tr>
                <tr><td>EDTA</td><td>292.24</td><td><button class="btn-use" onclick="fillPM(292.24)">Usar</button></td></tr>
                <tr><td>Glucosa</td><td>180.16</td><td><button class="btn-use" onclick="fillPM(180.16)">Usar</button></td></tr>
            </tbody>
        </table>
    </div>

    <div class="card" style="grid-column: span 1;">
        <h2>📝 Notas de Sesión</h2>
        <textarea id="labNotes" placeholder="Escribe aquí tus observaciones, cálculos de pesaje real, etc..."></textarea>
    </div>

</div>

<footer>
    LabCalc Professional 2026 - Herramienta de libre acceso
</footer>

<script>
    function fillPM(val) { document.getElementById('pm1').value = val; calcMolar(); }

    function calcMolar() {
        const m = parseFloat(document.getElementById('m1').value);
        const v = parseFloat(document.getElementById('v1').value);
        const pm = parseFloat(document.getElementById('pm1').value);
        if(m && v && pm) document.getElementById('resMolar').innerText = "Masa necesaria: " + (m * (v/1000) * pm).toFixed(4) + " g";
    }

    function calcDil() {
        const c1 = parseFloat(document.getElementById('c1').value);
        const c2 = parseFloat(document.getElementById('c2').value);
        const v2 = parseFloat(document.getElementById('v2').value);
        if(c1 && c2 && v2) document.getElementById('resDil').innerText = "Tomar de Stock (V1): " + ((c2 * v2) / c1).toFixed(2) + " mL";
    }

    function calcPerc() {
        const p = parseFloat(document.getElementById('p_val').value);
        const v = parseFloat(document.getElementById('p_vol').value);
        if(p && v) document.getElementById('resPerc').innerText = "Pesar Soluto: " + ((p / 100) * v).toFixed(4) + " g";
    }
</script>

</body>
</html>
