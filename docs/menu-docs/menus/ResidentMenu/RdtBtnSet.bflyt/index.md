##### [Volver a ResidentMenu.szs](../index.md)

# RdtBtnSet.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnSet.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBtnSet.bflyt`

<!-- prettier-ignore -->
!!! Información
    Estas no son todas las funciones, la mayoría son desconocidas o el componente no es importante.
	
## Árbol

-	**RootPane**
	-	**N_Root [pan 1]**
		-	**N_DecideKey [pan 1]**
			-	**N_DecideTouch [pan1]**
				-	**P_PictBase [pic 1]** `Color de fondo`
				-	**N_PicRotate [pan1]**
					-	**N_PictPos [pan1]**
						-	**P_Pict [pic1]** `Color del ícono`
				-	**N_ScaleDecide [pan 1]**
					-	**P_BtnDecideKey [pic 1]**
					-	**P_BtnTouch [pic 1]**
				-	**N_BtnFocusKey [pan 1]**
				-	**UF_Cursor [prt 1]**
			-	**P_Effect [pic 1]**
	-	**N_Tip [pan 1]**
		-	**L_Balloon [prt 1]**
-	**B_Hit [bnd 1]**	
---

<!-- prettier-ignore -->
!!! Información
    La edición de colores del material puede ser complicada, edite los colores de fondo (RGBA) `255;255;255;AAA` (Alfa 0-255 para opacidad)

-	**Materiales**
	-	**0: P_BtnDecideKey**
	-	**1: P_BtnTouch**
	-	**2: P_Effect**
	-	**3: P_PictBase** `(Fondo del ícono; Cambiar color de fondo no `_`ForegroundColor`_`)`
	-	**4: P_Pict**
---
	
##### [Volver a ResidentMenu.szs](../index.md)

**Archivo:** `ResidentMenu.szs/blyt/RdtBtnSet.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
