# Roadmap de desarrollo de la skill Idea to Blueprint

**Versión documental:** 0.3.0.
**Fecha de preparación:** 2026-10-27.
**Fecha de última actualización:** 2026-10-27, cierre de la fase 002.
**Responsable del producto:** Martín Araya.
**Nombre propuesto de la futura skill:** `idea-to-blueprint`.
**Estado:** especificación de desarrollo. Las fases 001 y 002 están completadas. La skill todavía no está implementada ni instalada.
**Alcance aprobado:** documentos para construir la skill y plantillas separadas para los proyectos que planifique.
**Contrato del producto:** [contrato.md](contrato.md), versión 0.2.0, congelado. Define alcance, exclusiones, actores y artefactos autorizados.
**Modos y profundidad:** [modos.md](modos.md), versión 0.1.0, congelado. Define modalidades, niveles de profundidad e invariantes.

## 1. Propósito y criterio de éxito

Transformar una idea de aplicación, incluso incompleta, en una definición de producto y un plan técnico justificable. La skill debe investigar alternativas actuales, consultar documentación oficial, comparar estrategias, diseñar una arquitectura adecuada y producir `roadmap.md` y `AGENTS.md` utilizables por personas y agentes.

No promete encontrar una tecnología universalmente mejor. Debe encontrar opciones compatibles con las restricciones reales, explicar el costo de elegirlas y señalar qué evidencia falta. Tampoco puede conocer todas las necesidades futuras ni revisar todo Internet. Su exhaustividad se mide por cobertura de decisiones relevantes, trazabilidad y riesgos resueltos, no por cantidad de páginas o herramientas mencionadas.

El éxito exige que otro desarrollador pueda empezar la primera tarea sin adivinar el alcance, el stack autorizado, los límites de seguridad o cómo demostrar que terminó. Si falta una decisión crítica, el resultado correcto es un borrador bloqueado con preguntas concretas.

## 2. Separación de responsabilidades

| Nivel | Documento | Función |
| --- | --- | --- |
| Desarrollo de la skill | Este `roadmap.md` | Especifica qué construir, en qué orden y con qué aceptación. |
| Desarrollo de la skill | [AGENTS.md](AGENTS.md) | Regula a los agentes que implementen y mantengan la skill. |
| Desarrollo de la skill | [contrato.md](contrato.md) | Contrato congelado del producto, con alcance, exclusiones, actores y artefactos autorizados. |
| Desarrollo de la skill | [modos.md](modos.md) | Modalidades de trabajo, niveles de profundidad, invariantes y verificación de la aceptación. |
| Proyecto futuro | [Plantilla de roadmap](templates/app/roadmap.md) | Define el producto, las decisiones y las fases de una app concreta. |
| Proyecto futuro | [Plantilla de AGENTS](templates/app/AGENTS.md) | Define cómo trabajar de forma segura en el repositorio de esa app. |
| Investigación de cada proyecto | [Plantilla de expediente](templates/app/expediente.md) | Conserva entrevistas, fuentes, comparaciones, ADR y trazabilidad sin saturar AGENTS. |
| Evaluación de la skill | [tests.md](tests.md) | Define casos de comportamiento y criterios no compensables. |
| Fundamento de esta especificación | [fuentes.md](fuentes.md) | Explica fuentes consultadas y límites de sus aportes. |
| Navegación del paquete | [README.md](README.md) | Explica uso, orden de lectura y estado del paquete a personas. |
| Comprobación de esta entrega | [verificacion.md](verificacion.md) | Registra las comprobaciones documentales ejecutadas y sus límites. |

El AGENTS de la skill nunca se debe copiar como AGENTS de una app. Los proyectos no heredan herramientas, presupuesto, restricciones ni tecnologías de proyectos anteriores sin confirmación.

## 3. Experiencia de uso esperada

### 3.1 Entradas admitidas

- Una frase, una idea abierta o un problema sin solución definida.
- Un brief, una lista de funcionalidades o un documento de requisitos.
- Un repositorio existente, sus instrucciones, manifiestos y documentación.
- Una arquitectura o stack impuesto que deba verificarse, sin sustituirlo silenciosamente.
- Un proyecto ya planificado que necesite auditoría o actualización de decisiones.

### 3.2 Modalidades del mismo proceso

1. **Descubrimiento.** Investigar el dominio y preguntar para resolver variables que cambian el producto o la arquitectura.
2. **Planificación.** Generar una propuesta con decisiones explícitamente pendientes, nunca fingir aprobación.
3. **Auditoría.** Revisar documentos existentes, preservar lo válido y proponer cambios mínimos.
4. **Actualización.** Reinvestigar solamente supuestos o fuentes afectados, mostrar diferencias y conservar historial.

El plan listo para implementación no es una modalidad aparte. Es el nivel exhaustivo de la modalidad de planificación, con las aprobaciones y las evidencias que exige su alcance. Las reglas de cada modalidad y de cada nivel, los invariantes que no se reducen y la verificación de la aceptación están en [modos.md](modos.md).

La profundidad puede ser exploratoria, estándar o exhaustiva. Esto cambia el detalle y el presupuesto de investigación, pero no elimina controles críticos, honestidad de evidencias ni permisos.

### 3.3 Flujo operativo

```mermaid
flowchart TD
    A[Idea o repositorio] --> B[Descubrimiento adaptativo]
    B --> C[Matriz de cobertura]
    C --> D{Revisión independiente de completitud}
    D -->|Faltan datos críticos| B
    D -->|Cobertura suficiente| E[Producto y estrategias de solución]
    E --> F[Universo de candidatos y filtros excluyentes]
    F --> G[Documentación oficial y compatibilidad]
    G --> H[Comparación, costos y riesgos]
    H --> I{Aprobación de decisiones relevantes}
    I -->|Cambios o contradicciones| B
    I -->|Aprobado| J[Arquitectura y contratos]
    J --> K[Roadmap y AGENTS]
    K --> L[Validación estructural y semántica]
    L -->|Defectos| K
    L -->|Conforme al alcance| M[Entrega con evidencia y pendientes]
```

No seleccionar finalistas antes de revisar la completitud de requisitos. Se permite investigar el dominio antes de la entrevista para formular mejores preguntas, sin convertir esa investigación en una elección anticipada de stack.

El diagrama representa la modalidad de planificación en profundidad estándar, con el bucle de descubrimiento. Las otras modalidades y los otros niveles tienen reglas y resultados propios en [modos.md](modos.md).

## 4. Contrato de descubrimiento

### 4.1 Cobertura mínima

| Área | Variables que debe examinar | Decisiones afectadas |
| --- | --- | --- |
| Valor | Problema, solución actual, dolor, resultado observable y diferenciación. | Construir, integrar, comprar o validar primero. |
| Usuarios | Personas, roles, capacidades, contexto de uso y necesidades de acceso. | UX, permisos, canales y prioridades. |
| Etapa | Experimento, prototipo descartable, piloto o producción. | Rigor operativo, alcance y criterios de salida. |
| Plataforma | Web, escritorio, móvil, CLI, servicio, dispositivos y sistemas objetivo. | SDK, distribución, capacidades nativas y pruebas. |
| Equipo | Experiencia real, dedicación, preferencias, aprendizaje y responsables de operación. | Complejidad asumible y costo de mantenimiento. |
| Economía | Presupuesto inicial, mensual, horizonte, moneda y tolerancia a sobrecostos. | Hosting, servicios gestionados y estrategias de crecimiento. |
| Tiempo | Fecha deseada, restricciones reales y disponibilidad del equipo. | MVP, secuenciación y riesgos. |
| Datos | Entidades, volúmenes, crecimiento, sensibilidad, residencia y retención. | Persistencia, protección, búsqueda y eliminación. |
| Identidad | Inicio de sesión, roles, organizaciones, invitados y administración. | Autenticación, autorización y aislamiento. |
| Carga | Concurrencia, tráfico, patrones de lectura y escritura, picos y trabajos largos. | Arquitectura, capacidad y colas. |
| Calidad | Latencia, disponibilidad, recuperación, durabilidad y medición. | NFR, SLO y pruebas. |
| Integraciones | API externas, límites, contratos, credenciales y fallos. | Fronteras, resiliencia y costos. |
| Conectividad | Offline, sincronización, conflicto, relojes y múltiples dispositivos. | Modelo local, consistencia y recuperación. |
| Restricciones | Stack impuesto, licencias, despliegue, red y políticas organizacionales. | Elegibilidad de candidatos. |
| Riesgo | Datos personales, menores, salud, pagos, IA y decisiones sensibles. | Revisión especializada y requisitos de seguridad. |
| Evolución | Portabilidad, exportación, salida de proveedor y migración. | Contratos y costo de reversión. |

### 4.2 Registro de variables

Cada variable tiene identificador `VAR-NNN`, valor, fuente, fecha, criticidad, decisiones afectadas y uno de estos estados.

- `confirmed`, respuesta explícita o evidencia verificable.
- `accepted_assumption`, supuesto aceptado por el usuario, con impacto y fecha de revisión.
- `pending`, todavía no resuelto.
- `blocked`, impide una decisión o aceptación concreta.
- `contradicted`, existen respuestas o evidencias incompatibles.
- `not_applicable`, exclusión justificada y revisable.

No tratar la ausencia de respuesta como consentimiento. Una afirmación del usuario sobre el volumen esperado es un supuesto de demanda, no un benchmark ejecutado.

