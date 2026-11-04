# Matriz de Reglas de Negocio y Validación

| ID   | Regla | Caso de uso | Tipo |
|------|--------|-------------|------|
| RN01 | El DNI debe tener exactamente 8 dígitos. | CU-002 / CU-003 | Validación |
| RN02 | La hora de la marcación la define siempre el servidor. | CU-002 | Regla de negocio |
| RN03 | El estado Puntual o Tardanza depende del horario del turno y de su tolerancia. | CU-002 | Regla de negocio |
| RN04 | La tolerancia máxima configurable es de 15 minutos. | CU-004 | Validación |
| RN05 | El registro de un trabajador exige su consentimiento de datos personales. | CU-003 | Validación |
| RN06 | El motivo es obligatorio en toda corrección de asistencia. | CU-006 | Validación |
| RN07 | Toda corrección conserva el valor anterior, quién la hizo y cuándo. | CU-006 | Regla de negocio |
| RN08 | Un trabajador dado de baja no puede registrar marcaciones. | CU-002 | Excepción |
