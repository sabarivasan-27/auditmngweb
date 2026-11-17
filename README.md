# AuditFlow — Centralized Enterprise Audit Management Dashboard

> **Production-Quality Quality Assurance Platform for Product Audits and Revalidation Audits in Manufacturing & Automotive Environments.**

Built with **React 18 + TypeScript + Vite**, **Tailwind CSS**, **Framer Motion**, **Recharts**, **TanStack Table**, **Zustand**, and **Lucide Icons**.

---

## 🌟 Key Features

1. **Role-Aware Workflows (4 Switchable Personas)**
   - **Auditing Head**: Executive plant assurance oversight, dynamic risk heatmaps, side-by-side evidence inspection, and digital cryptographic E-Signature seals.
   - **Auditor**: Daily shift timeline, interactive digital checklist execution wizard with instant NOK non-conformance logging, and physical evidence verification.
   - **Auditee**: Assigned NC dossier, 5-Why root cause investigations, CAPA action plans, and photo/PDF evidence attachments.
   - **Admin / Planner**: Monthly audit plan drag-and-drop CSV uploader with live syntax validator, 100% scheduled-coverage indicator, and conflict-aware auditor assignment.

2. **10 Production-Grade Functional Modules**
   - **1. Executive Dashboard**: Dynamic live KPI cards (Plan vs Completed %, Open NCs, Overdue NCs, Closed NCs, On-Time %, Lead Time, Ageing) with 5 interactive Recharts visualizations (Monthly Plan vs Actual, NC Lifecycle Donut, Ageing Buckets, Closure Trend Line, and Department Risk Heatmap).
   - **2. Monthly Audit Plan**: Calendar & table views, 100% coverage progress, drag-drop CSV/Excel import with instant row-level error validation.
   - **3. Daily Auditor Schedule**: 8-auditor day/week shift timeline, shift slotting, conflict collision detector (capacity limits).
   - **4. Digital Audit Checklist**: Step-by-step automotive quality checks (OK / NOK / NA), auto-save drafts with timestamps, instant Non-Conformance trigger modal with severity classification (Minor / Major / Critical).
   - **5. NC Management (Kanban & Data Table)**: 6-stage lifecycle board (Open → Action Submitted → Evidence Uploaded → Auditor Verified → Pending Head Approval → Closed).
   - **6. Evidence Verification Workbench**: Split-view comparison of original finding vs auditee fix with Accept/Reject controls.
   - **7. Auditing Head Approvals**: Batch approvals, cryptographic signature stamping, and celebratory confetti.
   - **8. SLA Escalations & Notifications Center**: 3-tier escalation ladder (Auditee → Dept Head → Auditing Head) with SLA countdown chips and configurable threshold rules.
   - **9. Audit History & Reports**: Full historical registry, multi-parameter search, saved view presets, and client-side CSV/PDF export.
   - **10. "Manual vs Digital" ROI Showcase**: Interactive economic payback calculator demonstrating 89% reporting effort reduction and 75% faster NC closure velocity.

3. **Global Command Palette (`Ctrl+K` / `Cmd+K`)**
   - Instant search across all audits, NCs, departments, and one-click role switching from anywhere.

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+)
- npm or pnpm

### Installation & Run
```bash
# 1. Install dependencies
npm install

# 2. Start Vite local development server
npm run dev

# 3. Build for production
npm run build
```

---

## 🎬 3-Minute Demo Walkthrough Script

1. **Role Switcher & Dashboard KPIs**
   - Switch between **Auditing Head**, **Auditor**, **Auditee**, and **Admin** via the selector in the top-right header.
   - Observe the welcome banner and primary actions dynamically tailor to each role.
   - Check the 7 KPI cards: notice tabular numbers and animated count-ups.

2. **Digital Checklist Execution & Instant NC Trigger**
   - Navigate to **Audit Checklist** (`/checklist`).
   - Select an active audit and mark an item as **NOK**.
   - Fill in severity (e.g. *Major*), defect description, and immediate containment. Click **Confirm & Raise NC**.
   - Notice the live notification trigger and the newly generated NC.

3. **NC Management & Auditee 8D CAPA**
   - Navigate to **NC Management** (`/nc-management`).
   - Open the newly raised NC to view its dossier.
   - Switch persona to **Auditee**. Fill in the 5-Why root cause fields and corrective actions.
   - Click **Upload New Evidence** to attach a photo or calibration report.

4. **Auditor Verification Desk**
   - Switch persona to **Auditor**.
   - Navigate to **Evidence Verification** (`/verification`).
   - Review the submission side-by-side. Click **Verify & Accept (Forward to Head)**.

5. **Auditing Head E-Signature Seal**
   - Switch persona to **Auditing Head**.
   - Navigate to **Head Approvals** (`/approvals`).
   - Click **E-Sign & Close Finding**, enter demo PIN `9481`, and click **Confirm Seal & Close**.
   - Enjoy the celebratory confetti! Return to the Dashboard and watch the Closed NC KPI increase and Open NC count decrease live!

---

## 📁 Architecture & Folder Structure

```
src/
├── components/
│   ├── common/             # Badges, StatCards, CommandPalette, OnboardingModal
│   └── layout/             # AppLayout, Header, Sidebar
├── features/
│   ├── approvals/          # Head approvals & digital e-signatures
│   ├── checklist/          # Interactive audit execution & NOK trigger
│   ├── dashboard/          # Role-aware dashboard, KPIs, 5 Recharts graphs
│   ├── escalations/        # SLA escalation ladder & notification rules
│   ├── impact/             # Manual vs Digital ROI comparison calculator
│   ├── monthly-plan/       # CSV plan uploader, calendar & coverage
│   ├── nc-management/      # Kanban board, data table, NC detail dossier
│   ├── reports/            # Historical audit query logs & client export
│   ├── schedule/           # Auditor timeline shift grid & conflict checker
│   └── verification/       # Evidence review workbench
├── lib/                    # Tailwind utils, date formatting, helpers
├── mocks/                  # 150 Seed Audits, 120 NCs, 8 Auditors, 15 Auditees
├── store/                  # Zustand store + Dynamic reactive KPI calculator
└── types/                  # Typed interfaces for Audits, NCs, Users, Checklist
```
