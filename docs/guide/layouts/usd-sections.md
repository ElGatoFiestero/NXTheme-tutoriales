##### :octicons-arrow-left-16: [Volver a Empezando](index.md)

# Secciones USD

Las secciones USD definen datos adicionales sobre otro panel. Normalmente, siguen al panel al que están relacionados, pero pueden estar en cualquier orden siempre y cuando tengan el nombre del panel al que pertenecen.

Este es un ejemplo simplificado de un panel seguido de una sección `usd`:


```json
{
	"pic1 - P_Item": {
		"name": "P_Item",
		"x translation": 100.0,
		"y translation": 100.0,
		"width": 50.0,
		"height": 50.0,
		"material": "P_Item"
	},
	"usd1 - P_Item": {
		"entries": [
			{
				"name": "S_DropShadowDrawMode",
				"type": 1,
				"unk1": 0,
				"data": [1]
			},
			{
				"name": "S_DropShadowColor",
				"type": 2,
				"unk1": 0,
				"data": [0.0, 0.0, 0.0, 1.0]
			},
			{
				"name": "S_DropShadowAngle",
				"type": 2,
				"unk1": 0,
				"data": [1.5]
			},
			{
				"name": "S_DropShadowDistance",
				"type": 2,
				"unk1": 0,
				"data": [0.0]
			}
		]
	}
}
```

<!-- prettier-ignore -->
!!! Importante
    El código JSON mostrado arriba es de 3DSKit y no puede ser copiado directamente a un diseño.  
    Todos los ejemplos a continuación *son* compatibles.

## Estructura

Una entrada USD tiene un nombre, tipo y sección de datos.

Nombre: `String`  
Tipo: `Int`


-   `0`: String
-   `1`: Int
-   `2`: Float

Formato: Matriz de valores de tipo especificado

## Propiedades compatibles

_Compatibles con el Inyector de Temas de Switch_

- Todas, incluso las no documentadas.

## Valores Globales de Color

El sistema tiene valores especiales que pueden ser utilizados en todo el sistema. Estos colores pueden cambiar según el tema del sistema (claro/oscuro), razón por la cual se utilizan con frecuencia.

<div class="color-table" markdown="1">

