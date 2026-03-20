# CHECKLIST DE VALIDACIÓN FINAL — Plataforma NRD-2

---

## 📁 1. Entregables generados
- [ ] `AUDITORIA_INICIAL.md` existe y tiene diagnóstico claro
- [ ] `RUTAS_AUDITADAS.md` existe con tabla completa
- [ ] `MATRIZ_NRD2.md` existe con todas las mejoras comparadas
- [ ] `CAMBIOS_REALIZADOS.md` lista archivos y funciones modificadas
- [ ] `RIESGOS_PENDIENTES.md` documenta lo que no se pudo completar
- [ ] `ESTADO_FINAL.md` clasifica el sistema claramente

---

## 🔒 2. Regla del 70%
- [ ] Con 69% o menos el usuario NO puede avanzar
- [ ] Con 70% o más el usuario SÍ puede avanzar
- [ ] Examen abandonado a mitad = reprobado
- [ ] Examen con respuestas incompletas = reprobado
- [ ] Escribir la URL de la fase siguiente manualmente = bloqueado y redirigido
- [ ] Recargar la página durante el examen no rompe la lógica
- [ ] La UI muestra un mensaje claro cuando se reprueba

---

## 💾 3. Persistencia y seguridad
- [ ] El progreso sobrevive una recarga de página
- [ ] El progreso sobrevive cerrar y reabrir el navegador
- [ ] No se puede alterar la nota desde la consola del navegador
- [ ] No se puede modificar el avance de fase desde localStorage manualmente
- [ ] No se puede acceder a la vista final sin haber completado todas las fases

---

## 🧭 4. Navegación
- [ ] Todos los botones de "continuar" funcionan
- [ ] Todos los botones de "volver" funcionan
- [ ] Todos los botones de "finalizar" funcionan
- [ ] No hay rutas que devuelvan error 404 o pantalla en blanco
- [ ] Los guards redirigen correctamente cuando el acceso no está permitido

---

## 🏆 5. Ranking Top 3
- [ ] El ranking solo aparece cuando se completan el 100% de las fases
- [ ] El ranking ordena correctamente por puntaje
- [ ] En caso de empate, penaliza por errores en preguntas críticas
- [ ] En segundo empate, desempata por menor tiempo
- [ ] El mensaje de recompensa aparece **únicamente** si el usuario clasifica en Top 3
- [ ] El mensaje dice exactamente: *"Felicidades. Has clasificado en el Top 3 y eres acreedor de una asesoría personalizada para la elaboración de tu plan NRD-2."*
- [ ] El mensaje **NO** aparece si el usuario no clasifica

---

## 🧩 6. Evaluaciones avanzadas
- [ ] El motor soporta o tiene preparada la estructura para preguntas con planos interactivos
- [ ] El motor soporta o tiene preparada la estructura para árboles de decisión
- [ ] El motor soporta o tiene preparada la estructura para active recall entre fases
- [ ] Las preguntas críticas están marcadas y afectan el desempate del ranking

---

## 📋 7. Documento "mejoras Nrd2"
- [ ] Todas las mejoras del documento fueron comparadas contra el código
- [ ] Las que se pudieron implementar están aplicadas
- [ ] Las que no se pudieron implementar tienen justificación técnica clara
- [ ] La matriz está completa sin filas vacías

---

## 🚦 Decisión final

| Estado | Criterio |
|---|---|
| ✅ Listo para revisión funcional | Más del 80% de checks marcados |
| 🔶 Listo para QA | Reglas de negocio completas, pendientes menores |
| 🟡 Listo para piloto | Todo crítico resuelto, mejoras avanzadas preparadas |
| 🔴 No apto para producción | Alguna regla crítica sin resolver |
