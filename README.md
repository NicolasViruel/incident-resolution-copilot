# Copiloto de Resolución de Incidentes

Un copiloto respaldado por evidencia para ayudar a los equipos de ingeniería a diagnosticar y resolver incidentes técnicos. El MVP transforma material aprobado sobre incidentes en respuestas fundamentadas y mantiene al operador humano al control de cada decisión operativa.

## Resultado del MVP

Una persona de ingeniería puede proporcionar un ticket o una consulta sobre un incidente y recibir:

- una clasificación del ticket o de la solicitud;
- un diagnóstico fundamentado en evidencia recuperada sobre incidentes;
- citas y una señal explícita de confianza;
- próximos pasos sugeridos y seguros para la revisión humana; y
- una forma de indicar si la respuesta fue útil.

## Alcance

| Capacidad | Propósito del MVP |
| --- | --- |
| Ingesta | Incorporar documentos y registros aprobados sobre incidentes a una base de conocimiento consultable. |
| Recuperación | Recuperar evidencia pertinente para una consulta o un ticket. |
| Respuestas fundamentadas | Presentar un diagnóstico basado en recuperación y generación, con citas y confianza. |
| Pasos sugeridos | Ofrecer acciones seguras y reversibles para la aprobación humana. |
| Clasificación | Categorizar los tickets entrantes para facilitar su derivación y clasificación inicial. |
| Comentarios | Recopilar comentarios humanos sobre la utilidad para mejorar la evaluación e iteraciones futuras. |

## Límites de seguridad

- No realiza acciones autónomas en producción.
- No emite diagnósticos sin citas.
- Requiere aprobación humana antes de cualquier cambio.

El copiloto puede explicar la evidencia y proponer un plan. No debe ejecutar cambios, afirmar una certeza mayor que la que permite la evidencia disponible ni reemplazar la responsabilidad sobre el incidente.

## Estructura del repositorio

| Ruta | Propósito |
| --- | --- |
| `app/` | Implementación futura del producto. |
| `tests/` | Pruebas automatizadas futuras. |
| `data/documents/` | Material fuente aprobado para la ingesta. No agregar secretos ni exportaciones de producción. |
| `fixtures/` | Muestras saneadas y reproducibles para desarrollo y evaluación. |
| `docs/architecture.md` | Arquitectura neutral respecto de la tecnología y modelo de seguridad. |
| `docs/evaluation.md` | Medidas de éxito del MVP y protocolo de evaluación. |

## Comenzar por aquí

1. Leer [la arquitectura](docs/architecture.md) para conocer los límites y el flujo previstos.
2. Leer [el plan de evaluación](docs/evaluation.md) antes de seleccionar detalles de implementación.
3. Leer [la guía de contribución](CONTRIBUTING.md) antes de proponer cambios.

## Estado actual

Este repositorio es únicamente un andamio documental. Aún no existe implementación de la aplicación, decisión de tecnología, configuración de despliegue ni integración con producción. Por lo tanto, no se puede iniciar ni probar funcionalmente en este momento.

## Próximo paso

Se requiere implementar el producto y tomar una decisión tecnológica documentada antes de poder iniciarlo o realizar pruebas funcionales.

## Contribuciones

Consultar [CONTRIBUTING.md](CONTRIBUTING.md). Las contribuciones deben preservar la trazabilidad de la evidencia, los límites de seguridad y la neutralidad tecnológica hasta que se tome una decisión de implementación.
