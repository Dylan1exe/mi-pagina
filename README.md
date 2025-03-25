<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selecciona tu género</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin: 50px;
        }
        .container {
            max-width: 400px;
            margin: auto;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            font-size: 18px;
            cursor: pointer;
        }
        #resultado {
            margin-top: 20px;
        }
        img {
            max-width: 100%;
            height: auto;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>¿Eres hombre o mujer?</h2>
        <button onclick="mostrarMensaje('hombre')">Hombre</button>
        <button onclick="mostrarMensaje('mujer')">Mujer</button>
        <div id="resultado"></div>
    </div>

    <script>
        function mostrarMensaje(genero) {
            let mensaje = "";
            let imagen = "";
            
            if (genero === "hombre") {
                mensaje = "Eres un gran hombre!";
                imagen = "https://via.placeholder.com/300x200/007BFF/FFFFFF?text=Hombre";
            } else {
                mensaje = "Eres una gran mujer!";
                imagen = "https://via.placeholder.com/300x200/FF69B4/FFFFFF?text=Mujer";
            }
            
            document.getElementById("resultado").innerHTML = `<h3>${mensaje}</h3><img src="${imagen}" alt="Imagen">`;
        }
    </script>
</body>
</html>
