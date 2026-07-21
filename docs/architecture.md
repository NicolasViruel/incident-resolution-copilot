# Arquitectura

El MVP es un asistente que prioriza la evidencia, no un respondedor autónomo de incidentes. Las decisiones tecnológicas se posponen deliberadamente.

## Flujo previsto

1. Incorporar conocimiento aprobado y saneado sobre incidentes, con metadatos de origen.
2. Normalizar e indexar ese material para su recuperación.
3. Recibir un ticket o una consulta sobre un incidente y clasificarlo.
4. Recuperar evidencia pertinente y elaborar un diagnóstico únicamente a partir de ella.
5. Devolver citas, confianza, incertidumbre y próximos pasos sugeridos y seguros.
6. Recopilar comentarios humanos sobre la utilidad para una evaluación posterior.

## Modelo de límites

| Límite | Responsabilidad | No debe hacer |
| --- | --- | --- |
| Ingesta | Preservar la identidad, la fuente, la marca de tiempo y las restricciones de acceso del documento. | Tratar material no aprobado o secreto como una entrada común. |
| Recuperación | Devolver evidencia pertinente y rastreable. | Ocultar fuentes o fabricar evidencia. |
| Razonamiento | Relacionar la evidencia con el síntoma informado y expresar la incertidumbre. | Producir un diagnóstico sin citas. |
| Recomendación | Sugerir pasos seguros, revisables y rutas de escalamiento. | Ejecutar acciones de producción. |
| Comentarios | Capturar si las personas consideraron útil una respuesta. | Dar a entender que los comentarios por sí solos demuestran corrección. |

## Contrato de respuesta

Cada respuesta dirigida a la persona usuaria debe diferenciar:

- **Clasificación:** la categoría del ticket y cualquier señal de derivación.
- **Diagnóstico:** la explicación respaldada por evidencia o un resultado explícito de evidencia insuficiente.
- **Evidencia:** las citas que identifican el material recuperado.
- **Confianza:** una indicación visible del respaldo y de la incertidumbre.
- **Pasos sugeridos:** acciones seguras revisadas por humanos y orientación para el escalamiento.

## Invariantes de seguridad

- El sistema no realiza acciones autónomas en producción.
- Un diagnóstico sin citas de respaldo se rechaza o se etiqueta como evidencia insuficiente.
- Todo cambio operativo requiere aprobación humana explícita fuera del copiloto.
- La evidencia ausente, contradictoria o débil reduce la confianza y se muestra a la persona usuaria.

## Decisiones diferidas

Este andamio no selecciona un lenguaje de programación, un marco de trabajo, un proveedor de modelos, un almacén vectorial, una integración con tickets, un modelo de identidad, una plataforma de alojamiento ni una estrategia de despliegue. Esas decisiones deben seguir un plan de evaluación y requisitos de seguridad documentados.
