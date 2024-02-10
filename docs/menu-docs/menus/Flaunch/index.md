**Archivo:** `Flaunch.szs`
**Archivo principal `bflyt`:** [`FlcCntMain.bflyt`](FlcCntMain.bflyt.md)
---

## Archivos de diseño en `Flaunch.szs`

<!-- prettier-ignore -->
!!! Info
    Estos no son todos los archivos, porque la función es desconocida o el componente no es importante.
	
	Flaunch.szs está vinculado en ResidentMenu.szs bajo RdtBtnFullLauncher.bflyt y es conocido como FullLauncher dentro de Nintendo.
	La mayoría de los usuarios lo conocerán como AllApps. Este archivo ahora contiene carpetas/grupos desde HOS 14.0.0.

| Nombre de archivo              | Nombre completo hipotético            | Función                                                                             |
| ----------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------- |
| AreaNml.bflyt                 | AreaNormal                          | Define el área de desplazamiento/toque/cursor                                       |
| AreaNmlL.bflyt                | AreaNormalLarge                     | Área de desplazamiento/toque/cursor más grande                                      |
| AreaNmlLGrp.bflyt             | AreaNormalLargeGroup                | Ventanas de grupo de área de desplazamiento/toque/cursor                             |
| AreaNmlNav.bflyt              | AreaNormalNavigation                | Área de navegación de desplazamiento/toque/cursor (lado de agregar/crear grupo)      |
| AreaNmlNavMain.bflyt          | AreaNormalNavigationMain            | Ventana principal de navegación de desplazamiento/toque/cursor (¿iconos?)            |
| BaseBg.bflyt                  | BaseBackground                      | Contiene un indicador de carga para cuando la lista todavía está cargando            |
| BaseChild.bflyt               | BaseChild (applet?)                 | Contiene información básica de diseño para partes del applet (encabezado/lateral/contenido principal) |
| BgNav_Root.bflyt              | BackgroundNavigation_Root           | Panel de fondo de navegación                                                        |
| BgNml.bflyt                   | BackgroundNormal                    | Contiene el panel de fondo del menú principal + '[exelixbg](../../../definitions.md#exelixbg)' |
| BtnIslandIcon.bflyt           | ButtonIslandIcon                    | Color de texto/ícono del contenido del botón (L R +)                                 |
| BtnIslandNml.bflyt            | ButtonIslandNormal                  | Información estándar del botón: color de texto                                       |
| BtnLineNml.bflyt              | ButtonLineNormal                    | Botón "en línea", ¿es una lista desplegable?                                         |
| BtnOpt_Root.bflyt             | ButtonOption_Root                   | Información del botón en el menú desplegable: incluye marca de verificación inválida y válida |
| BtnExpand.bflyt               | ButtonExpand                        | Menú desplegable [grupos/clasificación] posiblemente cambiado en 14.0                |
| Cursor3.bflyt                 | Cursor3                             | Cursor                                                                               |
| DBtmFlcSortAndFilter.bflyt    | BottomFullLauncherSortAndFilter     | Contiene la base de información del menú "ordenar y filtrar"                          |
| DBtmHeaderNml.bflyt           | BottomHeaderNormal                  | Contiene información del encabezado: icono/texto y línea superior                     |
| FlcBalloon.bflyt              | FullLauncherBalloon                 | Globo de nombre de la aplicación                                                      |
| FlcBtnGrp.bflyt               | FullLaunchButtonGroup               | Icono de grupo con iconos agrupados: incluye la opción de clasificación/texto          |
| FlcBtnGrpBlock.bflyt          | FullLaunchButtonGroupBlock          | Información del bloque de iconos de grupo en filas/espaciado                           |
| FlcBtnIconGame.bflyt          | FullLauncherButtonIconGame          | Diseño del ícono del juego. Se usa para todos los íconos                                |
| FlcBtnIconGameBlock.bflyt     | FullLauncherButtonIconGameBlock     | Información del ícono del juego en filas/espaciado                                      |
| FlcBtnIconGameEdit.bflyt      | FullLaunchButtonIconGameEdit        | Pantalla de edición del ícono del juego (ordenar/mover/comprobar)                       |
| FlcBtnIconGameEditBlock.bflyt | FullLaunchButtonIconGameEditBlock   | Información del diseño de edición del ícono del juego                                       |
| FlcBtnLineAddGrp.bflyt        | FullLaunchButtonLineAddGroup        | Botón de "crear grupo"                                                                  |
| FlcCntMain.bflyt              | FullLauncherContentMain             | Ventana principal de todas las aplicaciones                                                |
| FlcDGrpDelete.bflyt           | FullLaunchDialogGroupDelete         | Información del diseño del applet "eliminar grupo"                                       |
| FlcDGrpOption.bflyt           | FullLaunchDialogGroupOption         | Información de la lista desplegable "editar grupo"                                       |
| FlcGrpList.bflyt              | FullLaunchGroupList                 | Ventana principal de grupos/ordenar grupos (ambos diseños están en esta ventana)            |
| FlcGrpMain.bflyt              | FullLaunchGroupMain                 | Ventana de contenido de carpeta de grupo
		 		| IconoEspera				           | Icono de carga																	       |


<details>
  <summary>Tabla en inglés para desambiguación</summary>
  
 
