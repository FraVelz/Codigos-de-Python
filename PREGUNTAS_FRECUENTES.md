# Preguntas Frecuentes

## General

**P: ¿Necesito permisos especiales para ejecutar estos scripts?**
R: Algunos scripts (como KeyLogger) pueden requerir permisos elevados en ciertos sistemas operativos. En Windows, ejecuta como Administrador si es necesario.

**P: ¿Estos scripts funcionan en Linux y macOS?**
R: La mayoría funcionan, pero algunos requieren ajustes según el sistema operativo. Lee el README de cada proyecto para detalles específicos.

---

## Instalación

**P: ¿Cómo instalo las dependencias?**
R: Usa `pip install` según el proyecto. Mira GUIA_INSTALACION.md para instrucciones detalladas.

**P: ¿Puedo usar Python 2?**
R: No se recomienda. Usa Python 3.7 o superior.

**P: ¿Qué es un "entorno virtual"?**
R: Es un ambiente aislado para instalar paquetes sin afectar tu sistema. Mira GUIA_INSTALACION.md para crear uno.

---

## Descargador de YouTube

**P: ¿Qué formatos soporta?**
R: Depende de la librería instalada. Generalmente soporta MP4, MP3 y otros formatos comunes.

**P: ¿Es legal descargar videos de YouTube?**
R: Verifica la política de YouTube y los términos de servicio. Respeta los derechos de autor.

---

## Capturador de Pantalla

**P: ¿Dónde se guardan las capturas?**
R: En la carpeta `Images/` dentro del directorio del proyecto.

**P: ¿Puedo cambiar la ubicación de almacenamiento?**
R: Sí, edita el archivo `program.py` y modifica la ruta de la carpeta.

---

## KeyLogger

**P: ¿Es ético usar un keylogger?**
R: Solo para propósitos educativos en equipos propios. Su uso en otros equipos sin consentimiento es ilegal.

**P: ¿Cómo detengo el programa?**
R: Presiona la tecla ESC para mostrar un resumen y terminar, o Ctrl+C en la terminal.

---

## Escritura Automática

**P: ¿Por qué no funciona correctamente el posicionamiento?**
R: Asegúrate de que las coordenadas sean correctas. Prueba con pantallas múltiples desactivadas.

**P: ¿Puedo cambiar la velocidad de escritura?**
R: Sí, edita el parámetro de intervalo en `pyautogui.typewrite()`.

---

## Gestor de Atajos

**P: ¿Mis atajos no funcionan?**
R: Verifica que:
- El JSON tiene formato correcto (sin errores de sintaxis)
- Los atajos tienen una sola palabra
- Los archivos/URLs existen

**P: ¿Cómo añado un atajo nuevo?**
R: Edita `secrets-words.json` añadiendo una nueva entrada en la lista de shortcuts. Mira el README del proyecto.

**P: ¿Puedo usar atajos con múltiples palabras?**
R: Actualmente no está soportado, pero puedes modificar el código para hacerlo.

---

## Solución de Problemas

**P: Obtengo un error "Permission Denied"**
R: Intenta ejecutar con permisos elevados o verifica los permisos del archivo.

**P: El programa se congela**
R: Presiona Ctrl+C para interrumpir. Puede haber un bucle infinito en el código.

**P: ¿Cómo veo registros de errores?**
R: Ejecuta los programas desde terminal/cmd para ver los mensajes de error en tiempo real.

---

**¿No encontraste la respuesta?** Revisa el README del proyecto específico o abre un issue.