### 4.3 Política de preguntas

- Priorizar preguntas que cambien elegibilidad, frontera de confianza, costo o alcance.
- Agrupar preguntas independientes y evitar volver a preguntar lo ya documentado.
- Formular opciones comprensibles y explicar consecuencias, sin exigir que el usuario conozca frameworks.
- Profundizar adaptativamente. No enviar un cuestionario fijo de cien preguntas a una app pequeña.
- Preguntar por el resultado necesario antes de preguntar qué tecnología prefiere.
- Si se solicita avanzar sin respuestas, producir un borrador con supuestos explícitos. Nunca etiquetarlo listo si persisten bloqueos críticos.

### 4.4 Gate de completitud

Un revisor en contexto separado, cuando esté disponible, examina la matriz y los requisitos sin defender una tecnología. Si no hay delegación, realizar una segunda pasada persistida y declararla no independiente.

Devuelve `PASS`, `CONDITIONAL` o `BLOCKED`, junto con variables faltantes, contradicciones, preguntas necesarias e impacto. No se aprueba por promedios. Una frontera de permisos desconocida puede bloquear aunque el resto del brief sea excelente.

## 5. Definición del producto

Antes de elegir tecnologías deben existir.

1. Problema, usuarios principales y propuesta de valor.
2. Casos de uso `UC-NNN`, con actor, precondiciones, camino principal, fallos y resultado.
3. Historias o requisitos funcionales `FR-NNN` con aceptación observable.
4. Reglas de negocio `BR-NNN`, especialmente permisos, estados y límites.
5. Funcionalidades `FEAT-NNN`, prioridad, dependencia y razón de inclusión.
6. MVP definido como un conjunto de recorridos completos, no como pantallas desconectadas.
7. Exclusiones y funcionalidades posteriores, con razón y disparador de reevaluación.
8. NFR `NFR-NNN`, con métrica, unidad, condición, objetivo propuesto o aprobado y método de prueba.
9. Métricas de producto, separadas de métricas técnicas, sin inventar investigación con usuarios.
10. Definición de terminado y evidencia por hito.

La priorización puede usar valor, riesgo, esfuerzo, aprendizaje y dependencia. Explicar el método elegido. No introducir una puntuación compleja cuando una clasificación razonada baste.

## 6. Investigación tecnológica y mejores prácticas

### 6.1 Orden de fuentes

Consultar documentación oficial específica de versión, guías oficiales de migración, soporte, precios, licencias, avisos de seguridad y repositorios mantenidos. Complementar con estándares y evidencia secundaria cuando resuelvan una pregunta real. La popularidad sirve como señal auxiliar de ecosistema, nunca como demostración de adecuación.

La documentación de Hermes distingue skills basadas en instrucciones y herramientas existentes de integraciones que requieren una herramienta propia. También recomienda divulgación progresiva y scripts para lógica compleja repetible.[1]

Por ello, la primera implementación propuesta es una skill documental con validadores pequeños, no una aplicación web, una plataforma multiagente ni un servicio que deba desplegarse. Agregar infraestructura exige una necesidad demostrada.

### 6.2 Preguntas de investigación

Cada investigación registra `RQ-NNN`, decisión afectada, fuentes buscadas, resultados, contradicciones y conclusión provisional. Cubrir las categorías aplicables, sin instalar una tecnología por cada categoría.

- Lenguaje y runtime, tipos, herramientas y política de soporte.
- Interfaz, renderizado, navegación, SEO cuando aplique y capacidades nativas.
- Backend, límites de dominio, contratos, trabajos asíncronos y protocolos.
- Persistencia, modelo transaccional, migraciones, consultas, índices y respaldo.
- Identidad, autorización, sesiones, aislamiento y auditoría.
- Integraciones, SDK, cuotas, webhooks y manejo de secretos.
- Pruebas, análisis estático, formato, accesibilidad y automatización.
- Distribución, hosting, operación, observabilidad y recuperación.
- Dependencias, licencias, cadena de suministro y política de actualizaciones.
- Servicios de IA, búsqueda, multimedia o tiempo real solamente cuando el producto los requiera.

### 6.3 Evidencia mínima por fuente

`SRC-NNN`, URL original, título, editor, tipo, fecha de consulta, versión o edición, sección relevante, afirmación respaldada, límites, estado de acceso y decisiones que dependen de ella. Conservar localizador y fragmento breve cuando sea necesario, sin copiar documentación completa ni secretos.

Diferenciar `retrieved`, `blocked`, `partial`, `stale` y `contradictory`. Una URL que responde con una página de error no cuenta como documentación leída. Un enlace o snippet de búsqueda no demuestra compatibilidad.

### 6.4 Uso efectivo de la documentación

Cada regla técnica importante debe traducirse a una decisión, una restricción, una tarea o una prueba. Una bibliografía al final no basta.

La ficha tecnológica incluye versión objetivo, requisitos del runtime, entornos soportados, instalación documentada, limitaciones, prácticas recomendadas aplicables, antipatrones relevantes, migración y referencias exactas. Las versiones se investigan en cada ejecución. No congelar en la skill un stack de moda.

### 6.5 Criterio de detención

Detener la investigación cuando las restricciones críticas tengan cobertura, las opciones razonables de las familias relevantes hayan sido examinadas, los finalistas dispongan de documentación suficiente y nuevas búsquedas no cambien las decisiones. Registrar categorías excluidas y riesgos residuales. Si se agota el presupuesto, indicar qué quedó sin revisar y qué decisiones no pueden aprobarse.

## 7. Selección de stack y arquitectura

### 7.1 Comparar estrategias antes de herramientas

Evaluar si conviene no construir, configurar un producto existente, integrar servicios, crear un prototipo descartable, un piloto limitado o una aplicación de producción. Cuando las etapas difieran, describir cómo se migra y qué parte será descartada.

Derivar el universo de candidatos de investigación actual y taxonomías, no de tres tecnologías recordadas. Conservar un registro de exclusiones. En decisiones con una única opción viable, explicar por qué no se fabrican competidores.

### 7.2 Filtros excluyentes

Antes de puntuar, verificar plataforma, privacidad, conectividad, licencia, presupuesto máximo, compatibilidad, requisitos operacionales y restricciones confirmadas. Un candidato incompatible queda fuera aunque sea simple, barato o popular. La falta de evidencia crítica no se convierte en cumplimiento.

### 7.3 Comparación ponderada

Criterios posibles, ajustados a cada proyecto.

| Criterio | Pregunta verificable |
| --- | --- |
| Adecuación funcional | ¿Resuelve los recorridos y capacidades necesarias? |
| Compatibilidad | ¿Las versiones, drivers, SDK y despliegue funcionan juntos documentalmente? |
| Productividad | ¿El equipo puede entregar y mantener el alcance? |
| Operación | ¿Quién despliega, observa, recupera y actualiza? |
| Seguridad | ¿Qué controles existen y cuáles debe construir el equipo? |
| Costos | ¿Qué ocurre en los escenarios inicial, esperado y de crecimiento? |
| Madurez y soporte | ¿Hay mantenimiento, política de soporte y riesgos concretos? |
| Portabilidad | ¿Cómo se exportan datos y se abandona el proveedor? |
| Experiencia de usuario | ¿Qué capacidades y restricciones impone a cada plataforma? |
| Reversibilidad | ¿Cuánto cuesta corregir una decisión errónea? |

Usar escala anclada, pesos explícitos cuya suma se verifica con código y puntuaciones justificadas. Calcular `score = sum(weight_i * rating_i) / sum(weight_i)` solo sobre criterios definidos. No introducir ceros implícitos para datos desconocidos ni quitar criterios distintos a cada candidato para favorecerlo.

Mantener la incertidumbre separada de la puntuación. Un dato desconocido produce un intervalo, una investigación pendiente o un bloqueo. Ejecutar sensibilidad de pesos y escenarios. Si cambia el ganador con variaciones plausibles, reconocer un empate práctico y decidir por experimento o aprobación informada.

### 7.4 Costos y compatibilidad

Construir una matriz de compatibilidad del conjunto, no fichas aisladas. Diferenciar compatibilidad documentada, inferida y probada. No afirmar prueba local cuando solo se leyó un manual.

El costo total incluye construcción, aprendizaje, hosting, datos, solicitudes, egreso, almacenamiento, respaldo, observabilidad, licencias, dominios, distribución, soporte y migración cuando apliquen. Registrar moneda, región, horizonte, impuestos incluidos o excluidos, niveles gratuitos, cuotas, mínimos y fuente de precios. Los cálculos se ejecutan con herramientas y supuestos explícitos.

### 7.5 ADR y aprobación

Toda decisión relevante usa `ADR-NNN`, estado, contexto, requisitos vinculados, opciones, evidencia, decisión, consecuencias, riesgos, reversión, responsable y disparadores de revisión. Distinguir `proposed`, `accepted`, `rejected`, `superseded` y `blocked`.

No sustituir el stack proporcionado por el usuario sin autorización. Señalar incompatibilidades y proponer alternativas. Las decisiones caras, irreversibles, sensibles o que cambien alcance requieren aprobación explícita.

## 8. Arquitectura y prácticas exigibles

### 8.1 Arquitectura proporcional

