# 04 · Alcance, MVP y versiones

**Decisión central:** evitar una aplicación comercial completa antes de validar el núcleo técnico: editor de texto enriquecido y lápiz independiente sobre páginas estables. El producto final contempla **web para computadores y apps instalables para Android e iPadOS**.

## Etapa 0 · Documentación (actual)

**Entregables:** visión, requisitos, alcance, riesgos, pruebas y repositorio privado. Sin implementación ni compromisos comerciales.

**Se considera cerrada cuando:** el cliente revisa el alcance inicial y aprueba la prueba de concepto o registra ajustes. Crear el repositorio no significa aprobación del cliente.

## Etapa 1 · Prueba de concepto web local (P0)

**Debe permitir:**

- Ejecutar el prototipo del editor en navegador de computador Windows.
- Crear una página A4 con dimensiones fijas y cambiar el fondo (al menos blanco/cuadriculado).
- Escribir mediante teclado, justificar párrafos y aplicar formato esencial.
- Dibujar mediante ratón o puntero sobre la página y borrar trazos sin eliminar texto.
- Guardar y recuperar localmente el documento.
- Mantener texto y trazos alineados al cambiar el zoom.
- Definir un formato de datos de documento reutilizable para las aplicaciones móviles posteriores.

**No incluye:** aplicaciones móviles completas, cuentas, servidor, sincronización, paginación automática, PDF importado, cobros ni flashcards.

**Condición de salida:** texto y dibujo coexisten sobre una misma página estable, sin pérdida de datos ni interferencia accidental entre capas.

## Etapa 2 · Prototipos de aplicaciones instalables (P1-A / H2-A)

**Debe permitir:**

- Construir prototipos instalables para tablets Android e iPadOS.
- Cargar un documento compatible con el modelo creado en la versión web.
- Editar texto y dibujar sobre la página utilizando teclado y lápiz digital compatible en ambas plataformas.
- Borrar trazos sin afectar el texto y mantener la distribución con zoom.
- Validar rendimiento, fluidez y fidelidad visual en dispositivos físicos.
- Identificar restricciones de compilación, instalación y pruebas, especialmente para iPadOS.

**No incluye:** sincronización remota ni distribución pública en tiendas.

**Condición de salida:** prototipos móviles validados en **ambas** plataformas con evidencia de uso real; abrir la aplicación web en el navegador de una tablet no equivale a esta entrega. Si faltan dispositivos o credenciales, registrar el bloqueo y no dar el hito por aprobado.

## Etapa 3 · Prototipo sincronizado (P1-B / H2)

**Debe permitir:**

- Abrir el mismo documento en la aplicación web y en las apps instaladas Android/iPadOS.
- Sincronizar cambios de texto, creación y borrado de anotaciones sin exportación manual.
- Guardar los documentos en un servidor local con persistencia real.
- Mostrar estados de conexión, guardado y sincronización.
- Probar ediciones simultáneas, reconexiones y cambios válidos en los distintos dispositivos.

**No incluye:** alojamiento remoto público ni funcionamiento offline completo.

**Condición de salida:** intercambio bidireccional confiable entre las tres plataformas, persistencia comprobada y distribución del documento equivalente.

## Etapa 4 · Beta personal (P1-C / H3)

**Debe permitir:**

- Crear, eliminar y organizar cuadernos con varias páginas.
- Administrar carpetas, subcarpetas, nombres y colores.
- Seleccionar/mover trazos y deshacer/rehacer operaciones.
- Incorporar gradualmente listas, tablas, imágenes y controles de márgenes.
- Crear, editar, eliminar y estudiar flashcards **solo de texto** por cuaderno.
- Exportar o respaldar documentos de forma básica.

**Condición de salida:** una persona puede completar el ciclo crear → anotar → estudiar con la misma información disponible en las plataformas objetivo.

## Etapa 5 · Beta externa (P2 / H4)

**A evaluar e implementar progresivamente:**

- Registro, autenticación y permisos por usuario.
- Acceso remoto seguro por HTTPS.
- Distribución controlada de versiones de prueba instalables Android/iPadOS.
- Validación con modelos distintos de tablets y lápices digitales.
- Importación de PDF como contenido anotable, plantillas, funcionamiento sin conexión y lectura en voz alta.

**Condición de salida:** versión suficientemente estable y segura para pruebas externas, con incidencias y restricciones conocidas documentadas.

## Etapa 6 · Producto comercial (P3 / H5)

**A evaluar:** planes gratis/pagados, compra permanente, cobros, cuotas, soporte, políticas, monitoreo, respaldos y costos de distribución y operación.

## Fuera de alcance explícito por ahora

- Conversión perfecta de formatos externos de documentos a texto editable.
- Reconocimiento universal de escritura manuscrita y conversión automática a texto.
- Seguimiento automático de subrayados cuando el texto se desplaza.
- Tarjetas de estudio con multimedia o generación automática.
- Integración obligatoria con otros servicios de estudio.
- Chat, temporizador social, red de amistades y herramientas de colaboración multiusuario.
- Promesa de sincronización con latencia fija en milisegundos.
- Reproducción de todas las funciones de suites de oficina o aplicaciones especializadas en escritura manuscrita.

## Regla de cambio de alcance

Toda característica nueva se registra indicando propósito, prioridad, impacto en hito y criterio de aceptación. No se considera comprometida comercialmente hasta recibir aprobación expresa.
