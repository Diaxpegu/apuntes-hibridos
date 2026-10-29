# 09 · Riesgos, supuestos y registro de decisiones

## Riesgos

| ID | Riesgo | Impacto | Mitigación |
| --- | --- | --- | --- |
| R-01 | Paginación avanzada considerablemente más compleja que una página fija | Alto | Validar página única; postergar distribución automática |
| R-02 | Saltos de línea o posiciones distintas entre web, Android e iPadOS | Crítico | Formato común, control tipográfico y pruebas de fidelidad |
| R-03 | Diferencias de precisión, latencia, presión y gestos del lápiz entre Android e iPadOS | Crítico | Probar apps instalables en dispositivos físicos de ambas plataformas |
| R-04 | Pérdida de datos por persistencia deficiente o concurrencia | Crítico | Respaldos, almacenamiento durable y pruebas de reconexión |
| R-05 | Anotaciones quedan sobre otro texto después de cambios | Aceptado | Es comportamiento acordado; la persona ajusta los trazos |
| R-06 | Componentes comerciales de pago incompatibles con presupuesto $0 | Alto | Priorizar alternativas gratuitas y revisar licencias |
| R-07 | Añadir demasiadas funciones antes de validar el núcleo | Alto | Entregas por hitos y control de alcance |
| R-08 | Costos recurrentes incompatibles con compra permanente | Alto | Definir límites de servicios y costearlos antes de vender |
| R-09 | Exposición de datos privados o secretos | Crítico | Repositorio privado, .gitignore, permisos, HTTPS y control de acceso |
| R-10 | Falta de acuerdo de derechos y responsabilidades con cliente | Alto | Definir titularidad y entregables por escrito |
| R-11 | Restricciones de instalación, compilación y distribución iPadOS con presupuesto cero | Alto | Investigar herramientas y credenciales antes de comprometer una beta instalada |
| R-12 | Reutilización insuficiente o incompatibilidad del editor entre web y apps móviles | Crítico | Prototipo comparativo antes de implementar funciones avanzadas |

## Registro de decisiones

| Código | Decisión | Estado |
| --- | --- | --- |
| D-01 | Público: universitarios y profesionales en formación continua | Acordada |
| D-02 | Texto y trazos editables por separado | Acordada |
| D-03 | Trazos fijos en coordenadas de página tras modificar texto | Acordada |
| D-04 | Flashcards: solo texto, organizadas por cuaderno | Acordada |
| D-05 | Sincronización automática rápida entre dispositivos de una persona | Acordada como objetivo; falta prueba |
| D-06 | Web para computadores y apps **instalables** Android/iPadOS, con igual prioridad funcional | Acordada como alcance |
| D-07 | Página A4 fija y fondos personalizables | Propuesta inicial aceptada para prototipo |
| D-08 | Desarrollo local con herramientas gratuitas y presupuesto inicial CLP $0 | Acordada |
| D-09 | Next.js, React Native/Expo, Yjs y PostgreSQL como candidatos | Propuesta; requiere validación multiplataforma |
| D-10 | Repositorio GitHub privado inicialmente | Recomendación; confirmar al crear |
| D-11 | Freemium, suscripciones y posible compra permanente | Intención comercial; condiciones pendientes |
| D-12 | Validar prototipos instalables Android/iPadOS antes de cerrar sincronización multiplataforma | Acordada como estrategia de desarrollo |

## Pendientes no bloqueantes para H1

- Nombre/marca final y apariencia gráfica.
- Diseño final de iconos, barras y cuadernos.
- Límites comerciales y precios.
- Importaciones editables externas, voz y repaso espaciado.
- Decisión definitiva de motor visual de edición entre web y apps.

## Pendientes bloqueantes para declarar H2-A/H2 completados

- Evidencia de aplicación **instalable** en iPadOS y Android, no solo una web vista en tablet.
- Pruebas con teclado y lápiz real en ambas plataformas.
- Fidelidad visual suficiente y compatibilidad con el modelo de documento.
- Persistencia local y sincronización probada entre los clientes exigidos por el hito.

## Pendientes para comprometer una entrega comercial

- Pruebas de estabilidad y seguridad en dispositivos objetivo.
- Definición jurídica de titularidad, cesión y material aportado por cliente.
- Costos recurrentes y estrategias de respaldo/soporte.
- Acuerdo de alcance, aceptación, distribución, mantenimiento y soporte.
