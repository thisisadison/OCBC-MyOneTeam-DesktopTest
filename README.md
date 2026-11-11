# OCBC MyOneTeam

An agentic AI wealth-advisor concept for OCBC, shown as a mobile-first clickable prototype. Instead of a single generic robo-advisor, clients are matched with a team of specialist AI agents plus an Orchestrator that reconciles their input into one coherent plan, with clear hand-offs to a human Relationship Manager.

**Recognition:** 1st Prize, OCBC FRANKpreneurship 2026 (Agentic AI Wealth Advisor Platform), and recognised at the OCBC Experience Day.

## Live Demo

| Platform | URL |
|---|---|
| 🖥️ Desktop | [Open MyOneTeam →] https://github.com/thisisadison/OCBC-MyOneTeam-Test |
| 📱 Mobile | [Open MyOneTeam →] Discontinued |

> Designed mobile-first as an in-app experience, so it looks best on a phone or a narrow browser window.

## About the Project

MyOneTeam was developed as part of the OCBC FRANKpreneurship programme (May–Aug 2026). The team pitched a **human-in-the-loop proof of concept** to eight OCBC executives, including a draft of how the agents could sit on top of OCBC's existing infrastructure.

This repository contains the **front-end prototype** used to demonstrate that concept. The AI agents themselves are a proof of concept and were not implemented in production; everything in the demo is simulated on the client side.

## Concept

- **Money Identity quiz** in place of a generic risk questionnaire
- **Named, explainable agents** with their own focus areas, instead of one opaque model
- **An ongoing relationship**: life-event simulation and quarterly reviews, not a one-time setup
- **Human in the loop**: paper trade, send to a Relationship Manager, or trade live, so AI supports advice rather than replacing it

## User Journey

1. **Financial Profile**: a short "Money Identity" quiz that resolves to one of 8 personas (Bubble Tea, Kopi O Kosong, Sugarcane, Soya Milk, Honey Lemon, Bandung, Barley Water, Milo Dinosaur), each with its own risk and planning profile. All answer combinations are listed in [`ocbc-ea-combinations.txt`](ocbc-ea-combinations.txt).
2. **Build Your AI Team**: pick specialist agents based on your goals:
   - **Property Paige**: saving toward a home
   - **Retirement Ryan**: long-term retirement nest egg
   - **Growth Gary**: long-term growth
   - **Income Ivy**: regular passive income
3. **Goals & Risk Comfort**: set targets, timeline and risk appetite per goal.
4. **Plan Building**: individual agent views are reconciled by the **Orchestrator** into one blended portfolio (Fixed Income / Equities / Cash / Alternatives).
5. **Portfolio & Account Linking**: link external accounts and fine-tune the suggested basket.
6. **Path to Action**: paper trade, send to a Relationship Manager, or trade live.
7. **Ongoing Relationship**: MyOneTeam home, quarterly reviews, and a **Life Simulator** that models events such as buying a home or having a child and updates the plan.

## Tech Stack

- Single-file HTML, CSS and vanilla JavaScript. No build step, framework or dependencies.
- Client-side only. All state is held in memory, with a rule-based engine behind the Orchestrator chat.
- Roughly 20 screens driven by simple client-side routing inside one page.

## Running Locally

No installation needed.

```bash
git clone https://github.com/thisisadison/OCBC-MyOneTeam-MobileTest.git
cd OCBC-MyOneTeam-MobileTest
open index.html
```

To test on a phone over your network, serve it instead:

```bash
npx serve .
```

## Project Status

A high-fidelity prototype, not a production application.

- ✅ Fully clickable front end covering the whole journey above
- ❌ No backend, authentication or persistence
- ❌ No live brokerage, CPF or bank integrations
- ❌ No real market data; all figures are illustrative
- ❌ Agents are a proof of concept and are not connected to any model or OCBC system

## Repository Structure

```
.
├── index.html                  # entire app: markup, styles and logic
├── ocbc-ea-combinations.txt    # quiz answer combinations per persona
├── _redirects                  # hosting redirect rule
└── images/
    ├── agents/                 # agent and Orchestrator portraits
    ├── mbti/                   # persona artwork
    ├── questionnaire/          # quiz scene images
    ├── background/             # screen backgrounds
    └── articles/               # home-screen article thumbnails
```

## Disclaimer

Student prototype built for the OCBC FRANKpreneurship programme. It is not an official OCBC product and does not provide financial advice.