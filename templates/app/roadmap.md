# Roadmap de {{PROJECT_NAME}}

> PLANTILLA EDITORIAL. No es un proyecto definido ni una decisión técnica aprobada. La skill debe completar los marcadores, investigar las decisiones y retirar este aviso al generar el documento final. No presentar esta plantilla sin completar como lista para implementar.

**Identificador del proyecto:** {{PROJECT_ID}}.
**Versión del plan y contrato:** {{PLAN_VERSION}}.
**Fecha y zona horaria:** {{PREPARED_AT}}.
**Responsable de producto y aprobaciones:** {{OWNER}}.
**Estado:** {{DRAFT_OR_BLOCKED_OR_READY_FOR_IMPLEMENTATION}}.
**Modalidad de la ejecución:** {{SESSION_MODE}}.
**Profundidad acordada:** {{RESEARCH_DEPTH}}.
**Repositorio y situación inicial:** {{REPOSITORY_OR_GREENFIELD_STATUS}}.
**Expediente de decisiones:** [expediente.md](expediente.md).
**Reglas del repositorio:** [AGENTS.md](AGENTS.md).

El estado listo para implementación solo es alcanzable en la modalidad de planificación con profundidad exhaustiva, y sigue sin ser permiso de ejecución. Registrar también la fecha y el responsable de la decisión de modalidad y profundidad.

## 1. Resumen ejecutivo

- **Problema:** {{PROBLEM_AND_CURRENT_WORKAROUND}}.
- **Usuarios prioritarios:** {{PRIMARY_USERS_AND_CONTEXT}}.
- **Resultado que se busca:** {{OBSERVABLE_USER_OUTCOME}}.
- **Propuesta de valor:** {{VALUE_PROPOSITION}}.
- **Primera versión útil:** {{MVP_END_TO_END_RESULT}}.
- **Estrategia recomendada:** {{BUILD_BUY_INTEGRATE_VALIDATE_AND_REASON}}.
- **Decisiones aceptadas:** {{ACCEPTED_DECISION_IDS_OR_NONE}}.
- **Decisiones pendientes:** {{PENDING_DECISION_IDS_AND_IMPACT}}.
- **Bloqueos:** {{BLOCKERS_OR_EXPLICIT_NONE}}.

No sustituir este resumen por una lista de frameworks. Distinguir hechos confirmados y objetivos propuestos.

## 2. Contexto, restricciones y supuestos

### 2.1 Restricciones confirmadas

| ID VAR | Restricción exacta | Fuente o respuesta | Impacto | Estado |
| --- | --- | --- | --- | --- |
| {{VAR_ID}} | {{CONFIRMED_CONSTRAINT}} | {{SOURCE_OR_USER_ANSWER}} | {{AFFECTED_DECISIONS}} | {{VARIABLE_STATE}} |

Incluir plataforma, presupuesto, equipo, plazos reales, privacidad, conectividad, licencias, operación y tecnologías impuestas cuando correspondan. No transformar preferencias en restricciones excluyentes sin confirmación.

### 2.2 Supuestos aceptados

| ID | Supuesto | Quién lo aceptó y cuándo | Riesgo si cambia | Revisión |
| --- | --- | --- | --- | --- |
| {{ASSUMPTION_ID}} | {{EXPLICIT_ASSUMPTION}} | {{APPROVAL_EVIDENCE}} | {{IMPACT}} | {{REVIEW_TRIGGER}} |

### 2.3 Preguntas y contradicciones pendientes

| ID | Pregunta o contradicción | Decisión bloqueada | Responsable | Condición de resolución |
| --- | --- | --- | --- | --- |
| {{OPEN_ITEM_ID}} | {{OPEN_QUESTION}} | {{BLOCKED_DECISION}} | {{OWNER}} | {{REQUIRED_ANSWER_OR_EVIDENCE}} |

Un plan puede entregarse como borrador si quedan preguntas, pero no declararse listo cuando esas preguntas cambien seguridad, elegibilidad, costo comprometido o alcance esencial.

