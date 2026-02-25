---
stepsCompleted: [1, 2, 3]
inputDocuments: ["_bmad-output/brainstorming/brainstorming-session-2026-02-16.md"]
date: 2026-02-24
author: Ryan.carroll
---

# Product Brief: tradely

<!-- Content will be appended sequentially through collaborative workflow steps -->



## Executive Summary

Tradely is a next-generation Field Service Management (FSM) platform purpose-built for SMB trades businesses (1-20 trucks, including plumbers, electricians, HVAC). Unlike incumbent software that attempts to solve every problem at a shallow level, causing administrative bloat, Tradely is designed to make the business side of trades "automatic." By starting with an uncompromising, AI-driven "Smart Dispatcher," the platform eliminates the cognitive load of scheduling puzzle-solving, allowing owners and dispatchers to focus on revenue-generating activities while providing field techs and customers with frictionless, delightful experiences. The ultimate goal is to remove administrative overhead so tradesmen can focus purely on the work.

---

## Core Vision

### Problem Statement

Small-to-medium trades businesses are drowning in white-collar drudgery. The administrative overhead required to schedule, dispatch, notify customers, track parts, and invoice jobs is stifling growth. Specifically, the "cognitive puzzle" of dynamically mapping available techs to jobs based on location, priority, and skill level in real-time is a high-stress, manual failure point for most 1-20 truck fleets. 

### Problem Impact

When the dispatching and administrative nervous system fails or slows down, the entire business suffers. 
- **Owners & Dispatchers** spend hours daily fighting fires instead of growing the business.
- **Field Techs** are burdened with complex apps, data entry, and manual note-taking, slowing down job completion.
- **Customers** experience anxiety from poor communication regarding arrival times and expectations, leading to frustrated inbound calls to the office.

### Why Existing Solutions Fall Short

Incumbent tools like ServiceTitan and Jobber are feature-dense but experience-poor. They have built massive, sprawling platforms that attempt to be everything to everyone, resulting in shallow, bloated feature sets. They focus on *digitizing* manual processes rather than *automating* them. For example, when a tech calls in sick, current software still requires the dispatcher to manually drag-and-drop an entire day's worth of appointments rather than leveraging algorithmic intelligence to effortlessly re-optimize the schedule.

### Proposed Solution

Tradely acts as an intelligent "Command & Control" center for the SMB trades business, starting with a deeply focused Smart Dispatcher MVP. It automates the administrative overhead so the business runs itself. 
- **For Dispatch:** A "Panic Button" algorithmically re-optimizes the entire day's schedule based on parameters like job priority, tech skills, and geographic proximity with a single click.
- **For Techs:** A "Tech Command" interface focuses strictly on "What, Where, and Parts," replacing tedious data entry with a "Voice-to-Invoice" workflow where AI transcribes spoken notes into structured job details and invoice items.
- **For Customers:** An "Uber-style" VIP tracking system sends friendly, natural language SMS updates with live ETA and technician details.

### Key Differentiators

Our unfair advantage lies in deep, comprehensive feature execution rather than wide, shallow bloat. 
- **Effortless Intelligence:** Moving beyond manual "drag and drop" UI into algorithmic, one-click logic (The Panic Button).
- **Zero-Friction Field Experience:** Eliminating the white-collar keyboard drudgery for blue-collar workers via Voice-to-Invoice.
- **Customer Delight:** Transforming robotic, automated text messages into personalized, natural language updates that build immediate trust.

## Success Metrics

### Business Objectives
The primary objective for the MVP phase (Weeks 1-6) is to transition from concept to a tangible, deeply integrated product used daily by our pilot customer. The goal isn't immediate MRR growth, but rather irrefutable proof of value.
- **Goal:** Eubanks Electric successfully utilizes Tradely for its daily dispatching and scheduling operations without major disruptions.
- **Outcome:** At the end of the pilot, the customer explicitly requests to continue using the software instead of returning to their previous system or relying on manual whiteboards.

### Key Performance Indicators (KPIs)

- **Pilot Conversion:** 1 / 1. The software is successfully deployed to the pilot customer, and they agree to become a paying customer post-beta.
- **Daily Active Usage (DAU):** 100% adoption by the pilot dispatcher. The physical whiteboard is no longer the source of truth.
- **Time to Invoice (Leading Indicator):** A reduction in the time from job completion to invoice generation, driven by the Voice-to-Invoice feature replacing manual data entry.

## Target Users

### Primary Users

**1. The Dispatcher (The "Chess Master")**
- **Context:** Works in the office (or occasionally remote), managing the daily schedule for 1-20 field technicians. They are the nerve center of the business.
- **Problem Experience:** They spend their day playing a high-stakes puzzle game. When a tech calls in sick or an emergency job drops in, they must manually call/text techs, drag-and-drop calendar appointments, and guess at the most efficient routing. It is highly reactive and stressful.
- **Success Vision:** Reaching a state of "Command & Control." They hit the "Panic Button," and the system automatically suggests the new, mathematically optimal schedule based on tech skills, location, and job priority. They review and execute with a single click.

