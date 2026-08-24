Readme · MD
🎸 Los Olvidados del Rock Mexicano y Mas.
1. Nombre del proyecto

Recomendación de proyectos musicales de Rock Mexicano

2. Descripción

Descubre bandas recomendadas desde los años 60 hasta los 2020, con enlaces directos a su Facebook y Spotify. Explora, escucha y conoce cómo ha evolucionado el rock mexicano y proyectos que valen la pena escuchar a través de este espacio.

3. Tecnologías
HTML
CSS
Bootstrap
JavaScript
Git
GitHub
Claude AI
4. Proceso con IA

Prompt #1

Quiero una paleta de colores más típica del rock mexicano, no tan rosa/naranja/morado, algo más enfocado en décadas: 60s colores más psicodélicos, 70s más progresivos, 80s más electrónica y punk, 90s más alternativo, 2000s algo más novedoso. No lo metas al código, solo dame ideas.

Prompt #2

En el botón de "Conocer más" o "Explora más" irá a dar a otra página con información relevante de varios artistas. Lo que quiero es hacer cuadros de reseñas donde salgan otros cuatro artistas, en forma redonda, con 2 álbumes recomendados y abajo unos enlaces de YouTube. Quiero que esta página tenga cosas dinámicas — dame ideas, ya que ese será el esqueleto para las demás décadas.

5. Código generado vs. código propio
Generado con ayuda de la IA

La IA me ayudó bastante en los estilos, sobre todo en las animaciones:

css
/* Anillo exterior, gira sin parar */
.disco-giratorio::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: 50%;
  border: 3px dashed var(--acento-pagina, var(--mostaza));
  animation: girar-disco 7s linear infinite;
}

/* Segundo anillo, más tenue, gira al revés (efecto vinilo) */
.disco-giratorio::after {
  content: "";
  position: absolute;
  inset: 8px;
  border-radius: 50%;
  border: 1px solid rgba(255, 255, 255, 0.25);
  animation: girar-disco 5s linear infinite reverse;
}

.hero-overlay-degradado {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(24, 79, 4, 0.8), rgba(147, 4, 11, 0.8));
  z-index: 1;
}

.hero-contenido {
  position: relative;
  z-index: 2;
  min-height: 320px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
Código propio
css
.foto-artista {
  position: absolute;
  inset: 18px;
  width: calc(100% - 36px);
  height: calc(100% - 36px);
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--carbon-claro);
}

/* ===============================
   VARIABLES DE LA PALETA (fondo carbón + acentos por década)
   =============================== */
:root {
  --carbon: #1a1a1a;
  --carbon-claro: #242424;
  --oxido: #b23a2e;
  --mostaza: #0a4c4b;

  /* Acento propio de cada década */
  --acento-60: #d4a017;   /* mostaza psicodélica */
  --acento-70: #a67c27;   /* dorado envejecido progresivo */
  --acento-80: #00e5ff;   /* cian eléctrico punk/synth */
  --acento-90: #a6431b;   /* óxido grunge/alternativo */
  --acento-2000: #0057ff; /* azul digital */
  --acento-2010: #16a394; /* verde-azulado indie/streaming */
  --acento-2020: #e85d3f; /* coral vibrante */
}

/* ===============================
   TIPOGRAFÍA (personalización 1)
   =============================== */
body {
  font-family: 'Segoe UI', Verdana, sans-serif;
  background-color: var(--carbon);
  color: #e8e8e8;
}

/* ===============================
   NAVBAR (personalización 2: color)
   =============================== */
.mi-navbar {
  background-color: #141414;
  border-bottom: 3px solid var(--oxido);
}

.mi-navbar .nav-link {
  color: #e8e8e8;
  transition: color 0.3s ease; /* preparación para hover */
}

/* Hover en los links del navbar (personalización 3: hover) */
.mi-navbar .nav-link:hover {
  color: var(--mostaza);
}

/* ===============================
   TÍTULO PRINCIPAL (degradado)
   =============================== */
