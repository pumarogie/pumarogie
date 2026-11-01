# Phillips Oluwaseun Uwumarogie

Software engineer in Munich. I work on the layer where systems fail quietly: databases, overload, and data correctness.

Most of what is here started as a question I could only answer by building the thing and measuring it.

## Selected work

**Databases**

- **[pgwire-ocaml](https://github.com/pumarogie/pgwire-ocaml)**: a relational database written from scratch in OCaml that real `psql` connects to. It implements the Postgres wire protocol, a SQL parser, a cost-based planner, WAL, indexes and transactions in about 1,450 lines with no dependencies beyond the standard library.
- **[schema-drift-checker](https://github.com/pumarogie/schema-drift-checker)**: a CI gate that fails the build when the live Postgres schema and the migration history disagree. It works with Drizzle, Prisma, TypeORM, Sequelize and Kysely.
- **[claude-postgres-skills](https://github.com/pumarogie/claude-postgres-skills)**: operational Postgres rules (safe migrations, pooling, autovacuum, queue patterns) packaged so coding agents apply them while writing SQL, before the incident.

**Reliability and data quality**

- **[load-shedding](https://github.com/pumarogie/load-shedding)**: a lab that pushes a fixed-capacity server past its limit and compares eight shedding strategies (CoDel, adaptive LIFO, Gradient, deadline, priority and others) on goodput and tail latency. Without shedding, 4x load leaves 32 rps of useful work out of 200.
- **[bikeshare-dv](https://github.com/pumarogie/bikeshare-dv)**: a replication of Google's *Data Validation for ML* paper at 10^4 rows instead of 10^9. It injects five production-style faults into a daily-retrained model and scores which detectors catch them, and where the paper's assumptions break.

**Products**

- **[doki](https://github.com/pumarogie/doki)**: one document engine behind several PDF products: PDF/A conversion, XRechnung/ZUGFeRD e-invoicing, templated rendering, LLM extraction with confidence scores, and scheduled reports. It includes scoped API keys, quotas and signed webhooks.
- **[mold](https://github.com/pumarogie/mold)**: a Rust CLI that turns JSON into TypeScript types, Zod schemas and Prisma models.

## Writing

**[Software Engineering in 2026](https://swe.marogie.com)** is a handbook for engineers who direct AI agents. It covers the workflow from plan to merged PR, review, testing, security, and the toolkit I run.

## How I work

- Measure before arguing. The labs here publish the commands behind every number.
- Prefer the boring fix in the shared path over a clever patch at the call site.
- Write down trade-offs and the conditions under which a decision should be revisited.

## Contact

[uwumarogiephillips@gmail.com](mailto:uwumarogiephillips@gmail.com)
