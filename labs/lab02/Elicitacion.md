# Lab02: Elicitación y Análisis de Requerimientos 
## 1: ESPECIFICACIÓN IEEE 29148 Y TÉCNICAS DE RECOLECCIÓN
### 1.1. Nombre del proyecto
Sistema de Control de Asistencia Dasyar
### 1.2. Estructura SRS
El propósito de este sistema es digitalizar el registro de asistencia del personal. Los usuarios serán los trabajadores (registro de entradas/salidas mediante DNI) y el administrador (configuración de horarios y exportación de reportes a fin de mes).
### 1.3. Técnicas de Recolección 
#### 1.3.1. Técnica 1 (Entrevista)
Entrevistado: Administrador de la fábrica.
Dato clave obtenido: "Invierto demasiado tiempo revisando cuadernos físicos para cuadrar los horarios y tolerancias de cada turno, lo que retrasa el cálculo de las horas trabajadas".
#### 1.3.2. Técnica 2 (Encuesta):
Pregunta propuesta: ¿Considera que digitar su número de DNI en un teclado digital agilizará el proceso de ingreso en comparación con buscar su nombre y firmar en el cuaderno actual?
Resultado esperado: La gran mayoría indicará que sí, ya que digitar 8 números toma solo un par de segundos y evitará las aglomeraciones actuales.
#### 1.3.3. Técnica 3 (Observación):
¿Qué proceso manual o ineficiente observas actualmente?: Se observa a los trabajadores haciendo largas colas para firmar un cuaderno 4 veces al día. A menudo, las firmas son ilegibles o los operarios olvidan marcar, complicando el trabajo del administrador.

## 2: STAKEHOLDERS Y CATÁLOGO DE REQUISITOS (Subtema 2.2) 
### 2.1. Lista de Stakeholders: 
1. Trabajador / Operario de planta (Primario - Registra asistencia diaria).
2. Administrador de la fábrica (Primario - Configura horarios de trabajo y extrae reportes).
### 2.2. Catálogo de Requisitos (Escribe 2 RF y 2 RNF para tu proyecto): 
- RF-01: El sistema debe permitir registrar a un trabajador con los parametros nombre y DNI.
- RF-02: El sistema debe permitir registrar la hora de entrada y salida de un trabajador.
- RNF-01: Seguridad: El sistema debe garantizar la seguridad y protección de los datos sensibles de los trabajadores.
- RNF-02: Usabilidad: El sistema debe asegurar que el proceso de registro de asistencia de los trabajadores sea menos de 1 minuto, sin capacitacion previa.

## 3. VALIDACIÓN DE REQUISITOS Y RESOLUCIÓN DE CONFLICTOS
### 3.1. Posible conflicto entre Stakeholders
- Postura del Trabajador: Desea que el teclado para digitar el DNI esté en una zona de libre acceso para marcar rápido y entrar directo a su puesto.
- Postura del Administrador: Sabe que al usar solo el DNI existe el riesgo de "suplantación" (que alguien digite el DNI de un compañero que viene tarde). Exige que el registro sea seguro y confiable.
### 3.2. Matriz de Decisión
Opción A: Terminal bajo libre acceso sin supervision visual del administrador
Opción B: Terminal de libre acceso bajo supervision   
|  Criterio  |  Peso(%)  |  Opcion A  | Opcion B|
| - | - | - | - |
| Seguridad anti suplantacion  | 60% | 1 | 5 |
| Agilidad para el trabajador | 40% | 5 | 3 |
| Puntaje Ponderado Total | 100% | 2.6 | 4.2 |


Criterio 1 (60%):   - Puntaje A: 0.6   - Puntaje B: 3.0 
Criterio 2 (40%):   - Puntaje A: 2.0   - Puntaje B: 1.2 
Decisión final elegida: Se elige la OPCIÓN B. Dado que el sistema solo validará por DNI, ubicar el terminal bajo supervisión es la forma más efectiva de disuadir las suplantaciones sin necesidad de hardware adicional ni cambiar el alcance del software.


## 4. HERRAMIENTAS DE APOYO AL ANÁLISIS
### 4.1. Buyer Persona
- Nombre: Juan, el Operario de Producción (35 años).
- Rol: Trabajador de planta en la fábrica.
- Frase que lo defina: "Quiero marcar mi asistencia rápido al llegar para ir a mi puesto y evitar problemas."
### 4.2. Mapa de Empatía
| Piensa/Siente| Dice| Hace| Oye|
|-|-|-|-|
|Siente frustración cuando llega a tiempo, puesto que las colas para firmar lo retrasan.|"¿Alguien sabe si ya arreglaron el reloj de la entrada? No quiero que anoten mi hora mal".|Hace fila apresuradamente 4 veces al día, buscando su nombre en un cuaderno lleno de tachones.|Quejas de los compañeros y del administrador por el desorden en el cuaderno de firmas.|
### 4.3. Story Map
|Actividad Principal|Tarea 1|Tarea 2|
|-|-|-|
|Gestionar Asistencia y Reportes|Como trabajador operario, quiero registrar mi asistencia digitando rápidamente mi DNI, para evitar aglomeraciones y asegurar mi hora exacta de entrada/salida.|Como administrador, quiero exportar a Excel el reporte consolidado de horas trabajadas en los periodos de pago, para obtener la información exacta de las asistencias sin tener que sumar registros manuales.|