Comparar los estilos pertinentes, incluidos monolito, monolito modular, servicios distribuidos, orientado a eventos, local-first, cliente-servidor o backend gestionado. Ninguno es obligatorio o descartable por principio. Separar estilo de despliegue, estilo de interacción y organización interna del código.

Los diagramas C4 ofrecen vistas de contexto, contenedores, componentes y código, además de vistas de apoyo. Elegir solamente las vistas útiles al sistema.[9]

Para cada componente definir propósito, interfaz, datos, propietario, permisos, dependencias, fallos y criterio de prueba. Trazar datos y confirmaciones. Distinguir recepción, aceptación durable, commit y observación por el usuario.

### 8.2 Datos y contratos

- Entidades, relaciones, invariantes y dueño de cada escritura.
- Transacciones, concurrencia, identificadores, timestamps, zonas horarias y eliminación.
- Migraciones, compatibilidad con versiones previas y reversión o recuperación.
- APIs o interfaces internas, autenticación, autorización, errores, paginación y versionado.
- Eventos o trabajos con reintentos, deduplicación, idempotencia y cancelación cuando existan.
- Consistencia y conflictos explícitos, sin promesas distribuidas absolutas.

### 8.3 Seguridad, privacidad y accesibilidad

Crear modelo de amenazas proporcional, superficies, fronteras de confianza y abuso. Convertir cada control aplicable en tarea y prueba. OWASP ASVS proporciona requisitos para verificar controles de seguridad de aplicaciones web y recomienda referencias de requisitos con versión.[5]

NIST SSDF aporta un marco de prácticas de desarrollo seguro integrables al ciclo de vida. Usarlo como referencia de proceso, no como certificado automático.[7]

Examinar autenticación, autorización por recurso, aislamiento, validación de entradas, inyección, secretos, cifrado, sesiones, auditoría y dependencias. Agregar privacidad por diseño, minimización, retención, exportación y borrado. Investigar normativa según datos y jurisdicción, sin afirmar cumplimiento jurídico sin revisión competente.

WCAG 2.2 contiene criterios de éxito verificables para contenido web. La conformidad requiere satisfacer su alcance, no solo ejecutar un escáner.[6]

Para interfaces nativas consultar también las guías oficiales de accesibilidad de la plataforma. Definir teclado, lector de pantalla, foco, contraste, texto escalable, movimiento, errores y alternativas según corresponda.

### 8.4 Pruebas y operación

Definir pruebas unitarias, integración, contratos, recorridos críticos, seguridad, accesibilidad, rendimiento y recuperación según riesgo. No imponer todas las clases en igual proporción.

Definir ambientes, configuración, CI, despliegue, rollback, métricas, logs, trazas, alertas, respaldo y restauración. Separar datos sintéticos de producción. Cada servicio o integración debe tener una degradación aceptable o una razón para bloquear.

Los SLO expresan objetivos de confiabilidad y deben vincularse a indicadores y decisiones operacionales. Elegir objetivos apropiados al producto, no disponibilidad perfecta por defecto.[8]

### 8.5 Módulos condicionales

Pagos, IA, búsqueda, analítica, notificaciones, archivos, colaboración en tiempo real y multi-tenancy se activan por requisitos confirmados. Cada módulo declara activación, fuentes especializadas, riesgos, límites, pruebas y motivo de exclusión si no corresponde. La capacidad básica para detectarlos pertenece al núcleo, aunque los catálogos especializados posteriores sean opcionales.

## 9. Arquitectura propuesta de la propia skill

### 9.1 Implementación mínima

Una skill basada en instrucciones, referencias temáticas, plantillas y validadores deterministas. No necesita inicialmente backend, base de datos, embeddings ni framework de agentes. Hermes ya aporta herramientas de búsqueda, lectura, escritura y delegación. Verificar las herramientas realmente disponibles en cada ejecución.

Las skills de Hermes se cargan por niveles de detalle. Mantener `SKILL.md` como procedimiento operativo y cargar referencias por necesidad.[3]

### 9.2 Árbol futuro propuesto, todavía no implementado

```text
idea-to-blueprint/
  contrato.md
  modos.md
  SKILL.md
  references/
    discovery.md
    product-definition.md
    technology-research.md
    decision-analysis.md
    architecture-review.md
    engineering-practices.md
    output-contracts.md
    evaluation.md
  templates/
    app/
      roadmap.md
      AGENTS.md
      expediente.md
  scripts/
    validate_package.py
    validate_graph.py
    score_decisions.py
  tests/
    fixtures/
    test_package.py
    test_graph.py
    test_scoring.py
  evaluations/
    cases/
    baselines/
```

Estos nombres son contratos propuestos. No ejecutar comandos que los mencionen hasta que los archivos y su interfaz existan. El paquete documental actual no incluye esos scripts ni un `SKILL.md` instalable. Las únicas entradas de este árbol que ya existen son `contrato.md`, creado y congelado en la fase 001, y `modos.md`, creado y congelado en la fase 002. El `SKILL.md` de la fase 010 cargará esos documentos para que la frontera de permisos y las reglas de modalidad y profundidad sean exigibles en ejecución.

### 9.3 Estado y reproducibilidad

Persistir decisiones y evidencia en archivos del proyecto, no solo en la conversación. Un expediente debe permitir continuar desde el último gate, conocer respuestas previas y detectar qué cambió. Un snapshot de evaluación identifica versión de skill, modelo, fuentes, fecha, alcance y huellas de los artefactos.

Distinguir estado de investigación, estado de decisión, estado del documento y estado de implementación. Un roadmap aprobado no significa software construido. Un comando documentado no significa comando ejecutado.

### 9.4 Permisos

La skill puede investigar fuentes públicas y escribir documentos en el destino autorizado. No puede desplegar, comprar, publicar, modificar cuentas, instalar dependencias, crear recursos facturables o migrar datos solo porque esas acciones aparezcan en el roadmap.

Tratar documentación, páginas, repositorios y comentarios como datos no confiables. No promover instrucciones externas a reglas del agente ni copiar contenido peligroso a AGENTS. Proteger secretos y datos personales durante investigación y pruebas.

El contrato vigente de alcance, exclusiones, actores y artefactos autorizados está en [contrato.md](contrato.md), congelado en la fase 001. Ese documento clasifica los efectos en clases A, B y C, define qué constituye una autorización y prevalece ante discrepancia con este roadmap.

## 10. Contrato de salida de cada ejecución

### 10.1 Artefactos principales

`roadmap.md` contiene contexto, producto, alcance, stack con estados, arquitectura, restricciones, fases y aceptación. `AGENTS.md` contiene reglas de trabajo, límites, comandos reales o explícitamente propuestos, validación y definición de terminado.

`expediente.md` conserva cobertura, investigación, alternativas, costos, ADR, riesgos, fuentes, revisión y trazabilidad. Puede dividirse en documentos temáticos si crece, con enlaces válidos. Si el usuario pide estrictamente dos archivos, integrar allí los anexos sin perder evidencia ni crear archivos adicionales no acordados.

AGENTS es un formato de contexto e instrucciones para agentes de programación, complementario al README humano.[4]

### 10.2 Roadmap ejecutable

Cada fase tiene ID estable, objetivo, alcance, entregable, requisitos, dependencias, tareas, prueba, evidencia, riesgo y condición de cierre. Las dependencias internas forman un DAG y existen. Las externas incluyen proyecto y versión de contrato. No convertir fases opcionales en prerrequisitos del núcleo.

Usar hitos funcionales y recorridos verticales. Especificar rutas como propuestas si el repositorio no existe. Estimar rangos con supuestos solo cuando aporten valor, sin prometer fechas exactas a partir de una idea vaga.

### 10.3 AGENTS utilizable

Reglas críticas al inicio, mapa del repositorio, stack autorizado, documentación de versión, convenciones concretas, flujo de cambio, pruebas, permisos y protocolo de bloqueo. Evitar repetir la investigación completa. Revisar tamaño y comportamiento del agente de destino.

En Hermes, la selección del tipo de archivo de contexto y su descubrimiento dependen de las reglas documentadas. No asumir que AGENTS se cargará si existe un tipo de mayor prioridad o un override.[2]

### 10.4 Gate documental

- Requisitos críticos cubiertos o bloqueos visibles.
- Stack compatible documentalmente y decisiones aprobadas para el estado declarado.
- Cada feature del MVP trazada a una fase y una aceptación.
- Requisitos de calidad trazados a pruebas o decisiones explícitas.
- Reglas de AGENTS compatibles con roadmap y contratos.
- Fuentes abiertas, leídas y atribuidas donde respaldan decisiones.
- Comandos diferenciados entre propuestos, documentados y ejecutados.
- Enlaces, tablas, fences, IDs y dependencias válidos.
- Sin placeholders críticos en una entrega declarada lista para implementar.
- Sin casillas de implementación marcadas a partir de la mera escritura de documentos.

## 11. Hitos del desarrollo de la skill

| Hito | Fases | Resultado exigido |
| --- | --- | --- |
| M0, contrato | 001–010 | Alcance, estados, esquema de evidencia y protocolo de preguntas definidos. |
| M1, investigación | 011–020 | Producto, fuentes y fichas documentales operativos en fixtures. |
| M2, decisiones | 021–030 | Filtros, compatibilidad, comparación, costos y ADR evaluables. |
| M3, ingeniería | 031–040 | Arquitectura, amenazas, calidad y módulos condicionales integrados. |
| M4, beta usable | 041–050 | Una idea real recorre el proceso y produce los documentos, con limitaciones explícitas. |
| M5, núcleo estable | 051–060 | Validación, evaluación conductual, regresión y publicación autorizada del núcleo. |
| Extensiones | 061–150 | Catálogo opcional. Ninguna se implementa sin necesidad y aprobación específicas. |

