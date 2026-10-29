# 07 · Hoja de ruta

La planificación utiliza **hitos con condiciones de salida**, sin fechas comprometidas hasta comprobar la complejidad y la disponibilidad del desarrollador. **Android e iPadOS tienen igual prioridad funcional**, aunque su validación práctica sea progresiva.

## H0 · Documentación y repositorio

- [x] Recopilar visión y requisitos iniciales.
- [x] Separar funciones centrales de las avanzadas.
- [x] Documentar reglas de texto/lápiz y flashcards de texto.
- [x] Documentar web para computadores y aplicaciones instalables para Android/iPadOS.
- [ ] Validar el resumen con el cliente.
- [ ] Crear repositorio privado y subir documentación.

**Salida:** alcance inicial entendible y versionado; no implica que el cliente haya aprobado todavía.

## H1 · Página web local (primera implementación)

- [ ] Crear aplicación web inicial.
- [ ] Renderizar página A4 con fondos básicos.
- [ ] Integrar editor de texto, formato y justificación.
- [ ] Integrar capa de dibujo sin interferencia con texto.
- [ ] Agregar lápiz/puntero y goma, con ratón en la primera prueba.
- [ ] Guardar/recuperar documento localmente.
- [ ] Probar zoom, teclado y trazos en navegador de computador.
- [ ] Definir un formato de documento reutilizable entre plataformas.

**Salida:** página híbrida funcional en computador, sin cuentas ni servidor.

## H2-A · Prototipos instalables para tablets

- [ ] Preparar la base móvil (React Native + Expo como candidato, sujeto a prueba).
- [ ] Crear prototipo instalable para tablets Android.
- [ ] Crear prototipo instalable para iPadOS.
- [ ] Cargar un documento con el formato compartido.
- [ ] Validar edición con teclado físico/virtual en ambas plataformas.
- [ ] Validar escritura con lápiz digital compatible en Android.
- [ ] Validar escritura con Apple Pencil en iPadOS.
- [ ] Probar goma, zoom, desplazamiento y recuperación local.
- [ ] Comparar fidelidad visual con la versión web.
- [ ] Registrar limitaciones técnicas o de distribución sin dar por aprobada una plataforma no probada.

**Salida:** evidencia de viabilidad y uso de **apps instalables** en Android e iPadOS; el navegador de tablet no reemplaza estas pruebas.

## H2 · Sincronización multiplataforma local

- [ ] Definir formato de operaciones y cambios compartidos.
- [ ] Sincronizar texto entre aplicación web y apps instaladas.
- [ ] Sincronizar creación, edición y borrado de trazos.
- [ ] Persistir documentos en servidor local.
- [ ] Mostrar estados de guardado, conexión y sincronización.
- [ ] Probar ediciones simultáneas y reconexiones.
- [ ] Comparar distribución en web, Android e iPadOS con distintas resoluciones.

**Salida:** el mismo documento se sincroniza sin traslado manual entre los tres clientes, con persistencia comprobada.

## H3 · Cuadernos y flashcards

- [ ] Crear cuadernos con varias páginas, carpetas y subcarpetas.
- [ ] Personalizar nombres y colores.
- [ ] Incorporar selección/movimiento de trazos y deshacer/rehacer.
- [ ] Abrir panel lateral de flashcards de texto y estudiar por cuaderno.
- [ ] Añadir tablas, listas e imágenes de forma gradual según pruebas.
- [ ] Crear respaldo exportable y recuperación básica.

**Salida:** ciclo crear → anotar → estudiar funcional y probado en las plataformas comprometidas para el hito.

## H4 · Beta con usuarios

- [ ] Autenticación, privacidad y controles de acceso.
- [ ] Acceso remoto seguro mediante HTTPS.
- [ ] Distribución controlada de aplicaciones de prueba para Android e iPadOS.
- [ ] PDF anotable.
- [ ] Trabajo sin conexión y recuperación de cambios.
- [ ] Pruebas con estudiantes y profesionales; registrar modelos de tablets y lápices.

**Salida:** evidencia de estabilidad, utilidad y seguridad en uso real.

## H5 · Comercialización

- [ ] Costear infraestructura, respaldos, tiendas y soporte.
- [ ] Investigar disposición a pagar.
- [ ] Definir plan gratuito, suscripciones y compra permanente.
- [ ] Preparar políticas, términos, privacidad, pagos y atención al usuario.

**Salida:** producto apto para comercialización si la validación lo justifica.

## Criterio general para avanzar

No declarar aprobado un hito si hay pérdida reproducible de datos, desajuste grave de capas, fallos graves del lápiz o ausencia de una plataforma requerida. Las pruebas móviles y de sincronización pueden explorarse parcialmente en paralelo, pero se cierran por separado.
