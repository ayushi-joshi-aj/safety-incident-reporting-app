# Safety Incident Reporting App — Jindal Power Limited

> Chairperson Award — 1st Position · A mobile-first AppSheet application built on Google Sheets that replaced the desktop-only SORA portal for safety incident reporting — making incident logging accessible directly from the field with photo evidence, priority classification, department-wise monitoring, automated email assignment, and weekly management reports.

---

## The problem it solved

Jindal Power Limited had an existing safety incident reporting system called **SORA** — but it was desktop-only. Field engineers and technicians who identified a safety incident had to:

1. Note the incident manually in the field
2. Walk back to a desktop PC
3. Log into SORA and fill in the report

This process was a genuine barrier. The time gap between spotting an incident and reporting it meant details were forgotten, incidents were under-reported, and the hassle of the desktop workflow meant many field teams simply didn't report at all.

Safety incidents that go unreported don't get fixed. The result was incomplete incident data, unresolved hazards, and compromised safety compliance — all because the reporting tool wasn't accessible where the incidents actually happened.

---

## What the app does

### Mobile-first incident logging — from the field
- Field teams log incidents directly from their phone at the exact location of the incident
- No need to return to a desktop — report raised immediately while details are fresh
- Available to all departments across the plant

### Structured incident report
Every incident log captures:
- **Incident type** — categorised classification of the safety event
- **Location** — exact plant location where incident occurred
- **Description** — detailed account of what happened
- **Photo** — photographic evidence captured and uploaded directly from phone camera
- **Priority type** — severity classification based on the situation (low / medium / high / critical)

### Department-wise monitoring dashboard
- All reported incidents visible in a structured department-wise view
- **Status tracking** — each incident shows Completed or In Progress
- Safety officers and department heads can see open incidents across their area at a glance
- No incident can fall through the cracks — everything is tracked until closed

### Photo-mandatory closure
- The person assigned to fix an incident **must upload a photo** to mark it as Completed
- Visual proof of resolution before closure — prevents incidents being marked done without actual rectification
- Photo stored permanently in Google Sheets backend as evidence

### Automated email assignment
- When an incident is assigned to a person to resolve, AppSheet automatically sends them an email notification
- **HOD is in CC on every assignment email** — full visibility without manual escalation
- Assignee can open the app directly from the email to view the full incident report
- No incident assignment goes unnoticed

### Weekly management report
- Automated weekly summary report generated and sent to upper management
- Department-wise incident count, status breakdown, open vs closed, priority distribution
- Management visibility without needing to log into the app

---

## Impact

| Metric | Before (SORA) | After (this app) |
|---|---|---|
| Access | Desktop only | Mobile — from the field |
| Reporting friction | High — walk to PC, log in, fill form | Low — phone in hand, report in 2 minutes |
| Under-reporting | Common — hassle of desktop workflow | Significantly reduced — accessible anywhere |
| Incident closure proof | None | Photo upload mandatory before closure |
| Assignment notification | Manual | Automated email with HOD in CC |
| Monitoring view | No department-wise tracking | Department-wise Completed / In Progress dashboard |
| Management visibility | Ad hoc | Automated weekly report |
| Data completeness | Incomplete — many incidents not logged | Structured, consistent, complete records |

- Made safety incident reporting accessible to all field staff across the plant
- Photo-mandatory closure eliminated unverified incident sign-offs
- Automated HOD CC on assignments ensured zero incidents were ignored
- Deployed for Operations and C&I departments at Jindal Power Limited
- Recognised with the **Chairperson Award — 1st Position** at Jindal Power Limited for digitalization excellence
- Part of a three-project digitalization initiative that earned the highest company recognition

---

## Tech stack

| Layer | Technology |
|---|---|
| App platform | AppSheet (no-code / low-code) |
| Backend | Google Sheets |
| Photo storage | Google Drive |
| Notifications | AppSheet automated email with HOD CC |
| Weekly reports | AppSheet automated report generation |
| Access | Mobile and desktop browser — any device |

---

## Architecture

```
Field engineer spots safety incident
              ↓
   Opens app on mobile phone
              ↓
   ┌──────────────────────────────┐
   │     AppSheet Frontend         │
   │  · Incident type selection    │
   │  · Location + description     │
   │  · Photo capture + upload     │
   │  · Priority classification    │
   └──────────────────────────────┘
              ↓
   Google Sheets backend
   (incident stored with timestamp,
    reporter, department, priority)
              ↓
   AppSheet automation triggered
              ↓
   ┌──────────────────────────────┐
   │     Automated notifications   │
   │  · Assignment email sent to   │
   │    responsible person         │
   │  · HOD added in CC            │
   │  · Weekly report to mgmt      │
   └──────────────────────────────┘
              ↓
   Assignee opens app, resolves issue,
   uploads photo proof
              ↓
   Incident marked Completed
   Photo stored as permanent evidence
```

---

## Key design decisions

**Why mobile-first mattered**
The existing SORA system wasn't broken — it was inaccessible. Field engineers don't carry laptops. The entire value of this app came from meeting people where they already were — on their phones — rather than asking them to change their workflow to fit a desktop tool.

**Why photo-mandatory closure was critical**
Without photographic proof, "Completed" status was unverifiable. Incidents could be marked closed without any actual rectification. Making photo upload mandatory before closure created accountability and a permanent visual audit trail — both for safety compliance and for ISO audits.

**Why HOD CC on assignments worked**
Rather than building a separate escalation system, HOD visibility was achieved by simply adding them to CC on the automated assignment email. Zero extra steps for anyone — the HOD is informed automatically on every assignment without a separate notification workflow.

---

## Note on source code

This application is built on AppSheet (no-code platform) with Google Sheets as the backend. The app is deployed on the Jindal Power Limited plant environment. App configuration and data cannot be shared publicly for safety data confidentiality reasons.

This repository documents the problem statement, workflow design, architecture, and impact for portfolio purposes. A walkthrough is available during interviews upon request.

---

## Screenshots

> *(Screenshots of the live application have been withheld for operational confidentiality. Available for review during interviews upon request.)*

---

## Related projects

- [Power Plant Monitoring & Analysis Dashboard](../power-plant-monitoring-analysis-dashboard) — Python + HTML/CSS dashboard for PI/DCS trend analysis, equipment health monitoring, and DSM report automation
- [Plant Documentation App](../plant-documentation-app) — AppSheet digitisation of SOPs, manuals, Signal Flow Diagrams with digital checklists and HOD approval workflow
- All three projects recognised with the **Chairperson Award — 1st Position**, Jindal Power Limited

---

## About

Built independently by **Ayushi Joshi**, Assistant Manager — Control & Instrumentation, Jindal Power Limited, Tamnar, Raigarh.

- LinkedIn: [linkedin.com/in/ayushi-joshi](https://www.linkedin.com/in/ayushi-joshi-aj/)
- GitHub: [github.com/ayushi-joshi-aj](https://github.com/ayushi-joshi-aj)
- Email: ayushijoshi290799@gmail.com