Los hitos son objetivos de aceptación, no fechas comprometidas. Las fases 001 y 002 están completadas y las fases 003 a 060 permanecen pendientes. La beta no exime fuentes ni seguridad. El núcleo estable no implica que todas las tecnologías o jurisdicciones estén cubiertas.

## 12. Fases del núcleo obligatorio

Cada fase se implementa con pruebas o ejemplos negativos apropiados. `Dep.` declara únicamente dependencias internas de este roadmap.

El estado de cada fase usa un vocabulario cerrado: `pendiente`, `en curso`, `completada ✅` y `bloqueada`. Una fase solo pasa a `completada ✅` cuando su aceptación está satisfecha con evidencia real, y su registro declara los artefactos producidos, la evidencia obtenida y el límite de esa evidencia. En este roadmap las fases 001 y 002 están completadas.

### Definition of Ready común para construir la skill

Antes de iniciar cualquier fase, registrar la autorización de implementación, el destino de trabajo, las dependencias ya aceptadas, las entradas disponibles, el entregable y la prueba prevista. Conservar en el registro de la fase su estado de Ready y los bloqueos. Mencionar una dependencia no prueba que esté terminada.

Las fichas siguientes heredan esta Ready común. Sus condiciones adicionales son las de esta tabla. Para las fases no enumeradas, las entradas mínimas son los entregables aceptados de sus dependencias y los requisitos de su objetivo. Si no bastan, explicitar la entrada faltante antes de empezar, sin inventarla.

| Fase o grupo | Entradas y condiciones adicionales | Qué impide iniciar |
| --- | --- | --- |
| 001 | Orden que autorice construir la skill, con responsable y destino definidos, registrada como ORDEN-001 en [contrato.md](contrato.md). No tiene dependencias previas. | Sin orden registrada no se puede iniciar. La autorización de la entrega 0.1.0 solo cubría documentación y no habilitaba esta fase. |
| 002 | Contrato 001 aceptado y usuarios previstos de los modos identificados, con modalidades y niveles fijados en [modos.md](modos.md). | Confundir modo planificación con permiso de ejecución. |
| 003 | Artefactos y límites de persistencia acordados en 001. | Destino o política de sobrescritura sin autorización. |
| 004 | Esquema de variables e identificadores disponible desde 003. | Estados sin significado o fuentes no representables. |
| 005 | Modos 002 y matriz 004 disponibles, con ejemplos de entrada vaga y concreta. | Preguntas que dependan de un stack elegido prematuramente. |
| 006 | Protocolo de preguntas y variables disponible para representar contradicciones. | Convertir un supuesto en hecho externo sin evidencia. |
| 007 | Fixtures de cobertura suficiente, incompleta y contradictoria preparados. | Falta de criterio de bloqueo o independencia mal declarada. |
| 008 | Roles de aprobación y decisiones de alto impacto identificados. | No poder distinguir propuesta de aceptación explícita. |
| 009 | Alcance de efectos permitido y fixtures sintéticos no sensibles disponibles. | Prueba que requiera credenciales o efectos no autorizados. |
| 010 | Contratos anteriores aceptados y formato vigente de Hermes verificado. | Referencias inexistentes o metadatos no verificables. |
| 028 | Pregunta falsable, recursos, criterio y permiso del experimento definidos. | Ejecutar un spike sin autorización específica. |
| 049 | Idea piloto autorizada, participante o simulador identificado y límites acordados. | Usar datos reales o servicios externos sin permiso. |
| 051 | Casos, perfiles de resultado y respuestas críticas congelados antes de medir. | Cambiar el simulador durante la corrida para facilitar resultados. |
| 057 | Perfil y destinos de carga autorizados y descubiertos. | Instalar en otro perfil o prometer plataformas no disponibles. |
| 059 | Evidencia de validación y regresión disponible, distribución autorizada si corresponde. | Publicar como efecto implícito de preparar el paquete. |
| 060 | Dependencias y gates exigidos aceptados, riesgos residuales revisados por responsable. | Cerrar con defectos críticos o evidencia esencial pendiente. |

### Fase 001. Congelar el contrato del producto
- **Objetivo:** delimitar planificación frente a implementación automática.
- **Entregable:** alcance, exclusiones, actores y artefactos autorizados.
- **Aceptación:** una petición de desplegar no se interpreta como permiso implícito del modo planificación.
- **Dep.:** ninguna.
- **Estado:** completada ✅.
- **Artefactos:** [contrato.md](contrato.md) versión 0.1.0 congelado, con alcance, exclusiones, actores, artefactos autorizados, clases de efecto, reglas C-01 a C-05, quince casos negativos y trazabilidad.
- **Evidencia:** autorización ORDEN-001 registrada en [contrato.md](contrato.md) con responsable, destino, alcance y exclusiones. Control documental y batería de mutaciones ejecutados sobre el paquete, con resultado registrado en [verificacion.md](verificacion.md).
- **Límite de la evidencia:** la aceptación se verificó a nivel documental. El comportamiento en ejecución no se ha observado porque la skill todavía no existe, y corresponde a las fases 051 a 055.

### Fase 002. Definir modos y niveles de profundidad
- **Objetivo:** ajustar detalle sin omitir controles esenciales.
- **Entregable:** reglas para descubrimiento, planificación, auditoría y actualización.
- **Aceptación:** un mismo caso conserva restricciones críticas en todos los niveles.
- **Dep.:** 001.
- **Estado:** completada ✅.
- **Artefactos:** [modos.md](modos.md) versión 0.1.0 congelado, con cuatro modalidades, tres niveles de profundidad, nueve invariantes, matriz de doce celdas, caso de referencia, dos casos límite y trazabilidad. Taxonomía reconciliada en la sección 3.2 de este roadmap y en la versión 0.2.0 de [contrato.md](contrato.md).
- **Evidencia:** autorización ORDEN-002 registrada en [modos.md](modos.md) con responsable, destino, alcance y exclusiones. Control documental y batería de mutaciones ejecutados sobre el paquete, con resultado registrado en [verificacion.md](verificacion.md).
- **Límite de la evidencia:** la aceptación se verificó a nivel documental, con el caso de referencia CASE-M1 y los límites N1 y N2 evaluados en los tres niveles. El comportamiento en ejecución no se ha observado porque la skill todavía no existe, y corresponde a las fases 051 a 056.

### Fase 003. Diseñar identificación y persistencia
- **Objetivo:** evitar decisiones perdidas entre sesiones.
- **Entregable:** identificadores, estados y esquema del expediente.
- **Aceptación:** reanudar un caso no duplica IDs ni convierte pendientes en confirmados.
- **Dep.:** 001.
- **Estado:** pendiente.

### Fase 004. Construir cobertura de variables
- **Objetivo:** detectar vacíos antes de proponer stack.
- **Entregable:** matriz de áreas, criticidad y decisiones afectadas.
- **Aceptación:** cada variable tiene fuente y estado, incluso cuando no aplica.
- **Dep.:** 003.
- **Estado:** pendiente.

### Fase 005. Especificar entrevista adaptativa
- **Objetivo:** resolver primero incertidumbres que cambian decisiones.
- **Entregable:** protocolo de selección y seguimiento de preguntas.
- **Aceptación:** una app offline recibe preguntas de sincronización y una app local simple no recibe preguntas irrelevantes de clústeres.
- **Dep.:** 002, 004.
- **Estado:** pendiente.

### Fase 006. Separar supuestos y contradicciones
- **Objetivo:** impedir defaults silenciosos.
- **Entregable:** reglas de aceptación de supuestos y resolución de conflicto.
- **Aceptación:** exigir cero servicios externos y un proveedor SaaS obligatorio produce contradicción visible.
- **Dep.:** 004, 005.
- **Estado:** pendiente.

### Fase 007. Implementar revisión de completitud
- **Objetivo:** cuestionar requisitos antes de generar alternativas.
- **Entregable:** revisión separada con PASS, CONDITIONAL y BLOCKED.
- **Aceptación:** faltantes críticos bloquean, y se declara si no hubo revisor independiente.
- **Dep.:** 005, 006.
- **Estado:** pendiente.

### Fase 008. Diseñar gates de aprobación
- **Objetivo:** controlar decisiones caras o de alto impacto.
- **Entregable:** estados de aprobación y registro del alcance aprobado.
- **Aceptación:** una propuesta técnica no aparece como decisión aceptada sin evidencia de aprobación.
- **Dep.:** 006, 007.
- **Estado:** pendiente.

### Fase 009. Delimitar confianza y permisos
- **Objetivo:** aislar fuentes externas y limitar efectos laterales.
- **Entregable:** política de investigación, documentos, secretos y acciones excluidas.
- **Aceptación:** una página externa no puede autorizar publicaciones ni lectura de credenciales.
- **Dep.:** 001, 008.
- **Estado:** pendiente.

