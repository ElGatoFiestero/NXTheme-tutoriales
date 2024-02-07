##### :octicons-arrow-left-16: [Volver a la Introducción](index.md)

# Archivos de Menú

Para trabajar de manera eficiente, es importante entender la estructura de los menús de Switch y familiarizarse con la jerga del diseño de temas. Esta y las siguientes páginas te introducirán a algunos conceptos básicos.

Los menús de Switch se pueden encontrar en varios archivos del firmware, separados en [applets](../definitions.md#applet). La siguiente tabla muestra en qué lugares se pueden encontrar los siguientes menús (compatibles con temas):

| Nombre en Código del Applet | TitleID            | Menús                                                   |
| --------------- | ------------------ | ------------------------------------------------------- |
| qlaunch         | `0100000000001000` | común, Menú Principal, Pantalla de Bloqueo, Todas las Aplicaciones, Noticias, Configuración |
| playerSelect    | `0100000000001007` | Selección de Jugador                                    |
| myPage          | `0100000000001013` | Página de Usuario                                       |

Casi todos los applets relacionados con menús también tienen un archivo `common.szs` que define estructuras que deben usarse en todos los menús del applet. A menudo, contienen la barra inferior (estado del controlador, botones). Desafortunadamente, los temas personalizados solo admiten la modificación del archivo `common.szs` en el applet `qlaunch`, y no en los de `playerSelect` o `myPage`.

## Nombres de Archivos

Cada menú tiene su propio archivo. Aquí tienes una lista de los menús admitidos por el formato nxtheme y sus nombres de archivo:

| Menú             | Nombre de Archivo   |
| ---------------- | ------------------ |
| común (qlaunch) | `common.szs`       |
| Menú Principal        | `ResidentMenu.szs` |
| Pantalla de Bloqueo       | `Entrance.szs`     |
| Todas las Aplicaciones         | `Flaunch.szs`      |
| Noticias             | `Notification.szs` |
| Configuración         | `Set.szs`          |
| Selección de Jugador    | `Psl.szs`          |
| Página de Usuario        | `MyPage.szs`       |

# [Continuar a Tipos de Archivos](filetypes.md) :octicons-arrow-right-16:
