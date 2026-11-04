# Especificación de 3 Casos de Uso
## 1. CU-001: Autenticar administrador (cubre REQ-004)
|Campo|Detalle|
|-|-|
|Actor Principal|Administrador|
|Precondición|El administrador tiene un PIN registrado en el sistema.|
|Postcondición|El administrador queda con sesión iniciada y ve el panel principal.|
- Flujo principal:
  1. El administrador pulsa el botón "Administración".
  2. Ingresa su PIN.
  3. Pulsa "Ingresar".
  4. El sistema valida el PIN y muestra el panel principal.
- Flujos alternos:
  - Ninguno.
- Excepciones:
  - E1 (paso 4): si el PIN es incorrecto, el sistema rechaza el ingreso y muestra el motivo.
- Reglas de negocio:
  - Ninguno.
## 2. CU-002: Registrar marcación (cubre REQ-002)
|Campo|Detalle|
|-|-|
|Actor Principal|Trabajador|
|Precondición|El trabajador está registrado y activo, y tiene un turno asignado.|
|Postcondición|Queda registrada una entrada o una salida con la hora del servidor y su estado (Puntual o Tardanza).|
- Flujo principal:
  1. El trabajador escribe su DNI en el teclado numérico.
  2. Pulsa "Marcar".
  3. El sistema valida que el DNI tenga 8 dígitos y que esté activo.
  4. El sistema determina el turno del trabajador.
  5. El sistema registra la entrada, o la salida si ya hay una entrada, con la hora del servidor.
  6. El sistema calcula si la marcación es Puntual o Tardanza.
  7. El sistema muestra la confirmación con el nombre, la hora y el estado.
- Flujos alternos:
  - A1 (paso 5): si ya existe una entrada del día, el sistema registra una salida en lugar de una entrada.
- Excepciones:
  - E1 (paso 3): si el DNI no tiene 8 dígitos, el sistema rechaza la marcación y muestra el motivo.
  - E2 (paso 3): si el DNI no está registrado o el trabajador está dado de baja, el sistema rechaza la marcación y muestra el motivo.
- Reglas de negocio:
  - La hora de la marcación la define siempre el servidor.
  - Puntual o Tardanza depende del horario del turno y de su tolerancia (CU-004).
  - El DNI debe tener exactamente 8 dígitos.
## 3. CU-003: Gestionar trabajadores (cubre REQ-001)
|Campo|Detalle|
|-|-|
|Actor Principal|Administrador|
|Precondición|El administrador tiene sesión iniciada.|
|Postcondición|Los datos del trabajador quedan guardados (registrado, editado o dado de baja) con su consentimiento de datos personales.|
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre la sección de trabajadores.
  3. Elige registrar un trabajador nuevo (o editar o dar de baja a uno existente).
  4. Ingresa sus datos (DNI, nombres, apellidos y turnos) y registra su consentimiento de datos personales.
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
  - El registro del trabajador exige el consentimiento de datos personales.
  - Un trabajador dado de baja no puede registrar marcaciones.
