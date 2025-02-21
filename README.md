# Probando-otra-vez
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reserva de Salón - COHEP</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #1471ce;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 10vh;
            margin: 0;
            color: white;
        }
        .navbar {
            width: 100%;
            background: #eac508;
            padding: 15px;
            text-align: center;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        .navbar a {
            color: #000000;
            text-decoration: none;
            margin: 0 20px;
            font-size: 18px;
            font-weight: 600;
        }
        .navbar a:hover {
            text-decoration: underline;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            width: 80%;
            max-width: 500px;            
            margin-top: 40px;
            color: black;
        }
        h2 {
            text-align: justify;
            font-weight: 600;
        }
        input, select, button, textarea {
            width: 100%;
            padding: 8px;
            margin: 5px 0;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 14px;
        }
        button {
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 14px;
            padding: 10px;
            border-radius: 8px;
            transition: 0.3s;
        }
        button:hover {
            background-color: #0056b3;
        }
        .franja {
            background-color: #FFC107;
            color: #001f3f;
            padding: 10px;
            font-size: 18px;
            font-weight: bold;
            text-align: justify;
            border-radius: 8px;
            margin-top: 20px;
        }
        
        .checkbox-group {
            display:flow-root ;
            flex-direction: column;
            gap: 20px;
        }
       
    </style>
</head>
<body>
    <div class="navbar">
        <a href="index.html">Inicio</a>
        <a href="galeria.html">Galería de Salones</a>
        <a href="contacto.html">Contacto</a>
    </div>        
    <div class="container">
        <div style="text-align: center; margin-top: 20px;">
            <img src="https://www.elinformativo.hn/wp-content/uploads/2018/02/Cohep.jpg" alt="COHEP" width="300">
        </div>
        <h2>Reserva de Salón</h2>
        <form id="reservaForm">
            <label for="responsable">Persona Responsable:</label>
            <input type="text" id="responsable" name="responsable" required>            
            <label for="evento">Evento:</label>
            <input type="text" id="evento" name="evento" required>            
            <label for="lugar">Lugar:</label>
            <input type="text" id="lugar" name="lugar" required>            
            <label for="fecha_inicio">Fecha de inicio del evento:</label>
            <input type="date" id="fecha_inicio" name="fecha_inicio" required>            
            <label for="fecha_final">Fecha de finalización del evento:</label>
            <input type="date" id="fecha_final" name="fecha_final" required>            
            <label for="hora_inicio">Hora de inicio:</label>
            <input type="time" id="hora_inicio" name="hora_inicio" required>            
            <label for="hora_final">Hora de finalización:</label>
            <input type="time" id="hora_final" name="hora_final" required>            
            <label for="participantes">Cantidad de participantes:</label>
            <input type="number" id="participantes" name="participantes" required>            
            <div class="franja">Requerimientos</div>            
                <div class="checkbox-group">                
                    <label><input type="checkbox"> Laptop</label>
                    <label><input type="checkbox"> Grabación</label>
                    <label><input type="checkbox"> Audio</label>
                    <label><input type="checkbox"> Proyector</label>
                    <label><input type="checkbox"> Video Conferencia</label>
                    <label><input type="checkbox"> Fotos</label>
                    <label><input type="checkbox" id="microfonos" onchange="document.getElementById('cantidad_microfonos').disabled = !this.checked;"> Micrófonos</label>
                    <input type="number" id="cantidad_microfonos" name="cantidad_microfonos" placeholder="Cantidad" disabled>
                    <label><input type="checkbox"> Música ambiental de fondo</label>
                </div>
            <div class="franja">Alimentación</div>           
            <div class="checkbox-group">
                <label><input type="checkbox"> Desayuno</label>
                <label><input type="checkbox"> Almuerzo</label>
                <label><input type="checkbox"> Cena</label>
                <label><input type="checkbox"> Coffee-Break (Bocadillo, gaseosas, café)</label>
                <label><input type="checkbox"> Mini Coffee-Break (Galletas, agua y café)</label>
                <label for="hora_servicio">Hora de servicio:</label>
                <input type="time" id="hora_servicio" name="hora_servicio">
            </div>            
            <div class="franja">Apoyo de Servicio</div>
            <div class="checkbox-group">
                <label><input type="checkbox" id="edecanes" onchange="document.getElementById('cantidad_edecanes').disabled = !this.checked;"> Edecanes</label>
                <input type="number" id="cantidad_edecanes" name="cantidad_edecanes" placeholder="Cantidad" disabled>
                <label><input type="checkbox" id="meseros" onchange="document.getElementById('cantidad_meseros').disabled = !this.checked;"> Meseros</label>
                <input type="number" id="cantidad_meseros" name="cantidad_meseros" placeholder="Cantidad" disabled>
            </div>
            <div class="franja">Forma de Montaje</div>
            <div class="checkbox-group">
                <label><input type="checkbox"> Auditorio</label>
                <label><input type="checkbox"> Herradura</label>
                <label><input type="checkbox"> Mesa Redonda</label>
                <label><input type="checkbox"> Aula</label>
                <label><input type="checkbox"> Imperial</label>
                <label><input type="checkbox"> Mesa de apuntes</label>              
                <label><input type="checkbox" id="mesa_principal" onchange="document.getElementById('cantidad_mesa_principal').disabled = !this.checked;"> Mesa principal</label>
                <input type="number" id="cantidad_mesa_principal" name="cantidad_mesa_principal" placeholder="Cantidad" disabled>
                <label><input type="checkbox"> Mesa para coffee-break</label>
                <label><input type="checkbox"> Mesa de inscripción</label>
                <label><input type="checkbox"> Mesa para computadora</label>
            </div>
            <div class="franja">Licores</div>
            <div class="checkbox-group">
                <label><input type="checkbox" id="vino_basico" onchange="document.getElementById('cantidad_vino_basico').disabled = !this.checked;"> Vino básico</label>
                <input type="number" id="cantidad_vino_basico" name="cantidad_vino_basico" placeholder="Cantidad de botellas" disabled>                
                <label><input type="checkbox" id="vino_tinto" onchange="document.getElementById('cantidad_vino_tinto').disabled = !this.checked;"> Vino tinto</label>
                <input type="number" id="cantidad_vino_tinto" name="cantidad_vino_tinto" placeholder="Cantidad de botellas" disabled>                
                <label><input type="checkbox" id="vino_otro" onchange="document.getElementById('especificar_vino').disabled = !this.checked;"> Otros</label>
                <input type="text" id="especificar_vino" name="especificar_vino" placeholder="Especifique" disabled>
            </div>
            <div class="franja">Forma de Montaje</div>
            <div class="checkbox-group">
                <label><input type="checkbox"> Convocatoria de prensa</label>
                <label><input type="checkbox"> Voceros</label>
                <label><input type="checkbox"> Fotos prensa</label>
                <label><input type="checkbox"> Videos prensa</label>
                <label><input type="checkbox"> Conferencia Prensa</label>
                <label><input type="checkbox"> Nota de presa</label>  
                <label><input type="checkbox"> Moderador/Maestro de ceremonia</label>
                <label for="hora_inicio">Hora</label>
                <input type="time" id="hora_inicio" name="hora_inicio" required>
                <label for="hora_inicio">Hora:</label>
                <input type="time" id="hora_inicio" name="hora_inicio" required>
                <label for="hora_inicio">Hora:</label>
                <input type="time" id="hora_inicio" name="hora_inicio" required>  
            </div>
            <button type="button" onclick="guardarInformacion()">Guardar Información</button>
        </form>
    </div>
</body>
</html>
