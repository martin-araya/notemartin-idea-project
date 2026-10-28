# AGENTS.md de {{PROJECT_NAME}}

> PLANTILLA EDITORIAL. Este archivo debe completarse para una app concreta. No ejecutar sus marcadores. Retirar este aviso, las notas editoriales y las secciones no aplicables antes de entregar el AGENTS definitivo.

## 0. Invariantes del proyecto

**Proyecto y contrato:** {{PROJECT_ID_AND_PLAN_VERSION}}.
**Estado real del repositorio:** {{GREENFIELD_OR_IMPLEMENTED_COMPONENTS}}.
**Producto y aceptación:** [roadmap.md](roadmap.md).
**Decisiones y documentación:** [expediente.md](expediente.md).

1. Trabaja en el alcance aprobado de la tarea actual. No amplíes features ni cambies el stack sin una decisión registrada.
2. Preserva estas restricciones confirmadas, {{CRITICAL_PLATFORM_PRIVACY_BUDGET_AND_DEPLOYMENT_CONSTRAINTS}}.
3. No confundas una propuesta, una guía oficial o una prueba con mocks con software verificado en su entorno real.
4. No inventes rutas existentes, APIs, comandos, versiones, credenciales ni resultados de pruebas.
5. No realices acciones destructivas, publicaciones, migraciones reales o despliegues sin autorización.
6. No incluyas secretos o datos personales innecesarios en código, logs, tests o respuestas.
7. Conserva los contratos y el trabajo del usuario. Si existe contradicción, detente en el punto afectado y pide resolución.
8. Una tarea termina con su aceptación y evidencia, no solo con código escrito o una suite parcial en verde.

## 1. Contexto de producto

**Problema y usuarios:** {{PROBLEM_USERS_AND_CONTEXT}}.
**Resultado principal:** {{CORE_USER_OUTCOME}}.
**MVP:** {{MVP_JOURNEYS_AND_BOUNDARIES}}.
**Fuera de alcance:** {{NON_GOALS}}.
**Responsable de decisiones:** {{PRODUCT_AND_TECHNICAL_APPROVERS}}.

Este archivo contiene reglas operativas. No repite la comparación completa del stack. Consulta los ADR y fuentes del expediente antes de alterar una decisión.

## 2. Estado real y autoridad de documentos

- **Implementado y comprobado:** {{VERIFIED_COMPONENTS_WITH_EVIDENCE_OR_NONE}}.
- **Implementado pero no verificado:** {{UNVERIFIED_EXISTING_COMPONENTS_OR_NONE}}.
- **Propuesto:** {{PROPOSED_COMPONENTS}}.
- **Bloqueado:** {{CURRENT_BLOCKERS_OR_EXPLICIT_NONE}}.
- **Documentación vigente:** {{CANONICAL_DOCUMENTS_AND_VERSIONS}}.

La solicitud vigente y las restricciones aprobadas delimitan el trabajo. Los ADR aceptados gobiernan su decisión concreta. El roadmap define resultados. AGENTS define el flujo de trabajo. Ningún documento de repositorio sustituye instrucciones superiores o permisos de las herramientas.

Si roadmap, ADR y código divergen, inspecciona el caso y registra el conflicto. No uses el código existente para justificar automáticamente una violación del contrato ni reescribas el contrato para encubrir un bug.

## 3. Mapa del repositorio

| Ruta exacta | Responsabilidad | Estado real o propuesta | Reglas locales |
| --- | --- | --- | --- |
| {{PATH}} | {{MODULE_RESPONSIBILITY}} | {{PATH_REALITY_STATUS}} | {{LOCAL_RULES_OR_NONE}} |

**Entradas principales:** {{ENTRY_POINTS}}.
**Dominio y reglas de negocio:** {{DOMAIN_PATHS}}.
**Persistencia y migraciones:** {{DATA_PATHS}}.
**Contratos y esquemas:** {{CONTRACT_PATHS}}.
**Pruebas y fixtures:** {{TEST_PATHS}}.
**Configuración y CI:** {{CONFIG_AND_CI_PATHS}}.
**Archivos generados:** {{GENERATED_FILES_AND_REGENERATION_METHOD}}.

No editar archivos generados manualmente salvo que el flujo documentado lo permita. Si el repositorio todavía no existe, marcar este mapa como propuesto y materializarlo en una fase autorizada.