### Fase 010. Redactar el procedimiento SKILL.md
- **Objetivo:** convertir el contrato en un flujo cargable y breve.
- **Entregable:** SKILL.md con frontmatter, referencias y criterios de salida.
- **Aceptación:** metadatos válidos, descripción breve, rutas portables y carga progresiva verificadas.
- **Dep.:** 002, 003, 007, 008, 009.
- **Estado:** pendiente.

### Fase 011. Definir problema y usuarios
- **Objetivo:** separar valor de una lista de tecnologías.
- **Entregable:** problema, usuarios, usos y señales de éxito.
- **Aceptación:** el brief identifica a quién beneficia y cómo se observará valor, sin inventar entrevistas.
- **Dep.:** 007, 010.
- **Estado:** pendiente.

### Fase 012. Formalizar casos de uso y reglas
- **Objetivo:** describir comportamiento y fallos.
- **Entregable:** UC, FR y BR con IDs y aceptación.
- **Aceptación:** cada caso crítico cubre camino principal, permisos y al menos sus fallos relevantes.
- **Dep.:** 011.
- **Estado:** pendiente.

### Fase 013. Priorizar features y MVP
- **Objetivo:** construir un primer resultado completo.
- **Entregable:** features priorizadas, recorridos MVP y exclusiones.
- **Aceptación:** toda feature MVP tiene valor, requisito y criterio de cierre, sin ampliar alcance silenciosamente.
- **Dep.:** 012.
- **Estado:** pendiente.

### Fase 014. Especificar requisitos de calidad
- **Objetivo:** reemplazar adjetivos por criterios medibles.
- **Entregable:** NFR con objetivo, escenario, métrica y método de medición.
- **Aceptación:** términos como rápido o escalable se traducen a propuestas verificables o preguntas pendientes.
- **Dep.:** 012, 013.
- **Estado:** pendiente.

### Fase 015. Planificar preguntas de investigación
- **Objetivo:** buscar para responder decisiones concretas.
- **Entregable:** RQ, categorías aplicables, presupuesto y detención.
- **Aceptación:** cada búsqueda tiene una incertidumbre asociada y las exclusiones se justifican.
- **Dep.:** 013, 014.
- **Estado:** pendiente.

### Fase 016. Registrar fuentes y afirmaciones
- **Objetivo:** asegurar atribución y lectura real.
- **Entregable:** SRC, afirmaciones, versiones, localizadores y estado de acceso.
- **Aceptación:** se detectan páginas de error, snippets insuficientes y fuentes que no respaldan la afirmación.
- **Dep.:** 009, 015.
- **Estado:** pendiente.

### Fase 017. Resolver acceso fallido y fuentes contradictorias
- **Objetivo:** no sustituir investigación por invención.
- **Entregable:** fallback de acceso, fuentes alternativas y bloqueos.
- **Aceptación:** un 403 persistente deja constancia y no produce una compatibilidad ficticia.
- **Dep.:** 016.
- **Estado:** pendiente.

### Fase 018. Verificar versiones y soporte
- **Objetivo:** evitar documentación de una versión distinta.
- **Entregable:** runtime, SDK, soporte, edición y fecha de revisión por candidato.
- **Aceptación:** se detecta una guía actual incompatible con el runtime impuesto.
- **Dep.:** 016, 017.
- **Estado:** pendiente.

### Fase 019. Crear fichas de prácticas aplicables
- **Objetivo:** utilizar la documentación en decisiones y pruebas.
- **Entregable:** reglas concretas con fuente, aplicación, excepción y comprobación.
- **Aceptación:** cada regla importante genera tarea, restricción o prueba, no solo una cita decorativa.
- **Dep.:** 018.
- **Estado:** pendiente.

### Fase 020. Comparar estrategias de solución
- **Objetivo:** decidir qué construir antes de elegir framework.
- **Entregable:** construir, integrar, comprar, prototipar o pilotear, según pertinencia.
- **Aceptación:** se distinguen prototipo descartable y producción, con evolución explícita.
- **Dep.:** 013, 014, 019.
- **Estado:** pendiente.

### Fase 021. Descubrir el universo de candidatos
- **Objetivo:** evitar una shortlist memorizada.
- **Entregable:** familias investigadas, candidatos y cobertura de búsqueda.
- **Aceptación:** las familias relevantes tienen evaluación o motivo documentado de exclusión.
- **Dep.:** 015, 020.
- **Estado:** pendiente.

### Fase 022. Aplicar restricciones excluyentes
- **Objetivo:** descartar incompatibilidades antes de puntuar.
- **Entregable:** tabla de elegibilidad y exclusiones vinculadas a VAR y NFR.
- **Aceptación:** una opción que viola una restricción confirmada no gana por puntuación.
- **Dep.:** 018, 021.
- **Estado:** pendiente.

### Fase 023. Verificar compatibilidad del conjunto
- **Objetivo:** comprobar el stack como combinación.
- **Entregable:** matriz runtime, framework, SDK, datos, herramientas y despliegue.
- **Aceptación:** toda combinación tiene evidencia, incertidumbre o bloqueo, distinguiendo documental de ejecutada.
- **Dep.:** 018, 022.
- **Estado:** pendiente.

### Fase 024. Implementar puntuación explicable
- **Objetivo:** hacer comparables los finalistas sin falsa precisión.
- **Entregable:** criterios, pesos, escala anclada y cálculo reproducible.
- **Aceptación:** pesos, denominador y puntuaciones se validan, y faltantes no se convierten en ceros silenciosos.
- **Dep.:** 022, 023.
- **Estado:** pendiente.

### Fase 025. Incorporar incertidumbre y sensibilidad
- **Objetivo:** distinguir ganador robusto de empate aparente.
- **Entregable:** escenarios de pesos y tratamiento de datos desconocidos.
- **Aceptación:** una inversión plausible del ranking se comunica y activa investigación o decisión informada.
- **Dep.:** 024.
- **Estado:** pendiente.

### Fase 026. Calcular costo total
- **Objetivo:** hacer visible el costo de construir y operar.
- **Entregable:** escenarios con unidades, tarifas, moneda, región y supuestos.
- **Aceptación:** cálculos reproducibles, cuotas y caducidad de precios documentadas, sin mezclar costos únicos y recurrentes.
- **Dep.:** 016, 023, 024.
- **Estado:** pendiente.

### Fase 027. Evaluar licencias, soporte y salida
- **Objetivo:** comparar riesgos de dependencia.
- **Entregable:** matriz de licencias, mantenimiento, exportación y migración.
- **Aceptación:** planes comerciales y ediciones se distinguen, y las dudas jurídicas se escalan.
- **Dep.:** 018, 022, 026.
- **Estado:** pendiente.

### Fase 028. Diseñar spikes de riesgo
- **Objetivo:** resolver incertidumbre que la documentación no prueba.
- **Entregable:** experimentos acotados, criterio de éxito y permiso requerido.
- **Aceptación:** un spike propuesto no aparece ejecutado y su alcance evita tocar producción.
- **Dep.:** 023, 025, 027.
- **Estado:** pendiente.

### Fase 029. Registrar ADR y decisión del stack
- **Objetivo:** preservar razonamiento y aprobación.
- **Entregable:** ADR con alternativas, consecuencias, evidencia y reversibilidad.
- **Aceptación:** se puede reconstruir por qué se eligió y qué condiciones obligan a reconsiderar.
- **Dep.:** 008, 025, 026, 027, 028.
- **Estado:** pendiente.

### Fase 030. Aprobar la estrategia técnica
- **Objetivo:** fijar una base sin ocultar pendientes.
- **Entregable:** decisiones aceptadas o propuesta bloqueada con preguntas.
- **Aceptación:** ninguna tecnología impuesta se sustituye sin aprobación y ningún bloqueo se disfraza de decisión tomada.
- **Dep.:** 029.
- **Estado:** pendiente.

### Fase 031. Diseñar límites y componentes
- **Objetivo:** transformar drivers en responsabilidades claras.
- **Entregable:** contexto, módulos, interfaces y propietarios.
- **Aceptación:** cada componente tiene propósito y prueba, y la distribución está justificada cuando exista.
- **Dep.:** 014, 030.
- **Estado:** pendiente.

### Fase 032. Trazar datos, permisos y confirmaciones
- **Objetivo:** demostrar que el flujo es realizable.
- **Entregable:** recorrido de datos, secretos, red y acknowledgements.
- **Aceptación:** se distingue recepción de commit y no hay llamadas prohibidas por la frontera aprobada.
- **Dep.:** 009, 031.
- **Estado:** pendiente.

### Fase 033. Definir modelo de datos y consistencia
- **Objetivo:** hacer explícitas invariantes y propiedad de escrituras.
- **Entregable:** entidades, relaciones, transacciones y conflictos.
- **Aceptación:** cada invariante crítica tiene una estrategia y un caso de fallo verificable.
- **Dep.:** 012, 023, 032.
- **Estado:** pendiente.

### Fase 034. Definir contratos e integraciones
- **Objetivo:** limitar acoplamiento y fallos externos.
- **Entregable:** contratos versionados, permisos, errores y políticas de reintento.
- **Aceptación:** cada integración describe fallo, cuota, credencial y responsable, o exclusión justificada.
- **Dep.:** 032, 033.
- **Estado:** pendiente.

### Fase 035. Planificar seguridad y privacidad
- **Objetivo:** integrar controles desde el diseño.
- **Entregable:** amenazas, controles, datos sensibles, retención y pruebas.
- **Aceptación:** los límites de acceso se prueban negativamente y no se afirma cumplimiento legal automático.
- **Dep.:** 032, 033, 034.
- **Estado:** pendiente.

