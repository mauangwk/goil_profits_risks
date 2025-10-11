## Descripción de datos

Los datos de exploración geológica de las tres regiones se almacenan en archivos:

- `geo_data_0.csv`
- `geo_data_1.csv`
- `geo_data_2.csv`


- *id* — identificador único de pozo de petróleo
- *f0, f1, f2* — tres características de los puntos (su significado específico no es importante, pero las características en sí son significativas)
- *product* — volumen de reservas en el pozo de petróleo (miles de barriles).

### Analisis de negocio y Consideraciones

* Necesidades: 200 pozos
* Presupuesto: 100 mdd
* 1 Barril = 4.5 usd ingresos
* 1 Unidad = 1000 barriles = 4500 usd
* volumen de reserva = unidades = Miles de barriles
* Para evitar perdidas, un pozo debe producir 111.1 unidades o 500,000 dolares

Se debe seleccionar 
* La region con el beneficio promedio mas alto
* Riesgo de perdidas inferior a 2.5