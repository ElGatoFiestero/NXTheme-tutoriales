##### :octicons-arrow-left-16: [Volver a Animaciones: plantillas](anim-templates.md)

# Más sobre animaciones
---

## Tablas útiles

### Entradas de PaiTag y valores de AnimationTarget

Los valores de `AnimationTarget` y el comportamiento de la animación subsecuente cambian dependiendo del `PaiTag` definido. Una lista completa de Etiquetas y Objetivos de animación se puede ver en la siguiente página:

##### **[PaiTags y AnimationTargets](./paitags-and-targets.md) :octicons-arrow-right-16:**

### Archivos bflyt, bflan, szs

Algunos `.bflyt`, `.bflan` y sus correspondientes `.szs` también están documentados allí:

##### **[Archivos szs, bflyt, bflan](./szs-bflyt-bflan.md) :octicons-arrow-right-16:**

## Estados activos e inactivos

Podemos encontrar pares específicos de archivos `.bflan` para algunos `.bflyt`s como `<bflyt>_Active.bflan` / `<bflyt>_Inactive.bflan`.

En la sección principal del tutorial, trabajamos en `RdtBtnIconGame_Active.bflan` / `RdtBtnIconGame_Inactive.bflan`, pero también hay un par más, por ejemplo `RdtBtnSet_Active.bflan` / `RdtBtnSet_Inactive.bflan`.

##### **[Archivos szs, bflyt, bflan](./szs-bflyt-bflan.md) :octicons-arrow-right-16:**

- `<bflyt>_Active.bflan` anima los paneles `<bflyt>` cuando el elemento de la interfaz de usuario está **seleccionado**

- `<bflyt>_Inactive.bflan` anima los paneles `<bflyt>` cuando el elemento de la interfaz de usuario está **siendo deseleccionado**

!!! info
      Más archivos `.bflan` siguen una lógica similar, por ejemplo, `<bflyt>_FocusKey.bflan` / `<bflyt>_UnFocusKey.bflan`. Estos aún no están completamente probados ni documentados.

!!! warning
      Las ediciones realizadas para los archivos `.bflan` Inactivos sobrescribirán los valores que hayas definido en tu diseño `.json`. Por ejemplo, si has establecido la coordenada x del botón del álbum en `660px` en tu `.json` mientras está establecida en `680px` en el `.bflan` Inactivo, el valor `680px` tendrá prioridad sobre el `660px` y se aplicará.

## Animaciones en bucle

