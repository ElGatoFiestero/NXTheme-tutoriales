##### [Regresar a ResidentMenu.szs](../index.md)

# RdtBtnFullLauncher.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`

<!-- prettier-ignore -->
!!! Información
    Estas no son todas las funciones, la mayoría son desconocidas o el componente no es importante.
	
## Árbol

-   **RootPane [pan 1]**
	-	**N_Root [pan 1]**
		-	**N_DecideKey [pan 1]**
			-	**N_DecideTouch [pan1]**
				-	**P_PicBase [pic 1]** `color de fondo completa del lanzador`
				-	**N_Pict [pan1]**
					-	**P_Pict_00 [pic1]** `cuatro íconos cuadrados - Arriba a la izquierda`
						-	**P_PictBase_00 [pic 1]**
					-	**P_Pict_01 [pic1]** `cuatro íconos cuadrados - Arriba a la derecha`
						-	**P_PictBase_01 [pic 1]**
					-	**P_Pict_02 [pic1]** `cuatro íconos cuadrados - Abajo a la izquierda`
						-	**P_PictBase_02 [pic 1]**
					-	**P_Pict_03 [pic1]** `cuatro íconos cuadrados - Abajo a la derecha`
						-	**P_PictBase_03 [pic 1]**
				-	**N_ScaleDecide [pan 1]**
					-	**P_BtnDecideKey [pic 1]**
					-	**P_BtnTouch [pic 1]**
				-	**N_BtnFocusKey [pan 1]**
					-	**UF_Cursor [prt 1]**
		-	**N_Tip [pan 1]**
		-	**L_Balloon [prt 1]**
	-	**B_Hit [bnd 1]**

---

<!-- prettier-ignore -->
!!! Información
    La edición de colores del material puede ser complicada, edite los colores de fondo (RGBA) `255;255;255;AAA` (Alfa 0-255 para opacidad)

-	**Materiales**
	-	**0: P_BtnDecideKey**
	-	**1: P_Btn_Touch**
	-	**2: T_Main**
	-	**3: P_Effect**
	-	**4: P_Pict_00**
	-	**5: P_Pict_01**
	-	**6: P_Pict_02**
	-	**7: P_Pict_03**
	-	**8: P_PictBase_00**
	-	**9: P_PictBase_01**
	-	**10: P_PictBase_02**
	-	**11: P_PictBase_03**
	-	**12: P_PictBase** `(Fondo del lanzador; Cambiar el color de fondo no `_`ForegroundColor`_`)`

---

##### [Regresar a ResidentMenu.szs](../index.md)
**Archivo:** `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
