# Pruebas (v1.1-iter2)

| ID | Requisito | Qué se prueba | Resultado esperado |
|---|---|---|---|
| PRU-001 | REQ-001 | Registrar un trabajador con un DNI de 8 dígitos válido | Trabajador registrado y en estado Activo |
| PRU-002 | REQ-002 | Un trabajador Activo ingresa su DNI para marcar Entrada | Marcación de Entrada guardada con fecha y hora |
| PRU-003 | REQ-003 | Generar el reporte de asistencia de un periodo con datos | Reporte con la Asistencia de cada trabajador del periodo |
| PRU-004 | REQ-004 | Iniciar sesión como administrador con contraseña correcta | Acceso concedido al panel de administración |
| PRU-005 | REQ-005 | Configurar un turno y su tolerancia en minutos | Configuración guardada y aplicada al cálculo de tardanzas |
| PRU-006 | REQ-006 | Corregir una asistencia indicando el motivo | Asistencia corregida y motivo registrado |
| PRU-007 | REQ-007 | Cambiar la contraseña del administrador con datos válidos | Contraseña actualizada; el siguiente acceso usa la nueva |
| PRU-008 | REQ-008 | Calcular faltas y horas extras de un trabajador en un periodo | Faltas y horas extras calculadas según su Turno |
| PRU-005a | Tolerancia de 15 minutos (límite) | Se guarda la configuración | CR-001 |
| PRU-005b | Tolerancia de 20 minutos | Se rechaza y se muestra el mensaje de máximo 15 minutos | CR-001 |

