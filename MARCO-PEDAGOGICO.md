# Marco Pedagógico: Protocolo Fortaleza v2.0
## Arquitectura de la Pericia - CONRED NRD-2

### Fundamentos Científicos

**1. Recuperación Activa (Active Recall)**
- Los participantes NO leen pasivamente. Cada módulo inicia con preguntas diagnósticas.
- Cuestionarios tipo Socratic que fuerzan la construcción de respuestas antes de revelar la solución.
- Base: Karpicke & Blunt (2011) - Testing enhances learning.

**2. Repetición Espaciada (Spaced Repetition)**
- Flashcards técnicas con datos críticos (medidas, fórmulas, plazos legales).
- Cada fase refuerza conceptos de fases anteriores mediante vínculos cruzados.
- Base: Ebbinghaus Forgetting Curve + Leitner System.

**3. Metacognición**
- Sección "Despertar Legal" como checkpoint obligatorio antes de avanzar.
- Auto-evaluación: el participante calibra su confianza antes y después de cada módulo.
- Base: Flavell (1979) - Metacognitive monitoring.

**4. Codificación Dual**
- Videos + Audios podcast + Material escrito interactivo para cada fase.
- Combinación visual-auditiva-kinestésica (formularios interactivos).
- Base: Paivio (1986) - Dual Coding Theory.

**5. Chunking Cognitivo**
- Cada fase dividida en 3 módulos: Diagnóstico → Fichas Técnicas → Guía de Estudio.
- Máximo 4-5 conceptos por bloque para respetar la memoria de trabajo.
- Base: Miller (1956) - The magical number 7±2.

**6. Andamiaje (Scaffolding)**
- Progresión bloqueada: Fase N+1 requiere completar Fase N.
- Dificultad incremental: Conceptos → Aplicación → Análisis → Síntesis.
- Base: Vygotsky (1978) - Zone of Proximal Development.

### Estructura por Fase

Cada fase sigue el patrón **D-F-G**:
- **D**iagnóstico (Cuestionario de Recuperación Activa)
- **F**ichas Técnicas (Repetición Espaciada con Flashcards)
- **G**uía de Estudio (Metacognición y Modelos Mentales)

### Arquitectura Técnica

```
Protocolo-Fortaleza-v2/
├── index.html          ← Portal maestro (dashboard)
├── fase-0.html         ← El Despertar Legal (siempre primero)
├── fase-1.html         ← Diagnóstico de Amenazas
├── fase-2.html         ← Arquitectura de Respuesta
├── fase-3.html         ← NRD-2 y Señalización
├── fase-3-1.html       ← Guía de Señalización
├── fase-4.html         ← Inventario y Recursos
├── MARCO-PEDAGOGICO.md ← Este documento
└── README.md           ← Instrucciones para GitHub
```

Cada archivo HTML es **independiente** (CSS embebido). Modificar uno NO afecta a los demás.
El portal maestro (index.html) lee el progreso de localStorage para manejar bloqueos.
