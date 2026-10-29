# 08 · Plan de pruebas y criterios de aceptación

**Regla:** registrar cada resultado como «No probado», «Pasa» o «Falla», indicando plataforma, dispositivo, versión de aplicación, fecha y evidencia. Un prototipo en navegador móvil no certifica una app instalable.

## Registro recomendado

| Campo | Ejemplo |
| --- | --- |
| Caso | TC-004 |
| Plataforma | Web / Android / iPadOS |
| Dispositivo | PC Windows / tablet Android / iPad |
| Entorno | Firefox/Chrome/Edge / app instalada |
| Entrada | Teclado / ratón / lápiz digital / Apple Pencil |
| Versión | Prototipo H1 / H2-A / H2 |
| Resultado | No probado / Pasa / Falla |
| Fecha | AAAA-MM-DD |
| Evidencia | Captura, video o pasos de reproducción sin datos privados |
| Observaciones | Fuente, rendimiento, gestos, pérdida de datos, etc. |

## Primera prueba de concepto web (H1)

| Caso | Acción | Resultado esperado |
| --- | --- | --- |
| TC-001 | Abrir una página | A4 visible, sin elementos desplazados |
| TC-002 | Cambiar blanco ↔ cuadriculado | Cambia el fondo, no texto ni trazos |
| TC-003 | Escribir con teclado | Inserción y edición normales |
| TC-004 | Justificar párrafo | La alineación visible es justificada |
| TC-005 | Aplicar fuente, tamaño y color | Se aplican sin perder contenido |
| TC-006 | Dibujar con ratón encima de texto | Aparece el trazo sin modificar las letras |
| TC-007 | Dibujar en margen | El trazo se guarda en su posición |
| TC-008 | Borrar marca con goma | Desaparece el trazo; el texto queda intacto |
| TC-009 | Modificar texto bajo un trazo | El trazo permanece fijo en la página por diseño |
| TC-010 | Cambiar zoom | Texto y trazos escalan de forma coherente |
| TC-011 | Guardar, cerrar y reabrir | Se recuperan texto y trazos |
| TC-012 | Dibujar con ratón o puntero en la aplicación web | Los trazos se registran sin alterar el texto |

## Pruebas de aplicaciones instalables (H2-A)

| Caso | Acción | Resultado esperado |
| --- | --- | --- |
| TC-301 | Instalar y abrir prototipo iPadOS | La aplicación se ejecuta correctamente |
| TC-302 | Instalar y abrir prototipo Android | La aplicación se ejecuta correctamente |
| TC-303 | Editar texto con teclado en iPad | Se conserva el formato del documento |
| TC-304 | Editar texto con teclado en Android | Se conserva el formato del documento |
| TC-305 | Dibujar con Apple Pencil | Trazos fluidos sin alterar texto |
| TC-306 | Dibujar con lápiz Android compatible | Trazos fluidos sin alterar texto |
| TC-307 | Borrar anotaciones en ambas apps | Solo desaparecen los trazos seleccionados |
| TC-308 | Cambiar zoom mediante gestos táctiles | Texto y anotaciones mantienen posiciones relativas |
| TC-309 | Abrir documento equivalente en las tres plataformas | Se conservan márgenes y distribución; se registran diferencias |
| TC-310 | Cerrar y abrir ambas apps | Los cambios locales guardados se recuperan |

## Pruebas de sincronización (H2)

| Caso | Acción | Resultado esperado |
| --- | --- | --- |
| TC-101 | Editar desde aplicación web | Cambios visibles en apps conectadas de Android e iPadOS |
| TC-102 | Dibujar desde tablet Android o iPad | Los trazos aparecen en las demás plataformas |
| TC-103 | Borrar trazo desde cualquier tablet | Desaparece en los otros dispositivos y no reaparece |
| TC-104 | Reiniciar servidor local | Documento recuperado desde persistencia, sin perder cambios confirmados |
| TC-105 | Cortar conexión | Se indica desconexión sin afirmar sincronización |
| TC-106 | Reconectar | Se retoman actualizaciones y se gestionan cambios pendientes |
| TC-107 | Editar en varios clientes | No se pierden cambios válidos por sobreescritura total |
| TC-108 | Abrir en web, iPadOS y Android con distintas resoluciones | Distribución equivalente; diferencias reales documentadas |

## Pruebas de organización y estudio (H3)

| Caso | Acción | Resultado esperado |
| --- | --- | --- |
| TC-201 | Crear carpeta y subcarpeta | Navegación consistente |
| TC-202 | Asignar color HEX | Se conserva y muestra el color |
| TC-203 | Crear cuaderno con varias páginas | Páginas en orden correcto |
| TC-204 | Crear flashcard de texto | Frente/reverso guardados en cuaderno actual |
| TC-205 | Cambiar de cuaderno | Tarjetas no se mezclan entre cuadernos |
| TC-206 | Estudiar tarjetas | Frente, revelar reverso y continuar funcionan |
| TC-207 | Editar y borrar tarjeta | Cambios persistidos al reabrir cuaderno |

## Prueba de aceptación con usuarios

Invitar a estudiantes o profesionales con computador y tablet Android o Apple. Asignar tareas reales: redactar, justificar, anotar, cerrar/reabrir, alternar dispositivos y crear tarjetas. Registrar versiones, dispositivos, errores, esfuerzo y oportunidades de mejora. No presentar resultados hipotéticos como pruebas validadas.

## Bloqueantes para declarar un hito aprobado

- Pérdida reproducible de datos o respaldo imposible de recuperar.
- La goma elimina texto por accidente.
- El zoom desacopla dibujos y texto.
- El estado indica «sincronizado» cuando hay cambios pendientes.
- El documento tiene diferencias graves de formato o posición en una plataforma validada.
- El lápiz no permite las tareas mínimas en una tablet declarada compatible.
- No existe aplicación instalable o no se ha probado una plataforma requerida para H2-A/H2.
