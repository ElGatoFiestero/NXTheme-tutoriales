# Diffpatching

Esta guía es un ejemplo de Difusión usando un json pre hecho (diffpatch).<br> 
fue hecho por sodasoba para parchear Option.szs para que coincida con su tema switchdeck.

Option.szs tiene que ser parcheado manualmente ya que no es compatible con NXThemesInstaller pero puede ser parcheado en [switchlayouteditor](https://github.com/FuryBaguette/SwitchLayoutEditor/releases) el archivo parcheado se copia entonces a `SDMC:/atmosphere/contents/0100000001000/romfs/lyt` con los otros archivos szs

!!! cite "Ubicaciones de los SZS parcheados:"
    Consulta la página de [Archivos de menú](../menu-files.md) para los szs y sus ubicaciones dentro de `atmosphere/contents/<TITLEID>/romfs/lyt`

Sin el parche aplicado este es el SZS sin editar
![unpatched](<00opt.jpg>)

similar al ejemplo en la página de [diffpatch](index.md) este diffpatch tiene configuraciones que cambiarán:

 * _`option.szs/blyt/Line_Root.bflyt` - Eliminado_
 * _`option.szs/blyt/OptMain.bflyt` - Tema de color de fondo coincidente y tamaño de icono modificado_
 * _`option.szs/blyt/BgPlate.bflyt` - Color de fondo_
 * _`option.szs/blyt/OptNav.bflyt` - Movido hacia abajo_
 * _`option.szs/blyt/LineHeader_Root.bflyt` - Eliminado_
 * _`option.szs/blyt/BgNav_Root.bflyt` - Color de fondo / más oscuro_


Después de que se aplique el difpatch, el Option.szs ahora se verá así
![patched](<01opt.png>)

NXThemesInstaller extrae los archivos szs en la tarjeta SD de tu Switch a la ubicación: `SDMC:/themes/systemData/`. Ubica tu versión de _Option.szs_

![SDMC](<01-sdmc.png>)

Haz una copia de Option.szs en tu computadora y luego descarga y extrae el diffpatch

[Option-diffpatch-for-switchdeck.zip](Option-diffpatch-for-switchdeck.zip)

Abre switchlayouteditor y abre option.szs o arrastra option.szs al switchlayouteditor

![loadszs](<04-load-option.png>)

Una vez que option.szs esté abierto, se abrirá una ventana más pequeña, solo necesitamos cargar nuestro diffpatch y no editar nada en este ejemplo, pero podrías cargar un diffpatch y usarlo como punto de partida para la temática.

Haz clic en `Herramientas` > `Cargar parche JSON`

![unpatched](<05-load-diff-switchdeck.png>)

Localiza el diffpatch que deseas aplicar en tu computadora y ábrelo

![unpatched](<6-open-diff-switchdeck.png>)

Una vez que esté cargado, aparecerá un mensaje emergente indicando que se ha cargado

![unpatched](<7-loaded-diff-switchdeck.png>)

Ahora guarda el Option.szs parcheado

haciendo clic en `Guardar` > `Guardar`

![unpatched](<8-loaded-diff-switchdeck.png>)

Pega el Option.szs parcheado desde tu escritorio en la tarjeta SD

`SDMC:/atmosphere/contents/010000000001000/romfs/lyt/`

![unpatched](<9-loaded-diff-switchdeck.png>)

!!! cite "Ubicaciones de los SZS parcheados:"
	Consulta la página de [Archivos de menú](../menu-files.md) para los szs y sus ubicaciones dentro de `atmosphere/contents/<TITLEID>/romfs/lyt`
	
Reinicia tu Switch y listo.

# [Continúa con Tematización manual de SZS](../manualszs/index.md) :octicons-arrow-right-16:
