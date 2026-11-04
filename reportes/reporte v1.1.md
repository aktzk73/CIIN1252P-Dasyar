# Reporte de trazabilidad v1.1

| Métrica | Valor |
|---|---|
| Requisitos totales | 8 |
| Requisitos con prueba | 8 |
| Cobertura | 100 % |
| Requisitos modificados por CR-001 | REQ-005 |
| Artefactos modificados | SRS, CU-004, CLS-Turno, PRU-005a, PRU-005b |

## Cambios frente a v1.0
- REQ-005 pasó de "configurar turnos y tolerancia de entrada" a "configurar turnos y una tolerancia de entrada de hasta 15 minutos como máximo".
- Se agregaron 2 pruebas (PRU-005a y PRU-005b), 1 atributo (toleranciaMinutos) y 1 método (validarTolerancia).
