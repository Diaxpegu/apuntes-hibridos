# 03 · Requisitos no funcionales

**Estado:** objetivos iniciales de calidad; no equivalen a garantías contractuales. **Actualización:** 2026-10-29.

## RNF-01 · Compatibilidad multiplataforma

- **Computadores:** aplicación web desde navegadores modernos, con validación inicial en Windows; Linux y macOS quedan sujetos a pruebas posteriores.
- **Tablets Apple (iPadOS):** aplicación instalable, adaptada a pantalla táctil, Apple Pencil y teclado externo.
- **Tablets Android:** aplicación instalable, adaptada a pantalla táctil, lápices digitales compatibles y teclado externo.
- Android e iPadOS tendrán las mismas funcionalidades principales, sin privilegiar una plataforma por sobre la otra. La disponibilidad de presión u otras capacidades depende del hardware.
- Todas las plataformas deberán permitir crear, editar y consultar los mismos cuadernos y documentos.
- Las aplicaciones para tablets **no** se sustituirán en la entrega del producto por una página abierta en su navegador.
- Las interfaces podrán variar según pantalla y sistema operativo sin alterar la estructura y el contenido del documento.
- La compatibilidad se aceptará tras pruebas con aplicaciones instaladas y dispositivos físicos; no basta con pruebas de navegador móvil.

## RNF-02 · Fidelidad visual

- Las páginas deberán conservar dimensiones, márgenes y distribución definidos, independientemente del tamaño de pantalla o sistema operativo.
- El texto y las anotaciones deberán mantener sus posiciones relativas dentro de la misma página al cambiar el zoom.
- La representación del documento deberá ser equivalente entre la aplicación web y las aplicaciones instalables Android/iPadOS.
- Las fuentes, tamaños, interlineados y saltos de línea deberán mantenerse consistentes en los dispositivos validados.
- Cuadrículas e interlineados podrán necesitar un modo de ajuste para facilitar la escritura sobre líneas.
- No se promete identidad de píxeles universal; se documentarán diferencias de renderizado mediante pruebas reales.

## RNF-03 · Respuesta del lápiz y del editor

- La escritura debe sentirse fluida en dispositivos físicos compatibles, tanto Android como iPadOS.
- El editor no debe bloquearse al dibujar trazos habituales ni al pegar textos extensos.
- Los gestos táctiles y el trazo con lápiz no deben interferir indebidamente con la selección o edición de texto.
- La respuesta se evaluará con sesiones reales; no se promete un tiempo exacto universal ni capacidades de presión en todos los lápices.

## RNF-04 · Sincronización confiable

- Meta: propagar cambios tan pronto como permita la conexión y mostrar su estado de manera comprensible.
- Ante interrupciones o reconexiones, la interfaz no debe afirmar que un documento está sincronizado si quedan cambios pendientes.
- Se probarán cambios simultáneos, eliminaciones de trazos, reconexiones y persistencia antes de aprobar la función.
- La sincronización entre dispositivos de una persona es prioritaria; la edición colaborativa entre múltiples personas no se incluye en el alcance inicial.

## RNF-05 · Integridad y recuperación

- La aplicación web y ambas aplicaciones instalables deberán usar almacenamiento local persistente adecuado para su plataforma.
- Los documentos guardados deberán recuperarse tras cerrar y volver a abrir la aplicación, dentro de las capacidades del entorno utilizado.
- Los cambios locales no deberán desaparecer por interrupciones temporales de conectividad.
- Se incorporará respaldo exportable y restaurable antes de usar documentos importantes.
- En producción habrá persistencia en servidor, copias de seguridad y estrategia de restauración probada.
- El contenido almacenado solo en un dispositivo no se considerará respaldo suficiente.

## RNF-06 · Usabilidad y accesibilidad

- Las interfaces deberán ser intuitivas y adaptadas al dispositivo, sin exigir idéntica ubicación de controles.
- En web, facilitar uso con teclado y ratón; en tablets, pantalla táctil, lápiz y teclado externo.
- Las herramientas esenciales de edición, dibujo y navegación deberán ser accesibles sin operaciones innecesarias.
- Considerar gestos para desplazamiento y zoom, con prevención de trazos accidentales cuando corresponda.
- Incorporar contrastes adecuados, etiquetas comprensibles, indicadores de estado y posibilidad de zoom.
- La lectura en voz alta con seguimiento visual se contempla en una etapa posterior.

## RNF-07 · Seguridad y privacidad

- En el prototipo local no se deben usar datos personales reales ni credenciales de producción.
- No se incorporarán tokens, claves privadas ni contraseñas a Git.
- Antes de beta externa: autenticación, control de acceso por usuario, HTTPS, manejo seguro de archivos y política de privacidad.
- Los apuntes no serán públicamente visibles por defecto.
- Evaluar protección de los datos locales de las aplicaciones instalables antes de distribuir una versión de prueba.

## RNF-08 · Presupuesto y mantenibilidad

- Desarrollo individual, con presupuesto monetario inicial de CLP $0 y pruebas locales antes de contratar servicios.
- Preferir componentes gratuitos y licencias compatibles con el uso comercial futuro; verificar cada dependencia.
- Mantener separados los módulos de documento, texto, dibujo, almacenamiento, sincronización y flashcards.
- Favorecer reutilización del formato de datos y del código cuando sea viable, sin asumir que todos los componentes web funcionarán directamente en React Native.
- No depender de características comerciales de pago sin alternativa validada.
- Registrar decisiones y supuestos para reducir retrabajo.

## RNF-09 · Disponibilidad fuera de línea

- En una fase posterior, web, Android e iPadOS deberán permitir trabajar sin conexión sobre documentos disponibles localmente.
- Los cambios sin conexión deberán guardarse de forma persistente en cada plataforma.
- Al recuperar la conexión, se intentará sincronizar automáticamente y se informará de cambios pendientes o conflictos.
- La capacidad se implementará progresivamente después del guardado local y la sincronización básica.
- No se declarará «offline» si los cambios desaparecen al cerrar o reiniciar la aplicación.