.titulo-principal {
  background: linear-gradient(135deg, var(--oxido), var(--mostaza));
  padding: 60px 20px;
}

/* ===============================
   TÍTULOS DE CADA DÉCADA (personalización 4: bordes)
   =============================== */
.titulo-decada {
  color: var(--mostaza);
  border-left: 6px solid var(--oxido);
  padding-left: 12px;
  margin-bottom: 15px;
}

/* Cada década toma su propio acento */
#decada60 .titulo-decada   { color: var(--acento-60);   border-left-color: var(--acento-60); }
#decada70 .titulo-decada   { color: var(--acento-70);   border-left-color: var(--acento-70); }
#decada80 .titulo-decada   { color: var(--acento-80);   border-left-color: var(--acento-80); }
#decada90 .titulo-decada   { color: var(--acento-90);   border-left-color: var(--acento-90); }
#decada2000 .titulo-decada { color: var(--acento-2000); border-left-color: var(--acento-2000); }
#decada2010 .titulo-decada { color: var(--acento-2010); border-left-color: var(--acento-2010); }
#decada2020 .titulo-decada { color: var(--acento-2020); border-left-color: var(--acento-2020); }

/* ===============================
   CARDS (personalización 5: bordes + tamaño de imagen)
   =============================== */
.card-banda {
  background-color: var(--carbon-claro);
  border: none;
  border-top: 4px solid var(--oxido);
  border-radius: 16px;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.5);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* hover */
  animation: aparecer 0.6s ease both;
}

#decada60 .card-banda   { border-top-color: var(--acento-60); }
#decada70 .card-banda   { border-top-color: var(--acento-70); }
#decada80 .card-banda   { border-top-color: var(--acento-80); }
#decada90 .card-banda   { border-top-color: var(--acento-90); }
#decada2000 .card-banda { border-top-color: var(--acento-2000); }
#decada2010 .card-banda { border-top-color: var(--acento-2010); }
#decada2020 .card-banda { border-top-color: var(--acento-2020); }

/* Hover en las cards: se eleva y crece un poco */
.card-banda:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 16px 28px rgba(0, 0, 0, 0.6);
}

.card-banda .card-title {
  color: #f2f2f2;
}

.card-banda .card-text {
  color: #b8b8b8;
}

/* Contenedor de la imagen para el overlay al hacer hover */
.card-img-wrap {
  overflow: hidden;
  position: relative;
}

.card-banda img {
  height: 220px;
  width: 100%;
  object-fit: cover;
  transition: transform 0.4s ease;
}

/* La imagen hace zoom suave al pasar el mouse */
.card-banda:hover img {
  transform: scale(1.08);
}

/* Animación de entrada de las cards */
@keyframes aparecer {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ===============================
   BOTONES personalizados (personalización 6: colores + margen)
   =============================== */
.btn-mi-boton {
  background-color: var(--oxido);
  color: #ffffff;
  border: none;
  border-radius: 20px;
  padding: 6px 16px;
  margin: 4px 4px 0 0;
  font-size: 0.9rem;
}

.btn-mi-boton:hover {
  background-color: var(--mostaza);
  color: #1a1a1a;
}
6. Aprendizaje

No sabía cómo animar algunas secciones, y la IA me ayudó bastante a darle un poco más de dinamismo a la página.

También en la paleta de colores me recomendó tonos que iban de acuerdo a lo que quería, aunque hubo veces que yo mismo la modifiqué porque no me gustaba cómo se veía. Diría que fue un trabajo 50/50 entre lo que propuso la IA y mis propios ajustes.

7. Reflexión
¿Hubo algún momento en que la IA generó código que no comprendía?

Sí, hubo varios momentos. Aprendí que hay que saber preguntar bien para no repetir cambios innecesarios, ya que a veces al pedir un ajuste, la IA modificaba otras partes del código sin que yo lo pidiera.

¿Qué hice al respecto?

Siempre respaldé mis prototipos antes de volver a pedir o copiar nueva información, para no perder avances si algo salía mal.

📸 Capturas de la página


