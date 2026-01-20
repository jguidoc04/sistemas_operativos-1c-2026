# Guía General de CMD (Símbolo del Sistema de Windows)

## 1 ¿Qué es CMD?
CMD (Command Prompt) es una **interfaz de línea de comandos** que permite interactuar con el sistema operativo Windows mediante texto, sin usar interfaz gráfica.

### ¿Para qué se usa?
- Administración del sistema
- Automatización de tareas
- Diagnóstico de errores
- Gestión de archivos y carpetas
- Redes y conectividad

---

## 2 Cómo abrir CMD
- **Windows + R** → escribir `cmd` → Enter
- Menú Inicio → escribir `cmd`
- **Modo administrador**: clic derecho → *Ejecutar como administrador*

---

## 3 Estructura de un comando
```cmd
comando [opciones] [parámetros]
```

Ejemplo

```cmd
dir /w
```

## 4 Navegación por carpetas

### Comandos basicos

| Comando      | Descripción                   |
| ------------ | ----------------------------- |
| `dir`        | Lista archivos y carpetas     |
| `cd carpeta` | Entra a una carpeta           |
| `cd ..`      | Regresa a la carpeta anterior |
| `cd \`       | Va a la raíz del disco        |
| `tree`       | Muestra estructura en árbol   |

Ejemplo

```cmd
C:
cd Users
dir
```

## 5 Crear y eliminar carpetas

### Comandos

```cmd
mkdir nombre
rmdir nombre
rmdir /s nombre
```

Ejercicio 2 

```cmd
mkdir PracticaCMD
cd PracticaCMD
mkdir Docs Img Backups
rmdir Backups
```

## 6 Manejo de archivos


| Comando | Función           |
| ------- | ----------------- |
| `copy`  | Copiar archivos   |
| `move`  | Mover archivos    |
| `del`   | Eliminar archivos |
| `ren`   | Renombrar         |
| `type`  | Mostrar contenido |

Ejercicio 3

```cmd
echo Hola CMD > saludo.txt
type saludo.txt
ren saludo.txt mensaje.txt
del mensaje.txt
```

## 7 Información del sistema

```cmd
systeminfo
hostname
ver
tasklist
```


Ejercicio 4

```cmd
ver
tasklist
```


## 8 Redes y conectividad

| Comando    | Uso                 |
| ---------- | ------------------- |
| `ipconfig` | Información de red  |
| `ping`     | Probar conectividad |
| `tracert`  | Ruta de red         |
| `netstat`  | Conexiones activas  |

Ejercicio 5

```cmd
ipconfig
ping google.com
netstat -an
```

## 9 Comandos útiles del día a día

| Comando        | Función          |
| -------------- | ---------------- |
| `cls`          | Limpiar pantalla |
| `exit`         | Salir de CMD     |
| `help`         | Ayuda general    |
| `help comando` | Ayuda específica |
| `echo`         | Mostrar texto    |
| `pause`        | Pausar ejecución |


Ejercicio 6

```cmd
cls
echo Practicando CMD
pause
```
