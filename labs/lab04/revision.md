**Facilitador**: Repasemos las 7 historias. MoSCoW dejó cuatro Must (HU-01 a HU-04), dos Should (HU-05 y HU-06) y un Could (HU-07). La votación de 100 puntos coincide: las cuatro Must suman el 73% del valor, y HU-02 es la que más pesa, con 25. Empecemos por las Must.

**Product Owner**: Las cuatro son necesarias para que el sistema funcione: el acceso, la marcación, los trabajadores y los turnos. Deben ir en el primer sprint.

**Desarrollador 1**: HU-01 y HU-04 son pequeñas, 2 puntos cada una. HU-01 ya tiene el modal del PIN en la maqueta.

**Desarrollador 2**: HU-02 y HU-03 son de 3 puntos: la marcación valida el DNI, el turno y el estado, y la gestión incluye consentimiento y baja. Para probar HU-02 cargaremos trabajadores de prueba y así no dependemos de HU-03.

**Facilitador (con IA colaborativa)**: Le pedí a la IA que revisara las historias, sus criterios Gherkin y la priorización. Confirma que MoSCoW y los 100 puntos coinciden en lo esencial. También señaló que el cálculo diario de faltas y el cambio de contraseña no tienen historia propia.

**Product Owner**: Quedan en el backlog para decidir después, con prioridad para el cálculo de faltas. Dentro del Sprint 1, el orden lo marcan las dependencias: primero los turnos, luego el acceso, la marcación y por último los trabajadores. En el Sprint 2 va primero corregir (HU-06) antes que exportar (HU-07), por la integridad de los datos.

**Acuerdo final de sprint**
| Sprint | Historias (en orden)| Puntos |
|-|-|-|
|Sprint 1|	HU-04 → HU-01 → HU-02 → HU-03|	10|
|Sprint 2|	HU-05 → HU-06 → HU-07	|8|
|Backlog|	Cálculo diario de faltas (CU-009) y cambio de contraseña (CU-008)	|—|
