# como encontrar el explorador

## explorador por barra
![alt text](imagenes/image-1.png)


## windows + E
![alt text](image-1.png)

## windows + R
![alt text](image-2.png)

## control + shift + esc
![alt text](image-3.png)

## windows + X
![alt text](image-4.png)
-------------------------------

# parte 2

Una vez estés en el Explorador de archivos, identifica el panel izquierdo y selecciona Este equipo.
Localiza la unidad C: (unidad del sistema).
Haz clic derecho sobre C: → Propiedades.
Busca el campo Sistema de archivos e identifica si es NTFS, FAT32, etc.
Justifica por qué Windows 11 utiliza ese sistema de archivos.

![alt text](image-5.png) "juntos"
![alt text](image-6.png)

Windows 11 utiliza NTFS (New Technology File System) como su sistema de archivos principal por defecto debido a una combinación de seguridad, estabilidad, compatibilidad heredada y funciones avanzadas que los sistemas de archivos más antiguos (como FAT32) simplemente no pueden ofrecer.

-------------------------------

## Parte B. Comprobación mediante PowerShell
    
# Prueba 5 formas diferentes de acceder a PowerShell.

Existen diversas formas de abrir PowerShell en Windows 11:

    Menú Inicio (búsqueda rápida)
        Abre el Menú Inicio.
        Escribe PowerShell.
        Pulsa Enter o haz clic en Windows PowerShell.
![alt text](image-7.png)


    

    Atajo de teclado (Win + X)
        Pulsa Windows + X para abrir el menú avanzado.
        Selecciona Windows PowerShell o Windows PowerShell (Administrador).
        (En algunas versiones aparece Windows Terminal, explicado más abajo.)
![alt text](image-8.png)

    Cuadro de Ejecutar (Win + R)
        Pulsa Windows + R.
        Escribe powershell y pulsa Enter.
        Para abrirlo como administrador:

        "powershell -Command "Start-Process powershell -Verb runAs"

![alt text](image-9.png)

    Desde el Explorador de archivos
        Navega a cualquier carpeta.
        Haz clic en la barra de direcciones.
        Escribe powershell para abrirlo en esa ruta.

![alt text](image-10.png)

    Desde una ventana CMD

        CMD (Símbolo del sistema): consola antigua basada en texto, menos potente que PowerShell.

        Si tienes abierto CMD, escribe:

        powershell

# 2. Abre la aplicación Windows PowerShell.
    Ejecuta:

    Get-Volume
![alt text](image-11.png)
## que es get-volumen?
Su función principal es darte un informe rápido y detallado sobre el estado de todos los discos, 
particiones y unidades de almacenamiento (discos duros, SSD, pendrives USB) que están conectados a tu ordenador en ese momento

## Comprueba que el sistema de archivos coincide con el visto en la interfaz gráfica.

![alt text](image-12.png)

# Ejercicio 2. Gestión del sistema de archivos mediante herramientas gráficas

    Abre el Explorador de archivos.
    Activa Ver → Mostrar → Elementos ocultos para visualizar carpetas del sistema.
    Explora las siguientes rutas una por una:
        C:\
        C:\Windows
        C:\Program Files
        C:\Users
        C:\ProgramData
    En cada carpeta:
        Observa su contenido.
        Identifica qué tipo de archivos o subcarpetas contiene.
        Trata de deducir su función general dentro del sistema.
    Registra brevemente la función de cada directorio principal.

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

## En cada carpeta:

    Observa su contenido.
    Identifica qué tipo de archivos o subcarpetas contiene.
    Trata de deducir su función general dentro del sistema.

Registra brevemente la función de cada directorio principal.

---

## Ejercicio 3. Gestión del sistema de archivos mediante comandos (PowerShell)

    Abre PowerShell.
    Ejecuta:

|Get-ChildItem C:\

![alt text](image-20.png)

Observa qué elementos aparecen en la raíz del sistema.

---
4.
    Ejecuta ahora:

Get-ChildItem C:\Windows -Directory

![alt text](image-21.png)

---

## Analiza las carpetas mostradas y compáralas con lo visto en el Explorador.
    Ejecuta:

Get-Item C:\Users

    Observa los metadatos que aparecen (tamaño, atributos, etc.).

![alt text](image-22.png)

# Ejercicio 4. Estructura de directorios: análisis y funciones

# Localiza y examina estas carpetas clave:
        C:\Windows → archivos esenciales del sistema operativo.

![alt text](image-23.png)

        C:\Program Files → aplicaciones instaladas de 64 bits.
![alt text](image-24.png)

        C:\Program Files (x86) → aplicaciones de 32 bits.
![alt text](image-25.png)

        C:\Users → perfiles y datos de usuario.
![alt text](image-26.png)
        C:\ProgramData → datos compartidos y configuraciones globales.
![alt text](image-27.png)

    Describe qué función cumple cada carpeta.
    Indica qué tipo de información contiene cada una:
        Archivos del sistema
        Programas instalados
        Configuraciones
        Datos de usuario
        Datos globales o compartidos
---

## Ejercicio 5. Rutas absolutas y relativas

    Abre PowerShell.
    Ejecuta:

Get-Location

![alt text](image-28.png)

    Anota la ruta actual.
    Cambia de carpeta usando:

Set-Location C:\Windows
![alt text](image-29.png)
    Vuelve al directorio anterior con:

Set-Location ..
![alt text](image-30.png)
    Vuelve a ejecutar:

Get-Location
![alt text](image-31.png)

    Explica:
        Qué es una ruta absoluta.
        Qué es una ruta relativa.
        Qué ejemplos has utilizado en este ejercicio.