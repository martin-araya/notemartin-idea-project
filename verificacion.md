# Informe de verificación documental

**Fecha:** 2026-10-27.
**Paquete:** Idea to Blueprint, especificación 0.3.0.
**Alcance:** documentos y plantillas. No certifica implementación, instalación ni funcionamiento de la futura skill.
**Fase verificada en esta entrega:** 002, modos de trabajo y niveles de profundidad.

## 1. Inventario de entrega

1. [README.md](README.md).
2. [roadmap.md](roadmap.md).
3. [AGENTS.md](AGENTS.md).
4. [contrato.md](contrato.md).
5. [modos.md](modos.md).
6. [tests.md](tests.md).
7. [fuentes.md](fuentes.md).
8. [templates/app/roadmap.md](templates/app/roadmap.md).
9. [templates/app/AGENTS.md](templates/app/AGENTS.md).
10. [templates/app/expediente.md](templates/app/expediente.md).
11. Este informe.

## 2. Resultados observados en el cierre de la fase 002

El control documental se ejecutó sobre el paquete después de aplicar los cambios de la fase 002.

| Comprobación | Resultado observado |
| --- | --- |
| Archivos del paquete | 11 presentes, ninguno ausente. |
| Fases centrales | 60, secuencia completa 001–060. |
| Extensiones opcionales | 90, secuencia completa 061–150. |
| Grafo total | 150 nodos y 230 referencias de dependencia. |
| Dependencias internas | Todas apuntan a fases existentes y anteriores. |
| Dependencias del núcleo hacia extensiones | Ninguna. |
| Campos de fases centrales | Objetivo, entregable, aceptación, dependencias y estado presentes. |
| Estados de fases centrales | 2 completadas, que son 001 y 002, y 58 pendientes. |
| Evidencia de la fase completada | Artefactos, evidencia y límite de la evidencia presentes en las fichas de 001 y 002. |
| Cierre fuera del rango | El control rechaza una fase distinta de 001 y 002 marcada como completada. |
| Contrato | 15 casos negativos, 8 actores, versión 0.2.0 y 2 entradas de historial de cambios. |
| Modos | 4 filas de taxonomía, 3 de nivel, 9 invariantes, 12 celdas de matriz, 3 filas de verificación y 2 casos límite. |
| Casos conductuales especificados | 15, IDs EVAL-001–015 completos. |
| Estado de los casos conductuales | Todos not_run. |
| Rúbrica principal | Ocho dimensiones, pesos que suman 100. |
| Tablas Markdown | Cantidad de columnas coherente en las tablas inspeccionadas. |
| Fences de código | Sin bloques sin cerrar. |
| Enlaces locales | Destinos existentes, sin enlace fuera del paquete. |
| Marcadores de plantilla | Deliberados dentro de templates, sin marcadores concretos no resueltos en documentos principales. |
| Casillas de implementación completadas | Ninguna. |
| Estilo editorial | Sin punto y coma en prosa fuera de código. |
| Errores del control | 0. |
| Advertencias del control | 1, la de tamaño de AGENTS.md tratada en la sección 6. |

Huellas de los archivos de contenido en el momento de la comprobación.

| Archivo | Líneas | SHA-256 |
| --- | --- | --- |
| `README.md` | 77 | `9fb11784f194295a6cef9651b41179611f383c637384823fa3a293113fee20a6` |
| `roadmap.md` | 1003 | `ada9fae5c6ff2816da9f7affcc3e594961f0267ca6a770c6e7299c52cdeea865` |
| `AGENTS.md` | 290 | `2cabe2dd19623168be8fbd6a9bd3ea50ea6e7a86e065470edb8c1ff8e9527c6b` |
| `contrato.md` | 200 | `072b70cd7a210bbef7bb4f6a9afa8d8342eb577b45cacda0b873ffe5f7b72ea5` |
| `modos.md` | 266 | `be4576e15e1d57e4144e0e20e328323c46b7a551109f2267787a0c94345ec06d` |
| `tests.md` | 376 | `7fd31c6d79676742d2c105378bac72311cb439244f5f7705d0cae1530e639ae2` |
| `fuentes.md` | 127 | `e2ee0eb7208392d41abde7537568c4bd8c129d0d07cd42382d873e0bcef79a41` |
| `templates/app/roadmap.md` | 386 | `654b7e40e309a8ed1f3f852b1876a63c3aa37b74fd1651d2d32b9eef13d4c348` |
| `templates/app/AGENTS.md` | 290 | `8a3ffeab0d08961697bbf35fc0166e9c736ab5a3c90b3ac44b1df322eceffe33` |
| `templates/app/expediente.md` | 275 | `20386dc3127470adf9efd9dcb909cc999c15d97c54884eaeecc9364c2fddb091` |

La huella de este informe no se referencia porque cambiaría al escribir el propio dato.

## 3. Control negativo previo a la fase 002