## 3. Usuarios y casos de uso

### 3.1 Actores y permisos de alto nivel

| Actor | Necesidad | Recursos propios y compartidos | Acciones permitidas | Acciones denegadas |
| --- | --- | --- | --- | --- |
| {{ACTOR_ID}} | {{USER_NEED}} | {{RESOURCE_OWNERSHIP}} | {{PERMITTED_ACTIONS}} | {{FORBIDDEN_ACTIONS}} |

### 3.2 Ficha de caso de uso, repetir por cada uso relevante

**UC:** {{UC_ID_AND_TITLE}}.
- **Actor y contexto:** {{ACTOR_AND_CONTEXT}}.
- **Objetivo:** {{USER_GOAL}}.
- **Precondiciones y permisos:** {{PRECONDITIONS}}.
- **Entrada o disparador:** {{TRIGGER}}.
- **Camino principal:** {{NUMBERED_MAIN_FLOW}}.
- **Errores y alternativas:** {{FAILURE_AND_ALTERNATIVE_FLOWS}}.
- **Resultado y postcondiciones:** {{OBSERVABLE_RESULT}}.
- **Datos afectados:** {{DATA_AND_RETENTION}}.
- **Aceptación positiva:** {{POSITIVE_OBSERVABLE_CASE}}.
- **Aceptación negativa:** {{NEGATIVE_PERMISSION_OR_FAILURE_CASE}}.

## 4. Funcionalidades, reglas y alcance

### 4.1 Catálogo de features

| ID FEAT | Funcionalidad y valor | UC y FR vinculados | Prioridad y razón | MVP o posterior | Dependencias |
| --- | --- | --- | --- | --- | --- |
| {{FEATURE_ID}} | {{FEATURE_AND_VALUE}} | {{REQUIREMENT_IDS}} | {{PRIORITY_AND_REASON}} | {{SCOPE_STAGE}} | {{FEATURE_DEPENDENCIES}} |

### 4.2 Requisitos funcionales y reglas

| ID FR o BR | Comportamiento o invariante | Condición | Resultado esperado | Prueba de aceptación |
| --- | --- | --- | --- | --- |
| {{REQUIREMENT_ID}} | {{REQUIRED_BEHAVIOR}} | {{INPUT_OR_PRECONDITION}} | {{OBSERVABLE_OUTPUT}} | {{TEST_ID}} |

### 4.3 MVP

- **Recorridos completos incluidos:** {{MVP_JOURNEYS}}.
- **Usuarios y plataformas del primer lanzamiento:** {{INITIAL_AUDIENCE_AND_PLATFORMS}}.
- **Datos e integraciones indispensables:** {{MVP_DATA_AND_INTEGRATIONS}}.
- **Resultado mínimo verificable:** {{MVP_DEMONSTRATION}}.
- **Límites aceptados:** {{MVP_LIMITS}}.
- **Lo que no se puede diferir:** {{CRITICAL_SECURITY_QUALITY_AND_FUNCTIONS}}.

### 4.4 Fuera de alcance

| Elemento excluido | Razón | Consecuencia | Disparador para reconsiderar |
| --- | --- | --- | --- |
| {{EXCLUDED_CAPABILITY}} | {{EXCLUSION_REASON}} | {{ACCEPTED_CONSEQUENCE}} | {{REVISIT_TRIGGER}} |

No llamar extensión a una capacidad explícitamente necesaria para el producto aprobado.

## 5. Requisitos no funcionales

| ID NFR | Atributo y recorrido | Métrica y unidad | Objetivo y estado | Carga, ventana o entorno | Medición y aceptación |
| --- | --- | --- | --- | --- | --- |
| {{NFR_ID}} | {{QUALITY_ATTRIBUTE}} | {{METRIC_AND_UNIT}} | {{TARGET_AND_APPROVAL_STATE}} | {{MEASUREMENT_CONDITIONS}} | {{TEST_METHOD_AND_TEST_ID}} |

