##### [Regresar a ResidentMenu.szs](../index.md)

# RdtBtnIconGame.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`

<!-- prettier-ignore -->
!!! Información
    Estas no son todas las funciones, la mayoría son desconocidas o el componente no es importante.
	
## Árbol

-   **RootPane [pan 1]**
	-    **N_Root [pan 1]**
		-   **N_Delete [pan 1]**
			-   **N_DecideKey [pan 1]**
				-   **N_DecideTouch [pan 1]**
					-   **P_BtnBase [pic 1]** `el fondo blanco oculto detrás de un ícono de juego. Se puede ver brevemente después del arranque`
					-   **P_IconGame [pic 1]** `el ícono del juego`
					-   **P_Blank [pic 1]**
						-   **L_Loading [prt 1]** `el ícono de carga que se muestra encima de P_BtnBase`
					-   **N_Suspend [pan 1]**
						-   **N_SuspendPos [pan 1]**
							-   **N_TextPos [pan 1]**
								-   **P_Suspend_00 [pic 1]** `el fondo ovalado blanco detrás del texto`
								-   **T_Suspend [txt 1]** `el texto 'Jugando' cuando se abre un juego`
							-   **P_account_03 [pic 1]** `el icono de usuario que se muestra a la izquierda del indicador 'Jugando'`
							-	**P_account_02 [pic 1]** `el icono de usuario que se muestra a la izquierda del indicador 'Jugando'`
							-	**P_account_01 [pic 1]** `el icono de usuario que se muestra a la izquierda del indicador 'Jugando'`
							-	**P_account_00 [pic 1]** `el icono de usuario que se muestra a la izquierda del indicador 'Jugando'`
					-   **N_DL [pan 1]** `barras de carga sobre las que no tiene que preocuparse`
						-	**N_DlNml [pan 1]**
							-	**L_ProgressBarNml [prt1]**
						-	**N_DlErr [pan 1]**
							-	**L_ProgressBarErr [prt1]**
							-	**N_Offkine [pan 1]**
							-	**L_ProgressBarOffline [prt1]**
					-   **P_BtnDecideKey [pic 1]** `la superposición azul que se puede ver cuando se inicia un juego mediante el controlador`
					-   **P_BtnTouch [pic 1]** `la superposición azul que se puede ver al tocar/mantener presionado el ícono del juego`
					-   **P_InnerCursor [pic 1]** `el anillo blanco que se muestra entre el cursor azul y el ícono del juego`
					-   **N_BtnFocusKey [pan 1]**
						-   **UF_Cursor [prt 1]** `el cursor azul que se muestra alrededor del ícono del juego`
					-   **P_EffectDecide [pic 1]** `el efecto cuando se inicia un juego, se puede ver un segundo ícono de juego disolviéndose`
					-   **N_Promotion [pan 1]**
						-   **L_Promotion [prt 1]** `la función 'prueba' o 'intento' aún no utilizada para juegos`
-   **N_Tip [pan 1]** `se puede usar para posicionar RdtBalloon`
    -   **L_Balloon [prt 1]** - [`RdtBalloon.bflyt`](RdtBalloon.bflyt.md): el nombre/texto del juego en azul
-   **B_Hit [bnd 1]** `área de golpe de todos los elementos en N_DecideKey`

---

#####  [Regresar a ResidentMenu.szs](../index.md)

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../Rdt
