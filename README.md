# Apuntes Híbridos

**Estado:** documentación y definición del producto · **Versión:** 0.1.1 · **Fecha:** 29-10-2026  
**Nombre:** provisional; no corresponde aún a una marca registrada.  
**Modalidad de trabajo:** desarrollo individual, presupuesto monetario inicial de CLP $0.

> **Propuesta de valor:** una plataforma de apuntes que integra edición avanzada de texto, escritura manuscrita libre y sincronización rápida entre computadores y tablets Android y Apple. Permite crear y estudiar tarjetas de texto sin salir del cuaderno.

## Problema que resuelve

Quien estudia en computador y tablet suele tener que elegir entre un buen editor de texto y una buena experiencia de lápiz. Alternar aplicaciones y exportar documentos consume tiempo, puede alterar el formato y dificulta estudiar con ambos dispositivos. Se busca una experiencia única para crear, anotar, organizar y repasar apuntes.

## Usuarios previstos

- Estudiantes universitarios que usan computador y tablet.
- Profesionales en formación continua, especialización o preparación de exámenes y convalidaciones.

## Principios del producto

1. **Teclado y lápiz, ambos de primera clase.** El texto y los trazos son objetos independientes en la misma página.
2. **Fidelidad visual.** La distribución de las páginas debe verse lo más equivalente posible entre dispositivos; se validará con pruebas reales.
3. **Sincronización rápida y confiable.** Guardar primero, no perder información y mostrar los cambios tan pronto como sea razonable.
4. **Sencillez.** Pocas herramientas visibles a la vez; controles contextuales cuando aporten valor.
5. **Estudio integrado.** Flashcards exclusivamente de texto, vinculadas al cuaderno, con creación manual desde un panel lateral.
6. **Crecimiento por etapas.** Primero una página web local; luego prototipos instalables Android/iPadOS, sincronización, organización, estudio y oferta comercial.

## Alcance inicial acordado

- Página de tamaño fijo (A4 como valor predeterminado), con fondo blanco, rayado o cuadriculado.
- Escritura con teclado, estilos, títulos, justificación, colores, y posteriormente más opciones como tablas y encabezados.
- Capa de lápiz superpuesta: dibujar, escribir a mano, resaltar, rodear, borrar trazos sin borrar texto.
- Anotaciones **ancladas a coordenadas de la página**, no al texto. Si el texto cambia de posición, **el usuario ajusta sus marcas**; no se contempla reposicionamiento automático en el alcance inicial.
- **Computadores:** aplicación web accesible desde navegadores modernos, inicialmente probada en Windows.
- **Tablets Android e iPadOS:** aplicaciones instalables con lápiz digital y teclado; ambas tienen la misma prioridad funcional.
- Sincronización entre dispositivos como objetivo prioritario, implementada después de la prueba local del editor.

## Documentación

| Documento | Uso |
| --- | --- |
| [Resumen para el cliente](CLIENTE_RESUMEN.md) | Presentación sin detalles técnicos|
| [01 · Visión y usuarios](docs/01-vision-y-usuarios.md) | Problema, usuarios y flujos de uso |
| [02 · Requisitos funcionales](docs/02-requisitos-funcionales.md) | Funciones y prioridad |
| [03 · Requisitos no funcionales](docs/03-requisitos-no-funcionales.md) | Calidad, seguridad, rendimiento y compatibilidad |
| [04 · Alcance y versiones](docs/04-alcance-y-mvp.md) | Qué se entrega primero y qué no |
| [05 · Experiencia de edición](docs/05-experiencia-de-usuario.md) | Página, cuadrícula, texto, lápiz y flashcards |
| [06 · Arquitectura propuesta](docs/06-arquitectura-propuesta.md) | Opciones tecnológicas sujetas a prueba |
| [07 · Hoja de ruta](docs/07-hoja-de-ruta.md) | Etapas, entregables y condiciones para avanzar |
| [08 · Pruebas y aceptación](docs/08-pruebas-y-aceptacion.md) | Comportamientos verificables |
| [09 · Riesgos y decisiones](docs/09-riesgos-y-decisiones.md) | Compromisos, riesgos y acuerdos pendientes |
| [10 · Modelo de negocio](docs/10-modelo-de-negocio.md) | Freemium, suscripción y licencia permanente |
| [11 · Acuerdos con el cliente](docs/11-acuerdos-con-cliente.md) | Estado de respuestas y asuntos por aprobar |

## Estado y siguiente hito

**En documentación. No hay implementación comprometida ni funcionalidades desarrolladas en este repositorio.**

Primer hito de desarrollo: una página A4 con editor de texto justificado, cuadrícula y capa independiente de lápiz, con posibilidad de guardar y recuperar el documento. Las aplicaciones instalables de Android e iPadOS se validarán en un hito móvil; la sincronización se implementará después. **Abrir la web en una tablet no sustituye una aplicación instalable ni demuestra sincronización.**

## Confidencialidad, autoría y licencia

Este repositorio se recomienda **privado** mientras se validan alcance, titularidad y comercialización. No se incorpora por ahora una licencia de software de código abierto. La autoría y los derechos económicos/cesiones que correspondan al cliente o al desarrollador deberán definirse por escrito antes de un contrato o entrega comercial. No publicar contraseñas ni datos personales de prueba.
