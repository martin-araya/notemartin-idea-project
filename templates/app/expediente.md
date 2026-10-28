# Expediente de planificación de {{PROJECT_NAME}}

> PLANTILLA EDITORIAL. Completar con respuestas y evidencia reales. No considerar esta plantilla una investigación ejecutada. Mantener junto a roadmap y AGENTS o integrar sus secciones como anexos si el usuario exige solo dos archivos.

**Proyecto:** {{PROJECT_ID}}.
**Versión del plan:** {{PLAN_VERSION}}.
**Responsable:** {{OWNER}}.
**Fecha y zona:** {{PREPARED_AT}}.
**Estado:** {{DRAFT_BLOCKED_OR_APPROVED_FOR_SCOPE}}.
**Entrada original:** {{LITERAL_USER_IDEA_OR_REFERENCE}}.
**Alcance autorizado:** {{AUTHORIZED_OUTPUTS_RESEARCH_AND_SIDE_EFFECTS}}.

## 1. Inventario de contexto

| Recurso | Tipo y procedencia | Fecha o versión | Inspeccionado | Restricciones y valor probatorio |
| --- | --- | --- | --- | --- |
| {{RESOURCE_ID}} | {{USER_DOCUMENT_REPO_OR_PUBLIC_SOURCE}} | {{RESOURCE_VERSION}} | {{INSPECTION_STATUS}} | {{LIMITS_AND_RELEVANCE}} |

Preservar literalmente nombres y restricciones del usuario. Inspeccionar repositorio existente antes de proponer reemplazar tecnologías o estructura. La existencia de un documento no demuestra que su contenido sea correcto o que el software esté implementado.

## 2. Registro de entrevista

| ID | Pregunta literal | Motivo e impacto | Respuesta literal o referencia | Fecha | Pendiente asociado |
| --- | --- | --- | --- | --- | --- |
| {{QUESTION_ID}} | {{QUESTION_TEXT}} | {{DECISION_IMPACT}} | {{USER_ANSWER_OR_PENDING}} | {{ANSWER_TIME}} | {{OPEN_ITEM_ID_OR_NONE}} |

No registrar respuestas simuladas como reales. En evaluaciones, etiquetar explícitamente el origen del simulador. No repetir una pregunta ya resuelta salvo contradicción o cambio de contexto.

## 3. Matriz de cobertura

| ID VAR | Área | Variable y valor | Fuente | Estado | Criticidad | Decisiones afectadas | Revisión |
| --- | --- | --- | --- | --- | --- | --- | --- |
| {{VAR_ID}} | {{COVERAGE_AREA}} | {{VARIABLE_AND_VALUE}} | {{ANSWER_OR_SOURCE}} | {{VARIABLE_STATE}} | {{CRITICALITY}} | {{DECISION_IDS}} | {{REVIEW_TRIGGER}} |

Estados, `confirmed`, `accepted_assumption`, `pending`, `blocked`, `contradicted`, `not_applicable`.

Examinar problema, usuarios, etapa, plataformas, equipo, presupuesto, tiempo, datos, identidad, tenancy, carga, NFR, integraciones, red, privacidad, accesibilidad, licencias, operación y evolución. Agregar variables del dominio. Un estado `not_applicable` requiere razón.

## 4. Supuestos, contradicciones y aprobaciones

### 4.1 Supuestos

| ID | Enunciado | Razón para proponerlo | Impacto | Aceptación explícita | Revisión |
| --- | --- | --- | --- | --- | --- |
| {{ASSUMPTION_ID}} | {{ASSUMPTION}} | {{REASON}} | {{IMPACT}} | {{USER_APPROVAL_OR_PENDING}} | {{REVIEW_TRIGGER}} |

### 4.2 Contradicciones

| ID | Afirmaciones incompatibles | Fuentes | Decisiones bloqueadas | Pregunta de resolución | Resolución y evidencia |
| --- | --- | --- | --- | --- | --- |
| {{CONTRADICTION_ID}} | {{CONFLICTING_STATEMENTS}} | {{PROVENANCE}} | {{BLOCKED_DECISIONS}} | {{RESOLUTION_QUESTION}} | {{ACTUAL_RESOLUTION_OR_PENDING}} |

### 4.3 Aprobaciones

| ID | Qué se aprobó exactamente | Responsable | Fecha | Evidencia | Qué no autoriza |
| --- | --- | --- | --- | --- | --- |
| {{APPROVAL_ID}} | {{APPROVED_SCOPE}} | {{APPROVER}} | {{APPROVAL_TIME}} | {{RESPONSE_OR_RECORD}} | {{EXCLUDED_ACTIONS}} |

No interpretar aprobar un roadmap como permiso para desplegar, publicar, crear cuentas o generar gastos.

## 5. Revisión de completitud

**Revisor y contexto:** {{REVIEWER_AND_CONTEXT_SEPARATION}}.
**Independencia real:** {{INDEPENDENT_OR_SELF_REVIEW_WITH_LIMITS}}.
**Material revisado:** {{COVERAGE_AND_REQUIREMENTS_VERSION}}.
**Resultado:** {{PASS_CONDITIONAL_BLOCKED}}.
**Variables críticas abiertas:** {{CRITICAL_OPEN_VARIABLES}}.
**Requisitos no medibles:** {{UNMEASURABLE_NFRS}}.
**Contradicciones:** {{UNRESOLVED_CONFLICTS}}.
**Preguntas necesarias:** {{REQUIRED_FOLLOWUPS}}.
**Decisiones permitidas y prohibidas por ahora:** {{DECISION_BOUNDARIES}}.
**Respuesta a hallazgos:** {{RESOLUTION_AND_REVIEW_ITERATION}}.

## 6. Producto validado para planificación

**Problema y usuarios:** {{PRODUCT_CONTEXT}}.
**Casos de uso y reglas:** {{UC_FR_BR_SUMMARY}}.
**Features y MVP:** {{FEATURE_CATALOG_AND_MVP}}.
**No objetivos:** {{NON_GOALS}}.
**NFR y medición:** {{NFRS_WITH_STATUS}}.
**Validación comercial real frente a hipótesis:** {{MARKET_EVIDENCE_AND_HYPOTHESES}}.

No sustituir este apartado por afirmaciones genéricas de demanda o éxito. Si no hubo entrevistas con usuarios, indicar que la validación de producto está pendiente.

## 7. Plan de investigación

| ID RQ | Pregunta de decisión | Variables y requisitos | Familias a investigar | Evidencia suficiente | Presupuesto y estado |
| --- | --- | --- | --- | --- | --- |
| {{RQ_ID}} | {{RESEARCH_QUESTION}} | {{LINKED_REQUIREMENTS}} | {{RELEVANT_TAXONOMIES}} | {{EVIDENCE_THRESHOLD}} | {{BUDGET_AND_STATUS}} |

**Criterio de detención:** {{RESEARCH_STOPPING_RULE}}.
**Cobertura que no se promete:** {{RESEARCH_LIMITS}}.
**Fuentes que requieren revalidación:** {{VOLATILE_SOURCES}}.

## 8. Registro de fuentes

| ID SRC | URL original y localizador | Título y editor | Tipo | Versión o edición | Fecha de consulta | Estado de acceso | Afirmación respaldada y límites |
| --- | --- | --- | --- | --- | --- | --- | --- |
| {{SRC_ID}} | {{EXACT_URL_AND_SECTION}} | {{TITLE_AND_PUBLISHER}} | {{SOURCE_TYPE}} | {{VERSION_OR_EDITION}} | {{RETRIEVED_AT}} | {{RETRIEVED_PARTIAL_BLOCKED_STALE_CONTRADICTORY}} | {{SUPPORTED_CLAIMS_AND_LIMITS}} |

**Evidencia breve cuando sea necesaria:** {{SHORT_EXACT_EXCERPT_AND_LOCATION}}.

Confirmar cuerpo y título de cada página. Un resultado de búsqueda solo respalda lo que dice su snippet. No citar una página inaccesible como si se hubiera leído. Evitar enlaces genéricos cuando una decisión depende de una sección de soporte o precio específica.