## 4. Stack autorizado y documentación

| Responsabilidad | Tecnología, edición y versión | Decisión | Fuente oficial aplicable |
| --- | --- | --- | --- |
| {{STACK_LAYER}} | {{APPROVED_TECH_VERSION}} | {{ADR_ID_AND_STATE}} | {{VERSIONED_OFFICIAL_DOC}} |

**Compatibilidad aprobada:** {{COMPATIBILITY_TUPLE_AND_EVIDENCE}}.
**Gestor de dependencias:** {{DEPENDENCY_MANAGER}}.
**Lockfile:** {{LOCKFILE_POLICY}}.
**Política de soporte y actualizaciones:** {{SUPPORT_AND_UPDATE_POLICY}}.

No actualizar majors ni cambiar gestor de paquetes por conveniencia. Verificar de nuevo compatibilidad antes de agregar una dependencia que afecte runtime, compilación, plataforma, seguridad o licencia.

### 4.1 Reglas derivadas de documentación

| Regla obligatoria | Contexto | Fuente y versión | Validación | Excepción autorizada |
| --- | --- | --- | --- | --- |
| {{CONCRETE_TECH_RULE}} | {{RULE_CONTEXT}} | {{SOURCE}} | {{CHECK}} | {{EXCEPTION_OR_NONE}} |

Si una guía oficial cambia, no aplicar la nueva versión a un runtime antiguo sin revisar su compatibilidad. Una recomendación de un artículo no anula una restricción confirmada.

## 5. Preparación y comandos

### 5.1 Prerequisitos

**Sistema y toolchain objetivo:** {{SUPPORTED_ENVIRONMENT}}.
**Versiones necesarias:** {{EXACT_RUNTIME_AND_SDK_REQUIREMENTS}}.
**Servicios locales y puertos:** {{REQUIRED_SERVICES_OR_NONE}}.
**Variables de configuración no secretas:** {{NON_SECRET_CONFIGURATION}}.
**Mecanismo seguro para credenciales:** {{SECRET_PROVISIONING_METHOD}}.
**Datos de prueba:** {{SYNTHETIC_FIXTURES_AND_RESET_POLICY}}.

No pedir claves en chat ni imprimirlas. No asumir que una cuenta externa está conectada. Si falta acceso, usar el flujo autorizado y mantener bloqueadas las pruebas que lo requieren.

### 5.2 Registro de comandos reales o propuestos

| Uso | Comando exacto | Directorio | Prerequisitos | Efectos y autorización | Estado y evidencia |
| --- | --- | --- | --- | --- | --- |
| Preparar entorno. | {{SETUP_COMMAND_OR_NOT_APPLICABLE}} | {{SETUP_CWD}} | {{SETUP_REQUIREMENTS}} | {{SETUP_SIDE_EFFECTS}} | {{SETUP_VERIFICATION_STATUS}} |
| Desarrollo local. | {{DEV_COMMAND_OR_NOT_APPLICABLE}} | {{DEV_CWD}} | {{DEV_REQUIREMENTS}} | {{DEV_SIDE_EFFECTS}} | {{DEV_VERIFICATION_STATUS}} |
| Formato y lint. | {{LINT_COMMAND_OR_PENDING_IMPLEMENTATION}} | {{LINT_CWD}} | {{LINT_REQUIREMENTS}} | {{LINT_MUTATION_POLICY}} | {{LINT_VERIFICATION_STATUS}} |
| Tipos y análisis estático. | {{TYPECHECK_COMMAND_OR_NOT_APPLICABLE}} | {{TYPECHECK_CWD}} | {{TYPECHECK_REQUIREMENTS}} | {{TYPECHECK_SIDE_EFFECTS}} | {{TYPECHECK_VERIFICATION_STATUS}} |
| Pruebas rápidas. | {{UNIT_TEST_COMMAND}} | {{UNIT_TEST_CWD}} | {{UNIT_TEST_REQUIREMENTS}} | {{UNIT_TEST_SIDE_EFFECTS}} | {{UNIT_TEST_VERIFICATION_STATUS}} |
| Integración y contratos. | {{INTEGRATION_COMMAND}} | {{INTEGRATION_CWD}} | {{INTEGRATION_REQUIREMENTS}} | {{INTEGRATION_SIDE_EFFECTS}} | {{INTEGRATION_VERIFICATION_STATUS}} |
| Recorridos críticos. | {{E2E_COMMAND_OR_METHOD}} | {{E2E_CWD}} | {{E2E_REQUIREMENTS}} | {{E2E_SIDE_EFFECTS}} | {{E2E_VERIFICATION_STATUS}} |
| Build o empaquetado. | {{BUILD_COMMAND}} | {{BUILD_CWD}} | {{BUILD_REQUIREMENTS}} | {{BUILD_SIDE_EFFECTS}} | {{BUILD_VERIFICATION_STATUS}} |
| Migración local. | {{LOCAL_MIGRATION_COMMAND_OR_NONE}} | {{MIGRATION_CWD}} | {{MIGRATION_REQUIREMENTS}} | {{MIGRATION_APPROVAL}} | {{MIGRATION_VERIFICATION_STATUS}} |

