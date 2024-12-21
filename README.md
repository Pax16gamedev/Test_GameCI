# Errores en despliegue WebGL con GH Pages

**No olvidar que para funcione GH Pages el repositorio debe ser público**

> Unable to parse Build/Roguelike.framework.js.br! This can happen if build compression was enabled but web server hosting the content was misconfigured to not serve the file with HTTP Response Header "Content-Encoding: br" present. Check browser Console and Devtools Network tab to debug.

## Posibles soluciones: 

### Deshabilitar la compresión en Unity
Esta es la solución más sencilla si no puedes configurar los encabezados HTTP en el servidor (como ocurre con GitHub Pages).

1. Abre tu proyecto de Unity.
2. Ve a File > Build Settings > Player Settings.
3. En la sección Publishing Settings, busca la opción Compression Format.
4. Selecciona Disabled en lugar de Brotli o Gzip.
5. Vuelve a generar la build y sube los nuevos archivos a GitHub Pages.

### Habilitar Unity Loader para manejar compresión
Unity puede manejar la descompresión de los archivos si activas la opción de "Decompression Fallback". Esto requiere un pequeño ajuste en Unity:

1. Abre File > Build Settings > Player Settings.
2. En Publishing Settings, habilita la opción Decompression Fallback.
3. Genera nuevamente la build.
4. Sube los nuevos archivos a GitHub Pages.
5. Esto permite que Unity descargue los archivos comprimidos y los descomprima directamente en el navegador, eliminando la dependencia del encabezado Content-Encoding.