## 9. Registro de afirmaciones

| ID | Afirmación concreta | Fuente y ubicación | Versión y entorno | Estado de evidencia | Decisiones afectadas |
| --- | --- | --- | --- | --- | --- |
| {{CLAIM_ID}} | {{ATOMIC_CLAIM}} | {{SRC_AND_SECTION}} | {{CLAIM_SCOPE}} | {{DOCUMENTED_INFERRED_TESTED_UNVERIFIED}} | {{ADR_IDS}} |

Separar que un proveedor documente una función, que esté disponible en una edición y que se haya probado con la combinación del proyecto.

## 10. Estrategias, universo y exclusiones

### 10.1 Estrategias

| Estrategia | Qué resuelve | Etapa de producto | Costos y riesgos | Evolución o descarte | Elegibilidad |
| --- | --- | --- | --- | --- | --- |
| {{STRATEGY}} | {{PROBLEM_FIT}} | {{PROTOTYPE_PILOT_PRODUCTION}} | {{TRADEOFFS}} | {{EVOLUTION}} | {{ELIGIBILITY_AND_REASON}} |

### 10.2 Universo de candidatos

| Familia y candidato | Descubierto mediante | Necesidad que satisface | Restricciones relevantes | Estado |
| --- | --- | --- | --- | --- |
| {{CANDIDATE}} | {{RESEARCH_PROVENANCE}} | {{REQUIREMENT_FIT}} | {{HARD_CONSTRAINTS}} | {{INVESTIGATING_ELIGIBLE_EXCLUDED_BLOCKED}} |

### 10.3 Exclusiones

| Candidato o familia | Restricción incumplida | Evidencia | Definitivo o condicionado | Qué permitiría reconsiderar |
| --- | --- | --- | --- | --- |
| {{EXCLUDED_CANDIDATE}} | {{VAR_OR_NFR_ID}} | {{SOURCE_OR_CONTRADICTION}} | {{EXCLUSION_STATE}} | {{REVISIT_CONDITION}} |

## 11. Ficha tecnológica, repetir por cada finalista

**Candidato y función:** {{CANDIDATE_AND_ROLE}}.
**Edición, versión y soporte:** {{EDITION_VERSION_SUPPORT}}.
**Documentación oficial revisada:** {{VERSIONED_DOCS}}.
**Instalación documentada:** {{INSTALLATION_PROCEDURE_AND_REALITY_STATUS}}.
**Plataformas y runtime:** {{SUPPORTED_ENVIRONMENTS}}.
**Capacidades requeridas:** {{REQUIREMENT_COVERAGE}}.
**Limitaciones relevantes:** {{KNOWN_LIMITATIONS}}.
**Prácticas aplicables:** {{RULE_SOURCE_APPLICATION_TEST}}.
**Integraciones y compatibilidad:** {{DEPENDENCY_COMPATIBILITY}}.
**Licencia y restricciones:** {{LICENSE_AND_REVIEW_LIMITS}}.
**Costos y cuotas:** {{PRICING_AND_LIMITS}}.
**Mantenimiento y migración:** {{MAINTENANCE_AND_EXIT}}.
**Hechos no comprobados:** {{UNVERIFIED_POINTS}}.
**Conclusión provisional:** {{FIT_ASSESSMENT}}.

## 12. Comparación y sensibilidad

**Criterios y escala:** {{ANCHORED_CRITERIA}}.
**Pesos y razón:** {{WEIGHTS_AND_RATIONALE}}.
**Tratamiento de datos desconocidos:** {{MISSING_DATA_POLICY}}.

| Candidato elegible | Criterio | Peso | Valor | Justificación y fuente | Confianza o intervalo |
| --- | --- | --- | --- | --- | --- |
| {{CANDIDATE}} | {{CRITERION}} | {{WEIGHT}} | {{RATING}} | {{REASON_AND_SRC}} | {{UNCERTAINTY}} |

