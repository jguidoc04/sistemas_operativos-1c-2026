# Guía de Gestión de Archivos y Permisos en Bash

##  Listar archivos
```bash
ls
ls -l
ls -a
ls -lh
```

##  Crear archivos y carpetas
```bash
touch archivo.txt
mkdir carpeta
mkdir -p ruta/completa/de/carpetas
```

##  Ver contenido de archivos
```bash
cat archivo.txt
less archivo.txt
more archivo.txt
head archivo.txt
tail archivo.txt
tail -f archivo.log
```

##  Copiar archivos y carpetas
```bash
cp archivo.txt copia.txt
cp archivo.txt /ruta/destino/
cp -r carpeta/ carpeta_backup/
```

##  Mover y renombrar
```bash
mv archivo.txt nuevo_nombre.txt
mv archivo.txt /otra/ruta/
```

##  Eliminar archivos y carpetas
```bash
rm archivo.txt
rm -r carpeta/
rm -f archivo.txt
rm -rf carpeta/
```

##  Buscar archivos
```bash
find /ruta -name "archivo.txt"
find . -type f
find . -name "*.log"
```

## Gestión de permisos

### Ver permisos
```bash
ls -l
```

### Cambiar permisos (chmod)

#### Modo simbólico
```bash
chmod u+x archivo.sh
chmod g+w archivo.txt
chmod o-r archivo.txt
chmod a+r archivo.txt
```

#### Modo numérico
```bash
chmod 755 archivo.sh
chmod 644 archivo.txt
```

##  Cambiar propietario y grupo
```bash
chown usuario archivo.txt
chown usuario:grupo archivo.txt
chown -R usuario:grupo carpeta/
```

##  Cambiar grupo
```bash
chgrp grupo archivo.txt
```

##  Permisos avanzados (ACL)
```bash
getfacl archivo.txt
setfacl -m u:usuario:rwx archivo.txt
```

##  Practica paso a paso

* Paso 1: Crear un directorio de trabajo

```bash
mkdir practica_bash
cd practica_bash
```

Verifica

```bash
pwd
```

* Paso 2: Crear archivos y carpetas
```bash
mkdir documentos scripts
touch documentos/notas.txt
touch scripts/script.sh
```

 Verifica:
```bash
ls -R
```

* Paso 3: Escribir contenido en un archivo
echo "Hola, esta es mi primera práctica en Bash" > documentos/notas.txt


 Ver contenido:

```bash
cat documentos/notas.txt
```

* Paso 4: Copiar archivos
cp documentos/notas.txt documentos/notas_backup.txt


Verifica:
```bash
ls documentos
```

* Paso 5: Mover y renombrar archivos
```bash
mv documentos/notas_backup.txt documentos/notas_copia.txt
```