# Changelog

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
