# Beyond MVG — State of Cardano Governance


> A research initiative commissioned by Cardano DReps and delivered by Input Output Group (IOG) and Cardano Community Members.

[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-brightgreen)](https://github.com/kenerik/Beyond_MVG)
[![Cardano](https://img.shields.io/badge/Cardano-CIP--1694-blue)](https://cips.cardano.org/cip/CIP-1694)
[![Documents](https://img.shields.io/badge/documents-3-orange)](docs/)
[![Metrics](https://img.shields.io/badge/metrics-12-blueviolet)](README.md#governance-metrics-at-a-glance)
[![Version](https://img.shields.io/badge/version-1.1.0-lightgrey)](CHANGELOG.md)

## Overview

This repository contains the research outputs for the **State of Cardano Governance** project — a framework for measuring, tracking, and reporting on the health of Cardano's on-chain governance system as implemented through [CIP-1694](https://cips.cardano.org/cip/CIP-1694).

The project goes **beyond the Minimum Viable Governance (MVG)** baseline by establishing a rigorous, reproducible measurement methodology that combines on-chain quantitative metrics with qualitative stakeholder assessments.

---

## Authors

Commissioned by Cardano DReps; delivered by IOG and Cardano Community Members in alphabetical order:

| Name | Affiliation |
|---|---|
| Danielle Stanko | IOG |
| Fanny Wijaya | - |
| JM Martinez Felices | IOG |
| Kelvin Peter | IOG |
| Ken Erik Oelmheim | — |
| Maureen Wepngong | Giiyo Tech |
| Max van Rossem | — |
| Nana Safo | Wada Global |
| Richmond Oppong | Wada Global |
| Tevo Kask | SWARM |

Special thanks to everyone that contributed, had critical eyes, debated with us, responded to surveys, and made this report possible.

CIVICS Governance Health Working Group , Nicolas Cerny, Cathy Hermstad Patanakarun, Larisa Mcfarlane, Vaibhav Solanki, Thomas Lindseth, Mike Hornan, Cardano over coffee, 45B - Cardano Enablement, Epoch end, Cardano budget committee, Beatrice Anihiri, Will Eddie, Arman Abid, Van Rossem family, Cardano foundation, Charles Hoskinson and all employees at IOG, CIP-1694 contributors,

---

## Repository Structure

```
Beyond_MVG/
├── docs/                                         # Core research documents (PDF)
│   ├── M1-1D_ Governance Metrics Manual.pdf
│   ├── M1-1D_ State of Governance - Report Outline
│   ├── M1-1D_ State of Governance Measurement Framework
│   └── cardano-node-setup & Query DbSync - step by step   # Node setup reference
│   └── Visualization Derivation Plan - step by step (TBD according to feedback)
│
├── data/                                         # Data results from report queries and generated visualizations
│   ├── On-chain-measurements-epoch-537-609/      # Raw CSV metric data (epochs 537–609)
│   │   ├── ada-owner-metrics/                    # M1–M3: Voting %, delegators, stickiness
│   │   ├── DRep-Metrics/                         # M4–M7: Gini, Nakamoto, rationale, net change
│   │   ├── SPO-Metrics/                          # M8–M9: SPO engagement & stickiness
│   │   └── CC-Metrics/                           # M10–M12: Response time, rationale, abstain rate
│   │
│   ├── On-chain-visuals-epoch-537-609/           # Chart exports (PNG) for each metric
│   │   ├── ada-owner-metrics/
│   │   ├── DRep-metrics/
│   │   ├── SPO-metrics/
│   │   └── CC-metrics/
│   │
│   ├── Interview notes                           # Notes from carried out interviews
│   │
│   ├── Surveys response                          # Response from surveys
│   │   ├── ENG/
│   │   ├── ESP/
│   │   └── JPN/
│   │
│   └── workshops/
│       └── ms2-workshops-surveys-interviews/     # MS2 qualitative data
│           ├── raw-data/
│           │   ├── surveys/                      # 9 CSVs across 5 stakeholder groups (incl. JPN)
│           │   ├── interviews/                   # 5 CSVs — semi-structured interview responses
│           │   └── workshop-responses/           # Facilitator workshop summaries (4 sessions)
│           ├── visuals/                          # 7 Miro board PDF exports by topic
│           ├── sources.md                        # Links to Google Sheets & Miro boards
│           └── README.md                         # Full data manifest and metric reference
│
├── .github/
│   └── ISSUE_TEMPLATE/                           # Templates for feature requests
├── CHANGELOG.md                                  # Version history and document updates
├── CONTRIBUTING.md                               # How to contribute to this project
├── LICENSE                                       # MIT License
└── README.md                                     # This file
```

---

## Core Documents

### 1. [Governance Measurement Framework](docs/State_of_Governance_Measurement_Framework.pdf)
The foundational research document presenting the rationale and theoretical basis for measuring Cardano governance. Organizes metrics into four interconnected categories rooted in OSCE democratic principles and empirical DAO research:

- **Ada Holder Metrics** — Legitimacy & Participation
- **DRep Metrics** — Decentralization & Accountability
- **SPO Metrics** — Security & Oversight
- **Constitutional Committee Metrics** — Constitutional Adherence & Veto Oversight

### 2. [Click here for the Interactive Technical Manual](https://kenerik.github.io/Beyond_MVG/cardano-node-setup.html)
Step-by-step technical guidance for calculating each metric. Intended for tooling providers and technical community members who want to independently implement or verify measurements. Covers data sources, SQL query logic, and visualization specifications for all 12 defined metrics.

### 3. [Click here for technical manual on how to make visual from data ](https://kenerik.github.io/Beyond_MVG/on-chain-data-visualization.html)
Step-by-step technical guidance for calculating and generate visuals for each metric.
Intended for tooling providers and technical community members who want to independently implement or verify measurements.

### 4. [State of Governance Report Outline](docs/State_of_Governance_Report_Outline.pdf)
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
- **Epoch boundary snapshots** — On-chain CSV measurements for epochs 537–609 available in [`data/On-chain-measurements-epoch-537-609/`](data/On-chain-measurements-epoch-537-609/)
- **Surveys, interviews & workshops** — Qualitative data from 5 stakeholder groups (ADA holders, DReps, SPOs, CC Members, Builders) including Japanese community responses, available in [`data/workshops/ms2-workshops-surveys-interviews/`](data/workshops/ms2-workshops-surveys-interviews/)
- **Miro board exports** — 7 workshop visual PDFs mapping community discussions to governance metrics
- **Google Sheets (original workbook)** — [Full 16-sheet workbook](https://docs.google.com/spreadsheets/d/1_FWuTPjI0COb9A3PiQB_8g1U8ruAVUf5VRGSvoP2I18/edit) with all raw survey and interview data

---

## Methodology Notes

- **Quantitative metrics** use on-chain data queryable via cardano-db-sync and can be automated for continuous monitoring.
- **Qualitative data** (surveys, stakeholder interviews, workshops) supplements on-chain measurements to capture the "why" behind observed patterns.
- AI tools (Gemini CLI and Claude Code) were used to enforce consistency between documents and structure the analysis. All AI-assisted content was reviewed by Beyond MVG team.

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

```
  ____                             _   __  ____      _______ 
 |  _ \                           | | |  \/  \ \    / / ____|
 | |_) | ___ _   _  ___  _ __   __| | | \  / |\ \  / / |  __ 
 |  _ < / _ \ | | |/ _ \| '_ \ / _` | | |\/| | \ \/ /| | |_ |
 | |_) |  __/ |_| | (_) | | | | (_| | | |  | |  \  / | |__| |
 |____/ \___|\___, |\___/|_| |_|\__,_| |_|  |_|   \/   \_____|
              __/ |                                          
             |___/                                      2026
```