**Herramienta y cálculo realizado:** {{CALCULATION_METHOD_AND_REAL_OUTPUT}}.
**Escenarios de sensibilidad:** {{WEIGHT_AND_DEMAND_SCENARIOS}}.
**Estabilidad de recomendación:** {{ROBUST_WIN_TIE_OR_UNRESOLVED}}.
**Decisión que requiere usuario o spike:** {{NEXT_DECISION}}.

No producir un ranking con decimales que aparenten certeza inexistente. No permitir que una suma compense una restricción excluyente.

## 13. Costos y capacidad

| Concepto | Cantidad y unidad | Tarifa y fuente | Moneda, región e impuestos | Único o recurrente | Total calculado |
| --- | --- | --- | --- | --- | --- |
| {{COST_ITEM}} | {{QUANTITY_AND_UNIT}} | {{RATE_AND_SRC}} | {{FINANCIAL_SCOPE}} | {{COST_TYPE}} | {{TOOL_CALCULATED_TOTAL}} |

**Escenario inicial:** {{INITIAL_LOAD_AND_TOTAL}}.
**Escenario esperado:** {{EXPECTED_LOAD_AND_TOTAL}}.
**Escenario de crecimiento:** {{GROWTH_LOAD_AND_TOTAL}}.
**Aprendizaje y mantenimiento:** {{LABOR_AND_OPERATION_ASSUMPTIONS}}.
**Cuotas, niveles gratuitos y vencimientos:** {{LIMITS_AND_EXPIRATION}}.
**Riesgo de sobrecosto y salida:** {{COST_RISK_AND_EXIT}}.

## 14. Matriz de compatibilidad

| Combinación exacta | Requisito | Fuente de soporte | Estado | Prueba real o spike | Bloqueo |
| --- | --- | --- | --- | --- | --- |
| {{COMPATIBILITY_TUPLE}} | {{REQUIRED_BEHAVIOR}} | {{SRC_ID_AND_LOCATION}} | {{DOCUMENTED_INFERRED_TESTED_BLOCKED}} | {{ACTUAL_TEST_OR_PROPOSAL}} | {{BLOCKER_OR_NONE}} |

## 15. ADR, repetir por decisión relevante

### ADR {{ADR_ID}}. {{DECISION_TITLE}}

**Estado:** {{PROPOSED_ACCEPTED_REJECTED_SUPERSEDED_BLOCKED}}.
**Fecha y responsables:** {{DECISION_DATE_AND_OWNERS}}.
**Contexto:** {{PROBLEM_AND_FORCES}}.
**Requisitos y restricciones:** {{VAR_FR_NFR_IDS}}.
**Opciones viables:** {{OPTIONS_WITH_TRADEOFFS}}.
**Exclusiones relevantes:** {{EXCLUDED_OPTIONS_AND_REASON}}.
**Evidencia:** {{SOURCE_AND_EXPERIMENT_IDS}}.
**Decisión y alcance:** {{SELECTED_OPTION_AND_SCOPE}}.
**Razón:** {{REQUIREMENT_LINKED_ARGUMENT}}.
**Consecuencias positivas:** {{BENEFITS}}.
**Costos, límites y riesgos:** {{CONSEQUENCES}}.
**Reversibilidad y migración:** {{EXIT_AND_MIGRATION_PATH}}.
**Condiciones de revisión:** {{REVISIT_TRIGGERS}}.
**Aprobación:** {{ACTUAL_APPROVAL_REFERENCE_OR_PENDING}}.
**Acciones derivadas:** {{PHASE_AND_TEST_IDS}}.

## 16. Arquitectura y revisión de flujos

**Vistas necesarias:** {{CONTEXT_CONTAINER_DYNAMIC_OR_DEPLOYMENT_VIEWS}}.
**Interfaces y componentes:** {{COMPONENT_CONTRACTS}}.
**Dueño de cada escritura:** {{WRITE_OWNERSHIP}}.
**Red y llamadas externas:** {{CALL_OWNERSHIP_AND_PRIVILEGES}}.
**Secretos y datos sensibles:** {{SECRET_AND_DATA_BOUNDARIES}}.
**Estados de confirmación:** {{RECEIVED_DURABLE_COMMITTED_OBSERVED}}.
**Consistencia y concurrencia:** {{CONSISTENCY_MODEL}}.
**Modo degradado y recuperación:** {{FAILURE_AND_RECOVERY_PATHS}}.
**Revisión de viabilidad:** {{FLOW_REVIEW_FINDINGS}}.

