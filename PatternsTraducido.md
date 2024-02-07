[](#bienvenida)**Bienvenidos**,
========================

Este wiki es donde aprenderemos cómo editar el tema de fondo en movimiento y usar tus propias imágenes. Será una experiencia divertida e informativa, especialmente si estás aburrido de los mismos temas de siempre. Al menos eso espero. 😀

[](#lo-que-aprenderas)Lo Que Aprenderás:
--------------------------------------------

En este tutorial, aprenderás cómo tomar una imagen de patrón con una escala de 1:1, que puede duplicarse completamente y crear un fondo de pantalla gigante. Luego, harás zoom en una esquina y te moverás a la esquina opuesta antes de regresar a la posición original. El movimiento de ida y vuelta continuará hasta alcanzar el límite de fotogramas, que es de 64000 fotogramas (alrededor de 7.5 minutos).

[](#que-es-un-tema-de-fondo-animado)¿Qué es un tema de fondo animado?
----------------------------------------------------------------------------

Primero, hablemos sobre los conceptos básicos de crear un tema de fondo en movimiento. Un tema de fondo en movimiento es esencialmente un archivo de imagen que se repite continuamente en el fondo del menú de inicio de tu Nintendo Switch. La imagen generalmente está compuesta por un patrón o imagen que se repite y escala para crear una sensación de movimiento.

<div align="center">
  <video src="https://github.com/ElGatoFiestero/TutorialTemasNintendoSwitch/assets/159089859/f45c6285-934c-435d-a65a-347d5d9d026a" width="720" />
</div>






[](#requisitos)Requisitos:
------------------------------

Para crear tu propio tema de fondo en movimiento, necesitarás algunas cosas:

1.  Un patrón o imagen que pueda repetirse y escalarse sin problemas.
2.  Un software de edición que te permita editar imágenes.
3.  [Switch Theme Injector](https://github.com/exelix11/SwitchThemeInjector)
4.  Conocimiento sobre cómo editar un JSON.

[](#ejemplo)Ejemplo:
====================

Comencemos con el primer paso, que es encontrar un patrón o imagen que pueda repetirse y escalarse sin problemas. Una forma fácil de hacer esto es usar un programa como Adobe Photoshop o GIMP para crear un patrón repetitivo. En este ejemplo usaré Photoshop. Si vas a Vista previa de patrones, básicamente puedes verificar lo que obtendrás. ![1](https://user-images.githubusercontent.com/93286561/222496034-8ad8d9f6-cbec-4dd3-99ff-18c770157341.jpg) ![2](https://user-images.githubusercontent.com/93286561/222496353-e69c804c-39a6-465c-95f5-bf308e841b18.jpg)

Después de eso, deberás redimensionar la imagen al tamaño de 1280x720, lo cual es necesario ya que el nxtheme requiere una imagen que sea 1280x720. La imagen se deformará, pero está bien. En la animación, podemos cambiar la escala de la posición X, dándole nuevamente una relación de aspecto 1:1.

![3](https://user-images.githubusercontent.com/93286561/222497174-49542687-a230-417d-a4bc-d44139292d78.jpg)

Una vez que tengas tu patrón, deberás exportarlo como JPG, no lo exportes como PNG porque no queremos transparencia.

Después de eso, puedes usar esta plantilla JSON que utilizo en mi tema Patterns.

[Patterns. JSONs Vertical & 1x1](/JSON%20TEMPLATE%20FOR%20ANIMATION)

Si deseas utilizar tu propio tema JSON, debes cambiar el panel blyt/BgNml.bflyt en el JSON del menú principal por el siguiente:

`{ "FileName": "blyt/BgNml.bflyt", "Patches": [ { "PaneName": "P_Bg_00", "Position": { "X": 5000.0, "Y": 60000.0 } } ], "AddGroups": [ { "GroupName": "G_ZBG", "Panes": [ "exelixBG" ] } ], "Materials": [ { "MaterialName": "P_Custm", "Refs": [ { "Name": "White1x1A128^s", "WrapS": 5, "WrapT": 5 }, ], "Transforms": [ { "Name": "White1x1A128^s", "ScaleX": 10, "ScaleY": 10 } ] } ] }`

![4](https://user-images.githubusercontent.com/93286561/222501806-a8d6af91-1a4b-453f-bec6-405b9b89b4bf.jpg)

**Cambia a:**

![5](https://user-images.githubusercontent.com/93286561/222501842-1bb1c548-400b-40d2-8960-e2c86fc292df.jpg)

Este código indica cómo se comportará el fondo en el menú.

*   La posición, como dije antes, ya que estamos ampliados, debe estar en la esquina.
*   El wrapT y wrapS a 5 significa que la imagen se duplicará y creará un patrón.
*   La escala es el número de repeticiones que hará el patrón. Cuanto mayor sea el número, más pequeño será el fondo.

Haz esto **SÓLO DESPUÉS DE QUE TODAS TUS EDICIONES ESTÉN HECHAS EN EL EDITOR DE TEMAS DE SWITCH**, el Switch theme injector no está listo para temas en movimiento y reemplazará este panel con el Diff predeterminado. Por lo tanto, es realmente importante cambiar el blyt/BgNml.bflyt después de que hagas el DIFF y estés listo.

A continuación, las animaciones. Si usas mi JSON, la animación ya está configurada, pero permíteme explicar qué hace todo. Este BLFAN RdtBase\_Enter.BFLAN es el BLFAN principal para el fondo animado, es el que llama el Switch al entrar por primera vez en el menú.

Para este tutorial, ignoremos todo lo demás excepto estas 4 entradas en el FLPA. Estamos usando el Switch Layout Theme Editor. La primera entrada corresponde a la posición X del fondo de pantalla. Su animationTarget es 0.

![6](https://user-images.githubusercontent.com/93286561/222505972-a3559480-524a-4dfc-8187-9c0df5720927.jpg)

Como puedes ver, estamos moviendo el valor X desde -1800 hasta 1800 hacia adelante y hacia atrás, lo que significa que la imagen va de una coordenada a otra cada 8000 frames.

Lo mismo para el Valor Y. Su animationTarget es 1.

![7](https://user-images.githubusercontent.com/93286561/222506868-9285aa8d-be8b-4cf3-ab22-8ccaf9f186e5.jpg)

Los siguientes dos son la Escala de X e Y de la imagen. Aquí es donde podemos cambiar la imagen de 1280x720 a 720x720, este valor debe permanecer igual para obtener los mejores resultados.

![8](https://user-images.githubusercontent.com/93286561/222507258-fa7c05da-04d3-4e75-8fc9-ce5652daee85.jpg)

![9](https://user-images.githubusercontent.com/93286561/222507268-2e710866-555f-4a7c-91c1-f0c32096d186.jpg)

Ahora, necesitamos replicar todo esto en todos estos BFLANS:

- RdtBase_GameOut.bflan
- RdtBase_GameOutHideCnt.bflan
- RdtBase_StarterEnter.bflan
- RdtBase_Enter.bflan
- RdtBase_SystemAppletOut.bflan

**Si todo esto te parece un poco confuso, te recomiendo que uses mi JSON y hagas pequeños cambios en estos valores desde allí en lugar de empezar todo desde el principio.**

Eso debería ser todo. Necesitarás usar el inyector de temas de Switch para crear tu nuevo tema, usando tu imagen y el JSON editado.

[](#final-thoughts)Pensamientos Finales
=========================================

Siguiendo estos pasos, puedes crear un tema de fondo en movimiento completamente personalizado para tu Nintendo Switch. Puede tomar algo de tiempo configurar todo, pero el resultado final es un tema único y personalizado que puedes disfrutar cada vez que uses tu Switch.

¡Eso es todo! Si tienes alguna pregunta, no dudes en preguntar en cualquier momento. Espero que este tutorial te haya ayudado a crear un tema en movimiento para tu Switch. ¡Diviértete y sé creativo!

Resultado:

![IMG_3654_1](https://user-images.githubusercontent.com/93286561/222519069-6857b0df-0938-4f78-9e85-5a111598056c.gif)