El control documental se actualizó antes de aplicar los cambios, para que exigiera el estado objetivo. Se reconstruyó en una copia temporal el estado previo a la fase 002, quitando `modos.md`, devolviendo la fase 002 a pendiente y revirtiendo la versión del contrato, y se ejecutó el control sobre esa copia. Devolvió código de salida 1 con 71 errores: la ausencia de `modos.md` y de sus secciones, identificadores, filas de taxonomía, de nivel, de invariantes, de matriz, de verificación y de casos límite, la fase 002 sin completar, el contrato sin incremento de versión y sin historial de cambios, y los diez enlaces rotos hacia `modos.md`.

Ese resultado es la evidencia de que el control detecta el estado previo. No se declara como aprobación de la fase 002, porque la fase todavía no estaba implementada en ese momento.

## 4. Batería de mutaciones

Se ejecutó una comprobación positiva y veintiséis mutaciones negativas sobre copias temporales del paquete. El original no se alteró para estas pruebas.

| Caso | Resultado real |
| --- | --- |
| Paquete sin alteración | PASS. |
| Fase faltante o renumerada | Detectado. |
| Dependencia hacia una fase posterior | Detectado. |
| Caso de evaluación ausente o renumerado | Detectado. |
| Suma inválida de pesos | Detectado. |
| Enlace local roto | Detectado. |
| Punto y coma en prosa formal | Detectado. |
| Marcador concreto sin resolver fuera de templates | Detectado. |
| Casilla de implementación marcada | Detectado. |
| Tabla con columnas desiguales | Detectado. |
| Fence de código sin cierre | Detectado. |
| Fase completada sin línea de evidencia | Detectado. |
| Fase completada fuera de las permitidas | Detectado. |
| Regla nuclear del contrato eliminada | Detectado. |
| Identificador de caso negativo renumerado | Detectado. |
| Actor del contrato retirado | Detectado. |
| Enlace al contrato roto | Detectado. |
| Marcador sin resolver dentro del contrato | Detectado. |
| Contrato sin incremento de versión | Detectado. |
| Historial de cambios del contrato retirado | Detectado. |
| Modalidad retirada del documento de modos | Detectado. |
| Nivel de profundidad retirado | Detectado. |
| Invariante retirado | Detectado. |
| Celda de la matriz retirada | Detectado. |
| Fila de verificación de la aceptación retirada | Detectado. |
| Enlace a los modos roto | Detectado. |
| Marcador sin resolver dentro de los modos | Detectado. |

Estas pruebas corresponden a una herramienta temporal usada para revisar esta entrega. No son los validadores futuros de la skill, no implementan las fases 046–047 y no equivalen al corpus conductual de [tests.md](tests.md).

## 5. Segunda pasada, declarada no independiente

Se revisó la coherencia entre el documento de modos y el resto del paquete, buscando en todos los documentos las menciones a modalidad, profundidad, niveles y plan listo para implementación.

Hallazgos de la pasada.

1. Todas las menciones del plan listo para implementación, en el roadmap, el contrato, el documento de modos y la plantilla de una app, significan lo mismo, que es un estado del documento y nunca un permiso de ejecución.
2. Ninguna regla de los modos autoriza un efecto. Las clases A, B y C y las reglas C-01 a C-05 del contrato se aplican igual en los tres niveles, y el invariante INV-08 lo declara.
3. La profundidad no se confunde con el perfil de desenlace del corpus, y el documento de modos lo dice de forma expresa para que la evaluación de 051 no mezcle los ejes.
4. La definición de profundidad del roadmap y la del documento de modos coinciden, y el diagrama de la sección 3.3 declara que representa la modalidad de planificación en profundidad estándar.
5. La fila de Ready de la fase 002 conserva el guardia que impide confundir la modalidad de planificación con permiso de ejecución.

No se encontró contradicción. La revisión no fue independiente, la realizó la misma sesión que aplicó el cambio.

## 6. Advertencia de tamaño de AGENTS.md

El control advierte cuando `AGENTS.md` supera el piso de 20000 caracteres registrado para el contexto de arranque. La medición actual es de 20447 caracteres, 447 por encima.

Causa. El inventario de la sección 2.1 ahora incluye `modos.md`, la sección de autoridad documental declara que los modos y los niveles se aplican según ese documento, y el estado real menciona las dos fases completadas.

Decisión. La advertencia se acepta y se registra. No se eliminó ninguna regla para ganar espacio. El aviso de la herramienta indica que el límite activo real no se ha medido, y la revisión de tamaño frente al agente de destino corresponde a la fase 057. Si ese límite resulta vinculante, el detalle se traslada a referencias, como permite la sección 10.4 de AGENTS.

## 7. Citas y fuentes

En este cierre no se modificó ningún marcador de cita ni la bibliografía. El control de recuento de marcadores da 18 líneas con cita en `roadmap.md`, 8 en `AGENTS.md` y 18 en `fuentes.md`, antes y después del cambio. La comprobación de identidades de cita descrita en la entrega 0.1.0 no se volvió a ejecutar porque su herramienta no está disponible en el entorno actual. No se consultaron fuentes nuevas.

## 8. Revisión semántica separada de la entrega anterior

Un revisor en contexto separado examinó el paquete 0.1.0 y no reportó hallazgos críticos ni falsas afirmaciones de implementación. Reportó cuatro hallazgos que se contrastaron con los archivos y se corrigieron.

