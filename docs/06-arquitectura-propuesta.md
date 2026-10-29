# 06 · Arquitectura propuesta (sujeta a pruebas)

**Las tecnologías de este documento son candidatas, no decisiones irrevocables.** Antes de implementar el producto completo se comprobará el comportamiento real del editor y del lápiz entre las plataformas.

## Restricciones

- Desarrollo inicial por una sola persona; presupuesto monetario de CLP $0.
- Pruebas locales y prototipos antes de contratar servicios de nube.
- **Computadores:** aplicación web desde navegadores modernos, comenzando por Windows.
- **Tablets Android e iPadOS:** aplicaciones instalables, con lápiz digital y teclado externo compatible.
- Las dos aplicaciones móviles deben ofrecer las mismas funciones principales.
- Un mismo formato de documento debe conservar el texto, los trazos y sus coordenadas en todas las plataformas.
- Preferencia por herramientas gratuitas y abiertas; verificar licencias antes de comercializar.
- Las restricciones de compilación o instalación de iPadOS pueden requerir recursos o credenciales adicionales; no se presume que la publicación en tiendas sea gratuita.

## Componentes candidatos

| Área | Recomendación candidata | Motivo / precaución |
| --- | --- | --- |
| Web para computadores | Next.js + React + TypeScript | Experiencia previa del desarrollador y uso desde navegador |
| Apps instalables Android/iPadOS | React Native + Expo | Posible base compartida; validar capacidades reales del editor y lápiz |
| Estilos web | Tailwind CSS | Interfaz adaptable sin costo de licencia inicial |
| Editor de texto | Tiptap sobre ProseMirror | Texto enriquecido y justificación; integración móvil por decidir |
| Formato de documentos | Esquema estructurado compartido, con versiones | Independencia de la plataforma de representación |
| Dibujo en web | Pointer Events + SVG + perfect-freehand | Trazos editables y coordenadas; no equivale automáticamente a API móvil nativa |
| Dibujo en apps | Renderizador e interacción móvil por validar | Pruebas de presión, latencia, gestos y compatibilidad del hardware |
| Persistencia local web | IndexedDB | Guardar documentos en el navegador; añadir exportación de respaldo |
| Persistencia local móvil | Almacenamiento persistente apto para React Native, por definir | No presuponer disponibilidad de IndexedDB fuera del navegador |
| Sincronización | Yjs u otra solución de cambios compartidos validada | Comparar integración de texto y trazos y recuperación ante desconexión |
| Comunicación | WebSocket autoalojado, candidato | Sincronizar clientes con servidor inicialmente en red local |
| Servidor / API | Node.js + TypeScript, candidato | Reducir complejidad y evitar microservicios prematuros |
| Base de datos futura | PostgreSQL | Usuarios, carpetas, cuadernos, flashcards y metadatos |
| Pruebas | Vitest / Playwright para web; pruebas móviles y físicas por definir | Zoom, fidelidad visual, teclado, lápiz y persistencia |

## Diseño por módulos

```text
                     PRODUCTO
                        |
       +----------------+----------------+
       |                                 |
   APLICACIÓN WEB                 APPS INSTALABLES
       |                                 |
 Next.js / React                    React Native / Expo
       |                           +-----+------+
  Computadores                     |            |
                                 Android      iPadOS
       |                                 |
       +----------------+----------------+
                        |
              MODELO DE DOCUMENTO
       - Páginas, márgenes y fondos
       - Texto estructurado editable
       - Trazos independientes por página
       - Cuadernos y flashcards de texto
                        |
          Persistencia local por plataforma
                        |
                API / WebSocket
                        |
          Servidor local -> remoto
          Persistencia y sincronización
                        |
             PostgreSQL (posterior)
```

**Nota:** el diagrama es conceptual. Los clientes no deben depender del servidor para representar un documento ya disponible localmente; la comunicación se incorpora cuando exista sincronización.

## Módulos funcionales

