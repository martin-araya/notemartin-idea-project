# Idea to Blueprint, especificación de una skill

Una skill propuesta para transformar ideas de aplicaciones en producto definido, investigación tecnológica, decisiones justificadas, arquitectura y documentos listos para orientar el desarrollo.

**Estado de esta entrega:** documentación y plantillas. Las fases 001 y 002 están completadas, con el contrato congelado del producto y los modos con sus niveles de profundidad. No es todavía una skill implementada o instalada.
**Idioma:** español.
**Responsable del producto:** Martín Araya.
**Fecha de preparación:** 2026-10-27.
**Fecha de última actualización:** 2026-10-27, cierre de la fase 002.

## Archivos para construir la skill

- [roadmap.md](roadmap.md), especificación, contratos, fases del núcleo y catálogo opcional.
- [AGENTS.md](AGENTS.md), reglas para desarrollar y mantener la skill.
- [contrato.md](contrato.md), contrato congelado del producto, versión 0.2.0, con alcance, exclusiones, actores y artefactos autorizados.
- [modos.md](modos.md), modalidades de trabajo, niveles de profundidad, invariantes y verificación de la aceptación.
- [tests.md](tests.md), corpus de evaluación, simulación de usuarios, rúbrica y regresión.
- [fuentes.md](fuentes.md), fuentes primarias consultadas y límites de la investigación.
- [verificacion.md](verificacion.md), comprobaciones documentales ejecutadas sobre esta entrega.

## Plantillas para los proyectos que planifique

- [templates/app/roadmap.md](templates/app/roadmap.md), producto, features, stack, arquitectura y fases de una app concreta.
- [templates/app/AGENTS.md](templates/app/AGENTS.md), reglas y comandos para agentes que trabajen en esa app.
- [templates/app/expediente.md](templates/app/expediente.md), entrevistas, cobertura, fuentes, comparaciones, costos, ADR y trazabilidad.

Las plantillas contienen marcadores deliberados `{{...}}`. No son ejemplos de una app terminada y no deben usarse sin completar. Si una futura entrega exige solo dos archivos, el expediente puede integrarse como anexos en esos dos documentos.

## Cómo está pensado el proceso

1. Descubrir problema, usuarios, plataformas, presupuesto, equipo y restricciones.
2. Revisar en una pasada separada si se sabe lo suficiente para decidir.
3. Definir casos de uso, features, MVP, reglas y requisitos medibles.
4. Comparar estrategias de solución, no solo frameworks.
5. Investigar familias tecnológicas, documentación oficial, versiones y soporte.
6. Excluir candidatos incompatibles antes de puntuarlos.
7. Analizar compatibilidad, costos, riesgos, incertidumbre y reversibilidad.
8. Aprobar decisiones relevantes y diseñar límites, datos y contratos.
9. Producir el roadmap y el AGENTS específicos de esa app.
10. Revisar estructura, trazabilidad, evidencia y coherencia de la pareja.

La pregunta no es qué tecnología es siempre mejor. Es qué alternativa satisface mejor las necesidades y restricciones de este proyecto, con qué evidencia y a qué costo.

## Orden de lectura

Para comprender el producto, empezar por las secciones 1–10 del roadmap. Para implementarlo, leer después AGENTS y las fases 001–060. Para evaluar el comportamiento, usar tests.md. Para entender las salidas, revisar las tres plantillas de app.

El roadmap usa una convención extensa de 150 fases. Las primeras 60 definen el núcleo obligatorio, con beta en 050. Las fases 061–150 son un catálogo desactivado de extensiones posibles, no un compromiso de construirlas ni un prerrequisito para usar la skill. El roadmap de una app futura no tiene que copiar esta cantidad de fases.

## Qué no se hizo

- No se eligió un stack para una app aún no definida.
- No se creó un SKILL.md instalable ni los scripts propuestos.
- No se instalaron dependencias o skills.
- No se instaló esta skill ni se cambió la configuración de perfiles o proyectos anteriores.
- No se ejecutó el corpus conductual, porque la skill todavía no existe.
- No se crearon servicios, cuentas, recursos facturables ni publicaciones remotas.
- No se ejecutó ninguna acción de efecto externo al cerrar la fase 001. El contrato congela la frontera de permisos, no la ejecuta.

## Cómo usar este paquete después

Puedes entregar esta carpeta a un agente con una instrucción como la siguiente.

```text
Lee AGENTS.md, roadmap.md, tests.md y las plantillas.
Trabaja por fases y no amplíes el alcance.
Antes de implementar, identifica el estado real del repositorio,
las dependencias de la primera fase y las decisiones pendientes.
Conserva la separación entre plan, aprobación y ejecución.
No instales ni publiques la skill sin autorización adicional.
```

Ese texto es una propuesta para una sesión posterior, no una implementación ejecutada en esta entrega.

## Límites de la verificación

El informe documental puede comprobar fases, campos, enlaces, citas y estructura. No demuestra que la skill investigue bien, recomiende una arquitectura correcta o funcione instalada. Esas aceptaciones permanecen pendientes en el roadmap y en tests.md.
