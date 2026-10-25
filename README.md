# Miguel Villarreal

**Mechatronics Engineer · Python · SQL · Pandas · LLMs · .NET** · Monterrey, MX
Data Analyst · MBA (Finance) · M.Sc. in IT Management · Data Science (MIT xPRO)
[LinkedIn](https://www.linkedin.com/in/villarm3/)

I worked as a Billing Specialist in freight transportation (Nov 2023 – Jul 2025):
240+ bills of lading a day, 1,000+ invoices a month, with 99%+ billing accuracy
(figures from my CV). I came out of it with three specific, well-understood pains:
two sets of money records that should agree and nobody reconciles by hand,
customer claims that require decisions under policy, and files that go out badly
formatted and take the next system down with them. I'm especially interested in
the intersection of fintech and high-volume retail (payment rails like
OXXO/SPEI/card settlements). This profile is what I built for those three pains:
6 projects, ~380 tests, CI on every one.

## Projects

| # | Project | Stack | What it does |
|---|---|---|---|
| 1 | [Reconciliation engine](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/reconciliation-engine) | Python · pandas · DuckDB | Reconciles an operations ledger against the settlement file, reference by reference: 7 rules, conservation checks that stop the run. |
| 2 | [LLM support desk](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/llm-support-desk) | Python · Ollama · SQLite · Docker | Payment-claim triage: a local LLM proposes, deterministic rules decide and can only escalate. Every decision lands in a SQLite decision log. |
| 3 | [File layout automator](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/file-layout-automator) | C# · .NET 8 · WPF + CLI | Turns CSV into the fixed-width layout the downstream system demands; rejects a value instead of truncating it, and writes nothing while any row fails. |
| 4 | [Collections aging SQL](https://github.com/MVillarreal98/fde-portfolio/tree/main/projects/collections-aging-sql) | DuckDB SQL | Age of every open invoice counted from its due date, collections stages that only escalate, FIFO cash application and duplicate-payment candidates. |
| 5 | [Aire de Monterrey — BigQuery](https://github.com/MVillarreal98/aire-monterrey-bigquery) | Python · SQL · BigQuery · Looker Studio | ~1.5M hourly air-quality readings (SIMA network, 2015–2024): ingestion from SINAICA, partitioned & clustered BigQuery, queries and a live dashboard. [Dashboard](https://datastudio.google.com/reporting/fe47cccc-d1c9-4392-97d0-605069f4096c). |
| 6 | [iPhone vs Galaxy — Monterrey](https://github.com/MVillarreal98/iphone-vs-galaxy-monterrey) | SQLite · Python stdlib · Folium | Where iPhone is searched more than Galaxy, locality by locality, joining Google Trends + INEGI 2020 Census + StatCounter, with SQL quality checks. [Published map](https://mvillarreal98.github.io/iphone-vs-galaxy-monterrey/). |

## The honest part, said once

- None of these tools has users or a production deployment yet. Every dataset is
  synthetic, written for the demos: where a README of mine says "success
  metrics", those are definitions, not measurements. The projects grew out of
  pains I saw in operations, but they weren't used there: no company data or
  code appears in this profile.
- I built the code scaffolding with AI assistants. What I put under my own
  responsibility: the tests (~380 across the four fde-portfolio repos: 171
  reconciliation, 133 support desk, 38 xunit in .NET, 37 collections), the CI
  gates, the CHANGELOGs and the documented technical decisions.


## How to review this profile

2 minutes: [fde-portfolio](https://github.com/MVillarreal98/fde-portfolio) —
the project table, the "What the review rounds caught" section, and each
project's `sample_output/` (real CLI output, not a screenshot).
After that: [aire-monterrey-bigquery](https://github.com/MVillarreal98/aire-monterrey-bigquery)
for the data side (the "Limitaciones" section is the good part).

**En español:** Pasé cerca de dos años dentro de la operación de facturación
de transporte (240+ bills of lading al día, 1,000+ facturas al mes, 99%+ de
exactitud — cifras de mi CV). Ahora construyo las herramientas que le quitan
ese trabajo a la gente de sus pantallas: un motor de conciliación en
pandas/SQL, un agente de triage donde un LLM local propone y reglas
deterministas deciden (solo pueden escalar), y un generador de archivos de
ancho fijo en C#/.NET 8. Además dos proyectos de datos abiertos de Monterrey
(calidad del aire en BigQuery; búsquedas iPhone vs Galaxy mapeadas por
localidad). Todo corre con datos sintéticos y los READMEs lo dicen: lo real
es el problema, los tests y el CI.
