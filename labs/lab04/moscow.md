## MoSCoW

MoSCoW clasifica cada historia según qué tan indispensable es para que el sistema funcione:

- **MUST:** imprescindible; sin ella el sistema no cumple su propósito.
- **SHOULD:** importante, pero el sistema puede funcionar sin ella al inicio.
- **COULD:** deseable; aporta valor, pero no bloquea nada.
- **WON'T (por ahora):** queda fuera de la iteración actual.

### Resultado

| Historia | Épica | Clasificación | Justificación breve |
|---|---|---|---|
| HU-01 Autenticar administrador | Acceso | **MUST** | Sin PIN, las funciones de administración quedan sin protección. |
| HU-02 Registrar marcación con DNI | Marcación | **MUST** | Es la función central: sin marcación no hay asistencia. |
| HU-03 Gestionar trabajadores | Personal | **MUST** | Sin trabajadores registrados, nadie puede marcar. |
| HU-04 Configurar turnos y tolerancia | Configuración | **MUST** | Sin turnos y tolerancia no se puede determinar si una marcación es Puntual o Tardanza. |
| HU-05 Consultar y filtrar asistencia | Asistencia | **SHOULD** | Es el principal resultado para el administrador, pero los datos ya se guardan sin ella. |
| HU-06 Corregir asistencia | Asistencia | **SHOULD** | Protege la calidad de los datos, pero se necesita después de tener marcaciones. |
| HU-07 Exportar asistencia a Excel | Reportes | **COULD** | Facilita la planilla, pero la asistencia ya se puede consultar en pantalla. |


### Observaciones

- Las 7 historias entran en el alcance, por lo que ninguna quedó como **WON'T**.
- Las historias **Must** suman 10 de los 18 puntos de esfuerzo totales (HU-01: 2, HU-02: 3, HU-03: 3, HU-04: 2).
- El caso de uso CU-008 (cambiar contraseña) y el cálculo diario de faltas y horas extras (CU-009) no tienen historia propia, por lo que no se clasificaron aquí.
- Esta clasificación se contrasta con la técnica de 100 puntos en `paso5b_100_puntos_y_wsjf.md`.
