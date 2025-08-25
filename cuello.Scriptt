const preguntas = [
  {
    texto: "¿Qué es Starlink?",
    opciones: [
      "es un sistema planetario",
      "Un sistema de mundos",
      "Una red de planetas",
      "un mapa estelar"
    ],
    correcta: 1
  },
  {
    texto: "¿que es el sol?",
    opciones: [
      "un planeta",
      "una estrella",
      "una bola de fuego",
      "un gigante gaseoso"
    ],
    correcta: 2
  },
  {
    texto: "¿como se llama nuestro planeta?",
    opciones: [
      "tierra",
      "jupiter)",
      "saturno",
      "marte"
    ],
    correcta: 1
  },
  {
    texto: "¿el espacio es infinito?",
    opciones: [
      "no",
      "Si",
      "talves",
      "nose"
    ],
    correcta: 2
  }
];

let preguntaActual = 0;

function mostrarPregunta() {
  const p = preguntas[preguntaActual];
  document.getElementById("pregunta").innerText = p.texto;

  const opcionesDiv = document.getElementById("opciones");
  opcionesDiv.innerHTML = "";

  p.opciones.forEach((opcion, index) => {
    const div = document.createElement("div");
    div.className = "opcion";
    div.innerText = opcion;
    div.onclick = () => verificarRespuesta(index);
    opcionesDiv.appendChild(div);
  });

  document.getElementById("resultado").innerText = "";
}

function verificarRespuesta(indiceSeleccionado) {
  const p = preguntas[preguntaActual];
  const resultado = document.getElementById("resultado");

  if (indiceSeleccionado === p.correcta) {
    resultado.innerText = "✅ ¡Correcto!";
  } else {
    resultado.innerText = `❌ Incorrecto. La respuesta era: "${p.opciones[p.correcta]}"`;
  }
}

function siguientePregunta() {
  if (preguntaActual < preguntas.length - 1) {
    preguntaActual++;
    mostrarPregunta();
  } else {
    document.getElementById("pregunta").innerText = "🎉 ¡Trivia finalizada!";
    document.getElementById("opciones").innerHTML = "";
    document.getElementById("resultado").innerText = "";
  }
}

mostrarPregunta();
