---
stepsCompleted: [step-01-init.md, step-02-discovery.md, step-03-core-experience.md]
inputDocuments: ["_bmad-output/planning-artifacts/prd.md", "_bmad-output/planning-artifacts/product-brief-tradely-2026-02-24.md", "_bmad-output/brainstorming/brainstorming-session-2026-02-16.md"]
---

# UX Design Specification tradely

**Author:** Ryan.carroll
**Date:** 2026-03-26

---

## Executive Summary

### Project Vision
Tradely is a constraint-solving Field Service Management platform focused on extreme automation. The UX vision is to create a "frictionless magic trick" that eliminates cognitive overload for dispatchers and keyboard data entry for field technicians.

### Target Users
- **The Dispatcher:** Needs a high-trust, desktop-optimized "Command Center" to visualize and manipulate complex schedules.
- **The Field Tech:** Requires a rugged, massive-tap-target mobile interface prioritizing read-only Context Cards and Voice interactions over manual typing.
- **The End Customer:** Desires seamless, Uber-style transparency via automated SMS rather than an app download.

### Key Design Challenges
- **Zero-Friction Mobile UI:** Designing a mobile app that requires almost zero screen-tapping for technicians with dirty hands.
- **Trusting the "Black Box":** Designing the "Panic Button" results so dispatchers confidently approve algorithmic re-routes without feeling a loss of control.
- **Offline States:** Seamlessly communicating offline caching states to technicians without blocking their workflow.

### Design Opportunities
- **Proactive Anomaly Alerts (Roadmap):** Instead of waiting for a manual "Panic Button" press, the system proactively monitors for physical anomalies (e.g., GPS indicates a tech is running late) and pushes a visual alert to the dispatcher to re-optimize.
- **Algorithmic Satisfaction:** Using micro-animations and loading states to make the compilation of the re-optimized schedule feel extremely premium and satisfying.
- **Audio/Haptic Feedback:** Leaning heavily into haptic vibrations to confirm voice recordings, allowing techs to operate the app without looking at it.

## Core User Experience

### Defining Experience
The defining experience for Tradely isn't data entry—it's **trusting the automation**. 
For the Dispatcher, the core action is anomaly resolution: hitting the "Panic Button" and reviewing a mathematically perfect re-route. For the Field Tech, the core action is the "Voice-to-Invoice" dictation—replacing five minutes of sitting in a hot van tapping on a screen with 30 seconds of natural speech, coupled with frictionless photo capture and simple tap-to-edit corrections.

### Platform Strategy
- **Dispatcher / Owner:** Desktop Web or iPad tablet. High information density, focused on macro-level map views, routing health, and business metrics.
- **Field Technician:** Native Mobile iOS/Android (via Expo). Must have massive, high-contrast tap targets designed for outdoor glare and dirty hands. 
- **End Customer:** Ubiquitous SMS (Twilio webhook). Zero app installations required to view tracking.
- **Core Requirement:** The mobile app must remain fully operational in offline environments—caching Context Cards, photo uploads, and queuing voice transcriptions invisibly.

### Effortless Interactions
- **One-Click Re-routing:** The system automatically calculates travel time, tech skills, and job priority. The Dispatcher does no math—they just review and click "Approve."
- **Invisible Data Entry:** The Field Tech hits record and speaks, and snaps photos natively without diving into complex file pickers. The local on-device LLM handles all structuring. If the AI hallucinates, intuitive, chunky editing modules allow swift, annoyance-free corrections.
- **Background Syncing:** Network connectivity drops should never block a tech from marking a job "Done." The app handles large media and data queuing silently.

### Critical Success Moments
- **The "Aha" Dispatch Moment:** A tech calls in sick at 8:00 AM, and what used to take two hours of frantic whiteboarding takes five seconds of algorithmic sorting.
- **The "Look Ma, No Hands" Tech Moment:** A tech dictates a complex AC repair note while walking back to their van, quickly confirms the parsed accuracy, and the draft invoice with photos is ready before they start the engine.
- **The Customer Trust Moment:** A homeowner receives a text with the tech's photo and exact ETA, eliminating the anxiety of the "4-hour service window."

### Experience Principles
1. **Magic Over Manual:** If the system can calculate or infer it, never ask the user to input it.
2. **Audio/Haptic First (Field):** Assume the technician cannot look closely at the screen. Rely on bold colors and strong haptic feedback for success/failure states.
3. **Command & Control (Office):** Dispatchers must feel like orchestra conductors, not data entry clerks. Provide total visibility without clutter.

## Desired Emotional Response

### Primary Emotional Goals
- **Empowered & In Control (Dispatcher):** The dispatcher should feel like an orchestra conductor. Even though the AI is doing the heavy lifting, the UX must enforce that the dispatcher is the one making the final calls.
- **Unburdened & Efficient (Field Tech):** The tech should feel relief. Capturing photos and dictating notes should feel like an invisible assistant rather than a mandatory corporate tracking tool. Quick correction interfaces must prevent the "AI frustration" of fighting with the machine.
- **Relieved & Trusting (End Customer):** The customer should feel immediate relief from the anxiety of waiting, transitioning to complete trust in the service provider.

### Emotional Journey Mapping
- **Discovery / Onboarding:** "Finally, a tool that does the administrative work for me."
- **First Core Action (The Panic Button):** Initial skepticism over the "black box" algorithm → Delight and massive relief when the re-routed schedule is instantly generated and mathematically perfect.
- **Routine Use (Voice-to-Invoice & Photos):** The quiet satisfaction of walking back to the van, taking a quick completeness photo, speaking for 30 seconds, quickly reviewing the output, and driving away without ever typing on a small keyboard.

### Micro-Emotions
- **Trust vs. Skepticism:** The primary emotional hurdle. The system must earn trust every time it suggests a schedule change or parses an invoice. Allowing the tech to easily *correct* the AI builds trust that they are still in control.
- **Accomplishment vs. Frustration:** The dopamine hit of clearing the board (Dispatcher) or checking off the last job of the day (Tech) without being bogged down by paperwork or failing media uploads.

### Design Implications
- **Trust → Explainability UX:** When the "Panic Button" suggests a route, the UI must briefly explain *why* (e.g., "Sarah selected: 10 mins closer; HVAC Certified"). Transparency builds trust.
- **Relief → Distinct Haptics:** For Voice-to-Invoice, use a very distinct, satisfying haptic vibration and audio chime to confirm success.
- **Control → Forgiving AI:** The UI for editing the parsed AI dictation must be "chunky," utilizing large touch targets and forgiving text editors, ensuring that fixing an AI mistake is never more frustrating than just typing it manually.
- **Empowerment → High-Contrast Hierarchy:** The dispatcher dashboard should use calm, neutral colors for standard operations, reserving stark, high-contrast colors only for anomalies (like a tech running late).

### Emotional Design Principles
1. **Automation Requires Transparency:** Always show the user that the system is working for them, and never obscure the "why" behind an AI decision. Provide straightforward correction methods when the AI errs.
2. **Respect the Worker's Environment:** Design for the physical reality of the job (glare, dirty hands, driving). Effortless physical interaction breeds emotional relief.

<!-- UX design content will be appended sequentially through collaborative workflow steps -->