Estados permitidos, propuesto, documentado o ejecutado con evidencia. En un repositorio existente, extraer comandos de manifiestos y scripts inspeccionados. En greenfield, agregar una tarea de creación del harness antes de exigir comandos que aún no existen.

No ejecutar instrucciones copiadas de documentación sin revisar su efecto. Una salida esperada no puede registrarse como salida obtenida.

## 6. Arquitectura y límites que no se deben romper

**Estilo y ADR:** {{ARCHITECTURE_AND_ADR}}.
**Dirección de dependencias permitida:** {{ALLOWED_DEPENDENCY_DIRECTION}}.
**Límites de módulos:** {{MODULE_BOUNDARIES}}.
**Dueños de datos y escritura:** {{DATA_OWNERSHIP}}.
**Interfaces públicas:** {{PUBLIC_INTERFACES_AND_VERSIONING}}.
**Accesos prohibidos:** {{FORBIDDEN_COUPLING_AND_NETWORK_CALLS}}.

Para cada cambio revisar entrada, validación, autorización, efecto durable y observación por el usuario. No confundir petición recibida con operación completada.

No añadir una cola, un microservicio, caché, proveedor de IA o segundo almacenamiento sin requisito, costo operativo y aprobación. Tampoco simplificar una frontera que existe por seguridad, operación o compatibilidad confirmada.

## 7. Convenciones de implementación

### 7.1 Organización y tipos

**Nombres y estructura:** {{NAMING_AND_ORGANIZATION_RULES}}.
**Tipos y validación de límites:** {{TYPE_AND_RUNTIME_VALIDATION_RULES}}.
**Manejo de dependencias:** {{DEPENDENCY_INJECTION_OR_CONSTRUCTION_POLICY}}.
**Abstracciones admitidas:** {{ABSTRACTION_POLICY}}.

Mantener módulos con una responsabilidad comprensible. No introducir extensibilidad especulativa. Antes de duplicar una regla de negocio, inspeccionar su implementación existente y contrato.

### 7.2 Errores y contratos

**Modelo de error:** {{ERROR_MODEL}}.
**Exposición al usuario:** {{USER_SAFE_ERROR_POLICY}}.
**Logs y correlación:** {{LOGGING_CORRELATION_RULES}}.
**Compatibilidad de API:** {{API_COMPATIBILITY_POLICY}}.
**Paginación y límites:** {{PAGINATION_AND_LIMITS}}.

No incluir trazas, credenciales ni datos sensibles en mensajes públicos. No cambiar silenciosamente la forma de un contrato consumido por otros componentes.

### 7.3 Concurrencia y tareas de fondo

**Estado y propietario de trabajos:** {{JOB_OWNERSHIP_OR_NOT_APPLICABLE}}.
**Timeout, cancelación y reintentos:** {{JOB_CONTROL_POLICY}}.
**Idempotencia y deduplicación:** {{IDEMPOTENCY_POLICY}}.
**Orden y consistencia:** {{ORDERING_AND_CONSISTENCY}}.

Eliminar esta subsección si no aplica, dejando su exclusión justificada en el expediente. Un timeout del cliente no demuestra que se haya detenido el trabajo del servidor.

## 8. Datos y migraciones