| Filename                      | Hypothetical full name             | Function                                                                           |
| ----------------------------- | ---------------------------------- | ---------------------------------------------------------------------------------- |
| AreaNml.bflyt		      	    | AreaNormal				 	     | Defines scroll/touch/cursor area							      	  				  |
| AreaNmlL.bflyt		        | AreaNormalLarge			 		 | Scroll/touch/cursor Larger area									  				  |
| AreaNmlLGrp.bflyt	     	    | AreaNormalLargeGroup		         | Scroll/Touch/Cursor group windows							        			  |
| AreaNmlNav.bflyt	     	    | AreaNormalNavigation		       	 | Scroll/Touch/Cursor Navigation area (side of add/create group)		      	  	  |	
| AreaNmlNavMain.bflyt	        | AreaNormalNavigationMain(window?)  | Scroll/Touch/Cursor MainNavigation window (icons?)						  		  |
| BaseBg.bflyt                  | BaseBackground                     | Contains a loading indicator for when the list is still loading                	  |
| BaseChild.bflyt		        | BaseChild (applet?)		         | Contains Basic Layout information for applet parts (header/side/main content)	  |
| BgNav_Root.bflyt	   	        | BackgroundNavigation_Root	       	 | Navigation Background Panel									  					  |
| BgNml.bflyt                   | BackgroundNormal                   | Contains mainmenu background pane + '[exelixbg](../../../definitions.md#exelixbg)' |
| BtnIslandIcon.bflyt           | ButtonIslandIcon		       		 | Button contents text color/icon (L R +)							  				  |
| BtnIslandNml.bflyt	        | ButtonIslandNormal		         | Standard Button information text color								  			  |
| BtnLineNml.bflyt	       	    | ButtonLineNormal			 		 | Button "inline" ie dropdown list?								  				  |
| BtnOpt_Root.bflyt	       	    | ButtonOption_Root			 		 | Button information in drop down? Contains checkbox invalid & valid inc mark	  	  |
| BtnExpand.bflyt               | ButtonExpand                       | Drop Down Menu [groups?/sort] possibly changed in 14.0                             |
| Cursor3.bflyt                 | Cursor3                            | Cursor                                                                         	  |
| DBtmFlcSortAndFilter.bflyt    | BottomFullLauncherSortAndFilter    | contains the "sort and filter" menu base information					  			  |
| DBtmHeaderNml.bflyt	        | BottomHeaderNormal		         | Contains header information icon / text & top line						  		  |
| FlcBalloon.bflyt              | FullLauncherBalloon                | App name balloon 			                                                  	  |
| FlcBtnGrp.bflyt			    | FullLaunchButtonGroup		 	     | Group Icon with clustered Icon includes the sort allows / text				  	  |
| FlcBtnGrpBlock.bflyt		    | FullLaunchButtonGroupBlock		 | Group Icon block information scrolling/spacing of the 4 groupicon rows		  	  |
| FlcBtnIconGame.bflyt          | FullLauncherButtonIconGame         | The game icon layout. Used for all icons                                       	  |
| FlcBtnIconGameBlock.bflyt     | FullLauncherButtonIconGameBlock    | Game Icon information in Rows/padding                                         	  |
| FlcBtnIconGameEdit.bflyt	    | FullLaunchButtonIconGameEdit	 	 | Game Icon in edit screen (sort/move/check)							  			  |
| FlcBtnIconGameEditBlock.bflyt | FullLaunchButtonIconGameEditBlock  | Edit Game Icon Layout Padding information							  			  |
| FlcBtnLineAddGrp.bflyt	 	| FullLaunchButtonLineAddGroup	 	 | Create Group Button											  					  |
| FlcCntMain.bflyt		 		| FullLauncherContentMain		     | The Main AllApps screen window									  				  |
| FlcDGrpDelete.bflyt		 	| FullLaunchDialogGroupDelete 	 	 | "Delete Group" Applet layout information							  				  |
| FlcDGrpOption.bflyt          	| FullLaunchDialogGroupOption	 	 | "Edit Group" drop down list information							  				  |
| FlcGrpList.bflyt		 		| FullLaunchGroupList			 	 | Groups Main Window / Sort Groups Main Window (both layouts are in this window)	  |
| FlcGrpMain.bflyt		 		| FullLaunchGroupMain			 	 | Group Folder Contents Window (icons in group folder)					  			  |
| FlcGrpSoftArrangement.bflyt   | FullLaunchGroupSoftwareArrangement | Sort Software Contents Window (Sort Games in a Group Folder)				  		  |
| FlcGrpSoftEdit.bflyt		    | FullLaunchGroupSoftwareEdit        | Add/Remove Software Contents Window (Add & remove/search games window)		  	  |
| LineHeader_Root.bflyt         | LineHeader Root                    | The horizontal line that is shown in the header (size & relative position)      	  |
| NtfBtnSearchChannel.bflyt     | NotificationButtonSearchChannel	 | "Search by Keyword" Box/button & magnifier icon						  			  |
| TextH1.bflyt                  | TextHeader1                        | The complete main header component                                                 |
| TextH2.bflyt			 		| TextHeader2				 		 | Header Text within groups										  				  |
| Waitingicon.bflyt		 		| WaitingIcon				 		 | Loading icon												  						  |
</details>
