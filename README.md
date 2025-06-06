---
layout: default
title: Registro de Servicio
---

# 📄 Registro de Uso de Servicio

Por favor, completa el siguiente formulario para registrar el uso del servicio.

<form id="registroForm" method="GET" action="https://script.google.com/macros/s/AKfycbzyVlduzCWVu-4VOAjL18rMH0W3BflTbAnSZwiN8t-ey1Sd1djPXALuNJntAyYvn1Eg/exec">
  <label for="id">ID:</label><br>
  <input type="text" id="id" name="id" readonly><br><br>

  <label for="usuario">Usuario:</label><br>
  <input type="text" id="usuario" name="usuario" required><br><br>

  <label for="fechaHora">Fecha y Hora:</label><br>
  <input type="text" id="fechaHora" name="fechaHora" readonly><br><br>

  <button type="submit">Enviar</button>
</form>

<script>
  // Obtener ID desde la URL (si existe)
  const params = new URLSearchParams(window.location.search);
  document.getElementById('id').value = params.get('id') || 'N/A';

  // Obtener fecha y hora actual
  const fechaHora = new Date().toLocaleString('es-MX', {
    timeZone: 'America/Mexico_City'
  });
  document.getElementById('fechaHora').value = fechaHora;
</script>
