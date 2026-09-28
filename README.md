# LISTA-DE-ESPERA-MAMA

Dashboard estadístico de la lista de espera (mamografía, ecografía mamaria, consulta de mastología, biopsia, cirugía).

## Uso

1. Abre `index.html` en el navegador.
2. Pulsa **Cargar CSV o Excel** (o arrastra el archivo) con tu lista de espera. El archivo se procesa solo en el navegador; no se envía a ningún servidor.
3. Filtra por procedimiento, prioridad y establecimiento, y ajusta el umbral de días.

Sin archivo, el tablero muestra **datos de ejemplo ficticios**.

## Formato del archivo

Una fila por caso. Ver `plantilla_lista_espera.csv`. Columnas reconocidas (solo `fecha_ingreso` es obligatoria):

| Columna | Descripción |
|---|---|
| `id` | Identificador o RUT |
| `fecha_ingreso` | Fecha de ingreso a la lista (AAAA-MM-DD o DD/MM/AAAA) |
| `fecha_atencion` | Fecha de resolución; vacía si sigue pendiente |
| `estado` | Pendiente, Atendida o Cancelada |
| `prioridad` | Alta, Media, Baja |
| `procedimiento`, `establecimiento`, `edad` | Opcionales |

## Estadísticas

- Casos pendientes, mediana, promedio y percentil 90 de días de espera.
- Casos que superan el umbral (90 días por defecto) con nivel de alerta.
- Espera mediana hasta la atención y balance ingresos/atenciones de los últimos 90 días.
- Distribución por antigüedad, flujo mensual de 12 meses, pendientes por procedimiento, prioridad, establecimiento y tramo de edad.
- Los 15 casos pendientes más antiguos.
