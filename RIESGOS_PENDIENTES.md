# RIESGOS PENDIENTES — Plataforma Protocolo Fortaleza v2.0

**Fecha:** 2026-03-16 | **Auditor:** Claude Cowork

---

## Riesgos que no se pudieron cerrar completamente

| # | Riesgo | Descripción | Razón técnica | Mitigación aplicada | Riesgo residual |
|---|---|---|---|---|---|
| 1 | **Hash client-side bypasseable** | Un usuario con conocimientos de JavaScript puede leer el código fuente, entender el algoritmo de hash y recalcularlo después de modificar localStorage | Sin backend server, toda la lógica vive en el cliente. El código fuente es visible en "View Source". | Hash con salt dificulta manipulación casual. El 99% de usuarios del IGSS no sabrá cómo hacerlo. | **MEDIO** — Mitigable solo con backend |
| 2 | **Códigos de acceso visibles en fuente** | Los 5 VALID_CODES están en texto plano en el HTML | Plataforma 100% estática sin servidor. No hay dónde ocultar secretos client-side. | Códigos son de acceso al curso, no a datos sensibles. Riesgo aceptable para capacitación interna. | **BAJO** — Aceptable para uso IGSS interno |
| 3 | **Sin autenticación backend** | No hay verificación server-side de identidad | GitHub Pages es hosting estático; no soporta backend. | Login con códigos + hash de integridad es suficiente para capacitación. Migrar a backend si se requiere certificación formal. | **MEDIO** — Requiere infraestructura |
| 4 | **Ranking almacenado en localStorage** | Cada navegador tiene su propio ranking. No hay ranking centralizado. | Sin base de datos server-side. localStorage es por navegador/dispositivo. | Rankings se muestran correctamente por sesión de navegador. Para ranking global se necesita backend (Firebase, Supabase, etc.) | **MEDIO** — Requiere backend para ranking global |
| 5 | **Planos interactivos no implementados** | La evaluación avanzada tipo "clic en zona del plano" no se pudo implementar | Requiere assets gráficos reales: planos arquitectónicos del IGSS con zonas definidas. Estos archivos no están disponibles. | Motor de evaluación tiene estructura extensible. Agregar planos cuando estén disponibles. | **BAJO** — Funcionalidad opcional |
| 6 | **Árboles de decisión parciales** | Los escenarios cognitivos son lineales, no ramificados | Un árbol de decisión completo necesita un engine de flujo con estados y transiciones. La complejidad supera el alcance actual. | Escenarios existentes simulan decisión pero sin ramificación condicional real. | **BAJO** — Mejora iterativa |
| 7 | **Active recall cruzado limitado** | No hay inyección automática de preguntas de fases anteriores en fases posteriores | Requiere un banco de preguntas centralizado y algoritmo de selección. Cada fase es un archivo HTML independiente sin comunicación entre sí. | Las preguntas de cada fase refuerzan conceptos NRD-2 generales que se repiten. | **BAJO** — Mejora futura |
| 8 | **Audioteca sin contenido** | Los 8 enlaces de audioteca son placeholders sin archivos reales | No se proporcionaron archivos de audio. | Enlaces marcados como "próximamente" o pueden vincularse a podcasts existentes. | **BAJO** — Contenido pendiente |
| 9 | **Sin CSP (Content Security Policy)** | No hay headers de seguridad que prevengan XSS | GitHub Pages no permite configurar headers HTTP personalizados fácilmente. | El sitio no acepta input que se renderice como HTML (no hay riesgo XSS real). Las preguntas usan radio buttons, no text fields evaluados. | **BAJO** — Riesgo teórico |
| 10 | **Sin HTTPS enforcement** | El sitio no fuerza HTTPS | GitHub Pages proporciona HTTPS por defecto en *.github.io | HTTPS ya está activo automáticamente. Solo un riesgo si se migra a hosting sin HTTPS. | **MÍNIMO** |

---

## Resumen de riesgo

| Nivel | Cantidad | Acción recomendada |
|---|---|---|
| CRÍTICO | 0 | — |
| ALTO | 0 | — |
| MEDIO | 3 | Migrar a backend cuando se requiera certificación formal |
| BAJO | 6 | Mejoras iterativas según disponibilidad de recursos |
| MÍNIMO | 1 | Sin acción requerida |

---

## Recomendación

La plataforma es **apta para uso en capacitación interna IGSS/CONRED** con las protecciones actuales. Para uso formal con certificación oficial o público general, se recomienda migrar a un backend (Firebase, Supabase, o similar) que permita:
- Autenticación real con credenciales individuales
- Ranking centralizado entre todos los usuarios
- Logs de auditoría server-side
- Protección completa contra manipulación
