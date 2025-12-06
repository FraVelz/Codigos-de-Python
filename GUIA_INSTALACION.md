# Guía de Instalación

Esta guía te ayudará a instalar y configurar todos los proyectos en tu sistema.

## Requisitos Previos

Asegúrate de tener instalado:

- **Python 3.7+**
- **pip** (gestor de paquetes de Python)

## Instalación de Dependencias Globales

```bash
# Actualiza pip a la última versión
pip install --upgrade pip
```

## Instalación por Proyecto

### 1. Descargador de Videos de YouTube

```bash
cd Script-Python-Download-main/
pip install youtube-dl
# O alternativamente
pip install yt-dlp
```

**Uso:**

```bash
python download.py
```

---

### 2. Capturador de Pantalla

```bash
cd Script-Python-Screenshot-main/
pip install pillow
pip install pyautogui
```

**Uso:**

```bash
python program.py
```

---

### 3. Registrador de Teclas (KeyLogger)

```bash
cd Script-Python-KeyLogger-main/
# En Windows:
pip install keyboard
# En Linux:
pip install pynput
```

**Uso:**
```bash
python KeyLogger.py
```

**Nota de Seguridad**: Este programa captura eventos del teclado. Úsalo únicamente en tu propio equipo con propósitos educativos y éticos.

---

### 4. Escritura Automática

```bash
cd Script-Python-AutomaticWriting-main/
pip install pyautogui
```

**Uso:**
```bash
python main.py
```

---

### 5. Gestor de Atajos Personalizados

```bash
cd Script-Python-Top_Shortcut-main/
pip install keyboard
# En Windows:
pip install pyperclip
```

**Uso:**
```bash
python top_shortcut.pyw
```

---

## Verificar la Instalación

Para verificar que Python está correctamente instalado:

```bash
python --version
pip --version
```

## Solución de Problemas

### "Comando python no encontrado"

- En Linux/Mac, puede necesitar usar `python3` en lugar de `python`
- Verifique que Python está en el PATH del sistema

### "ModuleNotFoundError"

- Asegúrate de estar en el directorio correcto antes de ejecutar `pip install`
- Usa `pip list` para verificar los paquetes instalados

### Problemas de Permisos

- En Linux, puede necesitar usar `sudo` o crear un entorno virtual
- Se recomienda usar `venv` para evitar conflictos de dependencias

---

## Crear un Entorno Virtual (Recomendado)

Para aislar las dependencias de cada proyecto:

```bash
# Crear entorno virtual
python -m venv venv

# Activar entorno virtual
# En Windows:
venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate

# Instalar dependencias del proyecto
pip install -r requirements.txt
```

---

**¿Necesitas más ayuda?** Consulta el README específico de cada proyecto.

[Ir al Readme.md Principal](./readme.md)