Examinar rendimiento, disponibilidad, durabilidad, recuperación, seguridad, privacidad, accesibilidad, operabilidad, mantenibilidad, portabilidad y costos. Justificar no aplicación. No inventar percentiles ni disponibilidad objetivo sin relación con necesidades y presupuesto.

## 6. Estrategia y evaluación tecnológica

### 6.1 Estrategias consideradas

| Estrategia | Qué valida o resuelve | Ventajas | Costos y límites | Elegibilidad y evidencia |
| --- | --- | --- | --- | --- |
| {{SOLUTION_STRATEGY}} | {{STRATEGY_PURPOSE}} | {{BENEFITS}} | {{TRADEOFFS}} | {{ELIGIBILITY_AND_SOURCES}} |

Comparar construcción, integración, compra, prototipo y piloto cuando sean opciones relevantes. Explicar evolución y descarte de componentes temporales.

### 6.2 Universo, exclusiones y finalistas

- **Familias investigadas:** {{CANDIDATE_FAMILIES_AND_SEARCH_COVERAGE}}.
- **Restricciones excluyentes:** {{HARD_FILTERS_AND_VAR_IDS}}.
- **Candidatos descartados:** {{EXCLUDED_CANDIDATES_AND_EVIDENCE}}.
- **Finalistas viables:** {{ELIGIBLE_FINALISTS}}.
- **Opciones pendientes de evidencia:** {{UNCERTAIN_CANDIDATES}}.

| Criterio | Peso | Escala anclada | Evidencia necesaria |
| --- | --- | --- | --- |
| {{CRITERION_ID}} | {{NUMERIC_WEIGHT}} | {{SCORING_ANCHORS}} | {{EVIDENCE_REQUIREMENT}} |

**Cálculo:** {{CALCULATED_COMPARISON_AND_METHOD}}.
**Sensibilidad:** {{WEIGHT_AND_SCENARIO_SENSITIVITY}}.
**Incertidumbre y empates:** {{UNCERTAINTY_AND_TIE_HANDLING}}.
**Por qué se recomienda esta opción:** {{REQUIREMENT_LINKED_REASONING}}.

Mantener los datos completos en el expediente. No inventar puntuaciones para llenar una tabla.

### 6.3 Stack propuesto o aprobado

| Capa o responsabilidad | Tecnología y edición | Versión objetivo | Estado de decisión | Justificación y ADR | Documentación oficial |
| --- | --- | --- | --- | --- | --- |
| {{STACK_RESPONSIBILITY}} | {{TECH_AND_EDITION}} | {{TARGET_VERSION}} | {{DECISION_STATE}} | {{ADR_ID_AND_REASON}} | {{OFFICIAL_VERSIONED_SOURCE}} |

No agregar una herramienta por cada capa si la solución no lo requiere. Una app local puede no necesitar backend. Un servicio sin interfaz no necesita framework frontend.

### 6.4 Compatibilidad

| Combinación | Fuente específica | Estado documental o probado | Limitaciones | Acción pendiente |
| --- | --- | --- | --- | --- |
| {{RUNTIME_FRAMEWORK_SDK_DEPLOYMENT_TUPLE}} | {{COMPATIBILITY_SOURCE}} | {{DOCUMENTED_INFERRED_TESTED_BLOCKED}} | {{KNOWN_LIMITS}} | {{ACTION_OR_EXPLICIT_NONE}} |

### 6.5 Prácticas derivadas de documentación

| Regla concreta | Dónde aplica | Motivo y fuente | Excepción aprobada | Tarea o prueba |
| --- | --- | --- | --- | --- |
| {{TECHNICAL_RULE}} | {{TARGET_CONTEXT}} | {{REASON_AND_SOURCE}} | {{EXCEPTION_OR_NONE}} | {{PHASE_OR_TEST}} |

### 6.6 Costos

