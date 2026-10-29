# 02 · Requisitos funcionales

**Estado:** línea base de análisis · **Actualización:** 2026-10-29

## Convenciones

- **P0:** indispensable para la prueba de concepto local.
- **P1:** indispensable para una beta personal que valide la propuesta central en las plataformas objetivo.
- **P2:** deseable antes o durante lanzamiento posterior.
- **P3:** exploratorio/futuro.
- **Pendiente:** no implementado todavía. Que un requisito esté descrito no supone que ya exista.

## Editor, páginas y lápiz

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-001 | Crear una página de tamaño fijo, inicialmente A4. | P0 |
| RF-002 | Mostrar fondo blanco, rayado o cuadriculado. | P0 |
| RF-003 | Editar texto mediante teclado físico y virtual. | P0 |
| RF-004 | Aplicar negrita, cursiva, títulos, tamaño, fuente y color. | P0 |
| RF-005 | Alinear y **justificar** párrafos. | P0 |
| RF-006 | Dibujar y escribir libremente con lápiz o puntero sobre cualquier parte de la página. | P0 |
| RF-007 | Resaltar, rodear, subrayar y dibujar flechas como trazos. | P0 |
| RF-008 | Borrar trazos sin borrar contenido textual. | P0 |
| RF-009 | Guardar y recuperar localmente una página con texto y trazos. | P0 |
| RF-010 | Controlar zoom manteniendo las proporciones entre capas. | P0 |
| RF-011 | Deshacer/rehacer operaciones de texto y anotaciones. | P1 |
| RF-012 | Crear, eliminar y cambiar de página dentro de un cuaderno. | P1 |
| RF-013 | Configurar márgenes, espaciado e interlineado; opción de alineación con cuadrícula. | P1 |
| RF-014 | Insertar imágenes, tablas, listas y encabezados estructurados. | P1/P2, gradual |
| RF-015 | Distribuir automáticamente texto entre páginas al alcanzar el final de la hoja. | P2, sujeto a prueba |
| RF-016 | Permitir seleccionar, mover o eliminar conjuntos de trazos. | P1 |
| RF-017 | Exportar documentos a PDF con texto y anotaciones visibles. | P1/P2 |

## Regla de independencia de capas (acuerdo expreso)

El texto y la escritura manual se manipulan por separado. Si se modifica un párrafo y el texto se desplaza, los trazos **permanecen en la posición de la página** donde se dibujaron. Ajustarlos después corresponde a la persona usuaria. No se desarrollará seguimiento automático de fragmentos de texto en las primeras versiones.

## Organización y cuadernos

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-018 | Crear, renombrar y eliminar cuadernos. | P1 |
| RF-019 | Crear carpetas y subcarpetas para organizar documentos. | P1 |
| RF-020 | Personalizar nombres, colores mediante HEX e iconos opcionales. | P1/P2 |
| RF-021 | Seleccionar plantillas/portadas básicas y premium. | P2 |
| RF-022 | Importar PDFs como páginas anotables, sin prometer edición directa de su texto. | P2 |
| RF-023 | Permitir enlaces o navegación entre páginas del cuaderno. | P2 |

## Sincronización y almacenamiento

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-024 | Mostrar un mismo documento con apariencia equivalente en la web para computadores y las aplicaciones instalables Android e iPadOS. | P1 |
| RF-025 | Sincronizar cambios de texto y de lápiz automáticamente cuando haya conexión. | P1 |
| RF-026 | Mostrar estado de guardado/sincronización y fallos. | P1 |
| RF-027 | Permitir reintentar manualmente una sincronización fallida. | P1 |
| RF-028 | Trabajar sin conexión sobre contenido disponible y sincronizar al reconectar. | P2 |
| RF-029 | Crear copias de seguridad y recuperación de documentos. | P1 |

## Flashcards y estudio

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-030 | Abrir/cerrar un panel lateral pequeño sin abandonar el cuaderno. | P1 |
| RF-031 | Crear tarjetas con **frente y reverso únicamente de texto** mediante redacción o copiar/pegar. | P1 |
| RF-032 | Asociar cada tarjeta al cuaderno actual. | P1 |
| RF-033 | Editar y eliminar tarjetas creadas. | P1 |
| RF-034 | Estudiar tarjetas de un cuaderno mediante mostrar pregunta y revelar respuesta. | P1 |
| RF-035 | Ofrecer repaso espaciado de tarjetas dentro de la aplicación. | P2, algoritmo por definir |
| RF-036 | Seleccionar un fragmento para lectura en voz alta, cambiar velocidad y destacar el progreso. | P2 |

## Cuentas y comercialización

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-037 | Registrar/iniciar sesión con cuentas individuales. | P2, antes de beta externa |
| RF-038 | Ofrecer modalidad gratuita y suscripciones. | P3, antes de venta |
| RF-039 | Ofrecer compra permanente con límites claros de servicios recurrentes. | P3, por validar |
| RF-040 | Gestionar cuotas de cuadernos y almacenamiento según plan. | P3 |

## Plataformas y aplicaciones

| ID | Requisito | Prioridad |
| --- | --- | --- |
| RF-041 | Proporcionar una aplicación web para computadores, accesible desde navegadores modernos. | P1 |
| RF-042 | Proporcionar una aplicación instalable para tablets Apple con iPadOS, compatible con Apple Pencil y teclado externo. | P1 |
| RF-043 | Proporcionar una aplicación instalable para tablets Android, compatible con lápices digitales y teclados externos admitidos por el dispositivo. | P1 |
| RF-044 | Mantener las mismas funcionalidades principales y un formato de documento compartido entre web, iPadOS y Android. | P1 |

## Condiciones para aceptar requisitos

Los RF-041 a RF-044 forman parte del alcance P1, no de la primera prueba P0. La validación de aplicaciones instalables se realizará en H2-A y la sincronización entre plataformas en H2.

Cada requisito debe tener evidencia observable (prueba, captura, video o caso ejecutado). La función no se declarará «lista» solo porque el botón exista: tiene que conservar datos y funcionar en los dispositivos definidos para esa etapa.
