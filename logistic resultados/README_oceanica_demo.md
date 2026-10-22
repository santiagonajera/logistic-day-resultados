# Oceánica Internacional: resultados Logistic Day

## Contenido
- `forecast_oceanica.html`: dashboard con barra lateral (logo Oceánica arriba, DataChain abajo), pronóstico con slider y zoom, y sección de última milla con mapa de clientes y rutas.
- `modelos_forecast_tigre_chardon.md`: resumen de los modelos de Tigre Bol y CHARDON.
- Datos de trabajo en el equipo: `D:\Oceánica\datos_oceanica.xlsx` con las hojas historico_envios (53.193 filas), clientes, clientes_nicaragua (180), puntos_entrega, flota, viajes_transito y rutas_lastmile.

## Resultados del dashboard
- 53.193 envíos históricos (ene-2016 a ago-2026).
- Selección de modelo por AIC entre Holt-Winters aditivo y multiplicativo, SARIMAX, Theta y Fourier, en 20 series.
- WMAPE promedio del ganador: 13,0 %.
- Proyección a 12 meses (sep-2026 a ago-2027): 5.007 envíos, unos 417 por mes (−0,9 % frente a 5.053).
- Última milla: 30 clientes en 5 zonas (Jinotega, Ocotal, Managua, Juigalpa, León), 10 puntos de entrega y el puerto de Corinto; 1.961 km de rutas y 14 camiones.

## Uso en la presentación
Copiar `forecast_oceanica.html` y los logos (`oceanica.webp`, `datachaindesign.jpg`) a `D:\Oceánica\resultados` y abrir el HTML.
