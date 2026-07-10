# Changelog

## 2.6.9 - 2026-07-10 (vuelta al empaquetado clásico)

**Escritorio (Windows y Linux) 2.6.9:**
- **Revertido el empaquetado Nuitka de 2.6.8**: el binario nativo no arrancaba en algunos Windows (bloqueo silencioso del antivirus con ejecutables Nuitka sin firma). Se vuelve a PyInstaller, el empaquetado probado de todas las versiones anteriores.
- Sin cambios funcionales (Contactos activado y compartido en la nube, igual que 2.6.7).

## 2.6.8 - 2026-07-10 (nuevo empaquetado nativo con Nuitka)

**Escritorio (Windows y Linux) 2.6.8:**
- **Nueva tecnología de empaquetado (Nuitka)**: el programa ahora se compila a **binario nativo** — arranque más robusto y el código queda protegido (sustituye a PyInstaller+PyArmor en la edición moderna; la edición Win7 no cambia).
- Corrige de raíz el fallo del primer instalador 2.6.7 de Windows ("cannot import name 'create_app'"), causado por una ofuscación parcial de PyArmor.
- Sin cambios funcionales respecto a 2.6.7 (Contactos activado y compartido en la nube).

## 2.6.7 - 2026-07-10 (Contactos activado y en la nube + Facturas 1.3.0)

**Escritorio (Windows y Linux) 2.6.7:**
- **Módulo "Contactos" ACTIVADO**: en 2.6.6 aparecía "en mantenimiento" por un error de registro del menú (el módulo ya estaba construido).
- **Contactos en la nube**: el directorio de clientes y proveedores ahora vive en el servidor y es el MISMO que usa la app TecnoTáctil Facturas — lo que crees en una app aparece en la otra. Los contactos locales existentes se migran solos la primera vez que abres el módulo.
- Se siguen reutilizando al emitir facturas de venta/entrada y contratos (autollenado de nombre, NIT/CI, teléfono, banco…).

**Facturas (Android) 1.3.0:**
- La app pasa a llamarse **"TecnoTáctil Facturas"**, con icono propio de la marca.
- **Inicio de sesión** con tu usuario del negocio (los mismos usuarios/contraseñas de la Caja) + botón **"Sincronizar usuarios"** para traer usuarios recién creados en el escritorio.
- **Contactos**: crea y edita clientes y proveedores desde el móvil; al hacer una factura, elige un contacto y se autollenan sus datos (incluye nuevo campo NIT/CI en la factura).
- La portada muestra el **nombre real del negocio** (antes salía un ID); "Mis negocios" solo aparece en licencias multinegocio y las estadísticas de la portada son el **agregado de todos los negocios** de la licencia.

## 2.5.6 - 2026-07-08 (enlaces al navegador del sistema, logo sincronizado + Caja 1.3.0)

**Escritorio (Windows 7-11 y Linux):**
- Los enlaces externos (grupo de Telegram de soporte, web, WhatsApp) ahora abren el **navegador del sistema** (o la app correspondiente) en vez de una pestaña dentro de la ventana de la aplicación.
- **Logo del negocio**: al subirlo se **reduce automáticamente** (máx. 256px, muy ligero) y se **sincroniza con la Caja Android**, que lo muestra en su pantalla principal.

**Caja (Android) 1.3.0:**
- Pantalla principal rediseñada: arriba el logo + "TecnoTáctil — «nombre del negocio conectado»"; barra inferior siempre visible con **Sincronizar · Cerrar/Abrir Caja · Clientes · Opciones** y el total **«Ventas del turno»** en vivo.
- **Opciones**: cerrar sesión y **desvincular de la licencia** (libera el cupo de la caja al momento y borra los datos locales).
- **Gestionar clientes** (crear y eliminar) para usar la cuenta casa.

## 2.5.5 - 2026-07-08 (cumplimiento legal cubano + contratos + Caja 1.2.0)

