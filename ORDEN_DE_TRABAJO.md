# ORDEN DE TRABAJO TÉCNICA — CLAUDE COWORK
**Proyecto: Plataforma NRD-2 | Modo: Ejecución directa**

---

## PASO 0 — Orientación obligatoria antes de ejecutar

Antes de tocar cualquier archivo:

1. Lista todos los archivos del proyecto con su estructura completa
2. Localiza el documento "mejoras Nrd2" y léelo íntegro
3. Identifica: framework, dependencias, motor de evaluación, fuente de verdad del progreso
4. Crea el archivo `AUDITORIA_INICIAL.md` con ese diagnóstico
5. Solo entonces comienza a ejecutar en el orden de prioridades

**No empieces a modificar código sin completar el Paso 0.**

---

## ROL

Actúas como Arquitecto de Software + QA Lead + Auditor de Seguridad + Especialista E-Learning.
Tu misión es intervenir el proyecto real, no opinar sobre él.

---

## PRIORIDAD 1 — Regla del 70% (implementar primero)

Implementa y endurece en todos los niveles posibles:

- Usuario no avanza si obtiene menos del 70%
- Examen abandonado, incompleto o no enviado = reprobado automático
- Acceso por URL a fase siguiente = bloqueado con redirección
- Recarga de página no rompe la restricción
- La validación debe vivir en: renderizado, routing, estado, persistencia

Cuando termines, prueba estos 5 escenarios y documenta el resultado de cada uno:

1. Usuario aprueba con 75%
2. Usuario obtiene 60%
3. Usuario cierra el examen a mitad
4. Usuario escribe manualmente la URL de la fase siguiente
5. Usuario recarga la página durante el examen

---

## PRIORIDAD 2 — Persistencia y prevención de manipulación

Audita y endurece:

- localStorage, sessionStorage, estado global, query params
- Navegación directa a vistas protegidas
- Posibilidad de alterar nota, fase o ranking desde la consola del navegador

Documenta cada vulnerabilidad encontrada con: descripción, riesgo, corrección aplicada.
Si no se puede cerrar completamente por falta de backend, deja registro claro del riesgo residual.

---

## PRIORIDAD 3 — Integridad de navegación

Valida el 100% de rutas, botones, menús, enlaces internos y externos, guards y redirecciones.

Crea el archivo `RUTAS_AUDITADAS.md` con esta tabla por cada elemento:

| Ruta/Enlace | Estado inicial | Problema | Corrección | Estado final |
|---|---|---|---|---|

---

## PRIORIDAD 4 — Motor de evaluación avanzado

Refactoriza o extiende el motor de evaluación para soportar:

### A. Preguntas visuales (planos interactivos)
- El usuario hace clic sobre una imagen/plano
- Se valida si el clic fue en la zona correcta
- Se da feedback visual
- El resultado se registra en el scoring
- La pregunta puede marcarse como "crítica"

### B. Árboles de decisión
- Una respuesta determina qué pregunta o escenario sigue
- Se registra el recorrido completo del usuario
- Se diferencia entre error menor y error crítico

### C. Active recall intercalado
- Fases avanzadas pueden incluir preguntas de fases anteriores
- Las preguntas se etiquetan con su fase de origen
- Son compatibles con el scoring general y con marcación crítica

---

## PRIORIDAD 5 — Ranking Top 3 y recompensa

Implementa el ranking con esta lógica de desempate en orden estricto:

1. Mayor puntaje total
2. Menor cantidad de errores en preguntas críticas
3. Menor tiempo total

El ranking solo se muestra cuando el usuario completa el 100% de las fases.

Si el usuario clasifica en el Top 3, mostrar **exactamente** este mensaje:

> *"Felicidades. Has clasificado en el Top 3 y eres acreedor de una asesoría personalizada para la elaboración de tu plan NRD-2."*

Este mensaje no debe aparecer por error, manipulación del cliente ni navegación directa.

---

## DOCUMENTO "MEJORAS NRD-2" — obligatorio

Localiza el archivo, léelo y crea `MATRIZ_NRD2.md` con:

| Mejora solicitada | Evidencia en código | Brecha | Acción aplicada | Estado final | Observaciones |
|---|---|---|---|---|---|

Todo lo que no puedas implementar debe quedar documentado con razón técnica precisa.

---

## ENTREGABLES OBLIGATORIOS

Al finalizar debes tener estos archivos generados:

- `AUDITORIA_INICIAL.md` — diagnóstico del estado inicial
- `RUTAS_AUDITADAS.md` — inventario de navegación
- `MATRIZ_NRD2.md` — cumplimiento de mejoras
- `CAMBIOS_REALIZADOS.md` — archivos modificados, funciones afectadas, validaciones agregadas
- `RIESGOS_PENDIENTES.md` — qué no se pudo completar y por qué
- `ESTADO_FINAL.md` — clasificación del sistema

---

## RESTRICCIONES ABSOLUTAS

- No reportes como implementado algo que solo quedó sugerido
- No elimines lógica existente sin documentarlo
- No supongas que algo funciona sin probarlo
- Si falta backend, credenciales o contexto, documéntalo con precisión
- No cierres la tarea sin los 6 archivos de entregables creados
