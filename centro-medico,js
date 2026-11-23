// JavaScript para Centro Médico Vida

let horaActual = "10:00";

// Cambiar la hora seleccionada
function elegirHora(boton, hora) {
  let botones = document.querySelectorAll(".btn-hora");
  for (let i = 0; i < botones.length; i++) {
    botones[i].classList.remove("seleccionado");
    botones[i].textContent = botones[i].textContent.replace(" ✓", "");
  }

  boton.classList.add("seleccionado");
  boton.textContent = hora + " ✓";
  horaActual = hora;
  actualizarResumen();
}

// Actualizar los datos del cuadro de resumen
function actualizarResumen() {
  let esp = document.getElementById("especialidad").value;
  let med = document.getElementById("medico").value;
  let fec = document.getElementById("fecha").value;

  document.getElementById("res-esp").textContent = esp;
  document.getElementById("res-med").textContent = med;
  document.getElementById("res-fec").textContent = fec + ", " + horaActual;
  document.getElementById("res-hor").textContent = horaActual;
}

// Escuchar cambios en los campos
document.getElementById("especialidad").onchange = actualizarResumen;
document.getElementById("medico").onchange = actualizarResumen;
document.getElementById("fecha").onchange = actualizarResumen;

// Botón para agrandar la letra
document.getElementById("btn-letra").onclick = function () {
  document.body.classList.toggle("letra-grande");
};

// Confirmar cita al enviar el formulario
document.getElementById("formulario-cita").onsubmit = function (evento) {
  evento.preventDefault();

  let motivo = document.getElementById("motivo").value;
  if (motivo === "") {
    alert("Por favor, escribe el motivo de consulta.");
    return;
  }

  let numero = Math.floor(Math.random() * 900) + 100;
  let codigo = "CM-2026-X" + numero;
  document.getElementById("codigo").textContent = codigo;

  let estado = document.getElementById("estado");
  estado.className = "estado-confirmado";
  estado.textContent = "● CITA CONFIRMADA - Solicitud Registrada";

  alert("¡Cita confirmada! Tu código de reserva es: " + codigo);
};
