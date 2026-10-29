# 05 · Experiencia de uso y comportamiento del documento

## Plataformas e interfaces

- **Web para computadores:** interfaz optimizada para teclado y ratón, con las herramientas de edición y gestión de cuadernos.
- **App instalada Android:** interfaz táctil con acciones accesibles para lápiz digital y teclado externo compatible.
- **App instalada iPadOS:** interfaz táctil con acciones accesibles para Apple Pencil y teclado externo.
- El contenido y los formatos del documento serán compartidos; la posición de los controles puede adaptarse a cada dispositivo.
- Las apps instaladas no se consideran equivalentes a abrir la web desde un navegador de tablet.

## Concepto de interfaz

- **Vista de documentos:** carpetas de colores, subcarpetas y cuadernos.
- **Vista de edición:** hoja central de aspecto estable, barra breve de herramientas y controles contextuales.
- **Modo texto:** teclado físico o virtual; fuentes, estilos, títulos, justificación, tablas e imágenes progresivamente.
- **Modo lápiz:** escritura manual, marcador, círculos, flechas, selección y goma.
- **Panel de estudio:** lateral, pequeño y plegable, con frente/reverso de flashcard; el documento permanece visible.

## Página y coordenadas

Una página tiene dimensiones definidas, tipo de papel, márgenes, bloques de texto y una colección de trazos independientes expresados en coordenadas de página. En cada plataforma puede escalarse la **vista** sin reordenar voluntariamente los elementos.

**Importante:** las dimensiones fijas permiten una referencia común, pero no garantizan por sí solas saltos de línea idénticos entre los distintos motores de representación. Se necesitan fuentes y reglas de composición coherentes, y pruebas comparativas.

## Textos y trazos independientes

- El editor controla el contenido de texto; la capa de lápiz controla los trazos.
- La goma de lápiz borra marcas, no letras.
- Si un párrafo cambia de tamaño o se elimina, los dibujos **no lo siguen** automáticamente.
- La persona usuaria asume el ajuste manual de marcas que queden desalineadas.
- Se ofrecerá mover/seleccionar trazos más adelante para facilitar correcciones.
- En la primera fase se prioriza que un trazo permanezca en **su página**; mover texto entre páginas no arrastra automáticamente anotaciones.

Este comportamiento fue solicitado expresamente y no se registra como defecto.

## Cuadrícula y justificación

Un fondo cuadriculado es una referencia visual. **Justificar** distribuye espacios dentro de una línea; no alinea automáticamente las líneas de base del texto con los cuadros. Se contempla una opción de interlineado ajustado a cuadrícula, que puede limitar ciertas combinaciones de tipografía o tamaños.

## Flujo de flashcards

1. Abrir un cuaderno y dejar su apunte visible.
2. Abrir el panel lateral «Tarjetas».
3. Escribir o pegar texto en «Frente (pregunta)» y «Reverso (respuesta)».
4. Guardar; la tarjeta queda asociada al cuaderno activo.
5. Acceder a «Estudiar cuaderno» y ver frente, revelar reverso y avanzar.

**Limitación acordada:** contenido de tarjeta exclusivamente texto, sin imágenes, audio ni archivos. El repaso espaciado se deja para más adelante.

## Importaciones

- **PDF anotable:** las páginas originales se usan como contenido fijo o fondo y se superponen anotaciones.
- **Documento editable:** los textos creados en la aplicación se editan como texto.
- No se promete que importar un PDF permita editar sus párrafos directamente.

## Estados visibles propuestos

- Guardado local.
- Pendiente de sincronización.
- Sincronizado.
- Error al sincronizar / reintentar.

## Ejemplos de sesión

### En clase (Android o iPadOS)

La persona escribe un concepto con teclado en la app instalada en su tablet Android o Apple, cambia al lápiz digital compatible y rodea una definición; vuelve al teclado sin que se muevan la cuadrícula y los trazos.

### En casa

La persona escribe en la web desde un computador y destaca información con el lápiz desde la app instalada en una tablet Android o Apple. El documento debe mantenerse visualmente consistente entre las plataformas.

### Al estudiar

La persona lee un apunte, abre el panel de tarjetas, copia una pregunta y su respuesta, guarda y continúa leyendo sin cerrar el cuaderno.
