##### [Regresar a ResidentMenu.szs](../index.md)

# RdtBtnCtrl.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`

<!-- prettier-ignore -->
!!! Información
    Estas no son todas las funciones, la mayoría son desconocidas o el componente no es importante.
	
## Árbol

-   **N_Root [pan 1]**
	-	**N_DecideKey [pan 1]**
		-	**N_DecideTouch [pan1]**
			-	**N_Pict [pan 1]**
				-	**P_Form [pic 1]** `Contorno del controlador o icono reemplazado`
				-	**P_Stick [pic 1]**
				-	**P_Y [pic 1]**
				-	**P_X [pic 1]**
				-	**P_A [pic 1]**
				-	**P_B [pic 1]**
			-	**N_ScaleDecide [pan 1]**
				-	**P_BtnDecideKey [pic 1]**
				-	**P_BtnTouch [pic 1]**
			-	**N_Limit [pan 1]**
				-	**N_BtnFocusKey [pan 1]**
					-	**UF_Cursor [prt 1]**
			-	**P_Effect [pic 1]**
	-	**N_Tip [pan 1]**
		-	**L_Balloon [prt 1**]
-	**B_Hit [bnd 1]**	
---

<!-- prettier-ignore -->
!!! Información
    La edición de colores del material puede ser complicada, edite los colores de fondo (RGBA) `255;255;255;AAA` (Alfa 0-255 para opacidad)

-	**Materiales**
	-	**0: P_Form**
	-	**1: P_Effect**
	-	**2: P_BtnTouch**
	-	**3: P_BtnDecideKey**
	-	**4: P_B**
	-	**5: P_A**
	-	**6: P_X**
	-	**7: P_Y**
	-	**8: P_Stick**
	-	**9: P_PictBase** `(Fondo del icono; Cambiar el color de fondo no `_`ForegroundColor`_`)`

---

##### [Regresar a ResidentMenu.szs](../index.md)

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
