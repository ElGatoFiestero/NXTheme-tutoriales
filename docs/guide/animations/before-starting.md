# Animaciones: antes de empezar

## Recordatorio rápido sobre los archivos de Nintendo Switch

Crear temas significa alterar archivos `.szs`. Estos son archivos que contienen los elementos gráficos de la interfaz de usuario, todos ellos almacenados en archivos `.bflyt` y `.bflan`. Básicamente, toda la interfaz de usuario se divide en tales archivos. Por lo tanto, para crear animaciones, necesitaremos modificarlos.

Las imágenes, iconos, texto y prácticamente todo lo que se muestra en la pantalla de tu consola son objetos de tipo *pane* (panel) que se encuentran en archivos `.bflyt`. Estos archivos `.bflyt` también contienen información sobre la posición/tamaño/escala de los paneles y sus canales RGBA. En otras palabras, esos paneles son los objetos en los que nos centraremos en este tutorial, es decir, precisamente los objetos en los que adjuntaremos nuestras animaciones. Por lo tanto, es posible que desees **ver primero el** archivo `.bflyt` **que contiene el panel que deseas animar**.

En la práctica, **nos centraremos principalmente en los archivos** `.bflan`, **en los que se almacenan partes de los datos de animación para un archivo** `.bflyt` **específico**. Casi todo el proceso se realiza a través de Switch Layout Editor, que empezaré a presentar en la próxima subsección.

Volviendo a los archivos `.szs`, los encontrarás en `themes/systemData` en tu tarjeta SD, ya que estos han sido extraídos por la aplicación homebrew NXTheme Installer. Ten en cuenta que los archivos `.szs` contienen contenido protegido por derechos de autor, por lo que compartirlos es ilegal (esa es la razón por la que los modders implementaron el formato `.nxtheme` para evitar esto).

Cada archivo corresponde a un menú específico,


| `.szs` Archivo         | Menú                      |
|:----------------------:|:---------------------------:|
| `ResidentMenu.szs`   | Pantalla de inicio         |
| `Set.szs`            | Configuración              |
| `Psl.szs`            | Selección de jugador       |
| `Flauncher.szs`      | Todos los programas / lanzador completo |
| `Lock.szs`           | Pantalla de bloqueo        |
| `MyPage.szs`         | Página de usuario          |

así que si uno desea editar elementos de la interfaz de usuario en la página de inicio, necesitaríamos el archivo `ResidentMenu.szs`. Del mismo modo, si queremos hacer ediciones en la sección de todos los programas, el archivo `Flauncher.szs` es con el que trabajaremos. Ya entiendes la idea.

!!! info
    También encontrarás en `themes/systemData` otros archivos `.szs` que no se enumeran aquí, por ejemplo `Option.szs`. 
    Esos no son oficialmente admitidos por el inyector de temas, pero es posible editarlos manualmente de todas formas. Echa un vistazo a la sección de [diferenciación/Diffing de LayoutDocs](../diffing.md).

## Diferenciación con el Editor de Diseños

Es posible que estés acostumbrado a trastear con archivos `.json` y compilar temas con Switch Theme Injector, pero tal vez no estés familiarizado con Switch Layout Editor. Piénsalo como un lector/archivador de archivos `.szs` que también ofrece una vista previa real en pantalla de la posición de los paneles, lo que es bastante conveniente para la edición de diseños. Resulta que el Editor de Diseños también se utiliza para la edición de animaciones.

!!! tip
    Alternativamente, puedes usar Switch Toolbox (también incluido con [LayoutKit](https://github.com/ThemezerNX/LayoutKit)), que es otro software que tiene prácticamente los mismos propósitos que Layout Editor, al menos para nuestras necesidades actuales. Sin embargo, como he estado trabajando con el Editor de Diseños, no cubriré Switch Toolbox aquí, pero al final del día depende de tu preferencia.

Una vez que se hayan implementado las animaciones, necesitaremos hacer una *diferenciación de diseño* (como en *diffing*). Básicamente, queremos trabajar con dos versiones del archivo `.szs` elegido: el primero permanece intacto y el segundo contendrá todas las ediciones que se hayan hecho a través del Editor de Diseños. La diferenciación de diseño o diffing es el proceso de comparar (*diff*) ambos archivos `.szs` y producir un diseño `.json` que refleje todas tus ediciones. El archivo `.json` de salida puede luego ser utilizado en Switch Theme Injector para compilar el `.nxtheme` como lo harías normalmente.

!!! info
    Hacer animaciones basadas en color era muy tedioso y consumía mucho tiempo hasta la 15ª versión del Editor de Diseños de exelix. Esta versión no solo añade conveniencia para hacer animaciones basadas en color específicamente, sino que también facilita en gran medida todo el proceso de creación de animaciones al implementar plantillas definidas por el usuario. Se ha añadido una sección a este tutorial para reflejar esos cambios.

Repasaremos estos pasos generales que se aplican a **cualquier tipo de edición de animaciones**:

- hacer dos copias del archivo `.szs` elegido

- editar una de ellas con nuestras animaciones

- diferenciación de diseño

- compilar el `.nxtheme` usando el archivo `.json` de salida/diffpatch e instalarlo en la consola (proceso habitual con Switch Theme Injector y NXTheme Installer)


Dicho esto, finalmente podemos empezar a crear animaciones.

# [Continuar a Animaciones: Tutorial principal](main-tutorial.md) :octicons-arrow-right-16:
