# Mensajes personalizados/Texto/Traducciones

Es posible editar cualquier texto mostrado en un menú editando el archivo de cadenas de texto.

## Información

Los mensajes de texto se almacenan en `0100000000001000\romfs\message\<lang code>\<menu>.msbt.szs`

## Lo que necesitarás

- Archivos romfs de qlaunch (extraer firmware, extraer qlaunch)
- [Kuriimu v1](https://github.com/IcySon55/Kuriimu/releases)

## Ejemplo de pasos para cambiar la etiqueta del botón eShop

1. Copia el archivo `qlaunch.msbt.szs` del idioma que deseas editar desde el romfs de qlaunch (ver ruta arriba)
2. Abre Kuriimu y sigue esta ruta: ![image](https://cdn.discordapp.com/attachments/495784470377398282/495850689394638848/unknown1.png)
3. Selecciona `qlaunch.msbt.szs`
4. Te preguntará dónde descomprimirlo. Mantendrá el "szs" al final, pero dirá decomp.szs, así que estará desempaquetado
5. Ahora abre el `qlaunch.msbt.decomp.szs` en Kuriimu y debería verse como esta captura de pantalla (con una lista de nombres de cadenas de texto a la izquierda) ![image](https://cdn.discordapp.com/attachments/495784470377398282/495850914872295424/unknown.png)
6. Para cambiar la etiqueta del botón eShop, ve hacia abajo a los que están etiquetados como `RdtSystemTitle_Shop`
7. Cambia a lo que quieras, guárdalo. Luego repite los pasos de "Descomprimir" pero comprime esta vez
8. Renombra el archivo comprimido `.szs` a `qlaunch.msbt.szs`
9. Copia el `qlaunch.msbt.szs` modificado a `SD:\atmosphere\contents\0100000000001000\romfs\message\<lang code>\qlaunch.msbt.szs`

Para una guía más extensa (aunque aún no está terminada) [echa un vistazo a esta](https://github.com/bandithedoge/switch-pl/wiki) por bandithedoge
