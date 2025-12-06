# 💻 Guía de Mejores Prácticas

Recomendaciones para desarrolladores que trabajen con estos proyectos.

## 🛠️ Desarrollo y Testing

### Antes de Hacer Cambios

1. **Lee el README** del proyecto específico
2. **Crea una rama** si usas Git: `git checkout -b mi-feature`
3. **Prueba localmente** antes de compartir cambios
4. **Mantén compatibilidad** con versiones anteriores de Python

### Formato de Código

```python
# BIEN: Nombres descriptivos y comentarios claros
def obtener_coordenadas_cursor():
    """Obtiene las coordenadas actuales del cursor del ratón."""
    x, y = mouse.position()
    return x, y

# EVITAR: Nombres poco claros
def f(x):
    return x.pos()
```

### Documentación de Funciones

```python
def descargar_video(url, formato='mp4'):
    """
    Descarga un video de YouTube.
    
    Args:
        url (str): URL del video de YouTube
        formato (str): Formato de descarga (mp4, mp3, etc)
        
    Returns:
        bool: True si la descarga fue exitosa, False en caso contrario
        
    Raises:
        ValueError: Si la URL no es válida
    """
    pass
```

## Testing

### Crear Tests Básicos

```python
# test_main.py
import unittest
from main import mi_funcion

class TestMiFuncion(unittest.TestCase):
    def test_resultado_esperado(self):
        resultado = mi_funcion(parametro)
        self.assertEqual(resultado, valor_esperado)

if __name__ == '__main__':
    unittest.main()
```

### Ejecutar Tests

```bash
python -m unittest test_main.py
```

## 📦 Gestión de Dependencias

### Crear requirements.txt

```bash
pip freeze > requirements.txt
```

### Contenido recomendado

```
# Script-Python-Download-main/requirements.txt
yt-dlp==2023.x.x
requests==2.x.x
```

## Seguridad

### KeyLogger y Privacidad

**IMPORTANTE**: Solo usa scripts de monitoreo en equipos propios

```python
# Siempre solicita confirmación antes de activar monitoreo
respuesta = input("¿Deseas activar el monitoreo de teclas? (s/n): ")
if respuesta.lower() != 's':
    exit()
```

### Variables Sensibles

```python
# NUNCA hagas esto
API_KEY = "abc123xyz456"

# BIEN: Usa variables de entorno
import os
API_KEY = os.getenv('API_KEY', 'default_value')
```

## Convenciones de Nombres

### Variables

```python
# BIEN
velocidad_escritura = 0.1
coordenada_x = 100
archivo_configuracion = "config.json"

# EVITAR
v = 0.1
cX = 100
f = "config.json"
```

### Funciones

```python
# BIEN: Verbo + sustantivo
def obtener_pantalla()
def escribir_texto(texto)
def verificar_conexion()

# EVITAR
def pantalla()
def texto(x)
def conexion()
```

### Constantes

```python
# BIEN: Todo en mayúsculas
TIEMPO_ESPERA_MAXIMO = 30
RUTA_DESCARGAS = "/home/usuario/Descargas"
VERSION_PROGRAMA = "1.0.0"
```

## Debugging

### Usar Logging en Lugar de Print

```python
import logging

# Configurar logging
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s',
    filename='app.log'
)

# Usar logging
logging.info("Programa iniciado")
logging.error("Error crítico ocurrió")
```

### Captura de Excepciones

```python
# BIEN: Específico
try:
    resultado = division(a, b)
except ZeroDivisionError as e:
    logging.error(f"División por cero: {e}")

# EVITAR: Genérico
try:
    resultado = division(a, b)
except Exception:
    pass
```

## Control de Versiones (Git)

### Comandos Útiles

```bash
# Crear rama para feature
git checkout -b feature/nueva-funcionalidad

# Commit descriptivo
git commit -m "Añadir validación de entrada en escritura automática"

# Ver historial
git log --oneline -5

# Merge a main
git checkout main
git merge feature/nueva-funcionalidad
```

### Archivo .gitignore Recomendado

```
# Archivos de Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python

# Entornos virtuales
venv/
env/
ENV/

# Archivos del IDE
.vscode/
.idea/
*.swp
*.swo

# Logs
*.log
logs/

# Descargas
Downloads/
*.mp4
*.mp3

# Archivos de sistema
.DS_Store
Thumbs.db
```

## Recursos

- [PEP 8 - Guía de Estilo Python](https://pep8.org/)
- [Real Python - Best Practices](https://realpython.com/)
- [Documentación Oficial de Python](https://docs.python.org/3/)

## Checklist Antes de Publicar

- [ ] Código probado localmente
- [ ] Sin errores de sintaxis
- [ ] Documentación completa
- [ ] Nombres descriptivos
- [ ] Sin contraseñas/claves hardcodeadas
- [ ] README actualizado
- [ ] requirements.txt incluido
- [ ] .gitignore configurado

---

> Autor: Fravelz
