# Tutor-inteligente-ingles---EVA

# 🇬🇧 Tutor Virtual Inteligente Adaptativo para Aprender Inglés

Este proyecto desarrolla un agente inteligente que actúa como un tutor personalizado de inglés dentro de plataformas virtuales (Moodle/Canvas). El sistema detecta los errores del estudiante en tiempo real y ajusta las lecciones a su nivel exacto.

## 1. Contexto (El Problema)
En los cursos tradicionales de inglés en línea, todos los estudiantes reciben los mismos ejercicios de gramática y vocabulario, al mismo ritmo. 
* Si un estudiante no entiende un tema base (ej. el verbo To Be), la plataforma lo obliga a avanzar hacia temas complejos (ej. Present Perfect), generando frustración y deserción.
* Las correcciones de los profesores tardan días en llegar.

## 2. Pruebas y Diagnóstico (Lo que descubrimos)
Evaluamos modelos de Inteligencia Artificial para enseñar inglés y definimos 3 retos clave:
1. **Estudiantes nuevos (Cold Start):** Cuando alguien entra por primera vez, no sabemos su nivel inicial. Usamos un modelo probabilístico (BKT) para evaluar rápido sus primeras respuestas.
2. **Diagnóstico del error:** Diferenciamos si el alumno cometió un error por despiste (escribió mal una letra) o por falta de conocimiento gramatical profundo usando modelos de lenguaje (SBERT) y redes neuronales (DKT).
3. **Tiempo real:** El tutor debe responder en menos de 500 ms mientras el alumno chatea o resuelve ejercicios.

## 3. La Solución (Arquitectura en 3 Pasos)
El tutor de inglés trabaja mediante un ciclo continuo de 3 módulos:
1. **Percepción (Ver y escuchar):** Analiza las respuestas del estudiante en las guías y sus dudas escritas en el chat interactivo en inglés.
2. **Decisión (Pensar):** Mediante Aprendizaje por Refuerzo (Q-Learning), la IA decide si el alumno necesita una explicación más sencilla, un video corto o un ejercicio de menor dificultad.
3. **Acción (Actuar):** 
   - Da pistas gramaticales paso a paso sin darle la respuesta directa.
   - Ajusta la dificultad de las lecturas y quizzes.
   - Envía una alerta al profesor si el estudiante lleva más de 45 minutos atascado en un tema.