## 17. Seguridad, calidad y módulos condicionales

| Área o módulo | Activación o exclusión | Amenazas y controles | Fuente especializada | Pruebas y responsable |
| --- | --- | --- | --- | --- |
| {{QUALITY_AREA_OR_MODULE}} | {{APPLIES_WITH_REASON}} | {{RISKS_AND_CONTROLS}} | {{APPLICABLE_SOURCE}} | {{TEST_IDS_AND_OWNER}} |

No afirmar cumplimiento legal a partir de esta tabla. Registrar revisiones especializadas necesarias y sus límites.

## 18. Riesgos y experimentos

### 18.1 Riesgos

| ID RISK | Riesgo | Probabilidad y justificación | Impacto | Mitigación | Responsable | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| {{RISK_ID}} | {{RISK}} | {{LIKELIHOOD_WITH_EVIDENCE}} | {{IMPACT}} | {{MITIGATION}} | {{OWNER}} | {{RISK_STATE}} |

### 18.2 Spike

**ID y pregunta:** {{SPIKE_ID_AND_QUESTION}}.
**Alcance descartable:** {{BOUNDED_SCOPE}}.
**Autorización:** {{PERMISSION_OR_PENDING}}.
**Tiempo, costo, red y datos:** {{RESOURCE_LIMITS}}.
**Criterio de éxito y fracaso:** {{EXPERIMENT_ACCEPTANCE}}.
**Método y entorno:** {{REPRODUCTION_METHOD}}.
**Resultado real o pendiente:** {{ACTUAL_RESULT_WITH_ARTIFACT_OR_NOT_RUN}}.
**Limpieza y verificación:** {{CLEANUP_EVIDENCE_OR_PENDING}}.
**Decisión afectada:** {{ADR_ID}}.

## 19. Trazabilidad

| VAR | UC | FR, BR o NFR | FEAT | ADR y SRC | Componente | Fase | TEST | Estado |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| {{VAR_IDS}} | {{UC_ID}} | {{REQUIREMENT_ID}} | {{FEATURE_ID_OR_NOT_APPLICABLE}} | {{DECISION_AND_SOURCE_IDS}} | {{COMPONENT_ID}} | {{PHASE_ID}} | {{TEST_ID}} | {{COVERAGE_STATE}} |

## 20. Revisión de la entrega

**Revisión estructural:** {{CHECKS_AND_REAL_RESULTS}}.
**Revisión semántica:** {{REVIEWER_AND_FINDINGS}}.
**Coherencia roadmap y AGENTS:** {{PAIR_CONSISTENCY_RESULT}}.
**Marcadores críticos pendientes:** {{OPEN_PLACEHOLDERS_OR_NONE}}.
**Bloqueos:** {{BLOCKERS_OR_NONE}}.
**Estado de implementación real:** {{ACTUAL_IMPLEMENTATION_STATUS}}.
**Limitaciones de investigación:** {{RESEARCH_LIMITS}}.
**Próxima acción permitida:** {{NEXT_AUTHORIZED_ACTION}}.

## 21. Estado para reanudar

**Último gate completado:** {{LAST_COMPLETED_GATE}}.
**Entradas nuevas desde la última revisión:** {{NEW_INPUTS}}.
**Decisiones invalidadas por cambios:** {{INVALIDATED_DECISIONS}}.
**Preguntas por resolver:** {{NEXT_QUESTIONS}}.
**Archivos y versiones canónicas:** {{CANONICAL_ARTIFACTS}}.

## 22. Historial

| Versión | Cambio | Fuente del cambio | Decisiones afectadas | Reaprobación |
| --- | --- | --- | --- | --- |
| {{PLAN_VERSION}} | {{CHANGE}} | {{CHANGE_PROVENANCE}} | {{AFFECTED_DECISIONS}} | {{APPROVAL_STATE}} |
