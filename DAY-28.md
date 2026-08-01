PROMPT:
Hospital Admission Readiness Simulator

Single-file HTML app. HTML, Tailwind CSS CDN, Vanilla JavaScript.
style: same as previously established
Healthcare simulation design system. Task-first — no dashboard on load.
User plays Hospital Admission Coordinator.

Setup — collect:
- Provider, Attending Physician
- Diagnosis: Acute MI / CHF / Pneumonia / Elective Surgery / Hip Fracture
- Admission Type: Inpatient / Observation / Emergency / ICU / Same-Day Surgery
- PA Status, Admission Date

Observation Status must always show: 'CMS 2-Midnight Rule applies — different cost-sharing, SNF eligibility, and billing than inpatient. Medicare patients require written MOON notification.'
Label all provider/payer names as illustrative training data.

Button: 🏥 Analyze Admission Readiness

Initial Analysis
Generate status for: PA, Insurance, Bed, Documentation, Physician Orders, Consent.
Readiness Score 30–60%. Do not reveal final decision yet.

Score Weighting:
PA Status 25% · Clinical Documentation 20% · Physician Orders 20% · Insurance 15% · Consent 10% · Bed 10%
Denied PA + ICU admission cannot reach 70% from admin tasks alone.

PA Branches:
Approved → continue.
Pending → Follow Up, Upload Docs, Contact Physician.
Denied → Review Reason, Contact Insurance, Submit Appeal.
Successful appeal converts to Approved.

Workflow Actions:
Assign Bed / Verify Insurance / Upload Documentation / Complete Consent / Contact Physician / Notify Nursing / Prepare Patient Arrival

Acute MI and CHF trigger a criteria note:
'InterQual/Milliman thresholds apply — ensure documentation meets medical necessity standards before UR review.'

Timeline milestones:
PA Review → Insurance Verification → Bed Assignment → Documentation → Consent → Patient Arrival → Registration → Clinical Assessment → Admission Complete

Care Coordination Cards:
Attending / Case Manager / Nursing / Utilization Review / Discharge Planner
UR card must name: concurrent review, denial risk identification, InterQual, Milliman.

Risk Tracking:
Documentation Risk / Insurance Risk / Bed Risk / Clinical Risk
Clinical Risk weighted higher for Acute MI, CHF, ICU.

At Readiness ≥ 75% show Governance Snapshot:
'Industry benchmarks (estimates only): PA turnaround 3–5 days · Inpatient denial rate ~8–10% (CMS) · PA rework cost ~$11/transaction (CAQH)'

OUTPUT:

<img width="1850" height="845" alt="Screenshot 2026-08-01 112518" src="https://github.com/user-attachments/assets/bc93a2e0-7e74-4efa-be34-0d6d20b30df4" />
<img width="1841" height="849" alt="Screenshot 2026-08-01 112455" src="https://github.com/user-attachments/assets/49710374-14ac-464a-870d-e55cf2d81076" />

[admission-readiness-simulator.html](https://github.com/user-attachments/files/30612272/admission-readiness-simulator.html)

Final Decision:
≥ 90% → ✅ Admit — full summary.
< 90% → ⚠ Not Ready — missing items, required actions, remaining risks.

Day 28 — built. A quick note on the design system: since I don't have your earlier "previously established" style in this session, I used a clinical/coordination palette (deep clinical blue, teal accent, amber/green/red status pills, mono labels for data) that reads as trustworthy healthcare software — let me know if it should match a specific prior file instead and I'll align it.

Key behaviors implemented:
- Task-first setup form (no dashboard on load)
- Weighted scoring (PA 25/Doc 20/Orders 20/Ins 15/Consent 10/Bed 10), starts 30–60%
- Denied PA + ICU capped at 65% until appeal succeeds
- Full PA branching (Pending → Follow Up/Upload Docs/Contact Physician; Denied → Review Reason → Contact Insurance → Submit Appeal)
- Observation CMS 2-Midnight banner, Acute MI/CHF InterQual/Milliman note
- 9-stage timeline, 5 care coordination cards (UR names concurrent review/denial risk/InterQual/Milliman), 4 risk trackers with clinical risk upweighted for MI/CHF/ICU
- Governance snapshot unlocks ≥75%, final Admit/Not-Ready decision on FinalizeTry running through a Denied + ICU case and an Approved + Elective Surgery case — those two paths exercise most of the branching logic. Let me know if you want the scoring curve tuned or the visual style adjusted.