**Invariantes obligatorias:** {{DATA_INVARIANTS}}.
**Transacciones y concurrencia:** {{TRANSACTION_BOUNDARIES}}.
**Identificadores, fechas y zonas horarias:** {{IDENTIFIER_AND_TIME_POLICY}}.
**Migraciones y compatibilidad:** {{MIGRATION_COMPATIBILITY_POLICY}}.
**Respaldo y restauración:** {{BACKUP_RESTORE_POLICY}}.
**Retención, exportación y borrado:** {{DATA_LIFECYCLE_POLICY}}.

No reescribir migraciones ya aplicadas sin la estrategia aprobada. No probar destrucción o migración sobre datos reales. Los tests de restauración deben demostrar lectura y consistencia, no solo creación de un archivo de backup.

## 9. Seguridad y privacidad

**Fronteras de confianza:** {{TRUST_BOUNDARIES}}.
**Autenticación y sesiones:** {{AUTHENTICATION_POLICY_OR_JUSTIFIED_NONE}}.
**Autorización por recurso:** {{RESOURCE_AUTHORIZATION}}.
**Aislamiento de usuarios o tenants:** {{ISOLATION_POLICY_OR_NOT_APPLICABLE}}.
**Entradas y archivos no confiables:** {{UNTRUSTED_INPUT_POLICY}}.
**Secretos:** {{SECRET_HANDLING}}.
**Protección y retención de datos:** {{PRIVACY_RULES}}.
**Auditoría:** {{AUDIT_EVENTS_AND_RETENTION}}.

- Validar permisos en la frontera que realmente controla el recurso.
- No confiar en campos del cliente para probar propiedad o rol.
- Probar accesos denegados y recursos ajenos.
- No usar datos privados en fixtures o servicios externos sin permiso.
- Registrar hallazgos sensibles por el canal acordado, sin publicar detalles explotables innecesarios.
- No declarar cumplimiento normativo, certificación o seguridad completa por pasar tests locales.

## 10. UX y accesibilidad

**Recorridos críticos:** {{CRITICAL_USER_JOURNEYS}}.
**Carga, vacío, error y recuperación:** {{MANDATORY_UI_STATES}}.
**Interacción por plataforma:** {{PLATFORM_INTERACTION_RULES}}.
**Objetivo accesible y alcance:** {{ACCESSIBILITY_TARGET_AND_SCOPE}}.
**Pruebas manuales:** {{KEYBOARD_SCREEN_READER_TEXT_SCALE_AND_OTHER_TESTS}}.
**Pruebas automatizadas:** {{AUTOMATED_ACCESSIBILITY_CHECKS}}.

Si no existe interfaz, registrar la razón de no aplicación en el expediente. No crear UI únicamente para completar una plantilla.

## 11. Estrategia de pruebas y evidencia

### 11.1 Durante el cambio

1. Reproducir el problema o definir aceptación de la funcionalidad.
2. Añadir prueba que falle cuando el tipo de cambio lo permita.
3. Implementar lo mínimo para satisfacer el contrato.
4. Ejecutar la prueba específica y los checks afectados.
5. Revisar seguridad, errores y compatibilidad.
6. Ejecutar regresión proporcional al riesgo.
7. Conservar comando, entorno, salida y limitaciones.

No inventar una prueba fallida o verde para afirmar TDD. Si un cambio documental no necesita ciclo de código, validar sus contratos y enlaces apropiadamente.

### 11.2 Matriz mínima por cambio

| Tipo de cambio | Comprobación obligatoria | Evidencia y excepción |
| --- | --- | --- |
| Regla de negocio. | {{DOMAIN_TEST_REQUIREMENTS}} | {{DOMAIN_EVIDENCE_POLICY}} |
| Contrato o integración. | {{CONTRACT_TEST_REQUIREMENTS}} | {{INTEGRATION_EVIDENCE_POLICY}} |
| Datos o migración. | {{MIGRATION_TEST_REQUIREMENTS}} | {{DATA_EVIDENCE_POLICY}} |
| Permisos o privacidad. | {{NEGATIVE_SECURITY_TEST_REQUIREMENTS}} | {{SECURITY_EVIDENCE_POLICY}} |
| Interfaz. | {{UI_AND_ACCESSIBILITY_REQUIREMENTS}} | {{UI_EVIDENCE_POLICY}} |
| Rendimiento u operación. | {{PERFORMANCE_RECOVERY_REQUIREMENTS}} | {{OPERATIONS_EVIDENCE_POLICY}} |

Diferenciar pruebas con mocks, integración real, entorno local, staging y producción. No afirmar una capacidad real del proveedor a partir de un stub.