- **Editor:** contenido textual enriquecido y herramientas de formato.
- **Página:** dimensiones, fondos, márgenes y zoom coherente.
- **Anotaciones:** trazos con identificadores únicos y coordenadas independientes del texto.
- **Documentos:** formato versionado, importación/exportación y recuperación.
- **Organización:** carpetas, subcarpetas y cuadernos.
- **Flashcards:** pregunta y respuesta únicamente de texto por cuaderno.
- **Sincronización:** transmisión de modificaciones, estados, reintentos y persistencia.
- **Plataformas:** interfaces y almacenamiento local adaptados a web, Android e iPadOS.

## Modelo conceptual de datos (no esquema SQL definitivo)

- **Usuario:** identificador, cuenta y plan cuando se incorpore autenticación.
- **Carpeta:** identificador, nombre, color HEX, carpeta padre y propietario.
- **Cuaderno:** identificador, título, carpeta, plantilla y propietario.
- **Página:** identificador, cuaderno, orden, dimensiones, fondo y márgenes.
- **Contenido de texto:** estructura editable asociada a una página.
- **Trazo:** identificador, página, puntos, herramienta, color, grosor y estado.
- **Flashcard:** identificador, cuaderno, frente y reverso en texto, fechas de creación/actualización.
- **Estado de sincronización:** cambios confirmados, pendientes y versión de persistencia.

El esquema de tablas y la representación de documentos se definirán tras validar la primera página y su reutilización entre plataformas.

## Decisión técnica pendiente: motor de edición multiplataforma

El motor web basado en HTML/ProseMirror no se renderiza de forma nativa dentro de React Native sin adaptación. Antes de comprometer el producto completo, comparar mediante un prototipo:

1. **Motor compartido en una vista web integrada a las apps:** posible mayor reutilización y fidelidad, sujeto a pruebas de lápiz, teclado y rendimiento.
2. **Componentes de edición específicos por plataforma:** mayor control nativo pero más esfuerzo para conservar la misma distribución visual.

La decisión se tomará según resultados comprobados, no solo por compatibilidad declarada en bibliotecas.

## Decisiones por etapa

### H1 · Web local, sin servidor

Implementar página A4, texto y trazos, con guardado mediante IndexedDB y respaldo exportable cuando corresponda. No integrar aún base de datos central ni autenticación.

### H2-A · Prototipos de apps Android/iPadOS

Crear aplicaciones de prueba instalables, leer el formato compartido, probar teclado, lápiz digital, zoom, guardado local y fidelidad visual. Documentar restricciones de iPadOS, hardware o herramientas de desarrollo.

### H2 · Sincronización en red local

Agregar un servidor WebSocket con persistencia y conectar la web y las apps instaladas. Probar envío en ambos sentidos, borrado de trazos, reinicios y cambios simultáneos. No confiar solo en RAM del servidor.

### H3 · Cuadernos y estudio

Ampliar organización y páginas, incorporar flashcards de texto por cuaderno y exportación o respaldo básico.

### H4 · Beta externa

Agregar autenticación, autorización, HTTPS, distribución controlada de apps de prueba, copias de seguridad y alojamiento dentro de límites económicos viables. Validar compatibilidad física y recuperación sin conexión.

### H5 · Comercial

Costear nube, almacenamiento, respaldos, transferencias, soporte y distribución. Diferenciar los derechos de uso del editor de los servicios recurrentes para posibles compras permanentes.

## Riesgos técnicos principales

- Las páginas con distribución automática, tablas, imágenes y trazos independientes son bastante más complejas que una sola página fija.
- La fidelidad entre un motor de edición web y una aplicación instalada no se resuelve únicamente compartiendo JSON.
- No adoptar extensiones comerciales de paginación como dependencia obligatoria sin presupuesto.
- La sincronización debe conservar cambios de texto y operaciones de trazos sin sobrescribirlos indiscriminadamente.

## Seguridad mínima

- No usar contraseñas reales ni información personal en pruebas iniciales.
- No exponer directamente el servidor local a internet.
- No subir archivos `.env`, tokens, claves ni apuntes privados al repositorio.
- Antes de la beta externa, usar HTTPS, autenticación, autorización y respaldos probados.
