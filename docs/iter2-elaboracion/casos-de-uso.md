# Casos de uso (v1.1)

## CU-001: Autenticar administrador (cubre REQ-004)
- Actor: Administrador
- Flujo principal:
  1. El administrador pulsa el botón "Administración".
  2. Ingresa su PIN.
  3. Pulsa "Ingresar".
  4. El sistema valida el PIN y muestra el panel principal.

## CU-002: Registrar marcación (cubre REQ-002)
- Actor: Trabajador
- Flujo principal:
  1. El trabajador escribe su DNI en el teclado numérico.
  2. Pulsa "Marcar".
  3. El sistema valida que el DNI tenga 8 dígitos y que esté activo.
  4. El sistema determina el turno del trabajador.
  5. El sistema registra la entrada, o la salida si ya hay una entrada, con la hora del servidor.
  6. El sistema calcula si la marcación es Puntual o Tardanza.
  7. El sistema muestra la confirmación con el nombre, la hora y el estado.

## CU-003: Gestionar trabajadores (cubre REQ-001)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre la sección de trabajadores.
  3. Elige registrar un trabajador nuevo (o editar o dar de baja a uno existente).
  4. Ingresa sus datos (DNI, nombres, apellidos y turnos) y registra su consentimiento de datos personales.
  5. Pulsa "Guardar".
  6. El sistema guarda los datos del trabajador y confirma.

## CU-004: Configurar turnos y tolerancia (cubre REQ-005)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre la sección de configuración.
  3. Define el horario de cada turno y la tolerancia de entrada.
  4. Pulsa "Guardar".
  5. El sistema guarda la configuración y confirma.
- Flujo alterno: si la tolerancia es mayor a 15 min, el sistema rechaza la configuración y muestra el mensaje "La tolerancia máxima es de 15 minutos".

## CU-005: Consultar y filtrar asistencia (cubre REQ-003)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre el panel de asistencia.
  3. Elige los filtros (trabajador, fecha o turno).
  4. Pulsa "Consultar".
  5. El sistema muestra los registros de asistencia con su estado (Puntual, Tardanza o Falta).

## CU-006: Corregir asistencia (cubre REQ-006)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. En el panel de asistencia, elige el registro con error u omitido.
  3. Pulsa "Corregir".
  4. Ingresa el nuevo valor y el motivo de la corrección.
  5. Pulsa "Guardar".
  6. El sistema verifica la sesión y que el motivo no esté vacío.
  7. El sistema guarda quién corrigió, cuándo y el valor anterior, actualiza la marcación y recalcula el estado.
  8. El sistema muestra la confirmación.

## CU-007: Exportar asistencia a Excel (cubre REQ-003)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. Consulta la asistencia con los filtros que necesite.
  3. Pulsa "Exportar a Excel".
  4. El sistema genera el archivo y lo descarga.

## CU-008: Cambiar contraseña (cubre REQ-007)
- Actor: Administrador
- Flujo principal:
  1. El administrador inicia sesión.
  2. Abre la sección de su cuenta.
  3. Ingresa su PIN actual y el nuevo PIN.
  4. Pulsa "Guardar".
  5. El sistema valida los datos, actualiza el PIN y confirma.

## CU-009: Calcular faltas y horas extras (cubre REQ-008)
- Actor: Reloj del servidor
- Flujo principal:
  1. El reloj del servidor dispara el cálculo diario.
  2. El sistema toma las marcaciones del día y los turnos de cada trabajador.
  3. Compara las marcaciones con el horario y la tolerancia del turno.
  4. Calcula las faltas y las horas extras.
  5. El sistema guarda los resultados en la asistencia para consultarlos en los reportes.
