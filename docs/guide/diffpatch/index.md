El diffing es el proceso de crear un archivo JSON
con un conjunto de cambios entre el original y un SZS modificado.

Esto se puede hacer con [Switch Theme injector](https://github.com/exelix11/SwitchThemeInjector).

![diffing.png](<diffing.png>)

La salida de un parche diferencial puede parecerse al ejemplo siguiente:

<font size="0">
<pre><code>
{
	"PatchName": "Ejemplo DIFFPATCH",
	"AuthorName": "SodaSoba",
	"TargetName": "ORIGINAL.szs",
	"ID": "123456789",
	"Files": [
		{
			"FileName": "blyt/FlcGrpList.bflyt",
			"Patches": [
				{
					"PaneName": "N_PosAll",
					"Position": {}
				},
				{
					"PaneName": "NH_Root",
					"Position": {
						"Y": -50
					}
				},
				{
					"PaneName": "N_Top",
					"Position": {
						"Y": 50
					}
				}
			],
			"Materials": [
				{
					"MaterialName": "T_00",
					"ForegroundColor": "00000000"
				}
			]
		}
	]
}
</code></pre>
</font>
Este JSON (diffpatch) se puede aplicar a un archivo SZS ya sea con [Switch Theme injector](https://github.com/exelix11/SwitchThemeInjector) o con [LayoutKit](https://github.com/ThemezerNX/LayoutKit).

Aquí tienes un ejemplo de sodasoba sobre cómo aplicar un parche diferencial:

# [Continuar a Diffing](diff-example.md) :octicons-arrow-right-16:
