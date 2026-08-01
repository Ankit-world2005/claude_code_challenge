PROMPT:

Prior Authorization Workflow Simulator (gamified, drag-and-drop)

Build a single-file, self-contained HTML application (HTML + CSS + vanilla JavaScript, no external dependencies, no build step) that visually simulates the US healthcare Prior Authorization (PA) workflow as an interactive, gamified, drag-and-drop experience.

The simulator should include:

• Three workflow lanes: Patient, Provider, and Payer.
• Interactive drag-and-drop movement of cases between stages.
• Multiple patient scenarios (elective surgery, MRI, specialty medication, inpatient admission).
• Medical necessity evaluation.
• Prior Authorization document collection.
• Submission to payer.
• Review outcomes including Approval, Pend, Denial, Appeal, and Peer-to-Peer Review.
• Educational explanations after every step.
• Progress tracker across the top.
• Days elapsed counter.
• Efficiency score.
• Celebration animation on approval.
• Workflow summary on completion.
• Responsive modern UI using shades of blue with black text.
• Working Restart / New Patient button.
• Fully functional buttons and interactions.

Technical Requirements:
- Single HTML file.
- HTML, CSS and Vanilla JavaScript only.
- No frameworks.
- No CDNs.
- No localStorage.
- All workflow state managed in JavaScript memory.
- Well-commented code.
- Scenario data stored in an editable array near the top.
- Output only the complete HTML file without truncation.

OUTPUT:

<img width="1917" height="909" alt="Screenshot 2026-08-01 105332" src="https://github.com/user-attachments/assets/7b9675a3-f81f-40f7-80f4-df476a9c7558" />


[prior-auth-simulator.html](https://github.com/user-attachments/files/30612003/prior-auth-simulator.html)

Let me verify it renders and functions correctly before handing it off.No errors. Let's check the screenshots.Looks clean. Let's quickly run through the full workflow to a celebration/approval to confirm end-to-end logic works.This confirms the full workflow logic works end-to-end (documents, submission, review, and outcome determination all fire correctly with no console errors). The file is complete and self-contained.A single self-contained HTML file with everything you asked for:

- **4 scenarios** (elective knee surgery, lumbar MRI, specialty biologic, inpatient admission) editable in the `SCENARIOS` array near the top
- **3 drag-and-drop lanes** (Patient/Provider/Payer) with a real HTML5 drag interaction, plus guided in-lane actions so the flow stays valid
- **Full 8-stage tracker** at the top, days-elapsed counter, and a live efficiency score that reacts to wrong-lane drops and missing documents
- **Medical necessity evaluation, document checklist, submission, payer review**, and branching outcomes: Approval, Pend (with resubmission), Denial (with appeal), and Peer-to-Peer review
- **Educational explanation** after every step in the blue callout panel
- **Confetti celebration** on approval, and a **summary modal** with day count, efficiency, appeal/P2P usage, and full event timeline
- **Restart / New Patient** button that fully resets state (no localStorage — everything lives in JS memory as required)

I tested it end-to-end headlessly (scenario select → visit → necessity → docs → submit → review → outcome) with zero console errors.
