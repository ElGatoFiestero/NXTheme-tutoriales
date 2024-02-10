#####  [Volver a ResidentMenu.szs](index.md)

# RdtBase.bflyt (bflyt Principal)

**Archivo:** `ResidentMenu.szs/blyt/RdtBase.bflyt`<br>
**Este es el archivo bflyt principal**

---

## Diseño de `ResidentMenu.szs/blyt/RdtBase.bflyt `

<!-- prettier-ignore -->

## Árbol

-	**RootPane [pan 1]**
    -   **L_BgNml [prt 1]** `contiene el fondo original claro/oscuro, pero también el panel 'exelixbg' después de ser parcheado con un fondo personalizado`
    -   **N_Root [pan 1]**
		-	**N_ScrollArea [pan 1]** `área de desplazamiento de iconos de juego`
		-	**N_ScrollWindow [pan 1]** `ventana de desplazamiento de iconos de juego "Relacionada con el toque"`
		-	**T_Blank [txt 1]**
        -   **N_GameRoot [pan 1]** `panel que contiene todos los elementos que se desplazarán`
			-	**N_Game [pan 1]**
				-   **[`N_Icon[00-11] [pan 1]`](/docs/menu-docs/menus/ResidentMenu/RdtBtnIconGame.bflyt/index.md)** `los 12 iconos de juego. Utilizan el mismo diseño`
					-	**L_BtnChangeUser [prt 1]** `contiene "`:material-alpha-y-circle:` Cambiar usuario" RdtBtnChangeUser.bflyt`
				-   **N_Icon_12 [pan 1]** `El 13er icono: panel raíz de todas las aplicaciones`
					-   **L_BtnFlc [prt 1]** `botón de Todas las aplicaciones` [`RdtBtnFullLauncher.bflyt`](RdtBtnFullLauncher.bflyt/index.md)
        -   **N_System [pan 1]** `contiene todos los applets del sistema de Nintendo`
			-	**L_BtnLR [prt 1]** `botón de Nintendo Switch Online que no se puede ocultar mediante visibilidad`
            -   **L_BtnNoti [prt 1]** `el botón de notificaciones `
            -   **L_BtnShop [prt 1]** `el botón de la tienda en línea RdtBtnShop.bflyt`
            -   **L_BtnPvr [prt 1]** `el botón del álbum [RdtBtnPvr.bflyt](/docs/menu-docs/menus/ResidentMenu/RdtBtnPvr.bflyt/index.md)`
            -   **L_BtnCtrl [prt 1]** `el botón de los controles RdtBtnCtrl.bflyt`
            -   **L_BtnSet [prt 1]** `el botón de configuraciones RdtBtnSet.bflyt`
            -   **L_BtnPow [prt 1]** `el botón de encendido RdtBtnPow`
        -   **L_ChildLock [prt 1]** `el botón de bloqueo infantil`
        -   **N_Balloon [pan 1]**
        -   **N_MyPage [pan 1]** `panel raíz de iconos de usuario`
            -   **L_BtnAccount_[00-07] [prt1]** `todos los iconos de usuario que utilizan un único diseño`
        -   **L_Hud [prt 1]** `el HUD (reloj, red, batería) Hud.bflyt`
        -   **L_BalloonCtrl [prt 1]** `el globo que aparece cuando se (des)conecta un controlador RdtBalloonCtrl.bflyt`

#####  [Volver a ResidentMenu.szs](index.md)

**Archivo:** `ResidentMenu.szs/blyt/RdtBase.bflyt`<br>
