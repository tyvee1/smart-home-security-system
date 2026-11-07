# Design and Validation of a Smart Home Security System

Systems Engineering project submission.
**Ty** · November 2026

A residential security system comprising motion, door/window and water leak
sensors, cameras, an alarm annunciator, device controllers and a central
control unit, with local and remote interfaces. Designed local-first:
detection, recording, alarm sounding and logging all continue through a
broadband outage, and continuously recorded video never leaves the dwelling.

## Submitted documents

| File | What it is |
| --- | --- |
| `SysRS-Smart-Home-Security-System.pdf` | System Requirements Specification, 32 pages, following the course template and ISO/IEC/IEEE 29148:2018 Clause 9.5. 113 requirements across 23 areas, 26 specified interfaces, a verification matrix and a reliability apportionment. |
| `architecture.drawio` | System architecture — server with database and storage, sensors and controllers with their connectivity, user interaction, and the off-premises boundary. Open at [app.diagrams.net](https://app.diagrams.net). |
| `sysml-diagrams.txt` | Four SysML diagrams as PlantUML source: block definition, requirements with their relationships, the arming state machine, and an intrusion sequence. Paste into [plantuml.com/plantuml](https://plantuml.com/plantuml) or render with `java -jar plantuml.jar sysml-diagrams.txt`. |
| `sysml-block-definition.drawio` | The block definition diagram in draw.io form as well. |
| `sysml-block-definition.png` | Rendered block definition diagram. |
| `sysml-requirements.png` | Rendered requirement diagram showing derive, satisfy and verify relationships. |
| `sysml-state-machine.png` | Rendered state machine for the eight arming states. |
| `sysml-sequence.png` | Rendered sequence diagram for an intrusion, end to end. |
| `decision-matrices.xlsx` | Six weighted decision matrices — motion sensors, door/window sensors, water leak sensors, cameras, controllers, and server deployment. Each carries a sensitivity sweep and a written justification for every score. |
| `test-cases.xlsx` | 14 test cases exported from Testomat: 7 verification, 4 validation / user acceptance, 2 validation / load testing, and 1 additional reliability scenario. |

## A note on two numbers

The weighted totals in `decision-matrices.xlsx` are live `SUMPRODUCT`
formulas rather than typed values, so a reviewer can change a weight and
watch the decision move. Each sheet's sensitivity block reports how far a
weight has to move before the winner changes — for the server decision, the
local-first result holds across every single-weight variation swept.

The SysRS cites **Clause 9.5** of ISO/IEC/IEEE 29148:2018, which is the
System requirements specification content. Clause 9.4 in the 2018 edition is
the *Stakeholder* requirements specification. The section ordering follows
the course template exactly; only the clause citation differs, and the
document's front matter says so.