| Valor | Tema Claro                 | Tema Oscuro    | Uso                                                                                   |
| ----- | ----------------------------- | ------------- | --------------------------------------------------------------------------------------- |
| 0     | -                             | -             | default (apagado)                                                                           |
| 1     | white (255,255,255)           | (29,32,37)    |                                                                                         |
| 2     | black (0,0,0)                 | (0,0,0)       |                                                                                         |
| 3     | green (114,201,0)             | (149,231,0)   | Charge indicator                                                                        |
| 4     | white (255,255,255)           | (255,255,255) |                                                                                         |
| 5     | white (235,235,235)           | (45,45,45)    | Fondo de tema claro/oscuro                                                                    |
| 6     | white (255,255,255)           | (67,67,67)    |                                                                                         |
| 7     | white (255,255,255)           | (98,99,103)   |                                                                                         |
| 8     | white (255,255,255)           | (31,32,34)    |                                                                                         |
| 9     | dark grey (45,45,45)          | (255,255,255) | Indicador de controlador y color de texto                                                 |
| 10    | blue (50,80,240)              | (0,255,201)   |                                                                                         |
| 11    | white (255,255,255)           | (31,32,34)    |                                                                                         |
| 12    | grey (128,128,128)            | (160,160,160) |                                                                                         |
| 13    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 14    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 15    | white (255,255,255)           | (70,70,70)    |                                                                                         |
| 16    | green (114,201,0)             | (149,231,0)   |                                                                                         |
| 17    | green (114,201,0)             | (200,255,0)   |                                                                                         |
| 18    | blue (50,80,240)              | (0,255,201)   | olor de pastilla y texto de navegación (la lista a la izquierda) en, por ejemplo, ajustes cuando se selecciona |
| 19    | light blue (110,191,225)      | (0,151,130)   |                                                                                         |
| 20    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 21    | grey/blue (129,140,160)       | (160,180,179) |                                                                                         |
| 22    | green (114,201,0)             | (180,255,0)   |                                                                                         |
| 23    | green (140,241,0)             | (101,170,0)   |                                                                                         |
| 24    | red (240,19,0)                | (255,40,0)    |                                                                                         |
| 25    | green (0,160,0)               | (180,255,0)   |                                                                                         |
| 26    | white (255,255,255)           | (255,255,255) |                                                                                         |
| 27    | pink (255,40,91)              | (255,250,0)   |                                                                                         |
| 28    | grey (128,128,128)            | (200,200,200) |                                                                                         |
| 29    | neon blue (192,119,193)       | (25,214,210)  | Cursor                                                                                  |
| 30    | light neon blue (112,255,231) | (131,250,255) |                                                                                         |
| 31    | white (255,255,255)           | (80,80,80)    | Fondo circular del System Applets                                                         |
| 32    | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 33    | green/blue (87,255,219)       | (157,255,251) |                                                                                         |
| 34    | grey (110,120,121)            | (220,220,220) |                                                                                         |
| 35    | blue/grey-ish (129,140,160)   | (160,180,179) |                                                                                         |
| 36    | white (235,235,235)           | (22,22,22)    |                                                                                         |
| 37    | blue (7,163,203)              | (42,125,193)  |                                                                                         |
| 38    | blue (18,189,207)             | (2,136,199)   | Cursor                                                                                  |
| 39    | dark blue (15,89,114)         | (24,51,70)    |                                                                                         |
| 40    | light blue (29,241,255)       | (0,220,225)   |                                                                                         |
| 41    | light blue (29,241,255)       | (0,220,255)   | Resaltado azul al tocar                                                                   |
| 42    | light blue (0,190,200)        | (24,189,255)  | Texto del juego                                                                               |
| 43    | blue-ish (0,190,200)          | (24,189,255)  |                                                                                         |
| 44    | white (240,240,240)           | (70,70,70)    |                                                                                         |
| 45    | grey (255,255,255)            | (119,119,119) | Fondo circular de la selección del jugador                                                      |
| 46    | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 47    | white (255,255,255)           | (90,90,90)    |                                                                                         |
| 48    | dark blue (16,13,68)          | (0,0,0)       |                                                                                         |
| 49    | blue (50,80,240)              | (0,255,201)   |                                                                                         |
| 50    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 51    | white (255,255,255)           | (0,61,140)    |                                                                                         |
| 52    | white (235,235,235)           | (45,45,45)    |                                                                                         |
| 53    | grey (190,190,190)            | (190,190,190) |                                                                                         |
| 54    | white (240,240,240)           | (70,70,70)    |                                                                                         |
| 55    | green (0,200,0)               | (180,255,0)   |                                                                                         |
| 56    | green (140,240,28)            | (101,170,0)   |                                                                                         |
| 57    | green (0,170,0)               | (180,255,0)   |                                                                                         |
| 58    | dark grey (45,45,45)          | (255,255,255) | Icono de inicio de la pantalla de bloqueo                                                                   |
| 59    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 60    | grey (200,200,200)            | (120,120,120) |                                                                                         |
| 61    | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 62    | dark grey (45,45,45)          | (83,87,86)    | Tres puntos de la pantalla de bloqueo al desbloquear                                                 |
| 63    | white (255,255,255)           | (29,32,37)    |                                                                                         |
| 64    | dark blue (19,29,90)          | (0,0,0)       |                                                                                         |
| 65    | green/blue (0,91,186)         | (46,161,205)  | Cursor                                                                                  |
| 66    | blue (90,190,255)             | (0,255,201)   |                                                                                         |
| 67    | black (35,35,35)              | (45,45,45)    |                                                                                         |
| 68    | grey (114,114,114)            | (200,200,200) |                                                                                         |
| 69    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 70    | grey (200,200,200)            | (170,170,170) |                                                                                         |
| 71    | grey (45,45,45)               | (255,255,255) |                                                                                         |
| 72    | magenta (255,0,255)           | (0,0,0)       |                                                                                         |
| 73    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 74    | grey (128,128,128)            | (190,190,190) |                                                                                         |
| 75    | white (255,255,255)           | (255,255,255) |                                                                                         |
| 76    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 77    | blue (50,80,240)              | (0,255,201)   |                                                                                         |
| 78    | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 79    | white (255,255,255)           | (45,45,45)    |                                                                                         |
| 80    | blue (110,191,255)            | (0,151,130)   |                                                                                         |
| 81    | blue/grey-ish (129,140,160)   | (160,180,179) |                                                                                         |
| 82    | bright orange (240,19,0)      | (255,40,0)    |                                                                                         |
| 83    | white (255,255,255)           | (56,61,67)    |                                                                                         |
| 84    | white (255,255,255)           | (255,255,255) |                                                                                         |
| 85    | grey (201,201,201)            | (255,255,255) |                                                                                         |
| 86    | white (255,255,255)           | (56,61,67)    |                                                                                         |
| 87    | dark blue (19,29,90)          | (0,0,0)       |                                                                                         |
| 88    | red (255,59,69)               | (250,89,60)   | Notification applet                                                                     |
| 89    | soft orange (255,140,65)      | (255,140,65)  |                                                                                         |
| 90    | orange (255,160,0)            | (255,176,0)   | eShop applet                                                                            |
| 91    | grey (45,45,45)               | (255,255,255) |                                                                                         |
| 92    | blue (19,115,254)             | (30,160,255)  | Album applet                                                                            |
| 93    | blue (0,162,195)              | (49,231,255)  |                                                                                         |
| 94    | blue (60,160,255)             | (0,255,201)   |                                                                                         |
| 95    | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 96    | white (255,255,255)           | (30,19,59)    |                                                                                         |
| 97    | light blue (110,201,255)      | (99,255,231)  |                                                                                         |
| 98    | (101,116,147)                 | (160,180,197) |                                                                                         |
| 99    | green (140,241,0)             | (200,255,0)   |                                                                                         |
| 100   | grey (128,128,128)            | (80,80,80)    |                                                                                         |
| 101   | orange (255,140,65)           | (255,140,65)  |                                                                                         |
| 102   | white (255,255,255)           | (255,255,255) |                                                                                         |
| 103   | grey (190,190,190)            | (90,90,90)    |                                                                                         |
| 104   | white (255,255,255)           | (180,180,180) |                                                                                         |
| 105   | grey (154,154,154)            | (140,140,140) |                                                                                         |
| 106   | grey (45,45,45)               | (255,255,255) |                                                                                         |
| 107   | grey (148,148,148)            | (160,160,160) |                                                                                         |
| 108   | grey (128,128,128)            | (190,190,190) |                                                                                         |
| 109   | pink/orange (255,40,91)       | (255,250,0)   |                                                                                         |
| 110   | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 111   | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 112   | magenta (255,0,255)           | (255,0,255)   |                                                                                         |
| 113   | blue (50,80,240)              | (0,255,201)   |                                                                                         |
| 114   | blue (50,80,240)              | (0,255,201)   |                                                                                         |
| 115   | light green/blue (79,255,206) | (47,239,244)  |                                                                                         |
| 116   | green (114,201,0)             | (180,255,0)   |                                                                                         |
| ≥117  | black (0,0,0)                 | black (0,0,0) |                                                                                         |

