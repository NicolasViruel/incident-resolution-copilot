# Evaluación

El MVP tiene éxito cuando ayuda a quienes responden a incidentes a encontrar orientación segura y fundamentada más rápido que mediante una búsqueda sin asistencia, mientras preserva el control humano.

## Evaluar antes de ampliar

Usar un conjunto curado y saneado de evaluación con consultas, tickets y documentos fuente sobre incidentes. Mantener disponibles la evidencia esperada y el criterio de revisión para cada caso.

## Medidas principales

| Medida | Pregunta | Evidencia de éxito |
| --- | --- | --- |
| Cobertura de citas | ¿Cada diagnóstico cita material de respaldo? | Presencia de citas y trazabilidad de la fuente. |
| Fundamentación | ¿Las afirmaciones coinciden con la evidencia citada? | Revisión humana frente al material fuente. |
| Calibración de confianza | ¿La evidencia de menor calidad produce menor confianza? | Comparación de la confianza con el criterio de revisión. |
| Utilidad de la clasificación | ¿La categoría del ticket ayuda a la clasificación inicial o a la derivación? | Calificación de utilidad de la persona revisora. |
| Seguridad de la recomendación | ¿Los pasos sugeridos son adecuados para la aprobación humana? | Revisión de seguridad; sin ejecución autónoma. |
| Utilidad humana | ¿La respuesta ayudó a la persona que responde a avanzar? | Comentarios explícitos recopilados por respuesta. |

## Protocolo de evaluación

1. Crear fixtures que eliminen secretos e identifiquen la procedencia de su fuente.
2. Definir las citas esperadas, las clasificaciones aceptables y las restricciones de seguridad para cada caso.
3. Ejecutar los mismos casos contra una implementación candidata.
4. Solicitar a las personas revisoras que califiquen de forma independiente la fundamentación, la utilidad y la seguridad de las recomendaciones.
5. Investigar las afirmaciones sin citas, los pasos inseguros y las respuestas con exceso de confianza antes de ampliar el alcance.

## Criterios mínimos de aceptación

- Ningún diagnóstico aceptado carece de citas.
- La evidencia insuficiente se comunica en lugar de adivinar.
- Las sugerencias son revisables y requieren aprobación humana antes de realizar cambios.
- Cada caso de evaluación puede reproducirse a partir de fixtures saneadas.
- Los comentarios se almacenan por separado de los criterios de corrección.

## No es objetivo

La evaluación no autoriza la automatización en producción, no reemplaza la revisión experta de incidentes ni considera una puntuación positiva de utilidad como prueba de que una respuesta sea correcta.
