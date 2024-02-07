# Iniciar

Para esta guía, se espera que ya tengas conocimientos básicos sobre cómo instalar temas. Si no los tienes, se recomienda leer [esta página](https://nh-server.github.io/switch-guide/extras/theming/) para tener una idea básica de lo que estás a punto de hacer ;P

### Lo que necesitarás

- Switch hackeada, conectada por LAN o WiFi (usa, por ejemplo, [90dns](https://gbatemp.net/threads/90dns-dns-server-for-blocking-all-nintendo-servers.516234/) para bloquear conexiones a Nintendo).
- Una computadora con Windows.
- [NXThemes Installer](https://github.com/exelix11/SwitchThemeInjector/releases/latest) versión ≥2.6.2
    - Probablemente ya lo tengas.
    - Solo necesitas el archivo `NXThemesInstaller.nro`.
    - También puedes instalar esta aplicación homebrew desde la HB App Store.
- [LayoutKit](https://github.com/ThemezerNX/LayoutKit/releases/latest)
    - LayoutKit requiere una instalación de Windows. Aunque esta guía puede centrarse en LayoutKit, todo debería ser factible sin él.
- [sys-ftpd con soporte de reinicio](https://github.com/ThemezerNX/sys-ftpd-light-reboot/releases/latest)

<!-- prettier-ignore -->
!!! Información
    LayoutKit viene con las herramientas más utilizadas. Si no puedes o no quieres usar LayoutKit, consulta [esta lista de herramientas](../extras/tools.md), que incluye las utilizadas por LayoutKit.

## Configuración Inicial

1. Descarga e instala LayoutKit.
2. Instala NXThemes Installer.
3. Asegúrate de que NXThemes Installer funcione y estás ejecutando la versión ≥2.6.2.
4. Abre NXThemes Installer y sigue las instrucciones si es la primera vez que lo abres.
5. Ve a la pestaña 'Extract home menu' y haz clic en 'Extract home menu'.
6. Copia la carpeta `SD://themes/systemData` a tu computadora.
7. Copia el contenido del archivo comprimido de sys-ftpd a la raíz de tu MicroSD.
    - Se recomienda cambiar la contraseña de sys-ftpd. Hazlo editando `SD://config/sys-ftpd/config.ini`. Recuerda el valor que establezcas.

## Configuración de LayoutKit

1. Lee la pestaña 'Info' para familiarizarte con las características de LayoutKit.
2. Ve a la pestaña 'Settings' y completa la dirección IP de tu Switch. Puedes encontrarla yendo a `Configuración del sistema > Internet` bajo 'Estado de conexión'.
3. Configura la contraseña si la cambiaste de la predeterminada (`nxthemer`). Los cambios se guardan automáticamente.
    - El indicador en la esquina superior derecha de la aplicación debería dejar de girar y ponerse verde. Si no lo hace, verifica los detalles de tu FTP.
4. Ve a la pestaña 'Firmwares' y haz clic en 'Importar'. Haz clic en la casilla que dice 'ver.cfg path' y navega hasta el `ver.cfg` en la carpeta `systemData` que copiaste anteriormente.
    - La versión debería configurarse automáticamente.
    - Si ya tienes importada esta versión, no es necesario hacerlo de nuevo. LayoutKit se asegurará de que los archivos originales permanezcan sin modificar (excepto si comienzas a editar manualmente los datos de la aplicación, por supuesto).
5. Haz clic en 'Importar'.
6. Ve a la pestaña 'Projects' y modifica la configuración en la tarjeta 'Configuración rápida' a tu gusto. Puedes ver que también hay un botón para reiniciar manualmente la consola cuando está conectada. La instalación
7. En la pestaña 'Project Browser', haz clic en 'Nuevo' y completa los campos. Selecciona los menús que deseas incluir en tu entorno (puedes cambiar esto más tarde). El nuevo proyecto se selecciona automáticamente.
8. Puedes aplicar un diseño existente a cualquiera de los menús haciendo clic en 'Apply JSON'. Esto sobrescribirá el archivo.

    <!-- prettier-ignore  -->
    !!! Importante
        Siempre tendrás que volver a abrir Switch-Toolbox (ver próximo paso) después de haber aplicado un diseño.

9. Haz clic en cualquiera de los botones azules con un icono de llave inglesa. Esto abrirá Switch-Toolbox, en el que puedes hacer modificaciones en los menús.
    1. Ve a `Settings > Main Settings > Editor`, marca `Always compress on save` y haz clic en 'Guardar'. Esto reducirá la cantidad de clics necesarios al guardar un archivo.
    2. Si ahora haces doble clic en cualquiera de los archivos `bflyt` o `bflan` en las carpetas respectivas `blyt` y `anim`, Switch-Toolbox abrirá una segunda ventana.
    3. Después de realizar cambios, ve a `File > Save Layout` en la segunda ventana.
    4. Cuando hayas terminado de hacer cambios en los archivos `bflyt` o `bflan`, ve a `File > Save` en la primera ventana.
    5. El archivo en el disco ahora está actualizado.
10. LayoutKit detectará los cambios realizados en los archivos del proyecto activo actual, lo que significa que después de guardar un `szs`, el botón 'Install' en la tarjeta 'Configuración rápida' se iluminará.
    - Si habilitaste 'Instalar al cambiar', el botón mostrará automáticamente una animación de carga y se volverá a desactivar.

11. Puedes exportar todos los cambios realizados como un diseño haciendo clic en 'Save JSON'. Asegúrate de editarlo después y establecer tu nombre como autor.

### Pasos opcionales

- Si no incluiste todos los menús al crear el proyecto, puedes hacer clic en el lápiz verde junto a 'Copy' y seleccionar más.
- Puedes copiar un proyecto si quieres probar algo y no estropear el original. Puedes hacerlo haciendo clic en 'Copy'.
- Puedes eliminar firmwares, proyectos o menús de proyectos haciendo clic en el botón rojo de eliminar.

<!-- prettier-ignore -->
!!! Consejo
    Cualquier elemento eliminado se moverá a la papelera, así que si accidentalmente borras algo, ¡estás de suerte! Restaurar los archivos desde la papelera y hacer clic en el botón de actualización es suficiente.

# [Continuar a Archivos de Menú](menu-files.md) :octicons-arrow-right-16:
