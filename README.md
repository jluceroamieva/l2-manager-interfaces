# Interfaces para L2 Manager by Moet

Descargas de las interfaces que usa **L2 Manager** para Lineage II. La app las baja sola desde acá, comprueba su huella SHA-256 y las deja listas en la biblioteca. No hace falta descargarlas a mano.

Este repo no tiene código: solo el índice `interfaces.json` y los paquetes `.zip`, que están en [Releases](../../releases).

## Derechos

Cada interfaz pertenece a su autor y se publica con su autorización. Cada `.zip` incluye un `credits.json` con el autor, su sitio y los derechos. L2 Manager no modifica las interfaces.

| Interfaz | Autor |
|---|---|
| Silent Essence, Silent_Interlude, Silent_Classic, Silent_DarkLite, Silent_Dark_R2 | Silent (Silent Interface) |
| Custom | Un jugador de Ordinary World |

Lineage II es una marca de NCSoft. Este proyecto no está afiliado a NCSoft ni a ningún servidor.

## Formato de `interfaces.json`

```json
{
  "format": 1,
  "packs": [
    {
      "name": "Silent_DarkLite",
      "version": "Rev 1.7",
      "author": "Silent (Silent Interface)",
      "url": "https://github.com/jluceroamieva/l2-manager-interfaces/releases/download/<etiqueta>/Silent_DarkLite.zip",
      "sha256": "…",
      "size": 12920682,
      "installed": 67615861
    }
  ]
}
```

- `name` es el nombre de la carpeta en la biblioteca.
- `size` es lo que pesa el `.zip`. `installed` es lo que ocupa descomprimida.
- Si cambia la huella `sha256`, la app ofrece actualizar la interfaz.

Se genera con `tools\empaquetar-interfaces.ps1` del repo de L2 Manager. Primero se suben los `.zip` a la Release y después este archivo: la app lee el índice de la rama `main`.
