# Horacio-Garza <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contacto - QR Code</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrious/4.0.2/qrious.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .container {
            max-width: 500px;
            margin: auto;
            padding: 20px;
            border: 2px solid #333;
            border-radius: 10px;
            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.2);
        }
        h1 {
            color: #333;
        }
        #qrcode {
            margin-top: 20px;
        }
        .email-link {
            display: inline-block;
            margin-top: 15px;
            padding: 10px 15px;
            background-color: #007bff;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        .email-link:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Escanea el QR para enviar un correo</h1>
        <canvas id="qrcode"></canvas>
        <p>O haz clic en el botón para enviar un correo:</p>
        <a href="mailto:horaciogarzag@outlook.com?subject=Contacto desde QR" class="email-link">Enviar Correo</a>
    </div>

    <script>
        // Generar el QR con el enlace al correo
        var qr = new QRious({
            element: document.getElementById("qrcode"),
            value: "mailto:horaciogarzag@outlook.com?subject=Contacto desde QR",
            size: 200
        });
    </script>

</body>
</html>
