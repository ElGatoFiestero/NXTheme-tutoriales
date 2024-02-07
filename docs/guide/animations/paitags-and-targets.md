##### :octicons-arrow-left-16: [Volver a Animaciones: extras](./going-further.md)

# PaiTags y objetivos para animaciones FLAN

---

## PaiTags

Existen muchos tipos diferentes de animaciones, desde transformaciones simples hasta cambios de sombras o color. La tabla a continuación muestra todos los tipos de animaciones encontrados en el tipo de archivo (b)flan. El `PaiTag` indica qué tipos de animaciones se utilizarán, mientras que el `AnimationTarget` especifica una propiedad específica.

- Los elementos con un ✅ están correctamente entendidos y documentados, y son compatibles con muchas herramientas.
- Los elementos con un 🟧 están parcialmente entendidos y documentados.
- Los elementos con un ⛔ nunca han sido realmente probados, documentados ni implementados en ninguna herramienta. Su funcionamiento exacto es desconocido.


| `PaiTag`      |   | Nombre                                  | Utilizado para                                                                                            |
|---------------|---|-----------------------------------------|----------------------------------------------------------------------------------------------------------|
| [FLPA](#FLPA) | ✅ | **PA**ne SRT                            | Transformaciones básicas                                                                                 |
| [FLVI](#FLVI) | ✅ | **VI**sibility                          | Visibilidad (mostrado u oculto)                                                                         |
| [FLTS](#FLTS) | ✅ | **T**exture **S**RT                     | Transformaciones de textura                                                                              |
| [FLVC](#FLVC) | ✅ | **V**ertex **C**olor                    | Color de vértice                                                                                         |
| [FLMC](#FLMC) | ✅ | **M**aterial **C**olor                  | Color de material                                                                                        |
| [FLTP](#FLTP) | 🟧 | **T**exture **P**attern                 | Patrón de textura                                                                                        |
| [FLIM](#FLIM) | ✅ | **I**ndirect Texture SRT                | Transformaciones de textura indirecta (?)                                                                |
| FLAC          | ⛔ | **A**lpha Test                          | _desconocido_                                                                                            |
| [FLCT](#FLCT) | 🟧 | Sombra de fuente                        | Sombras de fuente                                                                                        |
| FLCC          | ⛔ | Transformación por carácter **C**urva   | _desconocido_                                                                                            |
| [FLEU](#FLEU) | ⛔ | **E**xtended **U**ser Information       | Parches USD (por ejemplo, color de batería basado en el nivel de carga). Estas animaciones son controladas desde el código de la aplicación |

¡A continuación se debe especificar un `PaiTag`! Este es el objeto que será animado. La tabla a continuación
muestra todos los tipos conocidos de objetivos en el tipo de archivo (b)flan. A continuación, el `AnimationTarget` indica qué propiedad específica se modificará
(por ejemplo, posición x, rotación y, etc.).

!!! Info
    Ten en cuenta que SwitchLayoutEditor no admite todos los PaiTags y PaiTargets, aunque los más importantes sí lo están.

Para obtener más información sobre estas etiquetas y las diferentes versiones entre consolas, consulta
[este archivo](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/Common.cs)
en Switch Toolbox.

### <a href="#FLPA"></a>FLPA (Pane SRT)

Relacionado con transformaciones básicas enumeradas a continuación.


| `AnimationTarget` | Name                         | Type  | Values        | 
|-------------------|------------------------------|-------|---------------|
| `0`               | X-axis translation           | float | any (px)      |
| `1`               | Y-axis translation           | float | any (px)      |
| `2`               | Z-axis translation           | float | any (px)      |
| `3`               | X-axis rotation (vertical)   | float | any (radians) |
| `4`               | Y-axis rotation (horizontal) | float | any (radians) |
| `5`               | Z-axis rotation (flat)       | float | any (radians) |
| `6`               | X-axis scale                 | float | any           |
| `7`               | Y-axis scale                 | float | any           |
| `8`               | X-axis size                  | float | any (px)      |
| `9`               | Y-axis size                  | float | any (px)      |

- Las traslaciones son relativas a las coordenadas (x, y) definidas en tu diseño `.json`, por lo que una traslación de (0, 0) significa que el panel mantiene su posición base.
- El escalado también es relativo a lo que se define en tu diseño `.json`. Para mantener el tamaño de tu panel en una proporción de 1:1, los valores de los KeyFrame deben establecerse en `1`.

### <a href="#FLVI"></a>FLVI (Visibilidad)

| `AnimationTarget` | Nombre  | Tipo | Valores                      |
|-------------------|---------|------|-----------------------------|
| `0`               | Visible | int  | `0` (oculto), `1` (visible) |


### <a href="#FLTS"></a>FLTS (Textura SRT)

| `AnimationTarget` | Nombre           | Tipo   | Valores       |
|-------------------|------------------|--------|---------------|
| `0`               | Traslación en U  | float  | cualquier (px)|
| `1`               | Traslación en V  | float  | cualquier (px)|
| `2`               | Rotación         | float  | cualquier (radianes) |
| `3`               | Escala en U      | float  | cualquier     |
| `4`               | Escala en V      | float  | cualquier     |

### <a href="#FLMC"></a>FLMC (Color de Material)


| `AnimationTarget` | Name                       | Type  | Values | 
|-------------------|----------------------------|-------|--------|
| `0`               | Black Color Red            | int   | 0-255  |
| `1`               | Black Color Green          | int   | 0-255  |
| `2`               | Black Color Blue           | int   | 0-255  |
| `3`               | Black Color Alpha          | int   | 0-255  |
| `4`               | White Color Red            | int   | 0-255  |
| `5`               | White Color Green          | int   | 0-255  |
| `6`               | White Color Blue           | int   | 0-255  |
| `7`               | White Color Alpha          | int   | 0-255  |
| `8`               | Texture Color Blend Ratio  | float | any    |
| `9`               | Tev Color 0 Red            | int   | 0-255  |
| `10`              | Tev Color 0 Green          | int   | 0-255  |
| `11`              | Tev Color 0 Blue           | int   | 0-255  |
| `12`              | Tev Color 0 Alpha          | int   | 0-255  |
| `13`              | Tev Color 1 Red            | int   | 0-255  |
| `14`              | Tev Color 1 Green          | int   | 0-255  |
| `15`              | Tev Color 1 Blue           | int   | 0-255  |
| `16`              | Tev Color 1 Alpha          | int   | 0-255  |
| `17`              | Tev Color 2 Red            | int   | 0-255  |
| `18`              | Tev Color 2 Green          | int   | 0-255  |
| `19`              | Tev Color 2 Blue           | int   | 0-255  |
| `20`              | Tev Color 2 Alpha          | int   | 0-255  |
| `21`              | Tev Konstant Color 0 Red   | int   | 0-255  |  
| `22`              | Tev Konstant Color 0 Green | int   | 0-255  |
| `23`              | Tev Konstant Color 0 Blue  | int   | 0-255  |
| `24`              | Tev Konstant Color 0 Alpha | int   | 0-255  |
| `25`              | Tev Konstant Color 1 Red   | int   | 0-255  |
| `26`              | Tev Konstant Color 1 Green | int   | 0-255  |
| `27`              | Tev Konstant Color 1 Blue  | int   | 0-255  |
| `28`              | Tev Konstant Color 1 Alpha | int   | 0-255  |
| `29`              | Tev Konstant Color 2 Red   | int   | 0-255  |
| `30`              | Tev Konstant Color 2 Green | int   | 0-255  |
| `31`              | Tev Konstant Color 2 Blue  | int   | 0-255  |
| `32`              | Tev Konstant Color 2 Alpha | int   | 0-255  |

### <a href="#FLVC"></a>FLVC (Vertex Color)

Relacionado con las transformaciones de colores de vértices listadas abajo.

| `AnimationTarget` | Nombre            | Tipo | Valores | 
|-------------------|-------------------|------|--------|
| `0`               | Rojo Superior Izquierdo  | int  | 0-255  |
| `1`               | Verde Superior Izquierdo | int  | 0-255  |
| `2`               | Azul Superior Izquierdo  | int  | 0-255  |
| `3`               | Alfa Superior Izquierdo  | int  | 0-255  |
| `4`               | Rojo Superior Derecho    | int  | 0-255  |
| `5`               | Verde Superior Derecho   | int  | 0-255  |
| `6`               | Azul Superior Derecho    | int  | 0-255  |
| `7`               | Alfa Superior Derecho    | int  | 0-255  |
| `8`               | Rojo Inferior Izquierdo  | int  | 0-255  |
| `9`               | Verde Inferior Izquierdo | int  | 0-255  |
| `10`              | Azul Inferior Izquierdo  | int  | 0-255  |
| `11`              | Alfa Inferior Izquierdo  | int  | 0-255  |
| `12`              | Rojo Inferior Derecho    | int  | 0-255  |
| `13`              | Verde Inferior Derecho   | int  | 0-255  |
| `14`              | Azul Inferior Derecho    | int  | 0-255  |
| `15`              | Alfa Inferior Derecho    | int  | 0-255  |

### <a href="#FLTP"></a>FLTP (Patrón de Textura)

| `AnimationTarget`               | Nombre  | Valores |
|---------------------------------|---------|--------|
| `0`                             | Imagen 1|        |
| _las siguientes filas no están confirmadas_ |         |        |
| `1`                             | Imagen 2|        |
| `2`                             | Imagen 3|        |
| etc.                            | etc.    |        |

### <a href="#FLIM"></a>FLIM (SRT de Textura Indirecta)

| `AnimationTarget` | Nombre         | Tipo   | Valores        |
|-------------------|----------------|--------|---------------|
| `0`               | Rotación       | float  | cualquier (radianes) |
| `1`               | Escala U       | float  | cualquier      |
| `2`               | Escala V       | float  | cualquier      |

### <a href="#FLCT"></a>FLCT (Sombra de Fuente)

| `AnimationTarget` | Nombre                | Tipo | Valores |
|-------------------|-----------------------|------|--------|
| `0`               | Rojo Color Negro     | int  | 0-255  |
| `1`               | Verde Color Negro    | int  | 0-255  |
| `2`               | Azul Color Negro     | int  | 0-255  |
| `3`               | Alfa Color Negro     | int  | 0-255  |
| `4`               | Rojo Color Blanco    | int  | 0-255  |
| `5`               | Verde Color Blanco   | int  | 0-255  |
| `6`               | Azul Color Blanco    | int  | 0-255  |
| `7`               | Alfa Color Blanco    | int  | 0-255  |

### <a href="#FLEU"></a>FLEU (Información Extendida del Usuario)

| `AnimationTarget` | Nombre                                   | Tipo                                                | Valores |
|-------------------|------------------------------------------|-----------------------------------------------------|--------|
| `0`               | Pane SRT                                 |                                                     |        |
| `1`               | Visibilidad                              |                                                     |        |
| `2`               | Color de Vértice / Transparencia         |                                                     |        |
| `3`               | Color de Material / Sombras de Texto     |                                                     |        |
| `4`               | Prueba Alfa                              |                                                     |        |
| `5`               | Patrón de Textura                        |                                                     |        |
| `6`               | Textura SRT                              |                                                     |        |
| `7`               | Desplazamiento de Transformación por Carácter |                                                  |        |
| `8`               | Información Extendida del Usuario        | Lista de valores de cadena, enteros o números reales |        |
| `9`               | Indirecto                                |                                                     |        |

# [Continuar a Animaciones: archivos szs, bflyt, bflan](./szs-bflyt-bflan.md) :octicons-arrow-right-16:

---

## Agradecimientos Especiales

- [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/)
- [3DSkit](https://github.com/Tyulis/3DSkit/)