**Escritorio (Windows 7-11 y Linux):**
- **Ficha de costo según el modelo OFICIAL de la Res. 148/2023 MFP (Anexo I)**: cabecera con UM, nivel de producción y % de utilización de capacidad; desglose obligatorio del Gasto Material (insumos, combustibles, energía, agua); "de ello: salarios" en las filas 4, 6 y 7; numeración y nombres oficiales (F5 COSTO TOTAL… F14 PRECIO O TARIFA, F15 precio unitario ajustado, F16 precios de referencia); tributos consolidados en la fila 10 (seguridad social + fuerza de trabajo) — el impuesto sobre ventas ya NO forma parte de la ficha (así lo define la norma); aviso cuando los gastos indirectos exceden el coeficiente legal (1.5× el salario directo; 1.0× en servicios).
- **Vector Fiscal = réplica del RC-04A real de la ONAT**: logo ONAT, columnas oficiales (incl. "Importe c/recargo" al 2%), códigos de tributo verificados con un vector real (0114022 ventas/servicios, 0510122 IIP mensual, 0530222 liquidación DJ, 0730122 documentos) y las notas generales del documento oficial. Eliminada la nota obsoleta del régimen simplificado (derogado por el DL 93/2024).
- **Contratos desde la aplicación**: generación de "Prestación de Servicios" y "Compraventa" con estructura de proforma legal cubana; la parte del negocio se autollena (titular, CI, licencia, NIT, cuentas CUP/MLC — se configuran una vez); cláusulas precargadas y editables; imprimible con logo y firmas.
- **Logo del negocio y pies de firma** (Elaborado por / Aprobado por, con cargo) configurables y aplicados a todos los documentos imprimibles.
- **Impuestos actualizados**: impuesto sobre ventas/servicios por defecto 10% (Ley 181 Presupuesto 2026, antes 21%); la cuota mensual TCP del 5% aplica el mínimo exento de 3.260 CUP; aviso de la liquidación anual por escala progresiva (5%–50%).
- **Contabilidad según tipo de negocio**: la vista de ingresos-gastos del TCP adopta el nombre oficial "Registro Control de Ingresos y Gastos" (Res. 272/2024) con el aviso legal según tipo e ingresos (NCIF para TCP ≥500.000 CUP y MIPYME/CNA, DL 88/2024).

**Caja (Android) 1.2.0:**
- Botón "Cerrar sesión" en la pantalla principal (con confirmación) y "Cambiar licencia" en el login.
- Corregido "Cambiar de negocio": ya no se re-activa solo sin dejar elegir; si no puede listar los negocios muestra el formulario para corregir el email del titular.
- Corregido el estado de la caja: tras abrirla, el botón "Cerrar Caja" aparece siempre (ahora en su propia fila, a lo ancho).
- El inventario ya no "revierte" lo vendido al sincronizar: la caja conserva sus descuentos locales hasta que el PC re-publica el stock real.
- El botón Sincronizar del login es ahora un botón grande siempre visible; la pantalla hace scroll con el teclado abierto.
- Al desinstalar la app se borran TODOS los datos, incluida la licencia (desactivado el auto-backup de Android).

## Facturas (Android) 1.1.1 - 2026-07-07 (fix multinegocio: negocio activo en Perfil y Facturas)

- **Perfil y Facturas del negocio elegido**: en el plan Administra Negocio, "Mis Negocios" ahora tiene un botón **"Usar"** por negocio — el negocio elegido pasa a ser el que muestran las pantallas de Perfil y Facturas. Antes siempre mostraban el negocio con que se activó la licencia, nunca los demás. (Estadísticas ya funcionaba por negocio y no cambia.)
- Misma firma que la versión anterior: se instala encima sin desinstalar.

## 2.5.4 - 2026-07-07 (fix multinegocio: cupo de negocios y negocio activo)

- **Cupo de negocios corregido (plan Administra Negocio)**: la app ya no muestra "límite alcanzado" con un cupo cacheado desactualizado — antes, si el valor local de `max_negocios` quedaba viejo (p.ej. plan ampliado después de activar), la app caía a 1 negocio aunque el plan pagado permitiera más.
- **Refresco del cupo antes de bloquear**: al crear un negocio, la app re-verifica el plan contra el servidor antes de rechazar por límite (si hay conexión); el servidor sigue revalidando siempre.
- **Perfil y Facturas del negocio activo**: en multinegocio, el perfil del negocio (identidad legal, socios, cuentas, actividades) y las facturas ahora corresponden al negocio SELECCIONADO en el escritorio — antes siempre mostraban el negocio con que se activó la licencia, nunca los demás negocios del plan. (Requiere tpv-core actualizado, ya desplegado.)
- Windows y Linux publicados con el mismo nombre de fichero de siempre (los enlaces no cambian).

## 2.5.3 - 2026-07-07 (release Linux + fixes legales + bloqueo licencia)

