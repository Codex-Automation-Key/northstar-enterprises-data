# Northstar Enterprise Universe

**One enterprise. Realistic problems. Continuous learning.**

A living synthetic enterprise dataset maintained by the School of Applied AI (SAAI), an initiative of Codex Automation Key Pvt. Ltd.

Northstar is a fictional subscription-based B2B software enterprise. Its operations span customer support, billing, accounts, product releases and service incidents. This public repository contains data and documentation only; the simulator and private assessments are not distributed.

## Initial release — v1.0.0

January–June 2026 (UTC): 25,000 support tickets, 401,235 tabular records across 21 CSV tables (including a 2,000-ticket development subset), 5,000 customers, 350 organizations, 12 products and 60 employees. SQLite and JSON exports represent the same data, not additional independent records.

## Start here

- [Company profile](docs/COMPANY_PROFILE.md)
- [Data dictionary](docs/DATA_DICTIONARY.md)
- [Dataset card](DATASET_CARD.md)
- [Optional exploratory analysis](docs/EDA.md)
- [Business rules and relationships](docs/BUSINESS_RULES.md)
- [Open assignment briefs](community/ASSIGNMENTS.md)
- [Project showcase](community/PROJECT_SHOWCASE.md)
- [Release policy](docs/RELEASE_POLICY.md)

Open `data/northstar.sqlite` in a SQLite client or import CSVs into your preferred analytical tool. `development_ingress.json` is a small application-development input; `replay.jsonl` provides chronological ingress records. The manifest records counts and SHA-256 checksums.

## Participate

Explore the Issues tab for business problems, build your own project in a separate repository and reference the dataset version and issue. Submit a showcase proposal or a data-quality report. SAAI enrollment and assessment are separate from access to this open dataset. Public contributions and showcasing are voluntary.

## License and attribution

Public data and documentation: [CC BY 4.0](LICENSE). Credit Northstar Enterprise Universe — School of Applied AI (SAAI), Codex Automation Key Pvt. Ltd.; include the source URL, version, license and changes where applicable. Commercial reuse is permitted under the license. Branding is excluded; no endorsement is implied.

All records are synthetic; they are not evidence of actual company operations. Historical routing labels may be wrong. Do not use post-ingestion fields as classification inputs.

https://saai.codexautomationkey.com