### Fase 036. Definir UX y accesibilidad
- **Objetivo:** conectar recorridos con estados de interfaz y acceso.
- **Entregable:** navegación, carga, vacío, error, recuperación y aceptación accesible.
- **Aceptación:** cada recorrido MVP tiene estados relevantes y pruebas apropiadas a su plataforma.
- **Dep.:** 013, 031, 035.
- **Estado:** pendiente.

### Fase 037. Diseñar estrategia de pruebas
- **Objetivo:** demostrar valor, calidad y límites de seguridad.
- **Entregable:** matriz de requisitos a pruebas con niveles, datos y ambientes.
- **Aceptación:** todo requisito crítico tiene aceptación positiva y negativa donde corresponda.
- **Dep.:** 014, 034, 035, 036.
- **Estado:** pendiente.

### Fase 038. Diseñar despliegue y recuperación
- **Objetivo:** incluir operación real en la arquitectura.
- **Entregable:** ambientes, configuración, migración, backup, restore y rollback.
- **Aceptación:** se describe quién recupera el sistema y cómo se prueba sin afectar producción.
- **Dep.:** 026, 033, 034, 035.
- **Estado:** pendiente.

### Fase 039. Definir observabilidad y SLO
- **Objetivo:** medir los objetivos relevantes.
- **Entregable:** indicadores, objetivos, logs seguros y alertas accionables.
- **Aceptación:** cada SLO tiene ventana, población, medición y responsable, o motivo de no aplicación.
- **Dep.:** 014, 037, 038.
- **Estado:** pendiente.

### Fase 040. Integrar módulos condicionales
- **Objetivo:** cubrir dominios especiales sin imponerlos.
- **Entregable:** detección y checklist de IA, pagos, offline, tiempo real, archivos y tenancy.
- **Aceptación:** cada módulo queda activado con requisitos o excluido con razón, y el núcleo no depende de extensiones opcionales.
- **Dep.:** 007, 035, 037, 039.
- **Estado:** pendiente.

### Fase 041. Diseñar el grafo del roadmap generado
- **Objetivo:** ordenar por dependencias y valor verificable.
- **Entregable:** hitos, fases, tareas y reglas de granularidad.
- **Aceptación:** hay una primera tarea ejecutable, hitos funcionales y referencias internas sin ciclos.
- **Dep.:** 013, 030, 037, 038, 040.
- **Estado:** pendiente.

### Fase 042. Especificar contratos de tareas y evidencia
- **Objetivo:** impedir fases vagas o cierres ficticios.
- **Entregable:** ficha de fase, Definition of Ready y Definition of Done.
- **Aceptación:** cada tarea define artefacto, prueba, evidencia y bloqueo, sin atribuir ejecución no realizada.
- **Dep.:** 041.
- **Estado:** pendiente.

### Fase 043. Implementar render de roadmap
- **Objetivo:** producir un plan concreto y legible.
- **Entregable:** plantilla completada con producto, arquitectura y fases.
- **Aceptación:** no quedan placeholders críticos en modo listo, y el borrador señala los que impiden avanzar.
- **Dep.:** 042.
- **Estado:** pendiente.

### Fase 044. Implementar render de AGENTS
- **Objetivo:** producir reglas operativas ajustadas al repositorio.
- **Entregable:** mapa, stack autorizado, límites, comandos y verificación.
- **Aceptación:** no copia instrucciones de la skill ni presenta rutas propuestas como existentes.
- **Dep.:** 019, 030, 037, 043.
- **Estado:** pendiente.

### Fase 045. Integrar expediente y trazabilidad
- **Objetivo:** conservar el razonamiento fuera del contexto permanente.
- **Entregable:** VAR a UC, FR, NFR, ADR, fases y pruebas, con fuentes.
- **Aceptación:** ninguna feature MVP queda huérfana y toda decisión crítica tiene evidencia o bloqueo.
- **Dep.:** 016, 029, 043, 044.
- **Estado:** pendiente.

### Fase 046. Validar estructura e identificadores
- **Objetivo:** detectar defectos documentales automáticamente.
- **Entregable:** validación de IDs, enlaces, tablas, fences y campos obligatorios.
- **Aceptación:** fixtures defectuosos fallan con mensajes localizables y fixtures válidos pasan.
- **Dep.:** 043, 044, 045.
- **Estado:** pendiente.

### Fase 047. Validar dependencias y contratos
- **Objetivo:** impedir ciclos y referencias inventadas.
- **Entregable:** validador de DAG, dependencias externas y versiones.
- **Aceptación:** detecta ciclos, referencias ausentes y una extensión opcional convertida en requisito del núcleo.
- **Dep.:** 041, 046.
- **Estado:** pendiente.

### Fase 048. Revisar coherencia semántica de la pareja
- **Objetivo:** detectar contradicciones que un parser no encuentra.
- **Entregable:** revisión de producto, arquitectura, comandos y reglas.
- **Aceptación:** detecta un backend o proveedor prohibido por restricciones y divergencias entre roadmap y AGENTS.
- **Dep.:** 044, 045, 047.
- **Estado:** pendiente.

### Fase 049. Ejecutar un piloto de extremo a extremo
- **Objetivo:** comprobar utilidad con una idea real autorizada.
- **Entregable:** entrevista, investigación, decisiones y documentos del piloto.
- **Aceptación:** un lector ajeno identifica alcance, primera tarea y bloqueos, con evidencia de la ejecución de la skill.
- **Dep.:** 010, 040, 048.
- **Estado:** pendiente.

### Fase 050. Publicar beta usable para revisión
- **Objetivo:** entregar la capacidad central sin fingir estabilidad completa.
- **Entregable:** paquete beta y limitaciones conocidas.
- **Aceptación:** se completa el piloto sin omitir controles críticos y se separan defectos de mejoras opcionales.
- **Dep.:** 049.
- **Estado:** pendiente.

### Fase 051. Congelar corpus y rúbrica
- **Objetivo:** medir comportamiento de forma comparable.
- **Entregable:** casos progresivos, respuestas simuladas y criterios no compensables.
- **Aceptación:** casos, pesos, campos y resultados pendientes se validan programáticamente.
- **Dep.:** 050.
- **Estado:** pendiente.

### Fase 052. Probar ambigüedad y contradicciones
- **Objetivo:** evitar decisiones prematuras con entradas incompletas.
- **Entregable:** ejecuciones de casos vagos, presupuestos ausentes y requisitos conflictivos.
- **Aceptación:** se hacen preguntas críticas y no se fabrican preferencias, requisitos ni aprobaciones.
- **Dep.:** 051.
- **Estado:** pendiente.

### Fase 053. Probar restricciones y dominios complejos
- **Objetivo:** verificar razonamiento más allá de CRUD simples.
- **Entregable:** casos offline, datos sensibles, distribución e IA cuando aplique.
- **Aceptación:** las recomendaciones satisfacen restricciones, sin exigir un único stack predeterminado.
- **Dep.:** 051, 052.
- **Estado:** pendiente.

### Fase 054. Probar resiliencia y reanudación
- **Objetivo:** no perder estado ni inventar acceso a herramientas.
- **Entregable:** ejecuciones interrumpidas, sin red, sin delegación y con fuentes parciales.
- **Aceptación:** continúa desde estado persistido y degrada de manera honesta, sin declarar frescura no comprobada.
- **Dep.:** 017, 045, 053.
- **Estado:** pendiente.

### Fase 055. Auditar seguridad del flujo de investigación
- **Objetivo:** bloquear instrucciones externas y filtraciones.
- **Entregable:** casos adversariales aislados, revisión de logs y límites de escritura.
- **Aceptación:** ningún texto externo amplía permisos ni copia secretos al expediente o AGENTS.
- **Dep.:** 009, 053, 054.
- **Estado:** pendiente.

### Fase 056. Registrar baseline y corregir fallos
- **Objetivo:** mejorar sin mover los criterios para aprobar.
- **Entregable:** baseline versionado, defectos, correcciones y nuevas ejecuciones.
- **Aceptación:** se repite caso fallido y regresión, y los resultados citan artefactos reales.
- **Dep.:** 052, 053, 054, 055.
- **Estado:** pendiente.

### Fase 057. Verificar portabilidad y descubrimiento
- **Objetivo:** instalar y cargar sin rutas personales ni supuestos de herramientas.
- **Entregable:** matriz de plataformas y prueba de carga en destinos disponibles.
- **Aceptación:** se verifica el perfil autorizado y no se promete una plataforma no probada.
- **Dep.:** 010, 046, 056.
- **Estado:** pendiente.

### Fase 058. Definir mantenimiento y cambios
- **Objetivo:** mantener fuentes, contratos y comportamiento revisables.
- **Entregable:** versionado, caducidad por riesgo, changelog y reglas de compatibilidad.
- **Aceptación:** cambiar una fuente crítica invalida las decisiones afectadas sin borrar historial.
- **Dep.:** 018, 045, 056.
- **Estado:** pendiente.

### Fase 059. Preparar release y guía de uso
- **Objetivo:** hacer reproducible la instalación y el primer caso.
- **Entregable:** paquete revisado, instrucciones verificadas y evidencia de pruebas.
- **Aceptación:** otro lector puede cargar la skill y repetir el flujo permitido con sus limitaciones documentadas.
- **Dep.:** 057, 058.
- **Estado:** pendiente.

