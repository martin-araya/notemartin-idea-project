# Fuentes y decisiones de diseño del paquete

**Fecha de consulta:** 2026-10-27.
**Tipo de entrega:** especificación de una futura skill, no comparación actual de frameworks para una aplicación concreta.
**Estado:** páginas primarias consultadas. Las recomendaciones del paquete son decisiones de diseño, no afirmaciones de certificación o implementación.

## 1. Qué se investigó

Se revisó cómo estructurar una skill de Hermes, cómo se cargan sus instrucciones de proyecto y qué propósito cumple AGENTS. También se consultaron referencias primarias para convertir seguridad, accesibilidad, confiabilidad y arquitectura en decisiones verificables.

No se investigó un stack de aplicación específico porque todavía no existe una idea concreta de app con restricciones. Elegir frameworks ahora contradice el objetivo de decidir por requisitos. La futura skill deberá investigar versiones, soporte, compatibilidad y costos en cada proyecto.

## 2. Aportes y límites de cada fuente

### Fuente 1. Hermes, Creating Skills

La guía oficial distingue una skill basada en instrucciones y herramientas existentes de una integración que necesita una herramienta propia. Documenta estructura, frontmatter, referencias, scripts, plataformas y divulgación progresiva.[1]

**Aplicación en el paquete:** arquitectura inicial documental con referencias y validadores pequeños. Mantener SKILL.md operativo y cargar detalles por tema.

**Límite:** no demuestra que una skill aún no implementada funcione. Los comandos o interfaces propuestos deben verificarse al desarrollarlos.

### Fuente 2. Hermes, Context Files

La documentación describe la prioridad de tipos de contexto, overrides, descubrimiento por directorios y límites que pueden truncar instrucciones.[2]

**Aplicación:** AGENTS con invariantes al principio, lectura completa cuando sea necesaria, detalles extensos en el expediente y revisión del contexto real del agente destino.

**Límite:** las reglas de Hermes no se deben atribuir a todos los agentes. Verificar la versión y el destino al instalar. No eliminar archivos prioritarios para forzar la carga de un AGENTS.

### Fuente 3. Hermes, Skills System

La guía describe skills como conocimiento cargado bajo demanda y documenta niveles de acceso a metadatos, contenido y referencias.[3]

**Aplicación:** referencias especializadas por dominio, sin cargar un catálogo completo en cada conversación. Verificar perfil y mecanismo vigente antes de instalar.

**Límite:** que exista un mecanismo de descubrimiento no significa que la nueva skill esté instalada. En esta entrega no se modificó el catálogo instalado.

### Fuente 4. AGENTS.md

El sitio del formato presenta AGENTS como contexto e instrucciones para agentes de programación, complementario al README humano, con ejemplos de entorno, comandos, pruebas y convenciones.[4]

**Aplicación:** separar el roadmap, el README y las reglas operativas. Diferenciar el AGENTS para construir la skill del AGENTS que esta generará para una app.

**Límite:** un formato común no garantiza idéntica precedencia, herencia, carga o truncamiento entre productos.

### Fuente 5. OWASP ASVS

ASVS proporciona requisitos para desarrollo seguro y verificación de controles técnicos de aplicaciones web. Su documentación recomienda identificar requisitos con versión para evitar ambigüedad entre ediciones.[5]

**Aplicación:** vincular controles aplicables a tareas y pruebas, con identificadores de la edición efectivamente utilizada. Examinar autorización por recurso y casos negativos.

**Límite:** no cubre por sí solo todos los dominios, aplicaciones nativas o exigencias jurídicas. No convierte un checklist en certificación ni demuestra seguridad absoluta.

### Fuente 6. WCAG 2.2

La recomendación describe criterios de éxito verificables y requisitos de conformidad para contenido web, con niveles y alcance definidos.[6]

**Aplicación:** accesibilidad con objetivos, pruebas manuales y automatizadas y límites explícitos. Para plataformas nativas investigar también sus guías oficiales.

**Límite:** una prueba automatizada aislada no demuestra conformidad completa. No se afirma que una app no construida satisfaga WCAG.

### Fuente 7. NIST SSDF

La publicación SP 800-218 describe un conjunto de prácticas de desarrollo seguro integrables en ciclos de vida de software.[7]

**Aplicación:** incluir seguridad en requisitos, desarrollo, verificación, dependencias y mantenimiento, en vez de dejarla como una fase final decorativa.

**Límite:** es referencia de proceso y vocabulario. No sustituye análisis de riesgo específico, evaluación competente ni obligaciones del producto.

### Fuente 8. Google SRE, Implementing SLOs

El capítulo explica SLO, indicadores de servicio y su uso para orientar decisiones de confiabilidad y priorización.[8]

**Aplicación:** NFR medibles, indicadores con población y ventana, y objetivos proporcionales al producto y presupuesto.

**Límite:** no imponer prácticas de una organización grande a cada proyecto. Una app local puede no necesitar un SLO de servicio remoto. Un objetivo propuesto no es confiabilidad observada.

### Fuente 9. C4 model

El sitio oficial describe abstracciones y vistas de arquitectura, desde contexto y contenedores hasta componentes y código, además de diagramas de apoyo.[9]

**Aplicación:** seleccionar vistas que permitan entender límites, interfaces y despliegue sin exigir todos los diagramas para toda app.

**Límite:** un diagrama no demuestra ejecución, aislamiento, consistencia o recuperación. Esas propiedades necesitan contratos y pruebas.

## 3. Decisiones propias de esta especificación

Las siguientes son políticas propuestas para esta skill, no mandatos atribuidos a las fuentes.

1. Descubrimiento adaptativo con matriz de cobertura antes de elegir finalistas.
2. Revisión separada de completitud y declaración honesta de independencia.
3. Universo abierto de candidatos, filtros excluyentes y comparación posterior.
4. Tratamiento explícito de incertidumbre y sensibilidad, sin falsa precisión.
5. Aprobación de decisiones relevantes antes de considerarlas aceptadas.
6. Expediente como fuente de trazabilidad y soporte de reanudación.
7. Roadmap y AGENTS como pareja indivisible para la aceptación documental.
8. Núcleo de fases 001–060 y catálogo opcional 061–150, sin compromiso de implementar extensiones.
9. Corpus inicial de 15 casos conductuales y gates no compensables.
10. Rúbrica y umbral propuesto, pendientes de calibración empírica.
11. No instalar la skill ni ejecutar la app como efecto implícito de escribir documentos.

## 4. Manejo de acceso y evidencia

Dos rutas inicialmente consultadas de la documentación de Hermes devolvieron páginas 404. No se usaron como evidencia. Se consultó el índice oficial y se recuperaron las rutas válidas bajo `user-guide/features/` y la guía de creación.

Las páginas extensas devolvieron extractos con límites de tamaño. Las afirmaciones del paquete se restringen al contenido efectivamente recibido y revisado, sin atribuir lectura completa de secciones omitidas.

No se ejecutaron instalaciones, llamadas de APIs de proveedores, pruebas de frameworks, benchmarks ni evaluaciones conductuales de la skill. La fecha de consulta no congela la validez futura de versiones, precios o reglas de carga.

## 5. Política para futuras fuentes de proyecto

El expediente de cada aplicación debe registrar URL original, versión, sección, fecha, editor, afirmación respaldada y límites. Usar fuentes oficiales específicas de soporte, precio y edición para decisiones que dependan de esos datos. Revalidar información volátil al decidir y antes de ejecutar una migración o release cuando su riesgo lo exija.

Las fuentes de esta página fundamentan el método, no una elección particular de lenguaje, framework o infraestructura para las próximas apps.

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
