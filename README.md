# Tutor inteligente ingles EVA
# Tutor Virtual Inteligente Adaptativo para Aprender Inglés

Sistema de Tutoría Inteligente (ITS) totalmente implementado y entrenado para su integración en plataformas LMS (Moodle/Canvas). El sistema combina algoritmos de rastreo del conocimiento, procesamiento del lenguaje natural y aprendizaje por refuerzo.

## Arquitectura del Agente Inteligente

El sistema opera bajo un ciclo continuo de tres fases principales:

1. **Percepción (Diagnóstico):**
   * **BKT (Bayesian Knowledge Tracing):** Calcula en tiempo real la probabilidad de dominio del estudiante basada en el historial de aciertos/errores.
   * **Módulo NLP:** Emplea algoritmos de distancia espectral/edición para discernir entre fallos gramaticales y despistes ortográficos (*slips*).
2. **Decisión (Aprendizaje por Refuerzo):**
   * **Q-Learning Entrenado:** Matriz Q pre-entrenada bajo la ecuación de Bellman que selecciona la intervención pedagógica con mayor recompensa esperada.
3. **Acción (Intervención Adaptativa):**
   * Emisión de retroalimentación inmediata, ajuste automático de dificultad o generación de alertas sincrónicas al docente.

## Estructura del Repositorio

* `tutor_ingles.py`: Código ejecutable del sistema con los modelos BKT y Q-Learning entrenados.
* `dataset_estudiantes.csv`: Dataset con datos de interacción y telemetría de estudiantes.
* `requirements.txt`: Lista de dependencias del entorno.

## Ejecución del Sistema

```bash
python tutor_ingles.py
