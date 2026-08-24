# Granja de Bots — Agentes cliente

Clientes del servicio **Granja de Bots** de TecnoTáctil. Se conectan al panel web
(que los gestiona vía el microservicio tt-farm) para reportar estado y ejecutar
tareas sobre los dispositivos.

## Descargas (siempre la última versión)

| Cliente | Para | Enlace fijo |
|---|---|---|
| **Agente-PC (Windows)** | Un PC con móviles conectados por USB/ADB | [`TecnoTactil_FarmAgent.exe`](https://github.com/tecnotactil-ia/tecnotactil-tpv-descargas/raw/main/granja/TecnoTactil_FarmAgent.exe) |
| **Agente-PC (Linux)** | Igual, en Linux (servicio systemd) | [`TecnoTactil_FarmAgent_linux.tar.gz`](https://github.com/tecnotactil-ia/tecnotactil-tpv-descargas/raw/main/granja/TecnoTactil_FarmAgent_linux.tar.gz) |
| **Agente-Android** | Un móvil que opera en solitario | [`TecnoTactil_FarmAgent.apk`](https://github.com/tecnotactil-ia/tecnotactil-tpv-descargas/raw/main/granja/TecnoTactil_FarmAgent.apk) |

Los enlaces son **fijos**: apuntan siempre al último build publicado. Verifica la
integridad con `SHA256SUMS.txt`.

## Instalación breve

- **Windows:** ejecuta el `.exe`, introduce la llave de servicio y el nombre de la
  granja; queda como tarea al arranque.
- **Linux:** `tar xzf TecnoTactil_FarmAgent_linux.tar.gz && cd … && sudo ./install.sh`,
  edita `/etc/tt-farm-agent/agent_config.json` y `systemctl start tt-farm-agent`.
- **Android:** instala el APK (permitiendo orígenes desconocidos), abre la app,
  introduce llave + nombre, y activa la accesibilidad si quieres automatización de UI.
