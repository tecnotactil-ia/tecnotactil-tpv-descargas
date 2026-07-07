# Escritorio — TecnoTáctil Negocio

Descargas oficiales del punto de venta de escritorio (Flask + Firefox portable — funciona
offline en Windows y Linux).

## Ficheros

| Sistema | Fichero | Enlace directo (nombre FIJO — no cambia entre versiones) |
|---|---|---|
| Windows (7/8/8.1/10/11, 32 y 64 bits) | `TecnoTactil_Negocio.exe` | https://github.com/tecnotactil-ia/tecnotactil-tpv-descargas/raw/main/escritorio/TecnoTactil_Negocio.exe |
| Linux (x86_64, Debian/Ubuntu/Fedora/Arch) | `TecnoTactil_Negocio_linux.tar.gz` | https://github.com/tecnotactil-ia/tecnotactil-tpv-descargas/raw/main/escritorio/TecnoTactil_Negocio_linux.tar.gz |

## Instalación en Linux

```bash
tar xzf TecnoTactil_Negocio_linux.tar.gz
cd TecnoTactilNegocio
bash install.sh
```

`install.sh` detecta si ya hay una instalación previa; si la hay, MATA los procesos activos
y actualiza el binario **conservando la BD del negocio**.

Para desinstalar limpiamente:
```bash
bash ~/.local/share/tecnotactil/TecnoTactilNegocio/uninstall.sh          # pregunta si borra los datos
bash ~/.local/share/tecnotactil/TecnoTactilNegocio/uninstall.sh --purge   # borra TODO
bash ~/.local/share/tecnotactil/TecnoTactilNegocio/uninstall.sh --keep-data  # borra la app, conserva BD
```

Requiere Firefox del sistema (`apt install firefox` en Debian/Ubuntu).

## Publicar una nueva versión

Sube el fichero SUSTITUYENDO el existente con el mismo nombre exacto:
- Windows: reemplaza `TecnoTactil_Negocio.exe`.
- Linux: reemplaza `TecnoTactil_Negocio_linux.tar.gz`.

El enlace en la web sigue funcionando solo — no cambia jamás.

Actualiza también `SHA256SUMS.txt` (`sha256sum TecnoTactil_Negocio.exe TecnoTactil_Negocio_linux.tar.gz > SHA256SUMS.txt`)
y añade la entrada al `CHANGELOG.md` del repo.
