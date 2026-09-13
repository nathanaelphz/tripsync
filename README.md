# TripSync by APUGOKGOK

| | |
|---|---|
| **Team** | Nathanael Phan Ern Shen, Lin Zhe Wei |
| **Problem Statement** | Travel Planner |
| **Video Presentation** | [Watch on YouTube](https://youtu.be/GRBT2-oDuFQ) |
| **Presentation Slides** | [View Slides](https://docs.google.com/presentation/d/1TSr42sfEEWnvQ6T0hCGIP3MUyKHG1ewT/edit?usp=sharing&ouid=117628435611642126909&rtpof=true&sd=true) |

---

## 1. Project Overview

**The Problem.** Group trips get planned across five apps and a chaotic group chat, with no single tool handling group consensus or disruption. Existing apps like Wanderlog and TripIt only solve one piece each — itinerary or budgeting — leaving travellers to manually replan everything when a flight is delayed or the weather changes.

**Our Solution.** TripSync turns everyone's budget, availability, and interests into one shared itinerary that keeps working when plans change. It rebuilds the plan automatically through Plan Rescue, lets users add places via an AI chatbot from any link or photo, and includes built-in directions and a shared expense splitter. The result is one app that replaces the five-app, one-group-chat workflow.

---

## 2. Ideation & Process

### 2.1 Ideas We Considered

| Idea | Why it was dropped / kept |
|---|---|
| **A (Chosen)** — Multiple plan options given for users to choose their final travel plan | Kept because it lets the group decide on a final plan that everyone accepts |
| **B (Chosen)** — Plan Rescue: when unexpected changes happen (flight delayed, weather changes), AI automatically regenerates a plan for the user | Kept because it acts as a backup plan so users don't need to worry about external factors |
| **C (Chosen)** — AI chatbot that can analyze external links or pictures and add the place as part of the plan | Kept because it acts like a "super member" of the team |
| **D** — Auto-detect nearby location and build a plan from it | Dropped due to too much uncertainty from the user's location — e.g. if a user is in a remote village, there may be nothing nearby worth suggesting |

### 2.2 Ideation Boards

[Mindmap](https://drive.google.com/file/d/1bY8-PT5ccENwLnVYtgYf8PlN44kWysqv/view?usp=sharing)
*Our early mindmap mapping the core problem (fragmented trip planning) to candidate features, showing how Plan Rescue and the AI chatbot emerged as the strongest directions.*

### 2.3 Mentor Consultation

| Date | Mentor | Feedback Received | What Was Changed |
|---|---|---|---|
| 9 September 2026 | Zach Khong | Make a feature that's unique from other groups; present the function/feature in a unique way | We added an AI chatbot that can take any information provided by the user, analyze it, and generate an updated plan |

Even where we disagreed with a piece of feedback, we engaged with it directly rather than dismissing it.

---

## 3. Design & Prototype

**UI Prototype:** [View on Figma](https://www.figma.com/design/WQ8XSvI9YZoxWo9GcXtLPh/TripSync-UI?node-id=0-1&t=hH9n1yEtw3ItrVnO-1)

---

## 4. What Makes It Different

**Plan Rescue** automatically recalculates the itinerary around budget, interests, and opening hours when something changes, instead of just alerting the user like other apps.

**The AI Chatbot** lets any member paste a link, photo, or file — in solo mode or by tagging it in the group chat — to instantly turn inspiration into an itinerary item with reviews and details.

**Built-In Directions** gives every itinerary stop in-app navigation and ETA, so travellers never need to leave the app for maps.

Together, these three features move TripSync from a static planner to an adaptive travel companion — addressing gaps existing apps leave open: no rebuilding after disruption, no way to act on spontaneous ideas from outside the app, and no navigation kept in one place.

---

## 5. Technical Architecture & Feasibility

**Tech Stack**

We're using Flutter for cross-platform speed, Firebase for authentication, real-time database, and hosting, and the Claude/OpenAI API for itinerary generation and the chatbot's place analysis. Google Places API handles location data and in-app directions, while a free-tier weather/flight-status API triggers Plan Rescue. Our main constraint is API cost and reliability, so live triggers fall back to a manually simulated disruption for the demo if needed. In the 3-week build phase, we're prioritising trip creation, AI itinerary generation, the budget splitter, and Plan Rescue as must-haves. The chatbot and in-app directions are should-haves, with group-chat tagging and live pricing/flight APIs as stretch goals we'll cut first if time runs short.

**Build Plan & Scope**

We are keeping the demo scenario to one pre-tested destination and a group of 2 members, so our AI prompts and Plan Rescue logic can be thoroughly tested before the final demo rather than risking untested live generation in front of judges.
