# Beyond MVG — State of Cardano Governance

> A research initiative commissioned by Cardano DReps and delivered by Input Output (IO) and Cardano Community Members.

![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-active-brightgreen)
![Cardano](https://img.shields.io/badge/Cardano-CIP--1694-blue)
![Documents](https://img.shields.io/badge/documents-3-orange)
![Metrics](https://img.shields.io/badge/metrics-12-blueviolet)

## Overview

This repository contains the research outputs for the **State of Cardano Governance** project — a framework for measuring, tracking, and reporting on the health of Cardano's on-chain governance system as implemented through [CIP-1694](https://cips.cardano.org/cip/CIP-1694).

The project goes **beyond the Minimum Viable Governance (MVG)** baseline by establishing a rigorous, reproducible measurement methodology that combines on-chain quantitative metrics with qualitative stakeholder assessments.

---

## Authors

Commissioned by Cardano DReps; delivered by IO and Cardano Community Members including:

| Name | Affiliation |
|---|---|
| Fanny Wijaya | — |
| Ken Erik Oelmheim | — |
| Maureen Wepngong | Giiyo Tech |
| Max van Rossem | — |
| Nana Safo | Wada Global |
| Richmond Oppong | Wada Global |
| Tevo Kask | — |

---

## Repository Structure

```
Beyond_MVG/
├── docs/                        # Core research documents (PDF)
│   ├── Governance_Metrics_Manual.pdf
│   ├── State_of_Governance_Report_Outline.pdf
│   └── State_of_Governance_Measurement_Framework.pdf
├── data/                        # Data outputs and epoch snapshots (future)
├── code/                        # Metric calculation scripts (future)
├── .github/
│   └── ISSUE_TEMPLATE/          # Templates for feature requests
├── CHANGELOG.md                 # Version history and document updates
├── CONTRIBUTING.md              # How to contribute to this project
├── LICENSE                      # MIT License
└── README.md                    # This file
```

---

## Core Documents

### 1. [Governance Measurement Framework](docs/State_of_Governance_Measurement_Framework.pdf)
The foundational research document presenting the rationale and theoretical basis for measuring Cardano governance. Organizes metrics into four interconnected categories rooted in OSCE democratic principles and empirical DAO research:

- **Ada Holder Metrics** — Legitimacy & Participation
- **DRep Metrics** — Decentralization & Accountability
- **SPO Metrics** — Security & Oversight
- **Constitutional Committee Metrics** — Constitutional Adherence & Veto Oversight

### 2. [Governance Metrics Manual](docs/Governance_Metrics_Manual.pdf)
Step-by-step technical guidance for calculating each metric. Intended for tooling providers and technical community members who want to independently implement or verify measurements. Covers data sources, SQL query logic, and visualization specifications for all 12 defined metrics.

### 3. [State of Governance Report Outline](docs/State_of_Governance_Report_Outline.pdf)
The template and structure for producing periodic State of Cardano Governance reports using the measurement framework. Defines sections covering methodology, key findings by GMF category, governance action analysis, and forward path recommendations.

---

## Governance Metrics at a Glance

| # | Category | Metric | Format |
|---|---|---|---|
| 1 | Ada Holder | % of circulating ADA actively voting (excl. abstain) | Percentage |
| 2 | Ada Holder | Number of unique stake addresses delegated to DReps | Count |
| 3 | Ada Holder | Stickiness of ADA holder to DRep delegation | Percentage |
| 4 | DRep | Gini coefficient of delegated voting power | 0–1 coefficient |
| 5 | DRep | Nakamoto coefficient for DRep power | Integer |
| 6 | DRep | % of DRep votes with published rationale | Percentage |
| 7 | DRep | Net change in active DRep count | Rate of change |
| 8 | SPO | SPO engagement in governance actions (overall & mandatory) | Percentage |
| 9 | SPO | Stickiness of ADA delegated to SPOs | Percentage |
| 10 | CC | Average CC response time to governance actions | Slots / days |
| 11 | CC | % of CC votes including rationale | Percentage |
| 12 | CC | CC abstain rate | Percentage |

---

## Data Sources

- **Cardano Node + cardano-db-sync** — Primary on-chain data source for all quantitative metrics
- **Epoch boundary snapshots** — Used for all delegation and voting metrics per CIP-1694

---

## Methodology Notes

- **Quantitative metrics** use on-chain data queryable via cardano-db-sync and can be automated for continuous monitoring.
- **Qualitative data** (surveys, stakeholder interviews, workshops) supplements on-chain measurements to capture the "why" behind observed patterns.
- AI tools (Gemini CLI and Claude Code) were used to enforce consistency between documents and structure the analysis. All AI-assisted content was reviewed by the research team.

---

## References

| CIP / Document | Description |
|---|---|
| [CIP-1694](https://cips.cardano.org/cip/CIP-1694) | On-Chain Decentralized Governance |
| [Cardano Constitution](https://cardano.org/constitution/) | Foundational governance document |
| [CIP-0100](https://cips.cardano.org/cip/CIP-0100) | Governance Metadata standard |
| [CIP-0119](https://cips.cardano.org/cip/CIP-0119) | Governance Metadata — DReps |

---

## Contributing

We welcome contributions from the Cardano community. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting issues or pull requests.

---

## License

This project is licensed under the [MIT License](LICENSE).
