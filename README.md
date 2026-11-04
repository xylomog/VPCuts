# VPCuts – Automatic Silence Remover for VEGAS Pro

VPCuts es un script para VEGAS Pro 21 que permite detectar y eliminar automáticamente los silencios de una pista de audio mediante FFmpeg.

Su objetivo es agilizar el proceso de edición, eliminando pausas innecesarias y cerrando los espacios resultantes para conseguir una línea de tiempo más limpia y fluida.

### Características principales

- **Detección automática de silencios:** analiza el audio mediante FFmpeg para identificar fragmentos sin sonido.
- **Umbral de detección configurable:** permite ajustar el nivel de volumen considerado como silencio.
- **Duración mínima:** establece cuánto debe durar un silencio para que sea detectado.
- **Margen de conservación:** añade tiempo alrededor de los fragmentos con sonido para evitar cortes demasiado ajustados.
- **Vista previa de cortes:** visualiza los fragmentos que se eliminarán y los que se conservarán antes de aplicar los cambios.
- **Modo Solo Audio:** elimina silencios modificando únicamente la pista de audio seleccionada.
- **Modo Video + Audio:** permite aplicar los cortes también a una única pista de video objetivo.
- **Cierre automático de espacios:** desplaza los eventos posteriores en las pistas modificadas para cerrar los espacios generados por los cortes.

### Requisitos

- VEGAS Pro 21.
- FFmpeg instalado en el equipo.
- Un evento de audio seleccionado en la línea de tiempo.

### Tecnologías

- C#
- VEGAS Pro Scripting API
- FFmpeg

VPCuts está diseñado para simplificar la eliminación de silencios y reducir el tiempo dedicado a tareas repetitivas durante la edición de video.