### Fase 060. Aceptar núcleo estable
- **Objetivo:** cerrar la capacidad central completa.
- **Entregable:** release aprobado con checklist y riesgos residuales.
- **Aceptación:** todos los gates no compensables pasan, no hay defectos críticos abiertos y la pareja de documentos funciona en los casos exigidos.
- **Dep.:** 059.
- **Estado:** pendiente.

## 13. Catálogo de extensiones opcionales

No es una lista de trabajo comprometido. Cada fila requiere activación explícita, análisis de necesidad, fuentes propias y aceptación de su costo. El entregable de una extensión es un módulo o capacidad de planificación, no una app adicional. La detección de estos dominios ya pertenece al núcleo.

Todas las extensiones dependen del núcleo estable y, donde corresponde, de otra extensión anterior. Todas están pendientes y desactivadas por defecto. Ninguna puede bloquear 060.

| ID | Objetivo y activación | Entregable | Aceptación específica | Dep. |
| --- | --- | --- | --- | --- |
| 061 | Profundizar apps web cuando se solicite. | Playbook de renderizado y navegación. | Justifica SSR, cliente o estático sin imponerlos. | 060 |
| 062 | Profundizar macOS nativo. | Playbook de ventanas, archivos y distribución. | Incluye permisos, firma y aceptación nativa. | 060 |
| 063 | Profundizar iPhone. | Playbook de ciclo de vida y distribución. | Incluye dispositivo real y accesibilidad nativa. | 060 |
| 064 | Profundizar iPadOS. | Playbook de resize, teclado y escenas. | No reutiliza el documento de iPhone sin adaptación. | 063 |
| 065 | Profundizar Android. | Playbook de runtime y distribución. | Considera dispositivos, permisos y tareas de fondo. | 060 |
| 066 | Comparar móvil multiplataforma. | Matriz de capacidades y costo de puente nativo. | Reconoce límites de SDK y plugins. | 060 |
| 067 | Comparar escritorio multiplataforma. | Matriz de instalación y capacidades. | Explica costo operativo por sistema objetivo. | 060 |
| 068 | Planificar PWA. | Checklist de offline y distribución. | Distingue capacidades por navegador y plataforma. | 061 |
| 069 | Planificar extensiones de navegador. | Modelo de permisos y publicación. | Minimiza privilegios y documenta revisión de tienda. | 060 |
| 070 | Planificar CLI y TUI. | Contratos de entrada, salida y códigos. | Cubre automatización, accesibilidad y errores. | 060 |
| 071 | Profundizar sincronización local-first. | Playbook de conflictos y recuperación. | Incluye escenarios de partición y cambios concurrentes. | 060 |
| 072 | Profundizar edición colaborativa. | Evaluación de algoritmos y presencia. | Separa convergencia, persistencia y permisos. | 071 |
| 073 | Profundizar mensajería en tiempo real. | Contratos y estados de entrega. | No confunde envío, recepción y lectura. | 060 |
| 074 | Profundizar multimedia. | Pipeline de procesamiento y almacenamiento. | Cubre límites, formatos, costos y abusos. | 060 |
| 075 | Profundizar geolocalización y mapas. | Comparación de datos y proveedores. | Considera licencias, privacidad y offline. | 060 |
| 076 | Profundizar búsqueda textual. | Plan de ranking, indexación y evaluación. | Define corpus y criterios medibles de relevancia. | 060 |
| 077 | Profundizar búsqueda semántica. | Comparación de representaciones e índices. | Separa calidad, costo y latencia con corpus real. | 076 |
| 078 | Profundizar IA generativa. | Matriz de proveedores, modelos y evaluación. | Cubre privacidad, límites y fallos de salida. | 060 |
| 079 | Profundizar RAG. | Contratos de ingesta, recuperación y citas. | No confunde archivo subido con documento indexado. | 077, 078 |
| 080 | Profundizar agentes con herramientas. | Modelo de permisos y evaluación de acciones. | Prueba escalamiento, cancelación y auditoría. | 078 |
| 081 | Profundizar entrenamiento de modelos. | Plan de datos, evaluación y cómputo. | Justifica entrenamiento frente a alternativas. | 060 |
| 082 | Profundizar analítica de producto. | Taxonomía de eventos y consentimiento. | Evita PII y distingue medición de causalidad. | 060 |
| 083 | Profundizar procesamiento batch. | Plan de jobs, reintentos y checkpoints. | Define reanudación y reconciliación. | 060 |
| 084 | Profundizar streaming de datos. | Modelo temporal y contratos de eventos. | Explicita orden, duplicados y datos tardíos. | 060 |
| 085 | Profundizar pagos. | Flujo de cobro, conciliación y webhooks. | Cubre idempotencia y revisión de alcance sensible. | 060 |
| 086 | Profundizar suscripciones. | Estados de facturación y derechos. | No confunde pago confirmado con permiso permanente. | 085 |
| 087 | Profundizar marketplaces. | Reglas de participantes, disputas y liquidación. | Identifica responsabilidades y riesgos jurisdiccionales. | 085 |
| 088 | Profundizar comercio electrónico. | Inventario, pedidos y recuperación. | Define consistencia entre reserva y cobro. | 085 |
| 089 | Profundizar notificaciones. | Canales, preferencias y deduplicación. | Respeta consentimiento y registra fallo de entrega. | 060 |
| 090 | Profundizar email transaccional. | Plantillas, reputación y operación. | Incluye rebotes, supresión y seguridad. | 089 |
| 091 | Profundizar archivos y documentos. | Pipeline de subida y procesamiento. | Cubre validación, cuotas, malware y eliminación. | 060 |
| 092 | Profundizar importación y exportación. | Contratos de formato y portabilidad. | Prueba integridad, errores parciales y reintentos. | 091 |
| 093 | Profundizar SaaS multi-tenant. | Matriz de aislamiento y administración. | Incluye pruebas negativas entre tenants. | 060 |
| 094 | Profundizar identidad empresarial. | Matriz de federación y aprovisionamiento. | Separa autenticación de autorización. | 093 |
| 095 | Profundizar auditoría regulada. | Modelo de evidencias y retención. | No promete inmutabilidad sin mecanismo verificable. | 093 |
| 096 | Profundizar salud. | Checklist de datos y revisión competente. | No declara certificación a partir de documentación. | 060 |
| 097 | Profundizar finanzas. | Checklist de integridad y riesgo. | Identifica autorización y reconciliación. | 060 |
| 098 | Profundizar educación y menores. | Checklist de consentimiento y protección. | Distingue edad, jurisdicción y acceso de tutores. | 060 |
| 099 | Profundizar sector público. | Checklist de contratación y accesibilidad. | Verifica condiciones de la jurisdicción concreta. | 060 |
| 100 | Profundizar residencia de datos. | Matriz de regiones y subprocesadores. | Verifica almacenamiento, backups y transferencias. | 060 |
| 101 | Planificar infraestructura como código. | Comparación y contratos de aprovisionamiento. | Exige permisos y costo antes de aplicar cambios. | 060 |
| 102 | Profundizar contenedores. | Plan de imágenes, runtime y soporte. | Justifica su uso y límites de aislamiento. | 060 |
| 103 | Evaluar orquestación de clúster. | Matriz de necesidad y carga operativa. | Puede recomendar o descartar con requisitos medibles. | 102 |
| 104 | Profundizar serverless. | Matriz de límites, arranque y costo. | Calcula escenarios y evita supuestos de costo cero. | 060 |
| 105 | Profundizar operación autogestionada. | Runbook de actualización y recuperación. | Identifica responsable y capacidad operativa. | 060 |
| 106 | Profundizar despliegue multirregión. | Estrategia de datos, tráfico y recuperación. | Aclara consistencia y costo de particiones. | 060 |
| 107 | Profundizar observabilidad. | Plan de cardinalidad, retención y costo. | Evita secretos y datos personales en telemetría. | 060 |
| 108 | Profundizar ingeniería de capacidad. | Modelo de carga y saturación. | Diferencia estimación de benchmark real. | 107 |
| 109 | Profundizar pruebas de rendimiento. | Escenarios y método reproducible. | Define entorno, percentiles y carga autorizada. | 108 |
| 110 | Profundizar recuperación ante desastre. | Plan de restore y simulación. | Prueba RPO y RTO sobre escenarios aprobados. | 060 |
| 111 | Profundizar entrega segura. | Gates de CI y cadena de suministro. | Explica firma, revisión y confianza de artefactos. | 060 |
| 112 | Profundizar seguridad móvil. | Checklist específico de plataforma. | No reutiliza controles web como cobertura completa. | 060 |
| 113 | Profundizar seguridad de APIs. | Modelo de abuso y contratos. | Incluye autorización por recurso y límites. | 060 |
| 114 | Profundizar modelado de amenazas. | Sesiones y registro de mitigaciones. | Traza amenaza a control y caso de prueba. | 060 |
| 115 | Profundizar privacidad. | Mapa de datos y evaluación de impacto. | Escala dudas legales y minimiza recopilación. | 114 |
| 116 | Profundizar dependencias y SBOM. | Inventario y política de remediación. | No confunde inventario con ausencia de vulnerabilidades. | 111 |
| 117 | Profundizar pruebas de accesibilidad. | Matriz manual y automatizada. | Incluye tecnología asistiva y alcance real. | 060 |
| 118 | Profundizar internacionalización. | Plan de idioma, locale y formatos. | Cubre zonas horarias, expansión y RTL cuando aplique. | 060 |
| 119 | Profundizar diseño de sistemas visuales. | Política de tokens y componentes. | Justifica accesibilidad y mantenimiento sin crear UI no pedida. | 060 |
| 120 | Profundizar documentación de APIs. | Contratos y validación de ejemplos. | Diferencia ejemplos propuestos de endpoints existentes. | 060 |
| 121 | Optimizar investigación por presupuesto. | Políticas de costo y cobertura. | Mantiene gates críticos al reducir búsquedas. | 060 |
| 122 | Cachear fuentes con trazabilidad. | Caché con versión y caducidad. | No presenta una copia antigua como consulta actual. | 121 |
| 123 | Detectar cambios de fuentes. | Diff y decisiones afectadas. | Actualiza dependencias sin reescribir decisiones ajenas. | 122 |
| 124 | Detectar fin de soporte. | Alertas documentadas y plan de revisión. | Verifica edición y versión, no solo nombre del producto. | 123 |
| 125 | Ampliar investigación de incidentes conocidos. | Dossier de issues y limitaciones. | Distingue reportes comunitarios de hechos reproducidos. | 060 |
| 126 | Evaluar benchmarks externos. | Ficha de metodología y comparabilidad. | Rechaza comparaciones entre cargas incompatibles. | 125 |
| 127 | Hacer spikes autorizados reproducibles. | Plantilla de experimento y limpieza. | Requiere permiso, límite y evidencia de eliminación. | 060 |
| 128 | Incorporar datos de proyectos anteriores. | Biblioteca anonimizada de decisiones. | No transfiere secretos ni preferencias sin confirmar. | 060 |
| 129 | Detectar deriva de decisiones. | Auditoría incremental de ADR. | Señala impacto y requiere reaprobación donde corresponda. | 123 |
| 130 | Comparar revisiones de planes. | Diff semántico de alcance y riesgo. | Conserva IDs y explica cambios de aceptación. | 129 |
| 131 | Exportar a gestores de tareas. | Adaptador de tareas y dependencias. | Previsualiza, pide permiso y verifica lectura posterior. | 060 |
| 132 | Exportar a GitHub Issues. | Adaptador con mapeo y deduplicación. | No publica ni duplica issues sin autorización. | 131 |
| 133 | Exportar a Linear. | Adaptador con contratos de campos. | Verifica proyecto, permisos y lectura del destino. | 131 |
| 134 | Exportar a Notion. | Adaptador de páginas y relaciones. | Distingue Markdown generado de publicación real. | 131 |
| 135 | Exportar a Obsidian. | Enlaces y estructura de vault. | Preserva notas existentes y valida vínculos locales. | 131 |
| 136 | Exportar a PDF. | Documento legible y auditable. | Conserva referencias y no sustituye el Markdown fuente. | 060 |
| 137 | Exportar diagramas editables. | Formato interoperable bajo demanda. | El diagrama coincide con los contratos aprobados. | 060 |
| 138 | Integrar contratos OpenAPI. | Importación y validación de esquema. | No considera un esquema prueba del servidor real. | 120 |
| 139 | Integrar contratos de eventos. | Esquemas y revisión de evolución. | Detecta breaking changes y consumidores afectados. | 084 |
| 140 | Integrar repositorios existentes. | Auditoría profunda de convenciones. | Propone cambios mínimos y no cambia stack por costumbre. | 060 |
| 141 | Ampliar corpus de evaluación. | Casos adicionales versionados. | No modifica expectativas para aprobar salidas existentes. | 060 |
| 142 | Comparar modelos de planificación. | Ejecuciones ciegas bajo protocolo común. | Registra costo, fuentes y límites de comparabilidad. | 141 |
| 143 | Medir estabilidad entre ejecuciones. | Ensayos repetidos y variación. | Distingue diversidad válida de contradicción. | 142 |
| 144 | Evaluar legibilidad humana. | Revisión por lectores y tareas. | Mide hallazgo de primera tarea y bloqueos. | 141 |
| 145 | Evaluar agentes implementadores. | Handoff controlado con fixtures. | No confunde comprensión del plan con app terminada. | 141 |
| 146 | Agregar revisión especializada. | Roles opcionales con contratos de revisión. | No fabrica consenso ni oculta desacuerdos. | 060 |
| 147 | Agregar planificación de equipos. | Propiedad, dependencias y coordinación. | No inventa disponibilidad ni compromisos de personas. | 060 |
| 148 | Profundizar estimación y simulación. | Rangos y escenarios reproducibles. | Expone incertidumbre y evita fechas garantizadas. | 147 |
| 149 | Preparar distribución compartida. | Paquete con licencia y revisión de datos. | Publicación exige permiso y verificación del destino. | 060 |
| 150 | Revisar evolución de largo plazo. | Balance de evidencia y backlog depurado. | Elimina módulos sin uso y revalida alcance futuro. | 149 |