**2. The Field Tech (The "Boots on the Ground")**
- **Context:** Out in the field, driving between jobs, often under a sink or in a cramped space. Their hands are dirty, and their primary focus is fixing the physical problem.
- **Problem Experience:** They hate administrative work. Typing out detailed job notes, manually calculating parts used, and navigating clunky apps on a small screen slows them down and frustrates them. 
- **Success Vision:** A zero-friction, read-only interface. They want to open the app, instantly see "What, Where, and Parts," do the job, and use Voice-to-Invoice to let the AI handle the paperwork while they drive to the next stop.

### Secondary Users

**1. The SMB Owner**
- **Context:** Owns the trades business. May still work in the field or might be fully focused on management.
- **Problem Experience:** They are the bottleneck. If the dispatcher is overwhelmed, the owner has to step in. They lack real-time visibility into the exact status and profitability of the day without making phone calls.
- **Success Vision:** A business that runs itself. Knowing that the dispatcher has the tools to handle emergencies flawlessly without the owner's intervention.

**2. The End Customer (Homeowner or Business)**
- **Context:** Waiting for service, often experiencing a stressful situation (e.g., broken AC in summer, burst pipe).
- **Problem Experience:** The "four-hour service window" leaves them trapped at home. They lack transparency on exactly who is coming and when, leading to anxious calls to the dispatcher ("Where is my tech?").
- **Success Vision:** The "Uber" experience. Receiving a natural language SMS with the tech's name, photo, and a precise, live-tracking ETA, completely eliminating anxiety and building instant trust.

### User Journey (The "Panic Scenario")

1. **The Trigger:** At 7:45 AM, Tech #2 calls the Dispatcher to report they are sick. The dispatcher has 4 jobs currently assigned to Tech #2.
2. **The "Panic Button" (Dispatcher):** The Dispatcher clicks the "Tech Out" button in Tradely. The AI instantly analyzes the remaining fleet's locations, skill sets (e.g., who is certified for HVAC), and job priorities (e.g., VIP customer).
3. **The Re-route (Dispatcher):** The system presents a newly optimized schedule. The Dispatcher clicks "Approve."
4. **The Update (Field Tech):** Field Tech #5 (already on the road) receives a push notification: "Schedule Updated: 1 urgent stop added." They tap to see the read-only Context Card detailing the new job and any required parts.
6. **Task Completion (Field Tech):** Mike finishes the job, hits the voice record button on his app, speaks what he did for 30 seconds, and drives away. Tradely's AI parses the audio to create a structured note and invoice draft for the back office.

## MVP Scope

### Core Features (The "Walking Skeleton" + 3 Magic Tricks)

To achieve our 6-week launch with a solo developer, we must ruthlessly constrict scope to the core dispatching flow and our primary differentiators. The architecture will rely on Next.js/React Native connected to a dedicated Node.js backend to ensure algorithmic scalability, utilizing Supabase primarily as a managed Postgres database (with pgvector and PostGIS) and for Auth.

**Module 1: The Command Center (Web App)**
- Secure Authentication (Clerk/Supabase).
- Admin Dashboard with a daily view of scheduled jobs and technician status.
- **The Panic Button:** Core algorithmic constraint solver that takes a dynamically changing calendar, considers technician tags (skills) and rough geographic clustering, and outputs a re-optimized schedule when triggered by a dispatcher.
- Job Creation interface (Customer info, Problem description, Priority flag).
- Simple Webhook/Stripe integration for sending generic invoices.

**Module 2: The Field Interface (Mobile Experience)**
- Cross-platform functionality (React Native/Expo).
- Technician Login & Daily Schedule View.
- Read-Only "Context Cards" per job (Customer name, address, notes).
- **Voice-to-Invoice:** 30-second audio recording capability that uses Whisper API + LLM to parse spoken notes into a structured readable summary and a line-item invoice list.
- One-tap deep linking to native maps (Google Maps/Apple Maps) for navigation to the job or supplier.

**Module 3: Customer VIP Communication (Background Service)**
- **Uber-SMS:** Twilio integration tied to job status updates. Automated SMS sent when a tech is assigned/dispatched, including tech name and estimated arrival window.

### Out of Scope for MVP

We are intentionally saying "no" to these features for the V1 pilot to prevent scope creep:
- Complex inventory tracking and predictive ordering.
- Multi-day project management or quoting/estimating workflows.
- Native QuickBooks deep integrations (we will rely on manual CSV exports or Zapier for V1).
- Timecard punching and payroll calculations.
- Customer-facing portals or mobile apps.

### Future Vision

If this MVP successfully proves the "Smart Dispatcher" wedge, the 12-24 month vision expands Tradely into a true, comprehensive FSM that runs the entire business on autopilot, supported by the scalable Node.js backend:
- **Phase 2 (Months 2-6):** Robust QuickBooks synchronization, integrated consumer financing/quoting, and advanced inventory APIs (e.g., automatically checking local Ferguson stock for parts).
- **Phase 3 (Months 6-12):** Autonomous Agents. Dispatching becomes entirely proactive. The system predicts maintenance windows for recurring customers and automatically suggests scheduling them during gaps in the route.
- **Phase 4 (Year 2+):** Transitioning from a tool to a fractional employee. The AI handles basic inbound customer SMS/calls regarding scheduling and automatically slots them into the calendar without human intervention.
