# VPCuts

TUTORIAL DE INSTALACIÓN DE VPCUTS PARA VEGAS PRO 21 CON FFMPEG

1. DESCARGAR FFMPEG

Primero, necesitas descargar FFmpeg, que es el programa encargado de analizar el audio y detectar los silencios.

Entra en la siguiente página:

https://www.gyan.dev/ffmpeg/builds/

Busca la sección de versiones y descarga el archivo:

ffmpeg-release-essentials.zip

Cuando termine la descarga, extrae el contenido del archivo ZIP.

Dentro de la carpeta extraída encontrarás varias carpetas. Entra en la carpeta bin y localiza el archivo ffmpeg.exe.

Este es el ejecutable que necesita el script para funcionar.

Para evitar perderlo o tener que buscarlo constantemente, puedes mover la carpeta de FFmpeg a una ubicación permanente, por ejemplo:

C:\FFmpeg\bin\ffmpeg.exe

2. INSTALAR EL SCRIPT EN VEGAS PRO

Ahora debes instalar el archivo VPCuts.cs.

Localiza la carpeta de instalación de VEGAS Pro 21. Normalmente se encuentra en:

C:\Program Files\VEGAS\VEGAS Pro 21.0\

Dentro de esta ubicación busca la carpeta Script Menu.

Si no existe, créala manualmente.

Copia el archivo VPCuts.cs dentro de esa carpeta.

La ruta final debería quedar así:

C:\Program Files\VEGAS\VEGAS Pro 21.0\Script Menu\VPCuts.cs

Una vez copiado el archivo, cierra y vuelve a abrir VEGAS Pro para que reconozca el script.

3. EJECUTAR VPCUTS

Abre VEGAS Pro 21 y carga el proyecto en el que quieras trabajar.

Selecciona un único evento de audio en la línea de tiempo.

Después, dirígete al menú:

Tools → Scripting → VPCuts

Al ejecutar el script, aparecerá su ventana de configuración.

Dentro de la interfaz encontrarás una opción para seleccionar FFmpeg. Haz clic en ella y busca el archivo ffmpeg.exe que descargaste anteriormente.

Por ejemplo:

C:\FFmpeg\bin\ffmpeg.exe

Selecciona ese archivo. Asegúrate de elegir ffmpeg.exe y no ffprobe.exe ni ffplay.exe.

4. CONFIGURAR LA DETECCIÓN DE SILENCIOS

Una vez configurado FFmpeg, podrás ajustar los parámetros de detección.

Umbral de silencio (-35 dB): determina qué nivel de volumen se considera silencio. Cuanto más alto sea el umbral, más sonidos pueden identificarse como silencio.

Duración mínima (0.50 s): establece cuánto tiempo debe durar un silencio para que pueda detectarse.

Margen conservado (0.10 s): añade un pequeño margen alrededor de los sonidos para evitar cortes demasiado ajustados.

Puedes modificar estos valores dependiendo del tipo de grabación y del resultado que quieras conseguir.

5. PREVISUALIZAR LOS CORTES

Antes de aplicar los cambios, puedes utilizar la vista previa para comprobar qué partes del audio serán eliminadas.

Las secciones rojas representan los fragmentos que se eliminarán.

Las secciones blancas representan los fragmentos que se conservarán.

Revisa la distribución de los cortes y ajusta los parámetros si es necesario.

Cuando estés satisfecho con el resultado, pulsa Aplicar cortes y confirma la operación.

6. MODOS DE FUNCIONAMIENTO

VPCuts incluye dos modos principales:

Solo Audio: modifica únicamente la pista de audio seleccionada. Es la opción recomendada cuando quieres eliminar silencios sin afectar el video.

Video + Audio: modifica la pista de audio seleccionada y una única pista de video asociada al proceso. Si no puede determinarse una sola pista de video, el script trabaja únicamente sobre el audio.

IMPORTANTE: las demás pistas del proyecto no se desplazan. Si tienes música, subtítulos, efectos de sonido u otros elementos en pistas diferentes, tendrás que revisar su sincronización después de aplicar los cortes.

7. SOLUCIÓN DE PROBLEMAS

El script no aparece en VEGAS:

Comprueba que VPCuts.cs esté dentro de la carpeta Script Menu correspondiente a VEGAS Pro 21. Después, reinicia el programa.

VEGAS no encuentra FFmpeg:

Abre la configuración del script y vuelve a seleccionar manualmente ffmpeg.exe. Comprueba que el archivo exista en la ubicación indicada.

La vista previa no funciona:

Verifica que FFmpeg esté correctamente instalado y que hayas seleccionado el ejecutable correcto.

El script no permite analizar el audio:

Comprueba que hayas seleccionado exactamente un evento de audio, que su archivo de origen exista y que el evento utilice una velocidad de reproducción de 1.0.

8. RECOMENDACIONES FINALES

Antes de aplicar los cortes, guarda una copia de seguridad de tu proyecto VEGAS utilizando la opción Guardar como.
También es recomendable realizar una prueba con un proyecto pequeño antes de utilizar el script en una edición importante.

Recuerda que VPCuts y FFmpeg son programas independientes: VEGAS ejecuta el script, mientras que FFmpeg se encarga del análisis del audio y la detección de silencios.