| Concepto | Unidad y tarifa | Fuente, región y moneda | Escenario inicial | Escenario esperado | Escenario de crecimiento |
| --- | --- | --- | --- | --- | --- |
| {{COST_ITEM}} | {{RATE_AND_UNIT}} | {{PRICING_PROVENANCE}} | {{CALCULATED_INITIAL_COST}} | {{CALCULATED_EXPECTED_COST}} | {{CALCULATED_GROWTH_COST}} |

**Horizonte:** {{COST_HORIZON}}.
**Únicos frente a recurrentes:** {{ONE_TIME_AND_RECURRING_SPLIT}}.
**Incluidos y excluidos:** {{TAXES_LABOR_FREE_TIERS_AND_EXCLUSIONS}}.
**Fecha de revalidación:** {{PRICING_REVIEW_TRIGGER}}.

## 7. Arquitectura

### 7.1 Estilo y razones

**Estilo seleccionado o propuesto:** {{ARCHITECTURAL_STYLE_AND_STATUS}}.
**Drivers:** {{LINKED_FR_NFR_AND_CONSTRAINTS}}.
**Alternativas y consecuencias:** {{ARCHITECTURAL_ALTERNATIVES_AND_ADR}}.
**Por qué no basta una opción más simple o distinta:** {{PROPORTIONALITY_ARGUMENT}}.

Separar modularización interna, protocolo de interacción y despliegue. No justificar microservicios con crecimiento hipotético ni descartarlos si una restricción confirmada los requiere.

### 7.2 Componentes y límites

| Componente | Propósito | Interfaz y contrato | Datos que posee | Permisos y secretos | Fallo y recuperación |
| --- | --- | --- | --- | --- | --- |
| {{COMPONENT_ID}} | {{RESPONSIBILITY}} | {{INTERFACE_AND_VERSION}} | {{OWNED_DATA}} | {{PRIVILEGE_BOUNDARY}} | {{FAILURE_POLICY}} |

**Diagrama de contexto o contenedores:** {{CONCRETE_DIAGRAM_OR_LINK}}.
**Flujo principal de datos:** {{END_TO_END_DATA_FLOW}}.
**Confirmaciones:** {{RECEIVED_ACCEPTED_COMMITTED_OBSERVED_STATES}}.
**Puntos de confianza:** {{TRUST_BOUNDARIES}}.

### 7.3 Modelo de datos

| Entidad | Identificador y propietario | Relaciones | Invariantes | Retención y eliminación |
| --- | --- | --- | --- | --- |
| {{ENTITY_NAME}} | {{ID_AND_OWNER}} | {{RELATIONSHIPS}} | {{BUSINESS_INVARIANTS}} | {{RETENTION_POLICY}} |

Definir transacciones, consistencia, concurrencia, zonas horarias, índices requeridos por consultas, migraciones y recuperación. Distinguir esquema propuesto de esquema existente inspeccionado.

### 7.4 Contratos e integraciones

| Contrato | Productor y consumidor | Versión | Entrada, salida y errores | Seguridad | Límites, reintentos y fallo |
| --- | --- | --- | --- | --- | --- |
| {{CONTRACT_ID}} | {{PARTIES}} | {{CONTRACT_VERSION}} | {{MESSAGE_OR_API_SHAPE}} | {{AUTHORIZATION_RULE}} | {{RETRY_AND_DEGRADATION}} |

Los endpoints, eventos y rutas nuevas deben marcarse como propuestas. Especificar paginación, idempotencia, deduplicación y cancelación solo donde sean pertinentes.

## 8. UX, seguridad, privacidad y accesibilidad

### 8.1 UX

- **Navegación y organización:** {{NAVIGATION_MODEL}}.
- **Estados de carga, vacío, error y recuperación:** {{UI_STATES}}.
- **Acciones destructivas y confirmación:** {{DESTRUCTIVE_ACTION_POLICY}}.
- **Adaptaciones por plataforma:** {{PLATFORM_SPECIFIC_ACCEPTANCE}}.
- **Validación con usuarios:** {{REAL_RESEARCH_OR_PROPOSED_VALIDATION}}.

### 8.2 Amenazas y controles

