# MATRIZ NRD-2 — Cumplimiento de Mejoras vs. Documento "Mejoras Nrd2.docx"

**Fecha:** 2026-03-16 | **Auditor:** Claude Cowork
**Fuente:** Mejoras Nrd2.docx (documento original del cliente)

---

## A. Mejoras de Optimización Estructural y Normativa

| # | Mejora solicitada | Evidencia en código | Brecha | Acción aplicada | Estado | Observaciones |
|---|---|---|---|---|---|---|
| 1 | Alineación taxonómica NRD-2: Carga de Ocupación debe usar fórmula CONRED, no genérica. Agregar campo que cruce aforo máximo con flujo real | Flashcard genérica "CO = Área / Factor de Uso" en fase-1 | Fórmula no vinculada a parámetros NRD-2 específicos | Pendiente: agregar campo cruzado en Auditoría de Contexto | 🔶 Pendiente | Requiere datos NRD-2 oficiales de factores de uso por tipo de edificación |
| 2 | Vulnerabilidad por envejecimiento: agregar categoría "Vulnerabilidad Sistémica / Obsolescencia" para edificios antiguos (ej. 1959) | Solo clasifica Interno/Externo/Ambos | Falta categoría de ciclo de vida del edificio | Pendiente: agregar categoría en Módulo D de fase-1 | 🔶 Pendiente | Crítico para IGSS que tiene edificios históricos |
| 3 | Integración datos espaciales: proyectar hacia BIM (ISO 19650) para rutas de evacuación 3D | Campos estáticos de dirección y niveles | Sin capacidad BIM ni visualización 3D | No implementable en HTML estático | ❌ No viable | Requiere plataforma 3D especializada; documentado como mejora futura |

## B. Mejoras de Refinamiento Cognitivo y Conductual

| # | Mejora solicitada | Evidencia en código | Brecha | Acción aplicada | Estado | Observaciones |
|---|---|---|---|---|---|---|
| 4 | Micro-escenarios situacionales en vez de definiciones: evaluar con casos reales, no terminología | Módulo D usa dropdowns con clasificación simple | Evaluación por definición, no por escenario | Parcial: examen fase-1 usa escenarios (Q9: fuga de gas) pero módulo D sigue con dropdowns | 🔶 Parcial | Examen tiene escenarios; módulo interactivo necesita reformulación |
| 5 | Psicología "Minuto Cero": incluir Designación de Roles de Mando con heurísticas de un solo paso para primeros 60 segundos | Módulo G de fase-1 tiene protocolo comunicacional genérico | Sin heurísticas de acción inmediata | Pendiente: agregar bloque "Primeros 60 segundos" en fase-1 y fase-2 | 🔶 Pendiente | Vinculable con Pentarquía de fase-2 |
| 6 | Separar Clima Laboral (interno) de Protestas/Entorno (externo) en matriz de conflictividad | Ambos bajo "Conflictividad Social" en fase-1 | Protocolos de mitigación opuestos mezclados | Pendiente: dividir en dos categorías separadas | 🔶 Pendiente | Cambio en HTML de fase-1, sección amenazas socio-organizativas |

## C. Mejoras de Interfaz y Captura de Datos

| # | Mejora solicitada | Evidencia en código | Brecha | Acción aplicada | Estado | Observaciones |
|---|---|---|---|---|---|---|
| 7 | Retroalimentación inmediata: al seleccionar causalidad, validar y explicar por qué es correcta/incorrecta | Dropdowns sin validación en Módulo D | Sin feedback en tiempo real | Parcial: examen da resultado global, pero Módulo D sigue sin feedback | 🔶 Parcial | Examen evalúa; interactivos del módulo D no |
| 8 | Métricas de escalabilidad: capturar checkboxes "Detectado en mi zona" para generar mapa de calor | Checkboxes existen pero datos se pierden al recargar | Sin tabulación ni persistencia de datos de zona | Pendiente: guardar selecciones en localStorage y generar resumen | 🔶 Pendiente | Implementable sin backend para vista individual |
| 9 | Flujo condicional: si edificio >3 niveles, desplegar requisitos más rigurosos automáticamente | Campo "Niveles del edificio" existe pero es estático | Sin lógica condicional basada en inputs | Pendiente: agregar JS condicional en Auditoría de Contexto | 🔶 Pendiente | Viable en JS vanilla |

## D. Mejoras de Consistencia y Calidad Editorial

