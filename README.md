# Miguel Villarreal

**Mechatronics Engineer · Python · SQL · Pandas · LLMs · .NET** · Monterrey, MX
Data Analyst · MBA (Finance) · M.Sc. en Gestión de TI · Data Science (MIT xPRO)
[LinkedIn](https://www.linkedin.com/in/villarm3/)

Trabajé como Billing Specialist en transporte de carga (Nov 2023 – Jul 2025):
240+ bills of lading al día, 1,000+ facturas al mes, con 99%+ de exactitud de
facturación (cifras de mi CV). De ahí me llevé tres dolores específicos y bien
entendidos: dos fuentes de dinero que no cuadran y nadie reconcilia a mano,
reclamos de clientes que exigen decisiones bajo política, y archivos que salen
mal formatados y se llevan por delante al sistema siguiente. Me interesa
especialmente la intersección de fintech y retail de alto volumen (payment
rails tipo OXXO/SPEI/liquidaciones de tarjeta). Este perfil es lo que construí
para esos tres dolores: 6 proyectos, ~380 tests, CI en cada uno.

## Proyectos

| # | Proyecto | Stack | Qué hace |
|---|---|---|---|
| 1 | [Reconciliation engine](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/reconciliation-engine) | Python · pandas · DuckDB | Concilia un ledger de operaciones contra el archivo de settlement: referencia por referencia, 7 reglas, checks de conservación que detienen la corrida. |
| 2 | [LLM support desk](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/llm-support-desk) | Python · Ollama · SQLite · Docker | Triage de reclamos de pago: un LLM local propone, las reglas deterministas deciden y solo pueden escalar. Todo queda en un decision log en SQLite. |
| 3 | [File layout automator](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/file-layout-automator) | C# · .NET 8 · WPF + CLI | Convierte CSV al layout de ancho fijo exigido por el sistema de abajo; rechaza el valor en vez de truncarlo y no escribe mientras haya filas malas. |
| 4 | [Collections aging SQL](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/collections-aging-sql) | DuckDB SQL | Edad de cada factura abierta desde la fecha de vencimiento, etapas de cobranza que solo escalan, cash aplicado FIFO y candidatos a pago duplicado. |
| 5 | [Aire de Monterrey — BigQuery](https://github.com/MVillarreal98/aire-monterrey-bigquery) | Python · SQL · BigQuery · Looker Studio | ~1.5 M mediciones horarias de calidad del aire (red SIMA, 2015–2024): ingesta desde SINAICA, BigQuery particionado y clusterizado, queries y dashboard en vivo. [Dashboard](https://datastudio.google.com/reporting/fe47cccc-d1c9-4392-97d0-605069f4096c). |
| 6 | [iPhone vs Galaxy — Monterrey](https://github.com/MVillarreal98/iphone-vs-galaxy-monterrey) | SQLite · Python stdlib · Folium | Dónde se busca más iPhone que Galaxy, localidad por localidad, cruzando Google Trends + Censo INEGI 2020 + StatCounter, con checks de calidad en SQL. [Mapa publicado](https://mvillarreal98.github.io/iphone-vs-galaxy-monterrey/). |

## Lo honesto, dicho una vez

- Ninguna de estas herramientas tiene usuarios ni producción todavía. Todos los
  datasets son sintéticos, escritos para los demos: donde en un README digo
  "métricas de éxito", son definiciones, no mediciones. Los proyectos nacieron
  de dolores que vi en la operación, pero no se usaron ahí: no hay datos ni
  código de la empresa en este perfil.
- Trabajé el andamiaje del código con asistentes de IA. Lo que pongo bajo mi
  responsabilidad: los tests (~380 entre los cuatro de fde-portfolio: 171
  conciliación, 133 support desk, 38 xunit en .NET, 37 collections), las gates
  de CI, los CHANGELOGs y las decisiones técnicas documentadas de cada proyecto.
- El siguiente proyecto de este perfil es una suite de automatización de
  navegador en Playwright; cuando la publique puede esperar el mismo estándar
  de tests, artefacts y CI.

## Cómo revisar este perfil

2 minutos: [fde-portfolio](https://github.com/MVillarreal98/fde-portfolio) —
la tabla de proyectos, la sección "What the review rounds caught", y el
`sample_output/` de cada proyecto (salida real del CLI, no captura).
Después: [aire-monterrey-bigquery](https://github.com/MVillarreal98/aire-monterrey-bigquery)
para el lado de datos (La sección "Limitaciones" es la parte buena).

**In English:** I spent about two years deep in freight billing operations
(240+ bills of lading a day, 1,000+ invoices a month, 99%+ accuracy — figures
from my CV) and now I build the tools that take that work off people's
screens: a reconciliation engine in pandas/SQL, a support-triage agent where a
local LLM proposes and deterministic rules decide (they can only escalate),
and a fixed-width file generator in C#/.NET 8. Plus two open-data projects on
Monterrey (air quality in BigQuery; iPhone vs Galaxy searches mapped by
locality). Everything runs on synthetic data and the READMEs say so — what's
real is the problem, the tests, and the CI.