| Amenaza o abuso | Activo y frontera | Control | Responsable | Prueba negativa y evidencia |
| --- | --- | --- | --- | --- |
| {{THREAT_ID}} | {{ASSET_AND_BOUNDARY}} | {{MITIGATION}} | {{CONTROL_OWNER}} | {{NEGATIVE_TEST}} |

Cubrir según aplicación autenticación, autorización por recurso, aislamiento, entradas no confiables, secretos, cifrado, auditoría y dependencias. No afirmar que cifrado reemplaza autorización ni que una red nominal prueba aislamiento.

### 8.3 Privacidad y revisión especializada

**Datos personales y sensibilidad:** {{DATA_CLASSIFICATION}}.
**Residencia y terceros:** {{DATA_REGIONS_AND_PROCESSORS}}.
**Minimización, retención y borrado:** {{DATA_LIFECYCLE}}.
**Exportación y portabilidad:** {{USER_DATA_EXPORT}}.
**Jurisdicciones y revisión necesaria:** {{LEGAL_REVIEW_SCOPE_AND_LIMITS}}.

### 8.4 Accesibilidad

**Objetivo y alcance:** {{ACCESSIBILITY_TARGET}}.
**Guías oficiales y versión:** {{PLATFORM_ACCESSIBILITY_SOURCES}}.
**Pruebas manuales y automatizadas:** {{ACCESSIBILITY_TEST_MATRIX}}.
**Limitaciones:** {{KNOWN_ACCESSIBILITY_GAPS}}.

No declarar conformidad por pasar una sola herramienta automatizada.

## 9. Módulos condicionales

| Módulo examinado | Activado o no aplicable | Requisito y razón | Riesgos especiales | Prueba y fuente |
| --- | --- | --- | --- | --- |
| {{AI_PAYMENTS_OFFLINE_REALTIME_FILES_TENANCY_OR_OTHER}} | {{MODULE_STATE}} | {{ACTIVATION_REQUIREMENT_OR_EXCLUSION_REASON}} | {{SPECIAL_RISKS}} | {{SPECIALIZED_TESTS_AND_SOURCES}} |

Para IA examinar calidad, costo, privacidad, comportamiento no determinista y límites de acción. Para pagos examinar idempotencia y conciliación. Para offline definir conflicto y sincronización. No agregar estas capacidades si no aportan al producto aprobado.

## 10. Estructura y herramientas de desarrollo

**Estructura propuesta o inspeccionada:** {{REPOSITORY_TREE_AND_REALITY_STATUS}}.
**Gestor de dependencias y lockfile:** {{PACKAGE_MANAGER_AND_LOCKFILE}}.
**Estilo, tipos y análisis estático:** {{STYLE_AND_STATIC_CHECKS}}.
**Ambiente local y versiones:** {{LOCAL_ENVIRONMENT}}.
**Convenciones de contratos y errores:** {{CONTRACT_AND_ERROR_CONVENTIONS}}.

| Comando | Propósito | Directorio | Prerequisitos y efectos | Estado y evidencia |
| --- | --- | --- | --- | --- |
| {{EXACT_COMMAND_OR_BLOCKED}} | {{COMMAND_PURPOSE}} | {{WORKING_DIRECTORY}} | {{REQUIREMENTS_AND_SIDE_EFFECTS}} | {{PROPOSED_DOCUMENTED_EXECUTED_WITH_EVIDENCE}} |

No dejar comandos vacíos en un plan listo para una fase que necesita ejecutarlos. Si aún requieren implementación, incluir una tarea previa que cree y pruebe la interfaz.

## 11. Estrategia de pruebas

| ID TEST | FR, BR, UC o NFR | Nivel | Caso positivo | Caso negativo o límite | Entorno y datos | Evidencia exigida |
| --- | --- | --- | --- | --- | --- | --- |
| {{TEST_ID}} | {{COVERED_REQUIREMENTS}} | {{TEST_LEVEL}} | {{POSITIVE_CASE}} | {{NEGATIVE_OR_BOUNDARY_CASE}} | {{TEST_ENVIRONMENT}} | {{EVIDENCE_ARTIFACT}} |

