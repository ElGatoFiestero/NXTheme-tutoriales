Para empezar, es esencial saber dónde encontrar partes específicas de los menús. Las siguientes páginas enumeran muchos componentes conocidos, pero también algunos que aún no están documentados. Siéntete libre de contribuir a este repositorio para ayudar a completar esta lista.

En las próximas páginas verás árboles de archivos para archivos bflyt que pueden ser modificados. Una breve descripción de un árbol bflyt puede contener:

- **panel [pan 1]** - `[pan 1] usualmente el panel Raíz pero puede haber más paneles dentro del panel raíz`
- **part [prt 1]** - `[prt 1] nombre de parte que está vinculado a un bflyt separado dentro del szs`
- **pic [pic 1]** - `[pic 1] relacionado con imágenes, podría ser un icono / botón, por ejemplo, o similar`
- **bnd [bnd 1]** - `[bnd 1] relacionado con botones`
- **txt [txt 1]** - `[txt 1] área de texto - el texto real no se puede cambiar, solo el color / opacidad, tamaño y ubicación`

Actualmente tenemos documentación parcial para:

| **Nombre Común**			   		| **Nombre del archivo SZS**			| **Descripción**									  			  					  |
| --------------------------------- | --------------------------------- | ----------------------------------------------------------------------------------- |
|**[Común](menus/common)** 		| `common.szs`						| compartido con el menú residente / tiene configuraciones de menú menores e iconos  |
|**[Menú Principal](menus/ResidentMenu)**| `ResidentMenu.szs`				| pantalla de inicio del switch o 'menú principal', iconos de applet, iconos de juegos|
|**[Pantalla de Bloqueo](menus/Entrance)** | `Entrance.szs`				| pantalla de inicio de bloqueo, iconos, HUD e información promocional en la pantalla de bloqueo |
|**[Todas las Aplicaciones](menus/Flaunch)** | `Flaunch.szs`				| Grupos, clasificación, añadir, eliminar y las antiguas todas las aplicaciones |
| Configuración						| `Set.szs` 						| página de configuración del switch												  |
|**[Selección de Jugador](menus/Psl)** | `Psl.szs`							| iconos, popup de nombre al elegir un juego y cargando un perfil					  |
| Página de Usuario					| `MyPage.szs`						| página de perfil de usuario														  |
| Noticias 							| `Notification.szs`				| página de noticias con los últimos lanzamientos de juegos e información de la consola|

!!! citar "no compatible"
	Los archivos a continuación no son compatibles con NXTheme
	algunos se pueden modificar pero las modificaciones pueden bloquear tu switch

| **Nombre Común**		    		| **Nombre del archivo SZS**		| **Descripción**																	  |
| --------------------------------- | --------------------------------- | ----------------------------------------------------------------------------------- |
| Eula								| `Eula.szs`						| contiene información sobre el acuerdo de licencia de usuario final					  |
| Gift							| `Gift.szs`						| 																					  |
| Interrupt						| `Interrupt.szs`					| contiene pantallas de alarma y pantallas de error / bloqueo de juego					  |
| Migration							| `Migration.szs`					| contiene pantallas de migración de cuenta											  |
| Option							| `Option.szs`						| contiene applets cuando presionas :material-plus-circle: en iconos de juegos		  |
| SaveMove					| `SaveMove.szs`					| panel de migración de guardado / información de guardado en la nube					  |


