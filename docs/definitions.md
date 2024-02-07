# Definiciones

Esta página intenta explicar tanto como sea posible el argot relacionado con la creación de temas.

## Lista de Palabras

### SZS

Un archivo comprimido. En los archivos de menú de Switch, contiene los archivos de diseño, animaciones y texturas. [_Más información_](guide/filetypes.md#szs-files)

### Applet

Un tipo de título/aplicación/juego. `Qlaunch`, `playerSelect`, `photoViewer` son todos applets. [_Más información_](guide/menu-files.md#menu-files)

### Botón de Applet

Un 'botón de applet' es un poco diferente de un 'applet'. Los botones de álbum, configuración, controlador, etc., en el menú de inicio son todos botones de applet.

### nxtheme

Desafortunadamente, los archivos `SZS` de los archivos de firmware de Switch contienen datos con derechos de autor y no se pueden compartir en línea. Con el fin de seguir compartiendo temas personalizados, se desarrolló el formato `nxtheme`. Un archivo `nxtheme` contiene detalles del tema (nombre, autor), imágenes y el diseño.

### exelixbg

El `exelixbg` es el nombre del panel que se crea cuando NXThemes Installer o Switch Theme Injector aplican una imagen de fondo.

### Diffing, JSON diferenciado, JSON de diseño

Un diseño se crea comparando un archivo `SZS` modificado con el original sin modificar. Los cambios detectados se guardan en un archivo de diseño `json`, que luego solo contiene datos diferenciales. De esta manera, compartir `nxthemes` es completamente legal.

### Paneles

Otro término para elementos en archivos `bflyt`. Por ejemplo, `P_Pict`, `N_Button`.

### Sección usd

`usd` (oficialmente llamada 'información de usuario extendida') es una parte del archivo `bflyt` que contiene datos adicionales y define, por ejemplo, sombras, radio, etc. A menudo, los paneles van seguidos de secciones `usd`. [_Más información_](guide/layouts/usd-sections.md)

### Actualización del sistema

Abreviatura de actualización del sistema