Seleccionar pruebas unitarias, integración, contratos, E2E, seguridad, accesibilidad, rendimiento y recuperación por riesgo. No presentar un mock como prueba del proveedor real ni un esquema como prueba de un servidor implementado.

## 12. Despliegue, operación y recuperación

- **Ambientes y responsables:** {{ENVIRONMENTS_AND_OWNERS}}.
- **Configuración y secretos:** {{CONFIGURATION_BOUNDARIES}}.
- **CI y gates:** {{CI_CHECKS_AND_APPROVALS}}.
- **Migraciones:** {{MIGRATION_PLAN}}.
- **Despliegue y rollback:** {{DEPLOY_AND_ROLLBACK}}.
- **Logs, métricas y trazas:** {{OBSERVABILITY_WITH_DATA_LIMITS}}.
- **SLO e indicadores:** {{SLO_AND_MEASUREMENT}}.
- **Backups y restauración:** {{BACKUP_AND_RESTORE_TEST}}.
- **RPO y RTO, si aplican:** {{RECOVERY_TARGETS_AND_APPROVAL}}.
- **Degradación ante dependencias caídas:** {{DEGRADED_MODE}}.
- **Costos y alertas:** {{COST_GUARDRAILS}}.
- **Actualización de dependencias:** {{UPDATE_POLICY}}.

Estas instrucciones no autorizan desplegar ni crear recursos facturables.

## 13. Hitos y fases

### 13.1 Índice de hitos

| Hito | Resultado funcional | Fases incluidas | Criterio de salida | Dependencias externas |
| --- | --- | --- | --- | --- |
| {{MILESTONE_ID}} | {{USABLE_RESULT}} | {{PHASE_RANGE}} | {{MILESTONE_ACCEPTANCE}} | {{PROJECT_AND_VERSION_OR_NONE}} |

La cantidad y numeración de fases se ajusta al proyecto. No copiar automáticamente las 150 fases de la skill ni fijar beta o estabilidad en números arbitrarios. Conservar convenciones existentes si el usuario las ha aprobado.

### 13.2 Ficha obligatoria de fase, repetir hasta cubrir el alcance

### Fase {{PHASE_ID}}. {{PHASE_TITLE}}

**Estado:** pendiente.
**Objetivo:** {{PHASE_OUTCOME}}.
**Valor o riesgo que aborda:** {{VALUE_OR_RISK}}.
**Requisitos:** {{UC_FR_BR_FEAT_NFR_IDS}}.
**Decisiones aplicables:** {{ADR_IDS}}.
**Dependencias internas:** {{EARLIER_PHASE_IDS_OR_NONE}}.
**Dependencias externas:** {{EXTERNAL_PROJECT_CONTRACT_VERSION_OR_NONE}}.
**Definition of Ready:** {{REQUIRED_DECISIONS_DATA_AND_TOOLS}}.
**Rutas reales o propuestas:** {{FILE_PATHS_AND_STATUS}}.

**Trabajo:**
- [ ] {{SMALL_CONCRETE_TASK_1}}.
- [ ] {{SMALL_CONCRETE_TASK_2}}.
- [ ] {{TEST_AND_REVIEW_TASK}}.

**Entregable:** {{CONCRETE_ARTIFACT_OR_BEHAVIOR}}.
**Aceptación positiva:** {{OBSERVABLE_SUCCESS_CASE}}.
**Aceptación negativa y límites:** {{FAILURE_PERMISSION_BOUNDARY_CASES}}.
**Verificación:** {{EXACT_REAL_COMMAND_OR_REQUIRED_VALIDATION_METHOD}}.
**Evidencia que debe conservarse:** {{OUTPUT_LOG_SCREENSHOT_READBACK_OR_REPORT}}.
**Riesgo y mitigación:** {{PHASE_RISK_AND_RESPONSE}}.
**Recuperación o reversión:** {{ROLLBACK_OR_RECOVERY}}.
**Condición de cierre:** {{ALL_ACCEPTANCE_CRITERIA_AND_REQUIRED_APPROVAL}}.

