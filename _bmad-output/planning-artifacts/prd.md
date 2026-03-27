---
stepsCompleted: [step-01-init.md, step-02-discovery.md, step-03-success.md, step-04-journeys.md, step-05-domain.md, step-06-innovation.md, step-07-project-type.md, step-08-scoping.md, step-09-functional.md, step-10-nonfunctional.md, step-11-polish.md]
inputDocuments: ["_bmad-output/planning-artifacts/product-brief-tradely-2026-02-24.md", "_bmad-output/brainstorming/brainstorming-session-2026-02-16.md"]
workflowType: 'prd'
documentCounts:
  briefCount: 1
  researchCount: 0
  brainstormingCount: 1
  projectDocsCount: 0
classification:
  projectType: saas_b2b
  domain: Field Service Management
  complexity: low
  projectContext: greenfield
---

# Product Requirements Document - tradely

**Author:** Ryan.carroll
**Date:** 2026-02-24T19:08:41-05:00

## Executive Summary
Tradely is a multi-tenant B2B Field Service Management (FSM) platform designed specifically for the SMB and solo-operator market. It focuses purely on "frictionless magic tricks," automating away the two largest pain points in field service: the "Dispatch Puzzle" via mathematical constraint solving, and the "Field Tech Administrative Burden" via local on-device Voice-to-Invoice AI. Tradely is uniquely built as a universal React Native application, providing a unified codebase for web, iOS, and Android.

## Success Criteria

### User Success
- **Dispatcher (The Chess Master):** Achieves "Command & Control" by eliminating reactive scheduling puzzle-solving. Validated when utilizing the "Panic Button" to re-optimize a disrupted daily schedule with a single click.
- **Field Tech (Boots on the Ground):** Achieves zero-friction administration by utilizing "Voice-to-Invoice" dictation instead of manual form entry on mobile devices.
- **End Customer:** Experiences anxiety-free "Uber-style" transparency, trusting the service via personalized SMS notifications with live ETAs and technician details.

### Business Success
- Immediate proof of value through pilot customer (Eubanks Electric).
- The business runs administrative tasks natively "on autopilot," eliminating manual dispatching bottlenecks.

### Technical & Measurable Success
- **Pilot Outcome:** Eubanks Electric exclusively utilizes Tradely during beta and converts to a paying customer (1/1 Conversion).
- **Adoption Rate:** 100% Daily Active Usage (DAU) by the pilot dispatcher, completely replacing physical whiteboards.
- **Efficiency Metric:** Measurable reduction in "Time to Invoice" (from job completion to invoice generation) driven by Voice-to-Invoice.
- **System Efficacy:** Core constraint solver ("Panic Button") outputs mathematically optimal schedules based on skills, location, and priority. Voice-to-Invoice accurately structures job descriptions into valid invoice items.

## Product Scope & Phased Development

### MVP Strategy (Phase 1)
**Approach:** "Magic Tricks" MVP targeting specific high-friction pain points: dispatch puzzles and field tech administrative overhead. 
**Excluded:** Quoting, estimates, advanced inventory tracking, QuickBooks integration, timecards.

**Must-Have MVP Capabilities:**
- Secure authentication and multi-tenant isolation.
- React Native Web/Mobile interfaces.
- Constraint algorithm ("Panic Button") acting on a NestJS backend.
- On-device local AI Voice-to-Invoice.
- Twilio outbound SMS integration.
- Stripe billing.

### Post-MVP Roadmap
- **Phase 2 (Growth - Months 2-6):** Consumer financing integrations, quoting workflows, and live inventory APIs (e.g., Home Depot/Ferguson).
- **Phase 3 (Expansion - Months 6-12+):** Proactive autonomous agents suggesting scheduling during gaps, automated handling of inbound customer texts/calls, and native QuickBooks deep integrations.

### Risk Mitigation Strategy
- **Technical Risk:** Voice-to-Invoice fails on older devices or hallucinates. *Mitigation:* System retains raw transcribed text and audio for manual admin review.
- **Market Risk:** Plumbers/Electricians reject algorithmic scheduling. *Validation:* The Eubanks Electric pilot success relies on abandoning whiteboards.
- **Resource Risk:** Triple-platform deployment delays a solo developer. *Contingency:* Utilize a single React Native Expo codebase.

## User Journeys

### 1. Job Creation (Dispatcher Success Path)
- **Context:** Sarah (Dispatcher) receives an inbound emergency call at 9:00 AM.
- **Action:** Enters customer details, sets "High Priority", and clicks "Find Slot".
- **Result:** Intelligent scheduler analyzes tech locations and certifications, suggesting a 10:30 AM slot. Sarah clicks "Assign," adding the job and triggering an SMS to the customer.

### 2. The Panic Scenario (Dispatcher Edge Case)
- **Context:** At 7:45 AM, a tech calls in sick, leaving 4 unassigned jobs including a VIP customer.
- **Action:** Sarah selects the sick tech and activates the "Panic Button" (Tech Out mode).
- **Result:** The system evaluates remaining technicians' proximity, skills, and priorities, returning a newly optimized fleet route within 5 seconds for Sarah's approval. 

### 3. Boots on the Ground (Field Tech Success Path)
- **Context:** Mike (Tech) hates administrative typing. He receives a push notification for a new urgent stop.
- **Action:** Views read-only Context Card, taps to navigate (Apple Maps), and completes the physical job. Taps the camera icon to quickly snap "Before/After" photos. Taps microphone to dictate: "Replaced faulty contactor on AC... Used one 40-amp contactor."
- **Result:** Tradely's local AI instantly transcribes and parses the audio into a structured draft invoice. Mike briefly reviews the parsed output, taps to correct a recognized part name, and hits "Complete Job."

