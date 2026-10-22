# Modelos de forecast: Tigre Bol y CHARDON

Resumen de lo reportado por cada agente el 22/10/2026.

## Tigre Bol (Tigre Bolivia)
- **Modelos:** selección dinámica por material del modelo con menor error reciente (decaimiento 0,6 sobre 8 meses). Candidatos: Chronos-Bolt, TimesFM 2.5, LightGBM, Croston y tensor de bajo rango. La política oficial promedia 50/50 la selección dinámica con Chronos; reconciliación jerárquica MinT-shrink (material, familia, categoría) e intervalo conformal del 80 %. Clasificación de demanda Syntetos-Boylan. Estacionalidad 50 % propia y 50 % de la familia.
- **Variables de entrada:** ventas mensuales (Anio, Mes, Segmento, Canal, Region, Material, Piezas, Kg): 155.144 filas, 2.040 materiales, ene-2021 a ago-2026. Maestro de productos (Familia, Grupo, Linea, Sistema). Las devoluciones no restan demanda.
- **Horizonte:** mensual, en piezas por material; validación de 1 a 3 meses.
- **Frecuencia:** mensual, corrida manual (ENTRADA\ a SALIDA\<periodo>\).
- **Métricas:** backtest rolling con 11 cortes, ponderado por kg.
  - Política oficial: WMAPE SKU 37,2 %, sesgo −6,0 %, WMAPE familia×mes 19,2 %, MASE 1,114.
  - Motor anterior: WMAPE SKU 48,2 %, sesgo +4,5 %, WMAPE familia×mes 25,3 %, MASE 1,207.
  - Chronos solo 36,6 %; TimesFM solo 36,9 %.

## CHARDON
- **Modelo actual:** clasificación ABC, XYZ (18 meses) y Syntetos-Boylan. SES, Holt, Croston y SBA con ajuste estacional multiplicativo; Prophet para A+suave+X y Darts ES para A con demanda Y/Z. El ganador por SKU es el de menor RMSE % en prueba de 6 meses.
- **Rediseño propuesto (no implementado):** StatsForecast (AutoETS, Theta, MSTL, Croston/SBA/TSB, ADIDA, IMAPA) más LightGBM, selección dinámica con decaimiento 0,6 sobre 8 meses y rango conformal del 80 %.
- **Variables de entrada:** ventas mensuales en unidades por SKU, 656 SKU, ene-2023 a jun-2026. Maestro de artículos (precio promedio, lead time, estado) y ABC.
- **Horizonte:** 18 meses.
- **Frecuencia:** mensual al cierre, corrida manual.
- **Métricas:** RMSE % en prueba de 6 meses, sin valor agregado documentado. El rediseño medirá WMAPE, sesgo, RMSE y MASE en 8 cortes, aún sin resultados.
