# Bienvenid@ a EPISD (Eva's Post Installation Script for Debian).
## VERSIÓN 2025.05.03-0.
(C) 2025 EVA DEBIAN.

---

## ¿QUÉ ES EPISD?

EPISD es un programa fácil de usar para finalizar la instalación de tu sistema operativo Debian.

Es importante decir que este script contiene acceso a los repositorios no libres (non-free) de Debian GNU/Linux e instalaciones de software privativo, de modo que si estás en contra de ello, por favor, no lo uses o modifica el script a tu gusto para eliminar las partes no libres del programa.

## ¿PARA QUÉ NECESITO EPISD?

Por defecto, una instalación de Debian GNU/Linux necesita la modificación del fichero de repositorios para poder instalar utilidades básicas y software de uso cotidiano para asegurar un correcto funcionamiento del sistema.

Este programa pretende facilitar toda esa tarea de modificar repositorios, instalar drivers y un largo etcétera, tanto a personas novatas en Debian como a los usuarios más avanzados del sistema.

Este script surgió como una simple idea personal: para evitar tener que escribir una cantidad de comandos considerablemente alta tras instalar Debian en cualquier equipo.

## ¿ES EPISD SOFTWARE LIBRE?

La respuesta corta es "sí". El código fuente es auditable y modificable; sin embargo, este añade el repositorio "non-free" al fichero sources.list e instala algún programa (como los controladores) que no son libres, o que permiten la ejecución de código no libre.

## USO DE EPISD

Primero asegúrate de que estás ejecutando el sistema operativo en modo X11 / XOrg. Si no es así, reinicia la máquina y en la pantalla de login, cambia el ajuste de Wayland a X11.

Para ejecutar el script, abre la consola de comandos y teclea:

    su root

Introduce la contraseña de la cuenta root configurada en la instalación del sistema. Esta clave NO es la de tu usuario principal.

Ahora, escribe el siguiente comando:

    sh ./ruta-al-script/evapisd.sh

El programa te dará a elegir las siguientes opciones:

### 1 - Sistema Debian recién instalado.

Esta opción la utilizaremos cuando nuestro sistema operativo esté recién instalado. Realizará las siguientes acciones:

- Añadir tu usuario al grupo sudo.
- Modificación del fichero sources.list.
- Actualización de la subversión del sistema operativo.
- Instalación de paquetes básicos de compilación y cabeceras del kernel.
- Instalación de drivers.
- Instalación de codecs multimedia.
- Instalación del JRE (Java Runtime Environment).
- Instalación de programas de uso cotidiano (Thunderbird, VLC...).
- Limpieza del sistema (esto no borrará información personal), sino que eliminará los archivos residuales del proceso de esta opción para reducir espacio en disco.

### 2 - Instalar WINE y preparar "Entorno Windows".

Usa esto si quieres ejecutar aplicaciones de Microsoft Windows.  
Nota que ejecutar programas de Windows no siempre funciona bien con software de este tipo. Esto no es culpa de EPISD sino de la compatibilidad de dicho software con WINE.

### 3 - Detección e instalación de drivers

**Nota:** este proceso **NO instala drivers de tarjetas gráficas**, sino que instala los paquetes básicos de firmware, iwlwifi, etc...  
Para la instalación del microcódigo o tarjetas gráficas, recomiendo buscar en Internet la información adecuada.

### 4 - Compartir ficheros (método LocalSend) RECOMENDADO.

Ideal para enviar y recibir ficheros desde o hacia tu ordenador (Linux, Windows o Mac) o desde o hacia tu móvil (Android e iOS) con el software 100% libre LocalSend.

Todo dentro de tu red local, sin exponer tus dispositivos a Internet.

Esta opción instalará LocalSend en este equipo, pero deberás instalarlo manualmente en el dispositivo desde el que vayas a enviar o recibir ficheros (por ejemplo, tu teléfono móvil).

La descarga está disponible para GNU/Linux, Windows, MacOS, Android e iOS.

### 5 - Crear carpeta compartida (método SAMBA).

Útil si tienes una multifunción y deseas enviar el "escaneo" o la digitalización de imágenes por red o si deseas compartir tu disco duro con una televisión o un dispositivo de reproducción de vídeo.

Esta función creará la carpeta "CompartidaSamba" en tu carpeta personal (`/home/tuusuario/CompartidaSamba`).

### 6 - Salir:

**IMPORTANTE:** Una vez realizada CUALQUIER ACCION, salir desde el menú CANCELAR o presionar la tecla ESC, NO revertirá ni descartará ningún cambio realizado en el sistema.

No es un "Salir sin guardar".

---

## AGRADECIMIENTOS Y CONTACTO:

Espero que EPISD te sea útil. No soy programadora profesional, por favor, tenedlo en cuenta para notificar cualquier cambio o error.  
Si queréis contactar conmigo, envia tu correo a `evadebian (at) disroot (period) org` y utiliza GPG siempre que puedas, tienes mi clave pública en [https://evadebian.github.io/web/gpg](https://evadebian.github.io/web/gpg)
