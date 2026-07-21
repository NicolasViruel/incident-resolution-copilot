# Contribuir

Ayude a construir un copiloto que sea útil durante los incidentes sin quitar el control a quienes responden ante ellos.

## Antes de contribuir

1. Leer `README.md`, `docs/architecture.md` y `docs/evaluation.md`.
2. Mantener las propuestas enfocadas en un único resultado que pueda revisarse.
3. Explicar cómo el cambio preserva la evidencia, las citas, la confianza y la aprobación humana.

## Principios de contribución

- Tratar el material fuente como evidencia: preservar su procedencia y evitar conclusiones sin respaldo.
- Mantener las acciones de producción explícitas y sujetas a aprobación humana.
- Usar muestras de prueba saneadas; nunca incluir secretos, credenciales, datos de clientes ni exportaciones sin procesar de incidentes de producción.
- Preferir cambios pequeños y reversibles con pruebas focalizadas cuando comience la implementación.
- Mantener la documentación concisa y alineada con el alcance del MVP.

## Cambios que se deben revisar

Cada cambio de implementación debe identificar:

- la evidencia de entrada y las citas esperadas;
- el comportamiento de la confianza, incluido qué sucede cuando la evidencia es insuficiente;
- los pasos propuestos y sus restricciones de seguridad;
- las pruebas o los casos de evaluación; y
- el límite de reversión.

## Guía para confirmaciones

Usar mensajes de confirmación convencionales. Mantener el código, las pruebas y la documentación que explica un comportamiento dentro de la misma unidad de trabajo.

Ejemplos:

```text
feat(ingesta): preservar la procedencia del documento
fix(recuperación): rechazar respuestas sin citas
docs(evaluación): definir la rúbrica de fundamentación
```

## Comunicar inquietudes

No incluir detalles sensibles de incidentes en incidencias públicas, confirmaciones ni fixtures. Si una contribución pudiera debilitar los límites de seguridad, pausar el cambio y comunicar la inquietud a las personas mantenedoras del repositorio.
