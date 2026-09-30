# 🇮🇳 India247
### *Your City. Your Voice. Your Right.*

> **Transforming civic grievance from a broken form into a two-way conversation between citizens and their government.**

India247 is an AI-powered civic complaint platform built for Indian cities. It replaces opaque, bureaucratic grievance portals with a transparent, accountable, and participatory ecosystem — where every pothole reported, every garbage pile flagged, and every broken streetlight documented moves through a verified, trackable pipeline from citizen to officer to resolution.

---

[![Live Demo](https://img.shields.io/badge/Live%20Demo-india247.shashankraj.in-brightgreen?style=for-the-badge&logo=vercel)](https://india247.shashankraj.in/)
[![Demo Video](https://img.shields.io/badge/Demo%20Video-Watch%20Now-red?style=for-the-badge&logo=google-drive)](https://drive.google.com/file/d/1oKSgoGd8TW02w94pK8SzEgNVk9F37st4/view?usp=sharing)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react)](https://react.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=flat-square&logo=node.js)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/atlas)
[![Firebase](https://img.shields.io/badge/Firebase-Auth-FFCA28?style=flat-square&logo=firebase)](https://firebase.google.com/)
[![Gemini AI](https://img.shields.io/badge/Gemini-3.8%20Flash-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)

---

## 🔴 The Problem

Every day, millions of Indian citizens encounter broken civic infrastructure — crumbling roads, overflowing drains, dead streetlights, uncollected garbage. Yet most never report these issues.

**Not because they don't care. Because the system doesn't make it easy.**

- **Filing is painful.** Government portals demand lengthy forms, category codes, ward numbers, and bureaucratic terminology most citizens don't know.
- **Submission is a black hole.** Once submitted, complaints disappear. There is no tracking, no timeline, no status update.
- **Accountability is absent.** Officers face no real consequence for delayed or sham resolutions. A complaint can be "closed" without the issue being fixed.
- **Citizens have no voice after submission.** If a problem resurfaces, there is no structured way to escalate.
- **Community awareness is zero.** Neighbours don't know what issues others have reported. There is no shared civic picture.
- **Manual routing is slow.** Complaints land in central inboxes and get manually sorted, often taking days before reaching the right department.

The result: civic decay continues. Citizens disengage. Trust erodes.

---

## ❌ Why Existing Systems Fail

| What Citizens Face Today | What India247 Delivers |
|---|---|
| Long, confusing online forms | Conversational AI — just describe the problem naturally |
| No idea which department to contact | Automatic AI classification routes the complaint |
| Complaint submitted → silence | Live tracking with a timestamped resolution timeline |
| Officers close issues without fixing them | Officers must upload proof (photo + note) to mark Resolved |
| No way to challenge a false closure | AI-validated Reopen system with image verification |
| Zero transparency into city-wide issues | Public community feed showing all active issues on a map |
| No incentive to participate | Gamified reward points, badges, and a city leaderboard |
| Complaints routed by chance | Workload-balanced, region-aware auto-assignment to officers |
| No oversight at the top | Admin dashboard with SLA monitoring |

---

## 💡 The India247 Solution

India247 is built around a single philosophy: **every civic issue deserves a structured, visible, accountable journey.**

```
REPORT  →  TRACK  →  RESOLVE
```

Citizens don't fill forms. They have a conversation with **Meera**, our AI assistant, who gathers the details, captures evidence, classifies the issue, and packages it into a verified complaint — all in under two minutes.

From there, the complaint is automatically assigned to the right officer in the right region based on real-time workload. Officers work through a structured pipeline. Citizens watch every stage update in real time. If an issue is falsely closed, citizens can request a reopen — backed by image evidence, validated by AI before the case moves back to Pending.

Every actor in the system — citizen, officer, admin, and government official — has a dedicated interface with the information and controls they need.

---

## 🧑‍🤝‍🧑 The Citizen Experience

### 1. Report — Chat with Meera AI
Instead of a form, citizens open a chat. **Meera** — our conversational AI assistant powered by Gemini 3.5 Flash-Lite — asks exactly the right questions: What's the issue? How long has it been there? Does it pose a safety risk? Meera adapts her questions to the context, never asks redundant ones, and supports English, Hindi, and Hinglish naturally.

Once enough detail is collected, Meera signals the app to transition to evidence collection.

### 2. Upload Photo Evidence
Citizens upload a photo of the civic issue directly from their camera or gallery. Gemini Vision analyzes the image to verify it is relevant to the reported problem — preventing spam before it enters the system.

### 3. Pin the Location
An embedded Google Maps interface with autocomplete lets citizens pin the exact location of the issue. GPS-assisted auto-location makes this effortless. The coordinates are stored and mapped for the community.

### 4. Track — Live Status Timeline
Every complaint gets a unique Tracking ID (e.g., `IND-2026-47821`). Citizens can look up their complaint at any time and see a full timestamped timeline:
`Complaint Filed → Sent to Department → Under Inspection → Work Started → Resolved`

The assigned officer's name, department, average resolution time, and completion rate are visible to the citizen — creating direct accountability.

### 5. Community Feed
A social-media-style feed shows all active and resolved complaints city-wide. Citizens can:
- Upvote issues to signal community priority
- Comment on complaints to add updates or share information
- Sort by Latest, Most Upvoted, or Trending (weighted by upvotes + comments + shares)
- Filter by category or proximity

### 6. Rewards & Leaderboard
Every civic action earns points:
- **+10 pts** for filing a complaint
- **+25 pts** when a complaint is resolved
- **+2 pts** per upvote received
- **+1 pt** per community comment

Points unlock badges (Beginner → Reporter → Contributor → Advocate → Expert → Champion) and a rewards catalog including Metro Smart Cards, mobile recharges, and app vouchers. A city-wide leaderboard publicly ranks the most active citizens.

### 7. Reopen — Challenge a False Closure
If a complaint is marked Resolved but the problem persists, citizens can request a Reopen. They must provide:
- A written reason explaining why the issue is still unresolved
- A new photo as evidence

Both are validated by Gemini AI before the complaint is pushed back to Pending — preventing system abuse while protecting genuine citizens.

---

## 👮 The Officer Experience

### Dedicated Dashboard
Officers log in to a role-gated portal that surfaces only their assigned complaints — filtered automatically by department and region. Three queues are clearly separated: active complaints, reopened escalations, and resolved cases.

### Workload-Based Assignment
When a complaint is filed, the backend's `assignmentService` automatically:
1. Identifies the correct department from the complaint's AI-classified category
2. Queries all active officers in that department and region
3. Assigns to the officer with the **lowest current complaint load** (`currentLoad`)
4. Increments the officer's load counter in real time

This prevents any single officer from being overwhelmed while others sit idle.

### Performance Metrics
Officers see their live metrics at a glance:
- **Current Load** — complaints currently assigned
- **Resolved** — total complaints closed
- **Reopened** — complaints citizens challenged after closure
- **Trust Score** — a platform accountability indicator
- **Citizen Rating** — average star rating from resolved complaints
- **Avg. Resolution Time** — historical speed of resolution

These metrics are also visible to citizens on the tracker, and to admins for oversight.

### Resolution with Proof
Officers cannot simply click a "Mark Resolved" button. To close a complaint, they must:
- Write a resolution note describing the work done
- Upload a photographic proof of the completed work

The backend enforces this — the API rejects any resolution attempt missing either the note or the image. This single rule eliminates false closures at the infrastructure level.

### Stage Workflow
Officers move complaints through structured stages:
`Sent to Department → Under Inspection → Work Started → Resolved`

Each transition is timestamped and appended to the complaint's timeline, which is immediately visible to the citizen.

---

## 🤖 AI in India247

AI is not a feature in India247 — it is the backbone of trust and efficiency.

### Meera — Conversational Reporting AI
**Model:** Gemini 3.5 Flash-Lite (server-proxied, API key never exposed to client)

Meera is a purpose-built AI persona designed for civic reporting. Her system prompt enforces strict conversational discipline:
- Asks **exactly one question per message** — never combines two
- Skips questions whose answers are already implied
- Detects user language (English / Hindi / Hinglish) and mirrors it
- Redirects out-of-scope issues (cybercrime, medical, financial fraud) to the appropriate government helplines
- Emits a hidden `[INTENT: "..."]` signal when she has understood the issue
- Emits `[READY_FOR_PHOTO]` only after a clean confirmatory statement — never inside a question

The result: a filing experience that feels like talking to a knowledgeable neighbor, not filling a government form.

### AI Classification — Department Routing
**Model:** Gemini 3.8 Flash (server-side, deterministic — temperature 0.0)

After Meera extracts intent, a second AI call classifies the complaint into one of 10 civic categories (Roads & Infrastructure, Sanitation, Water Supply, Electricity, Encroachment, Animal Welfare, Public Facilities, Construction & Safety, Taxes & Documentation, Other Civic Issues) and maps it to the responsible municipal authority (PWD, Jal Board, Municipal Sanitation Dept, Animal Control, etc.).

This classification is then used by `assignmentService` to route the complaint to the right department and officer — automatically, without any human dispatcher.

### AI Reopen Validation — Preventing Abuse
**Models:** Gemini 3.8 Flash (text) + Gemini 3.8 Flash Vision (image)

When a citizen requests a reopen, two independent AI checks run before the complaint is allowed back into the system:

1. **Text Validation:** Gemini evaluates whether the citizen's written reason is genuinely related to the original complaint and demonstrates the issue is unresolved — not spam, not an unrelated grievance.
2. **Image Validation:** Gemini Vision cross-checks the submitted photo against the original complaint description to verify it supports the reopen reason.

Both checks must pass. If either fails, the request is rejected with a clear explanation. This protects officers from serial abuse while preserving citizens' right to challenge genuine false closures.

---

## 🛡️ Accountability by Design

India247 does not rely on goodwill. Accountability is enforced at every layer of the system.

| Failure Mode | India247's Structural Response |
|---|---|
| **Complaint gets lost** | Unique Tracking ID generated at submission; complaint is findable by the citizen at any time |
| **Officer ignores assignment** | Current load tracked in real time; SLA countdown visible to Admin dashboard |
| **Officer falsely closes a complaint** | Backend rejects resolution without proof photo + written note |
| **Citizen abuses the reopen system** | AI validates both written reason and image before allowing a reopen; limit of 1 reopen per complaint |
| **No visibility for senior officials** | Admin dashboard shows SLA breaches, department analytics, and officer management |
| **No citizen feedback on resolution quality** | Citizens rate resolved complaints (1–5 stars); ratings aggregate into the officer's public performance score |
| **Routing biases** | Auto-assignment sorts by lowest current load — not seniority, not manual choice |
| **Complaint reassigned unfairly** | Admin can override with a full audit trail appended to the timeline ("Reassigned by Admin") |

---

## 🔄 End-to-End Workflow

```
┌─────────────────────────────────────────────────────┐
│                    CITIZEN                          │
│   Opens app → chats with Meera AI                  │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│                   MEERA AI                          │
│   Gathers context → extracts [INTENT]               │
│   Requests photo → signals [READY_FOR_PHOTO]        │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│              AI CLASSIFICATION                      │
│   Gemini classifies category + maps department      │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│              SMART ASSIGNMENT                       │
│   assignmentService finds dept → picks officer      │
│   with lowest currentLoad in matching region        │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│              OFFICER DASHBOARD                      │
│   Officer sees complaint → moves through stages     │
│   Complaint Filed → Under Inspection → Work Started │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│              RESOLUTION WITH PROOF                  │
│   Officer uploads photo + note → Resolved           │
│   Officer metrics updated; load decremented         │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│              CITIZEN FEEDBACK                       │
│   Citizen views timeline → rates officer (1–5 ★)   │
└─────────────────────┬───────────────────────────────┘
                      │
                 Issue persists?
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│           REOPEN REQUEST (if needed)                │
│   Citizen submits reason + new photo                │
│   AI validates both → Complaint → Pending again     │
└─────────────────────────────────────────────────────┘
```

---

## 🌆 Community & Civic Impact

India247 is not just a complaint tool. It is a civic participation platform.

**Transparency at scale.** Every filed complaint is visible on the community feed and map. Citizens can see, in real time, what issues are being reported in their city and whether they are being resolved. Civic infrastructure is no longer invisible.

**Collective voice.** Upvotes allow communities to signal which issues matter most. A pothole with 200 upvotes carries social weight that a single complaint never could. This creates organic pressure for faster resolution.

**Trust through visibility.** When citizens can see the assigned officer's name, department, and performance record — and when they can see the resolution photo — the system becomes verifiable. Trust is not asked for; it is earned through evidence.

**Positive reinforcement for good citizenship.** The rewards system turns civic engagement into a habit. Filing a complaint, commenting on a neighbour's issue, or getting a problem resolved earns tangible recognition. Over time, this creates a culture of civic participation rather than learned helplessness.

**A feedback loop that improves governance.** Citizen ratings on resolutions and SLA breach alerts for admins — this data surfaces patterns that help municipal bodies allocate resources more effectively.

**Replicable across cities.** The regional assignment logic, department taxonomy, SLA configuration, and role hierarchy are all parameterizable. Deploying India247 in a new city requires seeding departments, officers, and region boundaries — not rebuilding the platform.

---

## 📈 Expected Impact

**For Citizens:**
- Dramatically reduced friction in reporting civic issues — from a multi-step form to a two-minute conversation
- Full visibility into complaint status without needing to call anyone or visit an office
- A meaningful mechanism to challenge false closures, backed by AI verification
- A community platform that makes civic engagement social and rewarding

**For Officers:**
- Structured, prioritized workload — no more unfiltered inbox chaos
- Clear accountability metrics that reward genuine resolution
- SLA awareness prevents issues from quietly ageing past deadlines
- Performance data that can be used to recognize high-performing officers

**For Municipal Administration:**
- Department-level analytics revealing resolution bottlenecks
- SLA breach monitoring to surface systemic under-performance
- Officer reassignment capability for emergency rebalancing
- A data trail for every complaint from submission to closure

**For Governance:**
- City-wide civic data that was previously invisible, now structured and auditable
- A platform that makes accountability a default — not an exception

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                     FRONTEND (Vercel)                       │
│  React 19 + Vite SPA │ Tailwind CSS v4 │ Context API        │
│  Pages: Landing, Report, Map, Feed, Tracker, Rewards,       │
│         Officer Dashboard, Admin Dashboard                  │
└────────────────────────┬─────────────────────────────────────┘
                         │ HTTPS REST
┌────────────────────────▼─────────────────────────────────────┐
│                     BACKEND (Render)                         │
│  Node.js + Express │ Stateless REST API                      │
│  Routes: complaints, users, ai, officer, admin               │
│  Middleware: Firebase UID auth, role-based access control    │
│  Utils: assignmentService, classificationAI, reopenAI        │
└─────┬──────────────────┬────────────────┬────────────────────┘
      │                  │                │
      ▼                  ▼                ▼
┌───────────┐   ┌──────────────┐   ┌────────────────────┐
│ MongoDB   │   │  Gemini API  │   │   Cloudinary       │
│  Atlas    │   │  3.8 Flash   │   │   (Image Storage)  │
│(Mongoose) │   │3.5 Flash-Lite│   │                    │
└───────────┘   └──────────────┘   └────────────────────┘
      │
      ▼
┌───────────┐   ┌──────────────────────────┐
│ Firebase  │   │   Google Maps API        │
│   Auth    │   │   + React Leaflet        │
│  (Users)  │   │   (Location & Mapping)   │
└───────────┘   └──────────────────────────┘
```

---

## 🛠️ Tech Stack

| Domain | Technology |
|---|---|
| **Frontend** | React 19, Vite, Tailwind CSS v4, Lucide React, Axios |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB Atlas, Mongoose ODM |
| **Authentication** | Firebase Auth (synced to MongoDB for role management) |
| **AI — Conversational** | Google Gemini 3.5 Flash-Lite (Meera chat interface) |
| **AI — Classification** | Google Gemini 3.8 Flash (intent-to-category mapping) |
| **AI — Vision** | Google Gemini 3.8 Flash Vision (image & reopen validation) |
| **Cloud Storage** | Cloudinary (complaint images, resolution proofs) |
| **Mapping** | Google Maps API (autocomplete, location pin) |
| **Deployment — Frontend** | Vercel |
| **Deployment — Backend** | Render |

---

## ✅ Current MVP Scope

All features below are implemented and live in the deployed platform:

**Citizen**
- [x] Firebase authentication (sign up / sign in)
- [x] Conversational AI complaint filing via Meera (Gemini 3.5 Flash-Lite, server-proxied)
- [x] AI image verification of uploaded evidence (Gemini Vision)
- [x] Google Maps autocomplete + pin-based location selection
- [x] AI classification of complaint into category + department (Gemini 3.8 Flash)
- [x] Unique Tracking ID generation per complaint
- [x] Live complaint tracker with full timestamped timeline
- [x] Assigned officer profile + performance stats visible to citizen
- [x] AI-validated reopen request (text reason + image, 1 reopen per complaint)
- [x] Resolution rating system (1–5 stars on resolved complaints)
- [x] Community feed with sorting (Latest, Most Upvoted, Trending)
- [x] Category and proximity-based feed filtering
- [x] Optimistic upvoting with instant UI feedback
- [x] Commenting on community complaints
- [x] Points-based gamification (filing, resolution, upvotes, comments)
- [x] Badge progression (6 tiers: Beginner → Champion)
- [x] Rewards catalog with redemption (cashback, Metro card, recharge, vouchers)
- [x] City leaderboard (top 10 citizens by points)
- [x] Map-to-Feed deep linking (tapping a map marker scrolls to the Feed card)

**Officer**
- [x] Role-gated Firebase auth with officer dashboard
- [x] Workload-balanced auto-assignment (lowest `currentLoad` in region)
- [x] Structured complaint stage progression
- [x] Resolution proof upload (note + image enforced at API level)
- [x] Real-time personal metrics (load, resolved count, citizen rating, avg resolution time)
- [x] Separate queues for active, reopened, and resolved complaints

**Admin**
- [x] Platform overview (total, pending, in-progress, resolved, reopened)
- [x] Officer management with active/inactive toggle
- [x] Complaint reassignment with audit trail
- [x] SLA breach monitoring (complaints overdue relative to department SLA hours)
- [x] Department-level analytics (resolution rate, avg resolution time, reopen %)

---

## 🗺️ Future Roadmap

| Feature | Description |
|---|---|
| **Chief Minister (CM) Dashboard** | State-level oversight dashboard with department rankings, officer trust scores, regional analytics, and critical escalation tracking |
| **Municipal API Integration** | Direct integration with state-level grievance portals (e.g., CPGRAMS, IGRS) for automatic escalation |
| **Voice Reporting** | Voice-to-text complaint filing for citizens with low digital literacy |
| **Multilingual Support** | Formal support for 10+ Indian regional languages beyond Hinglish |
| **WhatsApp Reporting Channel** | File complaints directly via WhatsApp without opening the app |
| **Predictive Civic Analytics** | ML models to predict high-complaint zones and enable preventive maintenance |
| **Analytics Dashboard for Cities** | City-level data visualizations for municipal planners and urban policy teams |
| **Wider Deployment** | Region and department configuration to support any Indian city or state |
| **Mobile App (Native)** | Android and iOS apps for broader reach including low-end devices |
| **Officer SLA Notifications** | Push/SMS alerts to officers approaching SLA deadlines |
| **Public API** | Open API for researchers, journalists, and civic organizations to access anonymized civic data |

---

## 🎬 Demo

| | |
|---|---|
| **Live Platform** | [india247.shashankraj.in](https://india247.shashankraj.in/) |
| **Demo Video** | [Watch on Google Drive](https://drive.google.com/file/d/1oKSgoGd8TW02w94pK8SzEgNVk9F37st4/view?usp=sharing) |
| **API Base** | `https://api.india247.shashankraj.in` |

To explore the platform:
1. Sign up as a Citizen to file complaints, track them, and engage with the community feed
2. Contact us for Officer / Admin demo credentials for role-specific dashboards

---

## ❤️ A Clean City Is Everyone's Right

India247 was built on a simple conviction: civic infrastructure fails partly because the feedback loop between citizens and government is broken. When reporting is hard, citizens stop reporting. When accountability is invisible, officers stop being accountable. When nothing improves, communities disengage.

India247 repairs this loop — one civic complaint at a time.

**Citizen Voice → Government Action → Visible Outcome.**

Every pothole documented. Every drain reported. Every streetlight flagged. Tracked. Verified. Resolved.

---

*Built for India. Designed for accountability. Powered by the people.*
