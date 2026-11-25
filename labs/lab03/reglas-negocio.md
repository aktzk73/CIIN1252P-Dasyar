|ID |Regla | Caso de uso | Tipo |
| - | - | - | - | 
| RN01 | La hora de la marcación la define siempre el servidor | CU02 | Regla de negocio
| RN02 | El DNI debe tener exactamente 8 dígitos | CU02 / CU03 | Validación
| RN03 | El DNI de cada trabajador es único | CU03 | Validación
| RN04 | El motivo es obligatorio en toda corrección de asistencia | CU06 | Validación
| RN05 | Un trabajador dado de baja no puede registrar marcaciones | CU02 | Excepción
| RN06 | Un trabajador tiene entre 1 y 2 turnos | CU03 / CU04 | Validación
| RN07 | Puntual o Tardanza depende del horario del turno y de su tolerancia | CU02 / CU04| Regla de negocio
| RN08 | Si ya existe una entrada en el día, la siguiente marcación es una salida | CU02| Regla de negocio
| RN09 | Un día con turno y sin marcaciones se registra como FALTA | CU09 | Regla de negocio
| RN10 | Una entrada sin salida deja la asistencia como INCOMPLETO | CU09 | Regla de negocio
