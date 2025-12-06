# Gestor de Atajos Personalizados

Proyecto #5 con Python. Controla tus propios atajos de teclado.

Programa en Python que te permite crear atajos de teclado personalizados y configurarlos para ejecutar acciones, abrir páginas web, abrir aplicaciones o apagar la PC.

## Configuración

En el directorio del programa existe un archivo llamado `secrets-words.json`. Es un archivo JSON que debes modificar para configurar tus atajos de teclado personalizados.

> **Nota importante**: Hasta ahora solo se han probado atajos con una palabra por atajo. Si no sigues esta recomendación, el archivo puede no funcionar correctamente.

## Cómo Agregar Atajos o Palabras Clave

El archivo `.json` tiene el siguiente formato:

```json
{
    "shortcuts": [
        ["local", "fravelz", "turnOff.bat"],
        ["web", "youtube", "https://youtube.com/"],
        ["cmd", "notepad", "notepad.exe"]
    ]
}
```

### Estructura de cada Atajo

Cada atajo tiene esta estructura:

```json
["web", "youtube", "https://youtube.com/"]
```

Donde cada elemento significa:

- **"web"** (Tipo de acción): Especifica qué tipo de función ejecutar:
  - `local`: Ejecuta un archivo que está en el mismo directorio que el programa
  - `web`: Abre una página web en el navegador
  - `cmd`: Abre una aplicación del PC

- **"youtube"** (Palabra clave): La palabra que escribes mientras el programa está corriendo. Cuando escribas esta palabra, se ejecutará la función asociada.

- **"https://youtube.com/"** (Ruta o código): Lo que se ejecutará. Puede ser:
  - Una dirección web (para tipo `web`)
  - Un nombre de archivo (para tipo `local`)
  - Un comando ejecutable (para tipo `cmd`)

### Ejemplo Práctico

```json
["web", "youtube", "https://youtube.com/"]
```

Este atajo significa: _"Abre un **sitio web**, cuando escriba **youtube**, se abrirá la dirección **https://youtube.com/**"_

## Agregar Más Atajos

Cada vez que quieras añadir más comandos y atajos, simplemente:

1. Pon una coma (**,**) al final del último atajo
2. Continúa escribiendo siguiendo el mismo formato

## Recomendaciones

- Los atajos deben ser **preferentemente solo palabras en minúsculas y números**. Si no sigues esto, los atajos pueden no funcionar.

- Para una mejor experiencia, se recomienda **mover el programa (Top Shortcut) a la carpeta de inicio** del usuario para que los atajos estén disponibles cada vez que enciendas la PC:

```
C:\Users\%USERNAME%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
```

---

> Autor: Fravelz