</div>

## Lista de secciones USD conocidas

Estas son las secciones USD encontradas en todo el menú principal. No se pueden aplicar a todos los paneles.

---

### Relacionadas con el color

#### **`C_W`**

Un controlador de color dinámico que sobrescribe el BackgroundColor (Editor de Diseño de Switch)/Color Blanco (Caja de Herramientas de Switch) de un material.  
Una propiedad que se utiliza para dar a los elementos ciertos colores. Estos colores son dinámicos y pueden cambiar según el tema del sistema.
Usado casi en todas partes (todos los menús tienen que soportar temas oscuros y claros).

Tipo: `1`  
Formato: `[X, X, X, X]`

A menudo, solo el primer `X` es diferente de `0`. A veces, varios `X` son diferentes de `0`.

Para paneles de texto, el segundo `X` también puede ser utilizado. En el caso de que el flyt tenga una _clave de decisión_, tiene un estado especial: seleccionado por el cursor. En este caso, el primer `X` será el color cuando el texto esté _no seleccionado_, y el segundo `X` será el color una vez que el flyt **esté** seleccionado.

##### Ejemplo


```json
{
	"PropName": "C_W",
	"type": 1,
	"PropValues": [5, 0, 0, 0]
}
```

##### Valores

Utiliza los [valores globales de color](#valores-globales-de-color).

---

#### **`C_B`**

Un controlador de color dinámico que sobrescribe el ForegroundColor (Editor de Diseño de Switch)/Color Negro (Caja de Herramientas de Switch) de un material.  
No siempre tiene efecto. Parece ser utilizado, por ejemplo, en el cursor.

Tipo: `1`  
Formato: `[X, X, X, X]`

##### Ejemplo


```json
{
	"PropName": "C_B",
	"type": 1,
	"PropValues": [65, 0, 0, 0]
}
```

---

#### **`C_Id`**

_Funcionalidad desconocida_

El color no cambia cuando C_W se establece en otro color -> C_Id probablemente 'se superpone' a C_W.
El color del tema del sistema casi no tiene efecto (excepto para `0` ('apagado')).
Todo lo que se muestra aquí fue probado en la pantalla de bloqueo y puede variar según el menú.

Tipo: `1`  
Formato: `[X]`

##### Ejemplo

```json
{
	"PropName": "C_Id",
	"type": 1,
	"PropValues": [0]
}
```

##### Valores

<div class="color-table" markdown="1">

| Value | Light theme                | Comments                                      |               |
| ----- | -------------------------- | --------------------------------------------- | ------------- |
| 0     | -                          | -                                             | default (apagado) |
| 1     | white                      |                                               |               |
| 2     | white                      |                                               |               |
| 3     | white                      |                                               |               |
| 4     | black                      |                                               |               |
| 5     | black                      |                                               |               |
| 6     | black                      |                                               |               |
| 7     | black                      |                                               |               |
| 8     | dark blue (19,29,90)       |                                               |               |
| 9     | black                      |                                               |               |
| 10    | grey                       |                                               |               |
| 11    | black                      |                                               |               |
| 12    | blue-purpleish (50,80,240) |                                               |               |
| 13    | blue-purpleish (50,80,240) |                                               |               |
| 14    | white                      |                                               |               |
| 15    | ligher grey                | Parece superponerse al ícono del botón de inicio de entrada
 |               |
| 16    | white                      |                                               |               |
| 17    | white                      |                                               |               |
| 18    | white                      |                                               |               |
| 19    | black                      |                                               |               |
| 20    | white                      |                                               |               |
| 42    | grey                       | dark theme: white                             |               |

</div>

---

#### **`C_TI`**

_Functionality unknown_

Type: `1`  
Format: `[X]`

##### Ejemplo

```json
{
	"PropName": "C_Ti",
	"type": 1,
	"PropValues": [0]
}
```

##### Valores testeados

| Valor | Comentario |
| ----- | ------- |
| 0     | nothing |
| 1     | nothing |
| 10    | nothing |

---

### Borde

#### **`S_RoundRadius`**

Cambia el radio del borde de los paneles de imagen.
¿Porcentaje/píxeles?

Tipo: `2`  
Formato: `[X]`
Tipos de paneles: Solo imágenes

##### Ejemplo

```json
{
	"PropName": "S_RoundRadius",
	"type": 2,
	"PropValues": [50.0]
}
```

---

#### **`S_BorderDrawMode`**

_Functionality unknown_

Type: `1`  
Format: `[X]`  
Common value: `1`  
Example usage: `Cursor3`

##### Ejemplo

```json
{
	"PropName": "S_BorderDrawMode",
	"type": 1,
	"PropValues": [1]
}
```

##### Valores

| Valor | Resultado     |
| ----- | ---------- |
| 0     | No lo dibuje |
| 1     | Dibujelo       |
| other | Unknown    |

---

#### **`S_BorderVolume`**

Opacidad del borde.

Type: `2`  
Format: `[X]`

##### Ejemplo

```json
{
	"PropName": "S_BorderVolume",
	"type": 2,
	"PropValues": [1.5]
}
```

##### Valores

| Valor | Resultado        |
| ----- | ------------- |
| 0     | Sin opacidad    |
| 0-1   | Opacidad alternativa |
| 1     | Opacidad total  |

---

#### **`S_BorderSize`**

Tamaño del borde.

Tipo: `2`  
Formato: `[X]`  
Uso de ejemplo: `Cursor3`

##### Ejemplo


```json
{
	"PropName": "S_BorderSize",
	"type": 2,
	"PropValues": [5.0]
}
```

##### Valores

Ancho en pixeles

---

#### **`S_BorderColorSelect0`**

Establezca el color del borde. Sobreescribe [`S_BorderColor0`](#s_bordercolor0).

Type: `1`  
Format: `[X]`

##### Ejemplo

```json
{
	"PropName": "S_BorderColorSelect0",
	"type": 1,
	"PropValues": [1]
}
```

##### Valores

Usa [global color values](#global-color-values).

---

#### **`S_BorderColor0`**

Establezca el color del borde

Type: `2`  
Format: `[R, G, B, A]`

##### Ejemplo

```json
{
	"PropName": "S_BorderColor0",
	"type": 2,
	"PropValues": [5.0, 0, 0, 0]
}
```

##### Valores

Decimales RGB Normalizados, from 0-1

| Valor | Resultado (RGB normal) |
| ----- | ------------------- |
| 0     | 0                   |
| 0-1   | 0-255               |
| 1     | 255                 |

---

### Drop Shadow

#### **`S_DropShadowDrawMode`**

_Functionality unknown_

Type: `1`  
Format: `[X]`  
Common value: `1`  
Example usage: `RdtBtnIconGame`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowDrawMode",
	"type": 1,
	"PropValues": [1]
}
```

##### Valores

| Valor | Resultado     |
| ----- | ---------- |
| 0     | No lo dibuje |
| 1     | Dibujelo       |
| other | Unknown    |

---

#### **`S_DropShadowVolume`**

Densidad del color de la sombra

Type: `2`  
Format: `[X]`  
Example usage: `RdtBtnIconGame`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowVolume",
	"type": 2,
	"PropValues": [5.0]
}
```

---
#### **`S_DropShadowColorSelect`**

Establece el color de la sombra. Sobrescribe [`S_DropShadowColor`](#s_dropshadowcolor).

Tipo: `1`  
Formato: `[X]`  
Uso de ejemplo: `RdtBtnIconGame`

##### Ejemplo


```json
{
	"PropName": "S_DropShadowColorSelect",
	"type": 1,
	"PropValues": [1]
}
```

##### Valores

Utiliza el [global color values](#global-color-values).

---

#### **`S_DropShadowColor`**

Configure el color del Drop Shadow

Type: `2`  
Format: `[R, G, B, A]`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowColor",
	"type": 2,
	"PropValues": [1.0, 1.0, 1.0, 1.0]
}
```

##### Valores

Decimales RGB Normalizados, from 0-1

| Valor | Resultado (RGB normal) |
| ----- | ------------------- |
| 0     | 0                   |
| 0-1   | 0-255               |
| 1     | 255                 |

---

#### **`S_DropShadowAngle`**

Dirección de la sombra

Type: `2`  
Format: `[X]`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowAngle",
	"type": 2,
	"PropValues": [1.5]
}
```

##### Valores

Dirección en radianes.

| Valor          | Dirección |
| -------------- | --------- |
| 0              | right     |
| 1.57079632679  | down      |
| 3.14159265359  | left      |
| 4.71238898038  | up        |
| _Custom Angle_ | custom    |

---

#### **`S_DropShadowDistance`**

Distancia de la sombra fade/blur.

Type: `2`  
Format: `[X]`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowDistance",
	"type": 2,
	"PropValues": [5.2]
}
```

---

##### Valores

Distancia en pixeles

#### **`S_DropShadowSize`**

Tamaño de la sombra.

Type: `2`  
Format: `[X]`  
Example usage: `RdtBtnIconGame`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowSize",
	"type": 2,
	"PropValues": [10.0]
}
```

##### Valores

Ancho en pixeles

---

#### **`S_DropShadowFunction`**

_Functionality unsure_
Como es dibujado `S_DropShadowDistance` .Por ejemplo, blur o sólido?

Type: `1`  
Format: `[X]`  
Common value: `5` and `4`  
Example usage: `RdtBtnIconGame`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowFunction",
	"type": 1,
	"PropValues": [5]
}
```

---

#### **`S_DropShadowKnockout`**

_Functionality unsure_

Activa/desactiva el shadow fading?

Type: `1`  
Format: `[X]`  
Common value: `1`  
Example usage: `RdtBtnIconGame`

##### Ejemplo

```json
{
	"PropName": "S_DropShadowKnockout",
	"type": 1,
	"PropValues": [1]
}
```

# [Continue a Animaciones](../animations/index.md) :octicons-arrow-right-16:
