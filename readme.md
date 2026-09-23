# 🧬 Descubridor de Especies 3D (Taxonomía Interactiva)

¡Un juego interactivo HTML diseñado específicamente para estudiantes de **sexto grado**! Este proyecto gamifica el aprendizaje de las **claves dicotómicas** y la **nomenclatura binomial** en las clases de ciencias naturales.

## 🌟 Características

- **20 Preguntas Dicotómicas**: Llevan al estudiante paso a paso a través de características anatómicas, morfológicas y conductuales.
- **Barra de Progreso Animada**: Mantiene la motivación del estudiante visible en todo momento.
- **Diseño "Kid-Friendly"**: Colores pastel vibrantes, tipografía amigable (Nunito) y un uso intensivo de emojis para asociar conceptos biológicos visualmente.
- **Motor Taxonómico Linneano**: Genera un nombre científico en latín real (formato *Género especie*) combinando los sufijos de las respuestas elegidas.
- **Ruta Taxonómica**: Al final del juego, el estudiante puede leer su "bitácora" y ver exactamente qué características de la clave dicotómica definen a su especie.

## 🚀 Cómo usar el juego en clase

1. Descarga o clona este repositorio.
2. Haz doble clic en el archivo `index.html` para abrirlo en cualquier navegador web (Chrome, Edge, Firefox, Safari).
3. **No requiere internet** para funcionar (excepto para cargar la fuente de Google y las imágenes 3D que configures).

## 🎨 Integración de Imágenes 3D Premium

El juego incluye un contenedor especial (`div.image-3d-placeholder`) diseñado para mostrar **imágenes en calidad Premium 3D** de las especies descubiertas. 

**Para agregar tus imágenes 3D generadas:**

1. Genera tus imágenes de las especies usando tu herramienta de IA favorita (como *Midjourney*, *Bing Image Creator* o *Leonardo AI*).
   * *Prompt sugerido para la IA:* `"Un [animal], render 3D premium, estilo Pixar/Disney, hiperrealista, iluminación de estudio, colores vibrantes --ar 1:1"`
2. Guarda las imágenes en una carpeta llamada `img` junto a tu archivo `index.html`.
3. En el código JavaScript (`index.html`), dentro de la función `showResults()`, puedes programar que la imagen cambie dependiendo del hábitat o del nombre generado. 
   
*Ejemplo rápido para reemplazar la imagen desde el código:*
```javascript
// Dentro de la función showResults()
let finalImageSrc = `img/${genus}.png`; // Asegúrate de tener la imagen nombrada igual que el Género generado.
document.getElementById('species-image').src = finalImageSrc;