### 4. End Customer (Success Path)
- **Context:** David (Customer) anxiously awaits a technician during a heatwave.
- **Action:** David's phone buzzes.
- **Result:** Receives SMS: "Hi David! Mike is 15 mins away... driving the blue van. Live ETA link..." establishing immediate trust.

### 5. Monitoring (Admin/SMB Owner Path)
- **Context:** Ryan (Owner) is out doing an estimate and wants to verify the business is running smoothly.
- **Action:** Opens Tradely dashboard on iPad.
- **Result:** Views real-time schedule, generated invoices, and technician statuses, validating operations are running autonomously.

## Innovation Analysis

### Detected Innovation Areas
- **"The Panic Button" (Constraint-Solving Dispatch):** Replaces drag-and-drop calendars with a mathematical constraint solver, programmatically shifting the fleet scheduling burden to the system.
- **Voice-to-Invoice (On-Device Local AI):** Leverages offline-capable, native iOS/Android speech-to-text and lightweight on-device LLMs to convert spoken technician notes directly into line-item invoices, eliminating mobile typing and cloud latency.
- **"Uber-Style" Consumer Transparency:** Replaces vague service windows with automated Twilio SMS triggers tied to live geographic technician statuses.

## SaaS & Mobile App Specific Requirements

### Technical Architecture
- **Platform Strategy:** Unified React Native (Expo) codebase targeting Web, iOS, and Android.
- **Database & Authentication:** Supabase (PostgreSQL) enforcing stringent Row Level Security (RLS) for data isolation across multiple SaaS tenants (`tenant_id`).
- **Core API & Business Logic:** Dedicated NestJS backend executing the heavy "Panic" scheduling algorithm and managing secure webhooks (Stripe, Twilio). 

### Multi-Tenancy & Access Model
- **Business Owner/Manager:** Full read/write across all metrics, billing, configuration, and jobs.
- **Admin/Dispatcher:** Can modify schedules, create jobs, run the constraint solver, and monitor all technician progress. 
- **Field Technician:** Restricted read-only view of assigned jobs; write access limited solely to their personal job statuses and voice dictation.

### Device Permissions & Hardware Constraints
- **Microphone:** Essential for local Voice-to-Invoice.
- **Location Services (GPS) & Background Processing:** Required for maintaining accurate dispatch routing and triggering proximity alerts for SMS.
- **Offline Mode:** The mobile application must actively cache state and queue network requests when technicians are out of cellular service.

## Functional Requirements (The Capability Contract)

### Account & User Management
- FR1: System can securely authenticate users based on assigned roles.
- FR2: Admin can provision and manage accounts for business technicians and staff.
- FR3: System enforces strict data isolation based on tenant association.

### Job & Customer Management
- FR4: Admin can create jobs specifying customer details, problem description, and priority flags (e.g., "Emergency").
- FR5: Admin can view a high-level daily dashboard of total jobs, technician statuses, and generated invoices.

### Dispatch & Scheduling (Command Center)
- FR6: Admin can view all active and unassigned jobs on a temporal calendar interface.
- FR7: Admin can mark technicians as unavailable (e.g., "Sick") and manually override/assign jobs.
- FR8: System can execute a constraint-solving algorithm ("Panic Button") to calculate and suggest optimal fleet-wide routes based on geographic location, required skills, and job priority.
- FR9: Admin can approve system-suggested schedules, automatically disseminating route changes to field technicians.

### Field Operations
- FR10: Technician can view a chronological daily list of their assigned jobs and associated read-only Context Cards (problem, required parts, address).
- FR11: Technician can trigger device-native map navigation directly from an assigned job.
- FR12: Technician can sequentially update job statuses ("En Route", "Arrived", "Completed").

### Voice-to-Invoice & Billing
- **FR13:** Technician can capture and attach situational photos (e.g., "Before", "After", "Defect") to the job record.
- **FR14:** Technician can record voice audio detailing work performed and parts used.
- **FR15:** System can transcribe spoken audio into text utilizing local on-device OS capabilities.
- **FR16:** System can intelligently parse transcribed text to format a structured, line-item draft invoice.
- **FR17:** Technician can seamlessly review and manually edit/correct the AI-parsed transcription or generated line items before submission.
- **FR18:** System retains raw transcribed text to facilitate manual review or fallback.
- **FR19:** System can securely queue and transmit structured invoices and attached photos to the backend for Admin finalization.
- **FR20:** Admin can review, modify, and finalize draft invoices and photo reports into official records.
- **FR21:** System can dispatch billing webhooks to external processors (Stripe) upon invoice finalization.

### Customer Communications
- **FR22:** System can automatically dispatch outbound SMS notifications to the end customer triggered by specific technician status changes.
- **FR23:** System can automatically merge dynamic ETAs and specific technician details (Name, Vehicle) into SMS templates.

## Non-Functional Requirements

### Performance & Reliability
- **NFR1:** The mobile application shall maintain 100% functionality for viewing cached Context Cards and recording Voice-to-Invoice audio while operating in a 0% cellular connectivity environment (Offline Mode).
- **NFR2:** The constraint-solving algorithm shall return a complete, optimized global route suggestion for up to 10 technicians and 50 jobs in under 5 seconds.

### Integration Constraints
- **NFR3:** Voice-to-Text transcription shall execute entirely via local OS capabilities (iOS Speech / Android SpeechRecognizer) without relying on external cloud APIs.
- **NFR4:** The system shall trigger the webhook dispatch of the outbound Twilio SMS within 10 seconds following a technician status update.

### Security
- **NFR5:** Database Row Level Security (RLS) policies shall cryptographically prevent any tenant from querying, mutating, or accessing records linked to another `tenant_id`, independent of client application logic.