No marcar tareas completadas al escribir el plan. Si se conoce una ruta pero no sus líneas, no inventar referencias de línea. Separar resultados esperados de resultados obtenidos.

### 13.3 Extensiones opcionales

| Extensión | Disparador | Beneficio | Costo y riesgo | Dependencias | Aprobación |
| --- | --- | --- | --- | --- | --- |
| {{OPTIONAL_EXTENSION}} | {{ACTIVATION_TRIGGER}} | {{VALUE}} | {{COST_AND_RISK}} | {{DEPENDENCIES_NOT_BLOCKING_CORE}} | {{APPROVAL_STATE}} |

## 14. Riesgos, spikes y decisiones pendientes

| ID RISK | Riesgo e impacto | Evidencia actual | Mitigación o spike | Criterio de resolución | Responsable |
| --- | --- | --- | --- | --- | --- |
| {{RISK_ID}} | {{RISK_DESCRIPTION}} | {{CURRENT_EVIDENCE}} | {{MITIGATION_OR_BOUNDED_EXPERIMENT}} | {{EXIT_CRITERION}} | {{RISK_OWNER}} |

Todo experimento que instale, ejecute servicios, use datos o consuma recursos necesita alcance y permiso propios. Un spike propuesto no es una prueba pasada.

## 15. Trazabilidad y gate de entrega

| Feature o requisito | Caso de uso | Decisión y fuente | Componente | Fase | Prueba | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| {{REQUIREMENT_ID}} | {{UC_ID}} | {{ADR_AND_SRC_IDS}} | {{COMPONENT_ID}} | {{PHASE_ID}} | {{TEST_ID}} | {{COVERAGE_STATE}} |

- [ ] Las variables críticas están resueltas para el alcance aprobado.
- [ ] La revisión de completitud existe y declara independencia real o su ausencia.
- [ ] Las restricciones excluyentes se cumplen.
- [ ] El stack tiene compatibilidad y documentación de versión.
- [ ] Las decisiones relevantes tienen aprobación y riesgos visibles.
- [ ] Cada feature MVP y NFR crítico tiene fase y aceptación.
- [ ] El grafo no contiene ciclos, referencias ausentes ni opcionales obligatorias.
- [ ] Roadmap y AGENTS coinciden en reglas, tecnologías, rutas y comandos.
- [ ] Las fuentes respaldan las afirmaciones y decisiones relevantes.
- [ ] Los comandos están clasificados por realidad, no por apariencia.
- [ ] No quedan marcadores críticos en una entrega declarada lista.
- [ ] La implementación permanece pendiente salvo evidencia real previa inspeccionada.

## 16. Próxima acción autorizada

**Siguiente tarea:** {{NEXT_READY_TASK}}.
**Qué se puede hacer ahora:** {{AUTHORIZED_NEXT_ACTION}}.
**Qué requiere respuesta o permiso adicional:** {{REQUIRED_USER_DECISION_OR_PERMISSION}}.
**Lo que todavía no está construido:** {{UNIMPLEMENTED_SCOPE}}.

## 17. Historial y fuentes

| Versión | Cambio | Decisiones afectadas | Aprobación |
| --- | --- | --- | --- |
| {{PLAN_VERSION}} | {{CHANGE_SUMMARY}} | {{AFFECTED_ADR_IDS}} | {{APPROVAL_REFERENCE}} |

**Fuentes concretas del proyecto:** {{PROJECT_SOURCE_LIST_WITH_VERSION_AND_ACCESS_DATE}}.
**Afirmaciones no comprobadas y límite de investigación:** {{UNVERIFIED_CLAIMS_AND_RESEARCH_LIMITS}}.

Completar las fuentes para esta app. Las fuentes de la especificación de la skill no demuestran que el stack de este proyecto sea adecuado.
