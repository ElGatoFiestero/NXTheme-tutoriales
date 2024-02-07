# Agregar o editar una imagen de fondo personalizada a cualquier tema

*Escrito por [Capybara](https://themezer.net/creators/382997176307154945), marzo de 2023*

<div align="center">
<img src="https://avatars.githubusercontent.com/u/65415089?s=200&v=4" />
</div>

<br />
He estado recibiendo muchas solicitudes sobre eso, aunque el proceso es realmente simple. De una vez por todas, este breve tutorial describirá cómo personalizar un tema con la imagen de fondo de tu elección, independientemente del diseño base que elijas.

## Tabla de contenidos

*NB: applets no admitidos (por ejemplo, álbum, controladores, etc.) no están cubiertos aquí.*

- **[I. Elegir una imagen de fondo](##i-elegir-una-imagen-de-fondo)**
- **[II. Elegir un diseño](#ii-elegir-un-dise%C3%B1o)**
- **[III. Construcción con Switch Theme Injector](#iii-construcci%C3%B3n-con-switch-theme-injector)**

## Requisitos

- Windows 10 o 11
- [Switch Theme Injector](https://github.com/exelix11/SwitchThemeInjector/releases)
- El diseño de tu elección si los proporcionados por Switch Theme Injector no te satisfacen
- Tu imagen (obvio)
- Probablemente un editor de fotos (por ejemplo, Photoshop, paint.NET, GIMP, etc.)

## I. Elegir una imagen de fondo

Elige la imagen que desees, **siempre y cuando cumpla con estos dos requisitos**:

- Tamaño adecuado: **1280x720**
- Formato adecuado: `.jpg` con codificación de línea de base/estándar **O** `.dds` con codificación DXT1

Probablemente necesitarás un editor de fotos para que tu imagen cumpla con estas condiciones; de lo contrario, Switch Theme Injector no compilará tu tema. La parte de codificación debería ser sencilla, ya que el software que estés utilizando debería solicitarte que lo ajustes correctamente. Para convertir cualquier archivo de imagen a un `.dds` codificado con DXT1, recomiendo usar [paint.NET](https://www.getpaint.net/download.html#download).

*NB: mientras que `.jpg` no maneja la transparencia en absoluto, DXT1 `.dds` lo hace de manera muy deficiente. No recomiendo complicarte con la transparencia si usas `.dds`. Debería estar bien si tu imagen solo contiene áreas con transparencia completa, pero cualquier valor de opacidad intermedio en tu imagen causará problemas visuales feos.*

## II. Elegir un diseño

Los diseños determinan la posición, tamaño y colores (y animaciones en algunos temas) de los diferentes elementos de la interfaz de usuario, haciéndolos (a los diseños, eso es) la parte principal de un tema personalizado. Vienen como archivos `.json` y se utilizan para parchear los archivos `.szs` ubicados en `themes/systemData` en tu tarjeta SD para crear temas. Cada applet (por ejemplo, pantalla de inicio, pantalla de bloqueo, etc.) tiene su propio diseño.

Para no afectar la legibilidad, elige tu imagen en consecuencia, porque los colores del diseño que elijas obviamente no se ajustarán por sí mismos (en algunos casos, cambiar al modo oscuro o claro en la configuración de tu consola podría ayudar, sin embargo).

Switch Theme Injector proporciona diseños predeterminados. Si no te satisfacen, también puedes descargar cualquier diseño de [Themezer](https://themezer.net/) y usar tu propia imagen con él. Un diseño de tema se puede descargar desde la página de cualquier tema individual. Ten en cuenta que también puedes descargar la imagen de fondo de un tema desde la misma página.

*(captura de pantalla por proporcionar)*

Alternativamente, si tienes un archivo `.nxtheme` y deseas extraer sus recursos, puedes hacerlo a través de Switch Theme Injector. Se extraerán tanto los diseños como los archivos de imagen durante el proceso.

![image](https://github.com/ElGatoFiestero/TutorialTemasNintendoSwitch/assets/159089859/2d01962d-549d-4755-88c2-bfaf20698b59)


Ten en cuenta que algunos temas de pantalla de inicio también proporcionan un diseño común (`common.json`), que se necesitará para construir nuestro `.nxtheme`. En general, puedes decir a primera vista si la sección del pie de página (que contiene botones e iconos de controladores) ha sido alterada o no.

![image](https://github.com/ElGatoFiestero/TutorialTemasNintendoSwitch/assets/159089859/1bb21b74-920e-4d57-8e9f-8c967750b89a)


## III. Construcción con Switch Theme Injector

Ahora, para la parte final. Abre Switch Theme Injector y deberías estar en la pestaña `NXTHEME BUILDER`. Selecciona tu applet (pantalla de inicio en mi ejemplo), busca tu imagen de fondo y el diseño que elegiste y luego confirma haciendo clic en `BUILD NXTHEME`. Elige tu ubicación de guardado preferida. Si todo se hizo correctamente, no se te solicitará ningún mensaje de error y se generará un archivo `.nxtheme`. Luego puedes proceder a instalar tu tema usando NXTheme Installer después de poner tu archivo `.nxtheme` compilado en la carpeta `themes` de tu tarjeta SD.

![image](https://github.com/ElGatoFiestero/TutorialTemasNintendoSwitch/assets/159089859/4f60ba5d-d9f8-4c66-8a4a-797cf653786b)