| # | Mejora solicitada | Evidencia en código | Brecha | Acción aplicada | Estado | Observaciones |
|---|---|---|---|---|---|---|
| 10 | Unificar nombre de fase: "Diagnóstico taxonómico de amenazas y vulnerabilidades" | Título dice "Diagnostico de Amenazas", dentro "Diagnostico Taxonomico", simulador dice "Triaje de Riesgos" | Tres nombres diferentes para la misma fase | Pendiente: unificar a título único coherente | 🔶 Pendiente | Cambio rápido en HTML |
| 11 | Corregir acentos y ortografía: "Diagnostico" → "Diagnóstico", "Identificacion" → "Identificación", etc. | Múltiples palabras sin acentos en títulos y textos | Falta de acentuación general | Pendiente: revisar y corregir acentuación en los 5 HTML | 🔶 Pendiente | Cambio editorial masivo pero mecánico |
| 12 | Eliminar ruido visual: letras "D", "F", "G" sueltas entre secciones | Marcadores D-F-G visibles como letras aisladas | Residuo de maquetación | Pendiente: integrar como badges o eliminar | 🔶 Pendiente | Estético, no funcional |
| 13 | Separar definiciones: amenaza, vulnerabilidad, riesgo, causalidad con bloque introductorio | No hay bloque de definiciones al inicio | Usuarios responden por intuición sin criterio técnico | Pendiente: agregar bloque de definiciones operativas al inicio de fase-1 | 🔶 Pendiente | Mejora pedagógica significativa |
| 14 | Refinar ejemplos de clasificación: agregar mini-criterio debajo de cada fenómeno | Ejemplos sin contexto de decisión | Ambigüedad en clasificación | Pendiente: agregar guía "Clasifique según origen predominante..." | 🔶 Pendiente | — |
| 15 | Campos guiados en Auditoría de Contexto: rangos, ejemplos, validación, formato | Campos abiertos sin guía | Respuestas vagas posibles | Pendiente: agregar placeholders, rangos y ejemplos | 🔶 Pendiente | Implementable con attributes HTML |
| 16 | Flashcards más accionables: "Marque si ha ocurrido históricamente, es plausible o no aplica" | Checkboxes "Detectado en mi zona" (binarios) | Demasiado simple, sin matiz | Pendiente: cambiar a escala de 3 niveles | 🔶 Pendiente | — |
| 17 | Transición entre teoría y protocolo: frase puente entre taxonomía y comunicación | Salto directo entre módulos | Sin narrativa de transición | Pendiente: agregar párrafo de transición | 🔶 Pendiente | Cambio rápido |
| 18 | Estructurar algoritmo comunicacional: secuencia de 5 pasos (emisor → medio → receptor → confirmación → escalamiento) | Textarea libre para cadena de mando | Sin estructura guiada | Pendiente: reemplazar textarea con 5 campos estructurados | 🔶 Pendiente | Mejora significativa |
| 19 | Resumen automático antes de completar fase: amenazas identificadas, errores, datos faltantes | Botón "Completar Fase" directo (ahora con examen) | Sin resumen previo | Parcial: examen da resumen de score, pero no de contenido del módulo | 🔶 Parcial | Examen cubre validación; resumen de contenido pendiente |
| 20 | Elegir tono consistente: técnico-institucional O técnico-pedagógico, no mezclar | Mezcla de términos académicos y operativos | Inconsistencia de registro | Pendiente: definir guía de estilo y unificar | 🔶 Pendiente | Decisión de diseño que requiere dirección del cliente |

---

## Resumen de cumplimiento vs. "Mejoras Nrd2.docx"

| Estado | Cantidad | Porcentaje |
|---|---|---|
| ✅ Implementado completamente | 0 | 0% |
| 🔶 Parcialmente implementado | 4 (#4, #7, #9, #19) | 20% |
| 🔶 Pendiente (implementable) | 15 | 75% |
| ❌ No viable sin cambio de plataforma | 1 (#3 - BIM/3D) | 5% |

---

## Nota importante

Las mejoras del ORDEN_DE_TRABAJO.md (regla 70%, seguridad, ranking Top 3) SÍ se implementaron completamente. La brecha está en las mejoras **de contenido y pedagogía** del documento "Mejoras Nrd2.docx", que requieren edición detallada del HTML de cada fase. Estas mejoras son principalmente:

1. **Edición de contenido** (acentos, nombres, definiciones, ejemplos)
2. **Lógica condicional** (campos guiados, flujo según inputs)
3. **Reestructuración pedagógica** (micro-escenarios, heurísticas, transiciones)

Se recomienda implementar en orden de impacto:
1. Correcciones ortográficas y unificación de títulos (rápido, alto impacto visual)
2. Bloque de definiciones operativas al inicio (alto impacto pedagógico)
3. Campos guiados y lógica condicional (medio impacto, requiere JS)
4. Micro-escenarios y reestructuración profunda (alto impacto, mayor esfuerzo)
