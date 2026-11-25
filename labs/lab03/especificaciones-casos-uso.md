# Especificación de 3 Casos de Uso
## 1. CU-001: Autenticar administrador (cubre REQ-004)
|Campo|Detalle|
|-|-|
|Actor Principal|Administrador|
|Precondición|El administrador tiene una contraseña registrado en el sistema.|
|Postcondición|El administrador queda con sesión iniciada y ve el panel principal.|
- Flujo principal:
  1. El administrador pulsa el botón "Administración".
  2. Ingresa su contraseña.
  3. Pulsa "Ingresar".
  4. El sistema valida la contraseña y muestra el panel principal.
- Flujos alternos:
  - Ninguno.
- Excepciones:
  - E1 (paso 4): si la contraseña es incorrecta, el sistema rechaza el ingreso y muestra el motivo.
- Reglas de negocio:
  - Ninguno.
## 2. CU-002: Registrar marcación (cubre REQ-002)
|Campo|Detalle|
| - | - |
| Actor principal | Trabajador |
| Precondición | El trabajador está registrado y activo, y tiene un turno asignado. |
| Postcondición | Queda registrada una entrada o una salida con la hora del servidor y su estado (Puntual o Tardanza). Si ocurre una excepción, no se registra ninguna marcación. |
- Flujo principal
  1. El trabajador digita su DNI en el teclado numérico.
  2. Pulsa "Marcar".
  3. El sistema valida que el DNI sea válido (8 dígitos).
  4. El sistema valida que el DNI esté activo.
  5. El sistema determina el tipo de turno.
  6. El sistema valida que la marcación esté dentro del horario del turno.
  7. El sistema valida que el turno aún no tenga marcación de entrada y salida.
  8. El sistema calcula el estado de la marcación (Puntual o Tardanza).
  9. El sistema registra la marcación de asistencia (entrada, o salida si ya existe una entrada), con la hora del servidor.
  10. El sistema muestra la confirmación con el nombre, la hora y el estado.
- Flujos alternos
  - A1: si ya existe una entrada del día para el turno, el sistema registra una salida en lugar de una entrada.
- Excepciones
  - En todas las excepciones, el sistema resetea los campos ingresados y vuelve a solicitar el DNI.
  - E1 (paso 3): si el DNI no es válido, el sistema muestra el aviso "DNI inválido".
  - E2 (paso 4): si el DNI no está activo, el sistema muestra el aviso "DNI inactivo".
  - E3 (paso 6): si la marcación está fuera del horario del turno, el sistema muestra el aviso "Fuera de horario".
  - E4 (paso 7): si el turno ya tiene marcación de entrada y salida, el sistema muestra el aviso "Turno ya registrado".
- Reglas de negocio
  - La hora de la marcación la define siempre el servidor.
  - Puntual o Tardanza depende del horario del turno y de su tolerancia (CU-004).
  - El DNI debe tener exactamente 8 dígitos.
  - Solo se permite una entrada y una salida por turno.
## 3. CU-003: Gestionar trabajadores (cubre REQ-001)
|Campo|Detalle|
|-|-|
|Actor Principal|Administrador|
|Precondición|El administrador tiene sesión iniciada.|
|Postcondición|Los datos del trabajador quedan guardados (registrado, editado o dado de baja).|
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre la sección de trabajadores.
  3. Elige registrar un trabajador nuevo (o editar o dar de baja a uno existente).
  4. Ingresa sus datos (DNI, nombres, apellidos y turnos).
  5. Pulsa "Guardar".
  6. El sistema guarda los datos del trabajador y confirma.
- Flujos alternos:
  - A1 (paso 3): si elige editar, el sistema muestra los datos actuales del trabajador y el administrador modifica los que necesite.
  - A2 (paso 3): si elige dar de baja, el trabajador queda inactivo y ya no puede marcar asistencia.
- Excepciones:
  - E1 (paso 6): si el DNI no tiene 8 dígitos, el sistema rechaza el guardado y muestra el motivo.
  - E2 (paso 6): si el DNI ya está registrado, el sistema rechaza el guardado y muestra el motivo.
- Reglas de negocio:
  - El DNI debe tener exactamente 8 dígitos.
  - Un trabajador dado de baja no puede registrar marcaciones.
