# México Satelital — Clima en Tiempo Real 🌍🛰️

Visualizador meteorológico interactivo de alto rendimiento para el sector de la República Mexicana, que obtiene y renderiza imágenes satelitales en tiempo real del satélite **GOES-19 (East)** de la NOAA. 

Este proyecto es **100% estático**, optimizado para cargarse de forma instantánea y diseñado para poder alojarse de manera gratuita y segura en plataformas como **GitHub Pages**, Vercel o Netlify.

---

## ✨ Características

* **🛰️ Tres Productos Satelitales en Tiempo Real:**
  * **GeoColor:** Combinación de bandas visibles e infrarrojas para color verdadero durante el día y falso color infrarrojo en la noche (útil para detectar nubes bajas y niebla).
  * **GLM (Rayos):** Mapa continuo de la extensión e intensidad de la actividad eléctrica y relámpagos.
  * **Infrarrojo (Banda 13):** Banda térmica de ondas largas a 10.3 µm, ideal para medir la temperatura en el tope de nubes e identificar tormentas severas.
* **🔍 Interactividad de Alta Precisión:**
  * Zoom suave a través de botones dedicados o usando la rueda del mouse / gestos táctiles.
  * Paneo (arrastrar y soltar) para explorar zonas específicas del mapa de México a alta resolución.
* **⌨️ Atajos de Teclado:**
  * Presiona `R` para restaurar la vista y centrar el mapa.
  * Presiona `Espacio` para refrescar las imágenes satelitales con los datos más recientes.
* **📱 Diseño Premium & Responsivo:**
  * Interfaz de usuario pulida con modo oscuro de alta fidelidad, tipografía moderna, bordes suavizados y sutiles animaciones.
  * Adaptable a pantallas de escritorio, tabletas y móviles.

---

## 🛠️ Tecnologías Utilizadas

* **Framework:** [Svelte 5](https://svelte.dev/) (para una reactividad ligera y veloz)
* **Herramienta de Construcción:** [Vite](https://vite.dev/) (para compilación instantánea y optimizada)
* **Estilos:** Vanilla CSS (CSS puro con variables CSS personalizadas y diseño responsivo)
* **API de Datos:** Servidores CDN públicos de la [NOAA (National Oceanic and Atmospheric Administration)](https://www.noaa.gov/)

---

## 🚀 Instalación y Desarrollo Local

Sigue estos pasos para ejecutar el visualizador en tu computadora:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git
   cd nombre-del-repositorio
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Iniciar el servidor de desarrollo:**
   ```bash
   npm run dev
   ```
   Abre la dirección `http://localhost:5173` (o la indicada en la terminal) en tu navegador.

---

## 📦 Despliegue en GitHub Pages

Dado que la aplicación es puramente estática, desplegarla en GitHub Pages es extremadamente sencillo. 

### Paso 1: Generar los archivos de producción
Ejecuta el siguiente comando para compilar el proyecto:
```bash
npm run build
```
Esto creará una carpeta llamada `dist/` en la raíz de tu proyecto con los archivos optimizados (HTML, CSS y JS comprimidos).

### Paso 2: Publicar
Puedes usar herramientas como el paquete `gh-pages` para publicarlo directamente:

1. Instalar la herramienta de despliegue:
   ```bash
   npm install -D gh-pages
   ```
2. Añadir los scripts de despliegue en tu `package.json`:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
3. Ejecutar el despliegue:
   ```bash
   npm run deploy
   ```

O alternativamente, subir el contenido de la carpeta `dist/` a una rama de publicación en tu repositorio de GitHub, y configurar **GitHub Pages** en la pestaña de *Settings* de tu repositorio para que sirva desde esa rama.

---

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Las imágenes y datos satelitales son propiedad pública proveídos por la NOAA.
