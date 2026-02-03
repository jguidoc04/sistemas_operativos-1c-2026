# Guía para instalar Ubuntu en WSL (Windows Subsystem for Linux)

## ¿Qué es WSL?
WSL (Windows Subsystem for Linux) permite ejecutar distribuciones de Linux directamente en Windows sin usar máquinas virtuales pesadas.

## Requisitos
- Windows 10 versión 2004 o superior / Windows 11
- Virtualización habilitada en la BIOS
- Conexión a Internet

## Paso 1: Verificar versión de Windows
Presiona Windows + R y escribe:
```cmd
winver
```

## Paso 2: Instalar WSL automáticamente
Abre PowerShell o CMD como Administrador y ejecuta:
```cmd
wsl --install
```
Reinicia el equipo cuando se solicite.

## Paso 3: Verificar instalación
```cmd
wsl --list --verbose
```

## Paso 4: Configurar Ubuntu
Crea tu usuario y contraseña de Linux cuando se abra Ubuntu por primera vez.

## Paso 5: Actualizar Ubuntu
```bash
sudo apt update
sudo apt upgrade -y
```

## Paso 6: Verificar versión de Ubuntu
```bash
lsb_release -a
```

## Paso 7: Establecer WSL 2
```cmd
wsl --set-version Ubuntu 2
```

## Comandos útiles
```cmd
wsl --shutdown
wsl --list
wsl --unregister Ubuntu
```

## Error común
Si aparece el error 0x80370102, habilita la virtualización en la BIOS.

1) CAUSA 1 (MUY común): Hyper-V NO está activo aunque WSL sí

Aunque no uses Hyper-V, WSL2 lo necesita por debajo.

Haz esto:

Win + R → optionalfeatures
  
Asegúrate de que estén TODAS marcadas:

☑ Windows Subsystem for Linux

☑ Virtual Machine Platform

☑ Hyper-V

Hyper-V Platform

Hyper-V Management Tools

📌 Sí, aunque no lo uses.

👉 Reinicia obligatorio.

2) CAUSA 2: La virtualización está activada en BIOS, pero Windows NO la está usando

Vamos a confirmarlo por comando, no por intuición.

Abre CMD como administrador y ejecuta:
systeminfo | findstr /i "Virtual"

Debes ver:
Virtualization Enabled In Firmware: Yes


❌ Si dice No, el BIOS no quedó guardado correctamente
❌ Si no aparece nada → Windows no detecta virtualización

👉 En ese caso:

Vuelve a BIOS

Desactiva virtualización

Guarda

Reinicia

Vuelve a entrar a BIOS

Actívala de nuevo

Guarda y sal


## Conclusión
Ubuntu en WSL es ideal para aprender Linux y desarrollar sin salir de Windows.
