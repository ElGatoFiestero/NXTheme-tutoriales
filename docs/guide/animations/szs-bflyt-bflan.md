##### :octicons-arrow-left-16: [Volver a Animaciones: PaiTags y AnimationTargets](./paitags-and-targets.md)


# Archivos szs, bflyt, bflan 
---

Aquí tienes una lista no exhaustiva de componentes de la interfaz de usuario que pueden ser animados.

##### ResidentMenu.szs (home screen)

| `.bflyt`             | Elemento de la interfaz de usuario | Archivos `.bflan` destacados                                             |
|----------------------|-------------------------------------|--------------------------------------------------------------------------|
| `RdtBase`            | menú completo de la pantalla de inicio | `RdtBase_Enter` (animación al desbloquear la consola en la pantalla de inicio) |
| `RdtBtnIconGame`     | botón de juego                      | `RdtBtnIconGame_Active`, `RdtBtnGame_Inactive`                        |
| `RdtBtnFullLauncher` | botón de todas las apps| `RdtBtnFullLauncher_Active`, `RdtBtnFullLauncher_Inactive`            |
| `RdtBtnPvr`          | botón de  álbum         | `RdtBtnPvr_Active`, `RdtBtnPvr_Inactive`                              |
| `RdtBtnCtrl`         | botón de  los controles | `RdtBtnCtrl_Active`, `RdtBtnCtrl_Inactive`                            |
| `RdtBtnSet`          | botón de  ajustes       | `RdtBtnSet_Active`, `RdtBtnSet_Inactive`                              |
| `RdtBtnPow`          | botón de encendido                   | `RdtBtnPow_Active`, `RdtBtnPow_Inactive`                              |
| `RdtBtnMyPage`       | botón de perfil de usuario           | `RdtBtnMyPage_Active`, `RdtBtnMyPage_Inactive`                        |

##### Set.szs (applet de ajustes)

| `.bflyt`      | Elemento de la interfaz de usuario | Archivos `.bflan` destacados                          |
|---------------|------------------------------------|-------------------------------------------------------|
| `BtnNav_Root` | Pestaña del menú de navegación     | `BtnNav_Root_Active`, `BtnNav_Root_Inactive`          |

##### Flauncher.szs (applet de todas las aplicaciones)

| `.bflyt`             | Elemento de la interfaz de usuario                                               | Archivos `.bflan` destacados                              |
|----------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| `FlcBtnIconGame`     | Icono del juego en las pantallas principales y de grupo                           | `FlcBtnIconGame_Active`, `FlcBtnIconGame_Inactive`         |
| `FlcBtnIconGameEdit` | Icono del juego en las pantallas de crear grupo y agregar/eliminar software      | `FlcBtnIconGameEdit_Active`, `FlcBtnIconGameEdit_Inactive` |

# [Continuar con el diffpatch](../diffpatch/index.md) :octicons-arrow-right-16:

