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
| ----------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------ |
| AreaNml.bflyt		      	    | ÁreaNormal				 	           | Define área de desplazamiento/toque/puntero										  |
| AreaNmlL.bflyt		        | ÁreaNormalGrande			 		   | Área de desplazamiento/toque/puntero más grande									   |
| AreaNmlLGrp.bflyt	     	    | GrupoÁreaNormalGrande		           | Ventanas de grupo de desplazamiento/toque/puntero									   |
| AreaNmlNav.bflyt	     	    | NavegaciónÁreaNormal		       	   | Área de navegación de desplazamiento/toque/puntero (lateral de añadir/crear grupo)   |
| AreaNmlNavMain.bflyt	        | VentanaPrincipalNavegaciónNormal    | Ventana principal de navegación de desplazamiento/toque/puntero (iconos?)			   |
| BaseBg.bflyt                  | FondoBase                            | Contiene un indicador de carga para cuando la lista aún se está cargando               |
| BaseChild.bflyt		        | HijoBase (applet?)		           | Contiene información básica de diseño para partes de applet (encabezado/lado/contenido principal) |
| BgNav_Root.bflyt	   	        | FondoNavegación_Raíz		       	   | Panel de fondo de navegación												 	   |
| BgNml.bflyt                   | FondoNormal                         | Contiene panel de fondo del menú principal + '[exelixbg](../../../definitions.md#exelixbg)' |
| BtnIslandIcon.bflyt           | BotónIslaIcono		               | Color de texto/ícono del contenido del botón (L R +)								   |
| BtnIslandNml.bflyt	        | BotónIslaNormal		           	   | Información estándar del botón color de texto										   |
| BtnLineNml.bflyt	       	    | LíneaBotónNormal			 	       | Botón "en línea" es decir, ¿lista desplegable?									   |
| BtnOpt_Root.bflyt	       	    | OpciónBotón_Raíz			         | Información del botón en menú desplegable? Contiene marcado de casilla inválido y válido |
| BtnExpand.bflyt               | BotónExpandir                       | Menú desplegable [grupos?/ordenar] posiblemente cambiado en 14.0                       |
| Cursor3.bflyt                 | Cursor3                             | Cursor                                                                              |
| DBtmFlcSortAndFilter.bflyt    | OrdenarYFiltrarFondoCompletoLauncher| Contiene la información base del menú "ordenar y filtrar" cuando la lista todavía se está cargando |
| DBtmHeaderNml.bflyt	        | EncabezadoInferiorNormal		     | Contiene información de encabezado icono/texto y línea superior						   |
| FlcBalloon.bflyt              | GloboCompletoLauncher               | Globo de nombre de la aplicación                                                      |
| FlcBtnGrp.bflyt			    | GrupoBotonesCompletoLanzador		 | Icono de grupo con iconos agrupados incluye el botón de ordenar / texto				   |
| FlcBtnGrpBlock.bflyt		    | BloqueGrupoBotonesCompletoLanzador | Información de bloque de iconos de grupo desplazamiento/espaciado de las 4 filas de iconos de grupo |
| FlcBtnIconGame.bflyt          | IconoJuegoCompletoLanzador         | El diseño del icono del juego. Utilizado para todos los iconos                          |
| FlcBtnIconGameBlock.bflyt     | BloqueIconoJuegoCompletoLanzador   | Información del icono del juego en filas/espaciado                                    |
| FlcBtnIconGameEdit.bflyt	    | EdiciónIconoJuegoCompletoLanzador	 | Diseño del icono del juego en la pantalla de edición (ordenar/mover/comprobar)		   |
| FlcBtnIconGameEditBlock.bflyt | BloqueEdiciónIconoJuegoCompletoLanzador | Información de diseño del icono del juego en la pantalla de edición (espaciado)	   |
| FlcBtnLineAddGrp.bflyt	 	| AñadirGrupoLíneaBotónCompletoLanzador | Botón de crear grupo														  	   |
| FlcCntMain.bflyt		 		| ContenidoPrincipalCompletoLanzador | Ventana principal de AllApps												  	   |
| FlcDGrpDelete.bflyt		 	| EliminarGrupoDiálogoCompletoLanzador | Información de diseño de "Eliminar Grupo" applet									   |
| FlcDGrpOption.bflyt          	| OpciónGrupoDiálogoCompletoLanzador | Información de lista desplegable "Editar Grupo"									   |
| FlcGrpList.bflyt		 		| ListaGruposCompletoLanzador	     | Ventana principal de grupos / Ordenar grupos (ambos diseños están en esta ventana)	   |
| FlcGrpMain.bflyt		 		| PrincipalGrupoCompletoLanzador	 | Ventana de contenido de carpeta de grupo (iconos en carpeta de grupo)				   |
| FlcGrpSoftArrangement.bflyt   | DisposiciónSoftwareGrupoCompletoLanzador | Ordenar ventana de contenido de software (Ordenar juegos en una carpeta de grupo)	   |
| FlcGrpSoftEdit.bflyt		    | EdiciónSoftwareGrupoCompletoLanzador    | Agregar/eliminar ventana de contenido de software (Agregar y quitar/buscar juegos ventana) |
| LineHeader_Root.bflyt         | RaízLíneaEncabezado                 | La línea horizontal que se muestra en el encabezado (tamaño y posición relativa)        |
| NtfBtnSearchChannel.bflyt     | BotónBúsquedaCanalNotificación      | Cuadro/botón de "Buscar por palabra clave" e icono de lupa							   |
| TextH1.bflyt                  | TextoEncabezado1                    | El componente de encabezado principal completo                                         |
| TextH2.bflyt			 		| TextoEncabezado2			           | Texto de encabezado dentro de los grupos											   |
| Waitingicon.bflyt		 		| IconoEspera				           | Icono de carga																	       |


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
