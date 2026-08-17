# Memoria del Proyecto: Dedicatoria Personal

## Objetivo del Proyecto
Crear una experiencia web interactiva, íntima y personalizada para dedicar a una persona especial (Mónica). El proyecto consiste en un sitio web de estilo visual muy cuidado, con temática de naturaleza (tonos oscuros, verdes, azules), que incluye un control de acceso mediante una palabra clave y una navegación fluida por secciones (slides) acompañadas de música de fondo.

## Características Principales

1. **Control de Acceso (`index.html`)**:
   - Una página minimalista con efecto de partículas de fondo.
   - Requiere la contraseña **"xilofono"** (validada en JavaScript).
   - Al introducir la contraseña correcta, el panel se desvanece y aparece un mensaje ("Prepara tus audífonos") sobre un fondo semi-transparente que permite ver las partículas desenfocadas detrás. Se establece un token en `sessionStorage` para permitir el paso a la dedicatoria.

2. **Página de Dedicatoria (`dedicatoria.html`)**:
   - **Navegación por secciones (Slides)**: 8 secciones de altura completa (`100vh`). Se navega usando teclado (flechas, espacio), deslizando en móvil (swipe) o con el scroll del ratón.
   - **Protección de enlace directo**: Si se intenta acceder directamente a `dedicatoria.html` sin haber pasado por el index, el código JavaScript redirige automáticamente de vuelta al inicio.
   - **Música de fondo**: Se utiliza un archivo de audio local MP3 que arranca desde el segundo 15. Cuenta con un reproductor flotante animado ("escuchando / pausado") en la esquina inferior derecha.
   - **Animaciones CSS**: Textos e imágenes aparecen suavemente (`fade-in`) a medida que se hace scroll, gracias a un `IntersectionObserver`.
   - **Imágenes y Elementos Decorativos**: 
     - Fotos aportadas al proyecto (`aguila.jpg`, `kayak1.jpg`, `kayak2.jpg`, `kayak3.jpg`). Se restringe a un máximo de 2 por sección.
     - Ilustración generada con IA (Barrio Liberdade con un tono nostálgico).
     - Pájaros minimalistas integrados directamente como código SVG para combinar de manera impecable y sutil con el fondo oscuro, incrustados de forma alternada en cada sección.
   - **Video de YouTube**: Para solucionar restricciones de reproducción local en `iframe`, se implementó una miniatura interactiva. Al hacer clic, se pausa el audio MP3 local automáticamente y la miniatura es reemplazada por el reproductor de YouTube incrustado.

## Despliegue en GitHub Pages

Dado que el proyecto utiliza tecnologías web puras (HTML, CSS y JavaScript nativo) y no requiere servidor backend (Base de Datos o PHP/Node), es ideal para hospedarse en **GitHub Pages**. 

1. Se debe subir todo el contenido de esta carpeta (`index.html`, `dedicatoria.html`, el archivo de audio y la carpeta `images/`) a un repositorio de GitHub.
2. Ir a `Settings` -> `Pages` en el repositorio y habilitar GitHub Pages usando la rama `main` (o `master`).
3. El enlace resultante permitirá visualizar la página con un acceso seguro básico y la música funcionará sin los bloqueos típicos de archivos locales (`file://`).

## Archivos del Proyecto
- `index.html`: Portada de autenticación.
- `dedicatoria.html`: Contenido principal.
- `images/`: Carpeta con las fotos y diseños gráficos.
- `Madrugada - Help Yourself To Me (Official Music video) [AY032xVyMFA].mp3`: Archivo de audio.
- `texto.txt`: Archivo base con los textos originales entregados.
- `memoria.md`: Este documento descriptivo.
