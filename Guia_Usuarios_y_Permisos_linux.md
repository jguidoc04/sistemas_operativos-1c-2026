# Guía básica de usuarios y permisos en Linux

## 1. Crear usuarios

### Crear un usuario nuevo
```bash
sudo useradd nombre_usuario
```

### Crear usuario con directorio home
```bash
sudo useradd -m nombre_usuario
```

### Crear usuario y asignar shell
```bash
sudo useradd -m -s /bin/bash nombre_usuario
```

### Asignar contraseña al usuario
```bash
sudo passwd nombre_usuario
```

---

## 2. Editar usuarios

### Cambiar nombre de usuario
```bash
sudo usermod -l nuevo_nombre nombre_actual
```

### Cambiar directorio home
```bash
sudo usermod -d /nuevo/home nombre_usuario
```

### Agregar usuario a un grupo
```bash
sudo usermod -aG grupo nombre_usuario
```

---

## 3. Eliminar usuarios

### Eliminar usuario (sin borrar home)
```bash
sudo userdel nombre_usuario
```

### Eliminar usuario y su directorio home
```bash
sudo userdel -r nombre_usuario
```

---

## 4. Cambiar de usuario

### Cambiar a otro usuario
```bash
su nombre_usuario
```

### Cambiar a otro usuario cargando su entorno
```bash
su - nombre_usuario
```

### Volver al usuario anterior
```bash
exit
```

---

## 5. Superusuario (root)

### Ejecutar comando como superusuario
```bash
sudo comando
```

### Cambiar a root
```bash
sudo su
```

### Ejecutar sesión completa como root
```bash
sudo -i
```

---

## 6. Permisos de archivos y directorios

### Ver permisos
```bash
ls -l
```

Ejemplo:
```bash
-rwxr-xr--
```

- r = lectura
- w = escritura
- x = ejecución

Orden:
- Usuario
- Grupo
- Otros

### Cambiar permisos con chmod (modo simbólico)
```bash
chmod u+x archivo.sh
chmod g+w archivo.txt
chmod o-r archivo.txt
```

### Cambiar permisos con chmod (modo numérico)
```bash
chmod 755 archivo.sh
chmod 644 archivo.txt
```

### Cambiar propietario de un archivo
```bash
sudo chown usuario archivo.txt
```

### Cambiar propietario y grupo
```bash
sudo chown usuario:grupo archivo.txt
```

---

## 7. Práctica guiada

### Objetivo
Practicar la gestión de usuarios y permisos en Linux.

### Pasos

1. Crear un usuario llamado `estudiante`
```bash
sudo useradd -m estudiante
sudo passwd estudiante
```

2. Crear un archivo como root
```bash
sudo touch /home/estudiante/practica.txt
```

3. Cambiar el propietario del archivo
```bash
sudo chown estudiante /home/estudiante/practica.txt
```

4. Asignar permisos de lectura y escritura solo al usuario
```bash
chmod 600 /home/estudiante/practica.txt
```

5. Cambiar al usuario estudiante
```bash
su - estudiante
```

6. Intentar ejecutar el archivo (debe fallar)
```bash
./practica.txt
```

7. Volver a root y dar permiso de ejecución
```bash
exit
sudo chmod 700 /home/estudiante/practica.txt
```

8. Verificar permisos
```bash
ls -l /home/estudiante/practica.txt
```

---