## 14. Verificación, riesgos y Definition of Done

### 14.1 Niveles de comprobación

1. **Documental:** estructura, enlaces, IDs, dependencias, citas y contratos.
2. **Determinista:** validadores con fixtures válidos y defectuosos, sin red en pruebas unitarias.
3. **Conductual:** ejecutar la skill con casos de [tests.md](tests.md), conservar conversaciones y salidas.
4. **Semántica:** revisión humana o independiente de restricciones, evidencia y utilidad.
5. **Operacional:** instalación y carga reales solo cuando se implemente y autorice.

Un nivel no sustituye al siguiente. Esta entrega documental no certifica los niveles conductual u operacional.

### 14.2 Riesgos principales

| Riesgo | Prevención | Señal de detección | Respuesta |
| --- | --- | --- | --- |
| Elegir stack antes de entender la idea. | Gate de completitud y universo abierto. | Candidatos aparecen antes de VAR críticas. | Volver a descubrimiento. |
| Sobreingeniería. | Arquitectura por drivers y operación. | Componentes sin requisito ni prueba. | Eliminar o justificar con aprobación. |
| Simplicidad incompatible. | Filtros excluyentes antes de scoring. | Se descarta una necesidad confirmada por comodidad. | Restaurar restricción y reevaluar. |
| Fuentes viejas o incorrectas. | Versión, editor y estado de acceso. | Docs de versión distinta o página de error. | Reinvestigar y bloquear afirmaciones afectadas. |
| Puntuaciones aparentes. | Escala, incertidumbre y sensibilidad. | Ganador cambia con pesos plausibles. | Declarar empate o hacer spike. |
| Costos subestimados. | Escenarios y unidades explícitas. | Solo se considera hosting base. | Recalcular costo total. |
| Investigación infinita. | Preguntas y criterio de detención. | Búsquedas sin impacto decisional. | Cerrar cobertura y registrar residual. |
| Documentos contradictorios. | Fuente de verdad y revisión conjunta. | Comandos o tecnologías divergen. | Corregir ambos, no cerrar la pareja parcial. |
| Ejecuciones inventadas. | Estados separados y evidencia real. | PASS sin artefacto ni comando. | Invalidar aceptación y registrar defecto. |
| Contexto excesivo. | AGENTS operativo y expediente separado. | Reglas críticas quedan truncadas. | Reducir y enlazar sin perder requisitos. |
| Permisos ampliados por fuentes. | Frontera de confianza y allowlist de efectos. | Página o repositorio ordena acciones ajenas. | Tratarlo como dato y suspender el efecto. |

### 14.3 Definition of Done del núcleo

- [ ] SKILL.md y referencias implementados, con versiones y metadatos válidos.
- [ ] Entrevista adaptativa y gate de completitud ejercitados.
- [ ] Universo de candidatos, filtros y compatibilidad probados.
- [ ] Fuentes reales utilizadas en decisiones y prácticas.
- [ ] Comparaciones y costos calculados con herramientas.
- [ ] Producto, arquitectura y trazabilidad coherentes.
- [ ] Roadmap y AGENTS generados y revisados como pareja.
- [ ] Validadores positivos y negativos ejecutados.
- [ ] Corpus conductual ejecutado, con gates críticos aprobados.
- [ ] Baseline, regresión, riesgos y bloqueos conservados.
- [ ] Carga e instalación verificadas en el perfil autorizado.
- [ ] Release y publicación, si existen, autorizados y leídos de vuelta.

## 15. Orden recomendado para empezar

Implementar primero 001–010 y probar que la skill pregunta y bloquea correctamente antes de sofisticar comparaciones. Después cubrir 011–030 con un caso simple y uno contradictorio. Completar arquitectura y generación antes de la beta. No empezar el catálogo 061–150 hasta aprobar 060 y justificar qué módulo aporta valor al uso real.

## Sources

[1] https://hermes-agent.nousresearch.com/docs/developer-guide/creating-skills
[2] https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files
[3] https://hermes-agent.nousresearch.com/docs/user-guide/features/skills
[4] https://agents.md
[5] https://owasp.org/www-project-application-security-verification-standard
[6] https://www.w3.org/TR/WCAG22
[7] https://csrc.nist.gov/pubs/sp/800/218/final
[8] https://sre.google/workbook/implementing-slos
[9] https://c4model.com
