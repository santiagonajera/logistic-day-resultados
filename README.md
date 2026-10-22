# logistic-day-resultados

Repo privado: datos, scripts y resultados precomputados para la demo en vivo de **Agentes Logistic Day**.

No contiene información de Pronaca.

## Estructura

- `oceanica/` — Histórico de importaciones, ranking de modelos, resultados de forecast y dashboard HTML.
- `assets/` — Logos (Oceánica Internacional, DataChainDesign) y plantilla de dashboard (estilo TIGRE).
- `docs/` — Contexto de la empresa y notas de la demo.

## Oceánica Internacional

Forwarder costarricense (fundada 1998, matriz Río Segundo, Alajuela). Oficina en Managua, Nicaragua (~135 personas, único forwarder nicaragüense con servicio consolidado propio desde Qingdao, Hong Kong, Ningbo y Shanghái directo a Corinto). Crecimiento esperado >18% en 2026.

Servicios: FCL, LCL, aéreo, terrestre regional, aduana (COASA), bodegaje y distribución.

## Demo en vivo

Todo el cómputo pesado ya está hecho. El agente solo lee resultados precomputados y genera visualizaciones HTML (estilo dashboard con rail lateral, cards, Chart.js, colores cyan/graphite).

Narrativa: qué viene (forecast) → cuándo llega (dashboard de viajes) → cómo se reparte (last-mile desde Corinto).

Mañana: dramatizar “procesando 53 mil envíos, aplicando diez modelos” y luego mostrar el HTML.
