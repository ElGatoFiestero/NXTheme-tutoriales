##### [Regresar a ResidentMenu.szs](../index.md)

# RdtBalloonCtrl.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBalloonCtrl.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBalloonCtrl.bflyt`

<!-- prettier-ignore -->

## Árbol

- **RootPane [pan 1]**
    - **N_Change [pan 1]**
        - **P_Base [pic 1]** `el fondo emergente del controlador`
        - **P_Tip [pic 1]** `la flecha en el fondo emergente del controlador`
            - **P_TipShdw [pic 1]** `la sombra de la flecha en el fondo emergente del controlador`
        - **N_Ctrl [pan 1]** `Panel raíz de todos los iconos relacionados`
            - **P_CtrlJointH [pic 1]** `ícono del controlador / joycon horizontal`
            - **N_CtrlL [pan 1]** `Panel raíz del controlador izquierdo`
                - **N_CtrlLPos [pic 1]**
                    - **P_CtrlJointVL [pic 1]** `ícono del controlador izquierdo`
                - **N_BtnL [pan 1]** `Panel raíz del botón de gatillo`
                    - **P_BtnL [pic 1]** `botón de gatillo izquierdo`
                    - **P_CtrlJointVLGhost [pic 1]** `imagen fantasma/gris del joycon`
            - **N_CtrlR [pan 1]** `Panel raíz del controlador derecho`
                - **N_CtrlRPos [pic 1]**
                    - **P_CtrlJointVR [pic 1]** `ícono del controlador derecho`
                - **N_BtnR [pan 1]** `Panel raíz del botón de gatillo`
                    - **P_BtnR [pic 1]** `botón de gatillo derecho`
                    - **P_CtrlJointVRGhost [pic 1]** `imagen fantasma/gris del joycon`
