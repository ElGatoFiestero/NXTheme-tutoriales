##### [Regresar a ResidentMenu.szs](../index.md)

# RdtBalloon.bflyt

**Archivo:** `ResidentMenu.szs/blyt/RdtBalloon.bflyt`<br>
**Archivo principal `bflyt`:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Diseño de `ResidentMenu.szs/blyt/RdtBalloon.bflyt`

<!-- prettier-ignore -->
!!! Información
    Estas no son todas las funciones, la mayoría son desconocidas o el componente no es importante.
	
## Árbol

-   **N_Root [pan 1]**
    -   **N_Trans [pan 1]**
        -   **N_Size [pan 1]**
            -   **N_Scissor [pan 1]**
                -   **N_Offset [pan 1]**
                    -   **P_Reset [pic 1]**
                    -   **N_Scroll [pan 1]** `contiene todas las partes desplazables en el globo (así que solo realmente el texto)`
                        -   **T_Main [txt 1]** `el nombre del icono`
                        -   **N_Margin [pan 1]**
                        -   **T_Sub [txt 1]**
                    -   **W_Fade [wnd 1]**
                    -   **P_Color [pic 1]** `Color del texto del juego`
        -   **N_Card**
            -   **P_Card**: `ícono de la tarjeta de juego`
