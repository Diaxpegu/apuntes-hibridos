# 01 · Visión, problema y usuarios

**Estado:** visión inicial acordada · **Última actualización:** 2026-10-29

## Visión

Diseñar una aplicación de apuntes con edición de texto avanzada, anotaciones manuscritas libres y continuidad entre dispositivos, enfocada en quienes estudian con computador y tablet.

> **Propuesta de valor:** una aplicación de apuntes que integra texto avanzado, escritura libre con lápiz y sincronización rápida entre su versión web para computadores y sus aplicaciones instalables para tablets Android e iPadOS.

## Plataformas previstas

- **Web en computadores:** acceso desde navegadores modernos; la primera prueba se realizará en Windows.
- **Aplicación Android:** instalable en tablets, con herramientas de teclado y lápiz digital compatible.
- **Aplicación iPadOS:** instalable en tablets Apple, con teclado y Apple Pencil.
- Las aplicaciones para tablets tendrán las mismas funcionalidades principales. La apariencia del contenido se conservará mediante un formato de documento compartido y pruebas de fidelidad visual.

## Problema del usuario

- Elaborar apuntes con teclado es cómodo en computadores, pero trasladarlos a una tablet para anotarlos puede implicar pasos manuales y cambios de formato.
- Las aplicaciones centradas en escritura a mano pueden ser incómodas para producir textos formales o justificados.
- Se necesita incorporar tablas, imágenes, márgenes, encabezados, colores, fondos de cuadrícula y notas manuscritas sin sacrificar claridad.
- Las flashcards requieren hoy cambiar de pantalla o servicio, lo que interrumpe la lectura del cuaderno.

## Públicos objetivo

| Segmento | Necesidad representativa | Importancia |
| --- | --- | --- |
| Universitarios con PC + tablet | Redactar, destacar, dibujar y repasar material | Principal |
| Profesionales en formación continua | Estudiar contenidos complejos y conservar apuntes a largo plazo | Principal |
| Estudiantes con un solo dispositivo | Crear y repasar notas | Secundario |

No se presume una cantidad de usuarios, cuota de mercado ni disposición a pagar: deben validarse.

## Jornadas de uso

### J1 · Estudiar en computador y anotar en tablet

1. La persona abre el mismo cuaderno en ambos dispositivos.
2. Escribe, pega y formatea texto desde el computador.
3. Usa el lápiz en la tablet para subrayar, rodear conceptos, escribir notas al margen y dibujar flechas.
4. Espera que los cambios se guarden y aparezcan rápidamente en ambos equipos mientras tienen conexión.

### J2 · Tomar apuntes en tablet Android o Apple

1. Abre un cuaderno y selecciona el estilo de hoja.
2. Puede alternar teclado físico o virtual y lápiz digital compatible con su tablet.
3. El texto no debe moverse ni perder alineación de forma inesperada por el cambio de método de entrada.

### J3 · Estudiar mediante flashcards

1. Lee una sección del cuaderno.
2. Abre el panel lateral de tarjetas sin abandonar la página.
3. Copia o escribe el frente y el reverso, ambos de texto.
4. Guarda la tarjeta automáticamente en el cuaderno activo.
5. Más tarde, elige «Estudiar este cuaderno» y repasa sus tarjetas.

### J4 · Trabajar temporalmente sin internet

1. Se pierde la conexión.
2. La aplicación continúa permitiendo editar documentos almacenados localmente.
3. Marca el estado «Pendiente de sincronización».
4. Al reconectar, transmite los cambios pendientes y los combina o advierte si es necesaria intervención.

**J4 corresponde a una etapa posterior**, no al primer prototipo.

## Objetivos del producto

- Reducir la dependencia de exportación/reimportación de apuntes.
- Mantener una apariencia consistente de la página entre pantallas.
- Dar herramientas de lápiz y teclado dentro de un solo espacio.
- Simplificar creación y repaso de flashcards manuales.
- Ofrecer una interfaz comprensible sin mostrar todas las opciones a la vez.

## No objetivos iniciales

- Reproducir la totalidad de funciones de un procesador de texto profesional o de una aplicación especializada en escritura manuscrita.
- Crear una red social o chat grupal.
- Integrar herramientas externas de tarjetas de estudio o reproducir todas las modalidades de repaso espaciado.
- Generar tarjetas mediante IA.
- Garantizar edición offline simultánea y resolución perfecta de todos los conflictos desde el prototipo.