## 12. Flujo de trabajo

### 12.1 Antes de editar

Leer la fase, documentos y código relevante. Revisar instrucciones locales y cambios existentes. Identificar decisión, requisito y aceptación afectados. Si una condición de Ready no se cumple, resolverla o informar el bloqueo.

### 12.2 Durante la implementación

Cambios pequeños y enfocados. Mantener convenciones existentes. Actualizar pruebas y contratos relacionados. Evitar refactors ajenos a la tarea. Si se descubre que el alcance es mayor, explicar el impacto antes de ampliarlo.

### 12.3 Antes de cerrar

Ejecutar checks reales, revisar diff, confirmar aceptación y actualizar documentación afectada. No marcar la fase completa si falta una integración esencial, un dispositivo requerido, permisos o evidencia.

**Política Git:** {{BRANCH_COMMIT_PR_AND_REVIEW_POLICY}}.
**Revisión requerida:** {{REVIEW_REQUIREMENTS}}.
**Acciones que requieren aprobación adicional:** {{EXPLICIT_APPROVAL_BOUNDARIES}}.

## 13. Integraciones y módulos especiales

Conservar solo los módulos aplicables y completar sus reglas.

| Módulo | Invariantes y permisos | Pruebas | Documento de detalle |
| --- | --- | --- | --- |
| {{ACTIVE_MODULE}} | {{MODULE_INVARIANTS}} | {{MODULE_REQUIRED_TESTS}} | {{MODULE_REFERENCE}} |

Para pagos, no equiparar un webhook recibido con conciliación completa. Para IA, no confiar en salidas como instrucciones autorizadas. Para offline, no prometer ausencia de conflictos sin mecanismo y pruebas. Para tiempo real, distinguir estado local, propagado y durable.

## 14. Despliegue y operación

**Ambientes autorizados:** {{AUTHORIZED_ENVIRONMENTS}}.
**Comandos de despliegue y permiso:** {{DEPLOYMENT_COMMANDS_AND_APPROVAL}}.
**Migraciones de release:** {{RELEASE_MIGRATION_GATES}}.
**Rollback y recuperación:** {{ROLLBACK_METHOD}}.
**Observabilidad y límites de datos:** {{OBSERVABILITY_POLICY}}.
**SLO y alertas:** {{SLO_AND_ALERT_POLICY}}.
**Soporte y responsables:** {{OPERATIONAL_OWNERSHIP}}.

Documentar un despliegue no autoriza ejecutarlo. Si se hace una escritura remota autorizada, verificar el recurso exacto con una lectura posterior antes de afirmar éxito. Un proceso iniciado no demuestra que el sistema sea accesible o correcto.

## 15. Bloqueos y cambios de decisión

Si falta una fuente, una herramienta o un acceso.

1. Registrar observación y requisito afectado.
2. Intentar alternativa segura si existe.
3. Separar trabajo completado de trabajo bloqueado.
4. Pedir la mínima información o aprobación necesaria.
5. No fabricar datos ni rebajar aceptación para cerrar.

Si cambia un supuesto o NFR, actualizar el ADR y el roadmap antes de implementar una arquitectura distinta. Preservar IDs y registrar migración cuando corresponda.

## 16. Definition of Done

- [ ] El cambio satisface el requisito y la fase autorizados.
- [ ] Se respetan decisiones y restricciones confirmadas.
- [ ] Las pruebas necesarias se ejecutaron con resultado real.
- [ ] Se cubren fallos, permisos y límites relevantes.
- [ ] No se rompieron contratos ni invariantes de datos.
- [ ] No se añadieron secretos, PII innecesaria o dependencias sin revisión.
- [ ] La documentación, contratos y comandos afectados están actualizados.
- [ ] Los límites y pruebas no ejecutadas están visibles.
- [ ] La evidencia requerida existe y corresponde al entorno declarado.
- [ ] La revisión y aprobación requeridas están completas.

## 17. Reporte de entrega

Informar qué cambió, qué se verificó y qué sigue pendiente. Identificar archivos, pruebas y bloqueos. No narrar cada paso, no inventar resultados y no llamar terminada a una fase con criterios esenciales pendientes.

**Invariantes finales del proyecto:** {{SHORT_REPEAT_OF_CRITICAL_RULES}}.
