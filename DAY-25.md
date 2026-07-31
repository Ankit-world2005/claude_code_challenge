PROMPT:

You are an expert full-stack developer and product designer.
Build a complete, production-quality AI Shark Tank Simulator as a single self-contained HTML file.
Requirements:
1. USER IDEA INPUT
- Startup Name
- Problem Statement
- Solution
- Revenue Model
- Target Audience
- Funding Ask
2. AI JUDGES
Create 4 distinct AI judges:
🦈 Venture Capitalist
- Focus on market size and scalability
🦈 Founder
- Focus on execution
🦈 Customer
- Focus on usefulness
🦈 Angel Investor
- Focus on profitability
3. PITCH ROUND
- Display startup pitch
- Each judge asks 2 questions
- User can answer
- Judges react dynamically
4. SCORING SYSTEM
Score out of 100:
- Market Potential
- Innovation
- Business Model
- Execution
- Investment Worthiness
5. INVESTMENT DECISION
Generate:
- Invest
- Reject
- Acquire
- Come Back Later
Show:
- Suggested Valuation
- Funding Amount
- Reasoning
6. UI
- Modern dark theme
- Shark Tank style
- Animated cards
- Responsive design
7. BONUS
- Confetti on funding success
- Download Pitch Report PDF
- Leaderboard
- Share Result button
Deliver as a single HTML file with no backend required.

OUTPUT:

<img width="1525" height="1023" alt="Screenshot 2026-07-31 131243" src="https://github.com/user-attachments/assets/4d4e723c-1e04-4721-b3f4-7a44220f4b0e" />

[shark-tank-simulator.html](https://github.com/user-attachments/files/30579240/shark-tank-simulator.html)

Now I'll build the complete AI Shark Tank Simulator. Let me create this as a full production-quality HTML file:Here's your **AI Shark Tank Simulator** — fully self-contained, production-quality. 🦈

Here's what's packed in:

**The Full Experience:**
- **4 AI Judges** — Victoria Chase (VC), Marcus Reid (Founder), Priya Nair (Customer), Theo Blackwood (Angel) — each with distinct personalities and interrogation styles
- **Live Q&A Round** — 8 questions total (2 per judge), generated in parallel via Claude API, with real answer input or skip
- **Dynamic judge cards** that highlight and animate when each shark is speaking
- **5-metric scorecard** with animated ring dials (Market Potential, Innovation, Business Model, Execution, Investment Worthiness)
- **AI verdict** — INVEST / REJECT / ACQUIRE / COME BACK LATER — with valuation, funding amount, and reasoning
- **Per-judge reactions** based on your actual answers

**Bonus Features:**
- 🎊 **Confetti burst** on INVEST or ACQUIRE verdicts
- 📄 **PDF pitch report** with full scorecard, transcript, and judge reactions
- 🏆 **Persistent leaderboard** (localStorage) — survives page refresh, shows top 10 pitches
- 🔗 **Share button** — native share sheet on mobile, clipboard fallback on desktop
- 💡 **Demo pitch** pre-fills with a NeuraFit AI example to try instantly

**Design Details:**
- Deep space dark theme with amber-gold as the primary accent
- Bebas Neue for dramatic display typography, JetBrains Mono for data
- Progress bar tracks you through all 8 questions
- Fully responsive down to mobile