| Hallazgo | Corrección aplicada |
| --- | --- |
| Un supuesto podía aparentar elegibilidad tecnológica. | AGENTS exige evidencia suficiente o cambio explícito de la restricción. Un supuesto de demanda no prueba licencia, residencia o compatibilidad. |
| La rúbrica podía castigar un bloqueo correcto. | Se separó estado de ejecución de resultado esperado y se definieron perfiles previos, dimensiones aplicables y normalización. |
| Faltaba Ready para comenzar a construir la skill. | Se agregó Ready común y condiciones específicas para arranque, experimentos, piloto, baseline, instalación y cierre. |
| El simulador podía variar entre corridas. | Se exige congelar las respuestas críticas antes del baseline, versionar variantes y se concretó el fixture sintético de costos. |

Las correcciones se aplicaron antes de esta entrega y siguen vigentes. El cierre de la fase 002 no las afecta. No se afirma que ese revisor haya repetido una auditoría ciega del snapshot actual.

## 9. Archivos modificados en esta entrega

| Archivo | Cambio |
| --- | --- |
| `modos.md` | Creado, con autorización, ejes, taxonomía de cuatro modalidades, reglas por modalidad, tres niveles de profundidad, nueve invariantes, matriz de doce celdas, elección y registro, transiciones, verificación de la aceptación, relación con el corpus, trazabilidad y control de cambios. |
| `roadmap.md` | Versión 0.3.0, sección 3.2 con cuatro modalidades, nota del diagrama, inventario ampliado, `modos.md` en el árbol de rutas, cabecera con el contrato 0.2.0, fila de Ready de la 002, estados de fases y ficha de la 002 cerrada con su evidencia. |
| `contrato.md` | Frase de modalidades corregida, versión 0.2.0, sección de historial de cambios con dos entradas y nota de cierre sobre lo entregado en la fase 002. |
| `AGENTS.md` | Inventario con `modos.md`, regla que remite a los modos y a los niveles, y estado real con las dos fases completadas. |
| `README.md` | Entrada de `modos.md`, versiones del contrato y del paquete, y estado con las fases 001 y 002 completadas. |
| `templates/app/roadmap.md` | Campo de modalidad de la ejecución y aclaración de que el estado listo para implementación exige profundidad exhaustiva y sigue sin ser permiso de ejecución. |
| `verificacion.md` | Este informe. |

No se modificaron `tests.md`, `fuentes.md` ni las plantillas de AGENTS y expediente de una app.

## 10. No verificado y pendientes reales

- La skill no está implementada ni instalada.
- No existe un SKILL.md operativo en este paquete.
- No se ejecutaron los 15 casos conductuales.
- El comportamiento en ejecución de los modos y de los niveles no se ha observado. La aceptación de la fase 002 es documental, con el caso de referencia CASE-M1 y los límites N1 y N2 evaluados en los tres niveles.
- El esquema del expediente y su sección de parámetros, que registrarán la modalidad y la profundidad, pertenecen a la fase 003.
- Los fixtures de baseline completos todavía deben materializarse y congelarse al implementar 051.
- No se probaron stacks de aplicaciones, APIs de proveedores, precios de una app concreta ni benchmarks.
- No se ejecutaron despliegues, migraciones, publicaciones ni instalaciones.
- No se creó ni se actualizó el archivo comprimido de documentación. El helper de empaquetado existente apunta a la copia hermana, que conserva el estado anterior a la fase 001, espera nueve archivos y exige cero advertencias, por lo que requiere una orden y una actualización antes de usarse.
- No se inicializó Git, no hubo commit, no hubo push ni apertura de PR.
- No se verificó la carga efectiva de AGENTS en otro agente ni el límite de contexto activo de cada destino.
- No se renderizaron todos los documentos en todos los motores Markdown ni se comprobó conformidad de accesibilidad de una interfaz.
- La validez estructural no reemplaza revisión de producto, arquitectura, licencias o normativa de una app futura.

## 11. Reproducción de esta revisión en el entorno actual

La herramienta temporal de esta sesión se guardó en el directorio scratch de Hermes. No es una dependencia del paquete ni un comando portable instalado.

```text
python3 /Users/martin/.hermes/cache/scratch/validate_idea_to_blueprint_docs.py "/Users/martin/Desktop/projects/Skills/idea-to-blueprint 2"
python3 /Users/martin/.hermes/cache/scratch/probe_idea_to_blueprint_docs.py
```

La herramienta se actualizó para esta entrega. Exige `modos.md` entre los archivos esperados, valida el vocabulario de estados de fase, exige artefactos, evidencia y límite de evidencia en toda fase completada, admite como completadas solo 001 y 002, comprueba las secciones, identificadores, filas y casos del documento de modos, y exige que el contrato declare la versión 0.2.0 con historial de cambios. La batería de mutaciones apunta a este directorio de trabajo y no a la copia hermana.

Estas rutas corresponden únicamente al entorno donde se preparó esta entrega. Los scripts temporales pueden limpiarse. La implementación futura debe incorporar sus propios validadores portables y pruebas, como exige el roadmap.