Es posible hacer animaciones en bucle. Estas se pueden ver en el [diseño de Migush](https://themezer.net/creators/123859829453357056) llamado [JAG layout](https://themezer.net/layouts/homemenu/JAG-Layout-2), donde los iconos de juegos seleccionados siguen una animación de agrandamiento y reducción como actividad de inactividad. Todo lo que tienes que hacer para hacer una animación en bucle es establecer el valor de `Flags` en `1` (mientras que `0` desactiva el bucle) en la sección `Pai1` de un archivo `.bflan`. Desafortunadamente, **las animaciones más complejas que combinan múltiples transformaciones no se pueden lograr correctamente** ya que la bandera se aplica a todo el archivo `.bflan`. Más explícitamente, un icono de juego no sería capaz de moverse `10px` arriba Y LUEGO seguir una animación en bucle de agrandamiento y reducción. En tal caso, el desplazamiento en y también se repetiría.

## Animaciones de fundido de entrada y salida

Digamos que quiero un cursor parpadeante para el menú de navegación en la aplicación de configuración. Esto implica usar `FLVC` y `AnimationTarget` = `16`. Voy a describir brevemente el proceso, pero básicamente es lo mismo que en el tutorial principal:

1. Abre `Set.szs` y luego `BtnNav_Root_Active.bflan`. **Como siempre al crear animaciones personalizadas,** haz las modificaciones adecuadas en las secciones `Pat1` y `Pai1`. Agrega la entrada `N_BtnFocusKey` (panel de cursor) a la lista, crea una **entrada `FLVC`** (¡no `FLPA`!) justo debajo de ella, y luego otra entrada debajo de `FLVC`. Elegí configurar mis fotogramas clave como se muestra en las capturas de pantalla a continuación.
2. También editaremos `BtnNav_Root_Inactive.bflan`, de lo contrario, navegar por las pestañas interrumpirá la animación del cursor y lo bloqueará en un fotograma determinado (el mismo comportamiento que en nuestra animación anterior de iconos de juego). Considerando eso, simplemente "restablecemos" el estado de `N_BtnFocusKey` (después de agregar este panel a la lista) estableciendo su canal alfa en `0` en el fotograma `0`.
3. Para cada archivo `.bflan`, crea grupos con nombres adecuados en la sección `RootGroup` de `BtnNav_Root.bflyt`. **No olvides guardar todas tus ediciones.**
4. Realiza una diferencia de diseño o diffpatch, compila e instala, ¡y listo! Ahora tienes un cursor parpadeante que funciona.

| ![Configuración (1)](tuto14.jpg "Configuración (1)") | ![Configuración (2)](tuto15.jpg "Configuración (2)") |
|------------------------------------------------------|------------------------------------------------------|
| Agregar entrada `FLVC` (Activo)                      | Agregar entrada `FLVC` (Inactivo)                    |

## Fondos animados

Los fondos animados han estado de moda últimamente (en el momento de escribir esto). La verdad es que hay cierta complejidad detrás de los temas de fondo animados, así que **aclaremos de una vez por todas**.

**No hay una manera *adecuada* ni fácil conocida de hacer fondos animados.** Switch Theme Injector solo admite archivos `.dds` y `.jpg`.
Una solución alternativa sería animar el panel que contiene tu imagen de fondo personalizada. Eso *realmente* funciona, y hay algunos temas que ya lo han logrado. Para hacerlo, trabajando con `ResidentMenu.szs`, necesitas agregar `L_BgNml` a la lista de paneles en `RdtBase_Enter.bflan` y realizar tus ediciones según tu conveniencia. Sin embargo, esta solución tiene sus limitaciones:


- `RdtBase_Enter.bflan` contiene la animación de desbloqueo de la pantalla de inicio. Intenta hacer un bucle con tu animación usando el elemento `Flags` y tal vez puedas adivinar qué sucederá (inicio de bucle, fallas en la interfaz de usuario y en el sonido). Lo único que puedes hacer para reproducir de alguna manera un comportamiento en bucle es duplicar tu patrón de animación hasta llegar a una cantidad absurda de fotogramas clave. [Zhi](https://themezer.net/creators/239384767785730048) en realidad hizo esto en su [tema Patterns](https://themezer.net/packs/Patterns.-58f) con un límite de fotogramas de 64000 (lo que lo hace aproximadamente 8 minutos). Si estás interesado en aprender todo el proceso, puedes leer a través [de su propia documentación allí](/PatternsTraducido.md). Como nota adicional, es posible que desees estar atento a los próximos lanzamientos de Zhi porque tiene algunas ideas bastante buenas.

- Todavía estás atascado con una imagen de fondo estática ya que no hay soporte para imágenes animadas de ningún tipo, ni para archivos de video.
- Podrías hacer un collage de fotogramas en un fondo único (cada esquina una imagen de 360p). De esta manera podrías usar una animación para enfocar diferentes esquinas y hacer que parezca que tu fondo tiene cuatro fotogramas. Podrías reducir la calidad de cada imagen a ~480p. Aún tendrás que depender de agregar manualmente muchas entradas de fotogramas.
- Puedes hacer animaciones de degradado animando los colores de las esquinas superior/inferior izquierda/derecha, y no usar una imagen de fondo. Aún así, se requiere repetir manualmente los fotogramas.
- En las versiones del firmware 5.x y anteriores, podrías hacer bucles fácilmente con las animaciones de fondo, ya que la bandera `loop` no afectaba a la animación de 'entrada' al venir desde la pantalla de bloqueo.

Para otros applets (por ejemplo, configuración, página de usuario, etc.), en realidad no hay ninguna forma conocida de aplicar ningún tipo de animación a una imagen de fondo personalizada.

## Las animaciones *pueden* sobrescribir cosas

Si pasaste algún tiempo editando diseños `.json`, es posible que hayas encontrado casos en los que, no importa lo que hagas, los cambios que realices en un panel (por ejemplo, colores, posición, etc.), incluso teniendo habilitados los parches `C_W` y `C_B`, no den resultado. **En tales casos, es probable que una animación esté sobrescribiendo tus ediciones.**

Un caso notable es el botón de Volver a descargar software en la parte inferior de la página principal del applet de lanzamiento completo (`Flauncher.szs`). Los paneles correspondientes a este botón son `L_Shop` y `T_Empty`, y estos no se ocultarán simplemente adjuntando la propiedad `Visible: false` a ellos. Esto se debe a las entradas `FLVI` en `FlcCntMain_Type.bflan` que sobrescriben cualquier intento de modificación realizado dentro de tu código `.json`. Para resolver esto, los valores `KeyFrames` bajo cada entrada `FLVI` deben establecerse en `0` (`1` de forma predeterminada).


| ![Shop (1)](tuto16.jpg "Shop (1)") | ![Full launcher (2)](tuto17.jpg "Shop (2)") |
|------------------------------------|---------------------------------------------|
| `L_Shop` > `FLVI` > `KeyFrames`    | `T_Empty` > `FLVI` > `KeyFrames`            |

| ![Full launcher (1)](flaunch1.jpg "Full launcher (1)") | ![Full launcher (2)](flaunch2.jpg "Full launcher (2)") |
|--------------------------------------------------------|--------------------------------------------------------|
| Botón Redescargar software visible                      | Botón Redescargar software oculto                      |

Dando otro ejemplo, echa un vistazo a mi tema de menú de inicio Unison R: los juegos destacados tienen una tarjeta blanca redondeada alrededor de su icono. Los paneles correspondientes a estas tarjetas son `P_BtnBase` de `RdtBtnIconGame.bflyt`. Este panel en realidad tiene cierta transparencia definida a través de animaciones de forma predeterminada. Por lo tanto, para hacer que este panel sea completamente opaco, debemos analizar las animaciones de `P_BtnBase` y cambiar su valor de `KeyFrames` a `255` bajo la entrada `FLVC`.

# [Continuar con Animaciones: PaiTags y AnimationTargets](./paitags-and-targets.md) :octicons-arrow-right-16:
