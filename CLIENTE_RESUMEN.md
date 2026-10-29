# Propuesta funcional · Apuntes Híbridos

**Documento de conversación con el cliente** · Versión 0.1.1 · 29 de octubre de 2026  
**Nombre del producto:** provisional  
**Estado:** definición; sin desarrollo iniciado

## La idea en una frase

**Una plataforma de apuntes que combina edición avanzada de texto, escritura manuscrita libre y sincronización rápida entre computadores, tablets Android y tablets Apple.**

## ¿A quién va dirigido?

A estudiantes universitarios y profesionales que continúan estudiando. Especialmente personas que trabajan con teclado en un computador y anotan o subrayan con lápiz en una tablet.

## Problema actual

Se pierde tiempo al escribir en una aplicación, exportar el archivo a otra, ajustar su formato y volver a estudiar. Las aplicaciones especializadas en lápiz no siempre ofrecen una experiencia cómoda de teclado y formato; los editores tradicionales no siempre permiten anotar libremente sobre toda la página.

## Plataformas del producto

- **Computadores:** acceso desde una aplicación web, probada inicialmente en Windows.
- **Tablets Android:** aplicación instalable, diseñada para lápiz digital, pantalla táctil y teclado.
- **Tablets Apple (iPadOS):** aplicación instalable, diseñada para Apple Pencil, pantalla táctil y teclado.
- **Equivalencia funcional:** ambas versiones para tablets tendrán las mismas funciones esenciales, sujetas a compatibilidad del dispositivo; todas utilizarán un formato de documento común.

## Experiencia deseada

1. Crear o abrir un cuaderno, elegir página y personalizar su apariencia.
2. Escribir texto con teclado, justificar párrafos, colocar títulos, cambiar fuentes y destacar información.
3. Escribir o dibujar con lápiz en cualquier parte de la página: sobre texto, al costado, alrededor de una frase o en espacios en blanco.
4. Abrir el mismo cuaderno en PC y tablet sin exportar archivos y ver los cambios lo antes posible.
5. Abrir un panel lateral para crear una tarjeta de estudio de **pregunta y respuesta de texto**, copiar o redactar su contenido y guardarla en el cuaderno.
6. Seleccionar un cuaderno y estudiar únicamente sus tarjetas guardadas.

## Decisiones tomadas

- El texto y las marcas de lápiz son **independientes**. Una marca no se mueve automáticamente si el texto cambia; quien edita es responsable de corregirla.
- El contenido de las flashcards es **solo texto**; no se planean imágenes, audio ni fórmulas especiales en la primera etapa.
- Se prioriza que las páginas conserven **la misma composición** en distintos dispositivos. Se validará la fidelidad de forma práctica.
- El servicio deberá permitir trabajo sin internet en una etapa posterior, con sincronización automática al recuperar la conexión.
- La organización incluirá carpetas, subcarpetas, colores personalizables y cuadernos.
- Habrá un modelo gratuito más modalidades de suscripción y compra permanente, con condiciones por validar.

## Entregas progresivas

| Etapa | Propósito | Resultado esperado |
| --- | --- | --- |
| H1 · Prueba web local | Validar el núcleo híbrido | Página con texto, trazos independientes y guardado local en computador |
| H2-A · Apps instalables | Validar las tablets | Prototipos para Android e iPadOS con teclado y lápiz |
| H2 · Sincronización | Validar continuidad | Un mismo documento se actualiza entre web y apps instaladas |
| H3 · Beta personal | Convertirlo en herramienta útil | Cuadernos, organización y flashcards de texto |
| H4 · Beta externa | Probar con usuarios | Acceso seguro, PDF anotable y trabajo offline de forma gradual |
| H5 · Comercial | Preparar lanzamiento | Planes, pagos, políticas y soporte |

**Los plazos y precios se estimarán después de validar la primera prueba de concepto.** El presupuesto inicial de herramientas es CLP $0; esto no equivale a que el desarrollo no tenga costo de tiempo ni a que la operación comercial sea gratuita.

## Qué se aplaza deliberadamente

Conversión perfecta de formatos externos a documentos editables, colaboración simultánea entre múltiples personas, generación automática de tarjetas, tarjetas multimedia, funciones sociales, reproducción de todas las capacidades de suites ofimáticas y reposicionamiento automático de anotaciones.

## Cómo sabremos que el proyecto avanza bien

- Es cómodo escribir con teclado y dibujar con lápiz sin modificar accidentalmente la otra capa.
- La página no cambia de distribución de forma imprevista entre equipos de prueba.
- Los datos sobreviven a cierre y reapertura.
- En la fase de sincronización, editar desde la web se refleja en las apps instaladas de Android e iPadOS, y viceversa, sin exportaciones.
- Es posible crear una tarjeta de pregunta y respuesta y estudiarla desde su cuaderno.

## Decisiones comerciales todavía por validar

- Número de cuadernos gratuitos y cuotas de almacenamiento.
- Precio definitivo de suscripción y de compra permanente.
- Condiciones y límites de nube de una licencia permanente.
- Titularidad del software, permisos de uso de imágenes/plantillas y condiciones de contratación.

**Siguiente acuerdo recomendado:** validar la visión y la primera prueba de concepto; la entrega de ambas apps instalables forma parte del alcance del producto, pero su viabilidad técnica y distribución se validarán por etapas.
