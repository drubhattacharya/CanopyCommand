# canopy-command

Administrator-facing companion to the Canopy Navigator patient-encounter simulation.

Where Canopy Navigator follows a single LEP encounter **forward through time** — 16 tablet steps, touchpoints T1→T7, each button-press cascading into a Z-code and a billing line — **Canopy Command** observes those same cascades **across** a thousand encounters, rolling them up into LAI domain performance for the person responsible for the language-access program.

## Landing screen — Mission Control

Ten KPI tiles, one per LAI domain, with live values computed from `LAI_Q1_2026_Sample_Dataset.xlsx` (1,000 encounters, Q1 2026):

| # | Domain | KPI | Current | Target |
|---|---|---|---|---|
| 01 | Access | ED interpreter ≤10 min | 3.1% | ≥90% |
| 02 | Patient Experience | Provider explained clearly | 30.7% | ≥85% |
| 03 | Clinical Outcomes | Preventive service completion | 17.1% | ≥80% |
| 04 | Compliance | Section 1557 documented | 44.2% | ≥95% |
| 05 | Patient Engagement | Teach-back in preferred language | 1.7% | ≥80% |
| 06 | Financial Stewardship | Reimbursement captured | 37.2% | ≥95% |
| 07 | Quality & Safety | Adverse event rate | 4.3% | ≤1.5% |
| 08 | Workforce Development | QBS-qualified providers | 6.8% | ≥15% |
| 09 | Workflow Optimization | All T1–T7 complete | 2.3% | ≥85% |
| 10 | Technology Innovation | High-integration deployment | 33.5% | ≥80% |

Every tile shows current · target · 24h delta, and routes to Domain Deep-Dive on tap. Below the tiles: a service-line × domain heatmap (ED · Inpatient · OB · BH · Outpatient) and below that, the LAI composite banner with stage classification.

## Navigation sequence — nine destinations

Organized by the cognitive rhythm of a language-access director's day: **react → investigate → understand → quantify → plan → prepare → report**.

**Today (reactive)**
1. **Mission Control** · 10 KPIs, heatmap, live signals (landing)
2. **Live Alerts** · threshold breaches, SBAR routing, named owners
3. **Encounter Audit** · T1–T7 forensic trail — direct admin mirror of the Navigator patient view

**Understand (both)**
4. **Domain Deep-Dive** · 10 LAI domain panels with evidence anchors, KPI bars against targets, gap-of-record narrative

**Quantify (reactive, rolled-up)**
5. **Financial Monitor** · six ROI levers · exposure vs. captured · per-encounter Navigator capture rolls up here

**Plan (proactive)**
6. **Workforce Intel** · QBS pipeline · training calendar · language-match gap by shift × unit
7. **Intervention Planner** · scenario sliders · "what happens to LAI and $ if I fund this?"

**Report (proactive)**
8. **Audit Readiness** · Section 1557 evidence package · encounters that would fail a spot review today
9. **Board Briefing** · governance synthesis in CLEAR Module 7 four-component format · export-ready

## Persistent live-signals rail

Right side of the screen at all times. Every T1–T7 event streaming across the system in a 24h rolling window — alerts, triggers, info, successes. This is the direct counterpart to the Navigator's per-encounter "Live system events" panel, scaled to the whole system.

## Design continuity with Navigator

- Same navy (#1F3864) / teal (#006D6B) palette
- Same event-log treatment (color-coded left borders, timestamps in monospace)
- Same encounter-timeline pattern (admin Encounter Audit uses the identical T1–T7 structure)
- Landscape tablet orientation (designed for a wide administrator console)

## Files

```
canopy-command/
├── index.html    ← Full admin console, single-file
└── README.md
```

Self-contained, no build step, no external dependencies. Open `index.html` directly or deploy to GitHub Pages the same way as Canopy Navigator.