- **Fichas de costo**: actualizada la referencia legal de Res. 20/2014 → **Res. 148/2023 MFP** (Gaceta Of. No. 64/2023 del 6-jul-2023). La 20/2014 quedó derogada implícitamente por 148/2023 y las intermedias (62/2021, 337/2021).
- **Bloqueo por licencia vencida + 7 días de gracia**: cuando la licencia expira, la app avisa en gracia durante 7 días; pasado ese periodo la app queda BLOQUEADA (solo se puede acceder a Mi licencia, Sincronizar, Configuración, Ampliar plan y Asistente Jurídico) hasta renovar y sincronizar.
- **Refresco automático de límites**: `refrescar_estado()` ahora lee `limites.max_negocios` y `extra_cajas` del verificar de tpv-core y los guarda locales — al ampliar el plan en la web, basta con pulsar Sincronizar en el escritorio.
- **Asistente Jurídico** integrado en el panel general: nueva tarjeta con acceso rápido (5 consultas gratis por usuario en tecnotactil.com; abre en el navegador del sistema).

## 2.5.3 - 2026-07-07 (release Linux)

- Escritorio Linux: primer bundle oficial `TecnoTactil_Negocio_linux.tar.gz` (x86_64, Debian/Ubuntu/Fedora/Arch). Mismo funcional que el .exe de Windows.
- Instalador `install.sh` con detección automática de instalación previa (modo actualización), matando procesos activos del binario y del Firefox embebido antes de reemplazar.
- Desinstalador `uninstall.sh` con 3 modos: interactivo (pregunta), `--purge` (borra TODO incluida la BD del negocio) y `--keep-data` (conserva la BD para reinstalación posterior).
- Datos del negocio en `~/.local/share/tecnotactil/negocio/` (convención XDG).
- Requiere Firefox del sistema (`apt install firefox` en Debian/Ubuntu; la app también acepta `firefox-esr`).

## 2.5.3 - 2026-07-02

- Escritorio: instalador UNICO para Windows 7 a 11 con navegador propio integrado (ya no depende de WebView2 ni de componentes del sistema; funciona 100% offline).
- Escritorio: modo Administrador de Negocios (multinegocio) con aislamiento total por negocio, fichas de costo (Res. 20/2014), impuestos y reportes ONAT (Registro de Ingresos y Gastos, Vector Fiscal RC-04), contratos, facturas de entrada, cajeros para la Caja Android y panel de dispositivos.
- Sincronizacion mas robusta: corregida la perdida de cambios locales del catalogo entre sincronizaciones; las ventas del PC ahora tambien se respaldan en el servidor.
- Licencias: la aplicacion re-verifica la licencia al sincronizar (las renovaciones se reflejan al momento).
- Caja (Android) 1.1.0: activacion multinegocio en 2 pasos (elige el negocio y ponle nombre a la caja); IVA calculado igual que en el escritorio; login de cajeros creado desde el PC.
- Facturas (Android) 1.1.0: NUEVO - Estadisticas de venta (hoy / 7 dias / mes + top productos y ticket promedio), "Mis Negocios" con estadisticas por negocio y pantalla de Ajustes.
- Nota: version de PRUEBA con trial generoso de 15 dias en todos los planes. Si encuentras algun error, escribenos por Telegram (t.me/tecnotactil) y lo corregimos rapido.

## 2.0.0 - 2026-06-23

- Nueva aplicacion de escritorio con interfaz web moderna (WebView2): mas rapida, clara y consistente con la web.
- Distribucion mediante INSTALADOR de Windows (asistente Inno Setup) en lugar de un ejecutable suelto.
- Codigo de la aplicacion protegido/ofuscado para distribucion comercial.
- Completados los modulos de Contabilidad (ingresos, gastos y balance por periodo) y Configuracion (negocio, IVA, moneda y mensaje del ticket).
- Build mas liviano (~21 MB) al retirar dependencias graficas no usadas.
- Corregido el arranque tras la instalacion (dependencias internas ahora empaquetadas correctamente).

## 1.1.0 - 2026-05-24

- Agregado modelo de sincronizacion offline-first para servidor remoto y futuras cajas Android.
- Agregado modulo de sincronizacion en la aplicacion de escritorio.
- Agregada contabilidad de gastos del negocio y pagos de servicios.
- Agregada exportacion de reportes financieros en PDF.
- Mejorada configuracion del negocio e impuestos para comprobantes y reportes.
- Mejorado modelo de permisos personalizados por usuario, modulo y accion.
- Mejorada interfaz visual con logo correcto en login y navegacion compacta con iconos.
- Actualizada documentacion tecnica para servidor de licencias, sincronizacion y contabilidad solo PC.

## 1.0.0 - 2026-05-22

- Primera version estable de TecnoTactil TPV.
- TPV, ventas, clientes, inventario, caja y contabilidad.
- Activacion de licencia contra `www.tecnotactil.com`.
- Titularidad de licencia por email.
- Modo demo con limites.
- Asistente de primer arranque.
- Configuracion de negocio e impuestos.
- Permisos personalizados por usuario.
- Build protegido para distribucion.
