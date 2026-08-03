PROMPT:

You are an expert frontend developer, UX designer, game designer, and supply chain consultant.
Build it so a complete beginner can play it — plain language, context before every decision, 'why does this matter' explanations, and guidance that makes you feel smart rather than lost.
Build a complete single-file HTML app named 'Operation Lifeline: Supply Chain Crisis Lab'.
Requirements:
• Output ONLY one HTML file.
• React via CDN + Babel JSX.
• Plain HTML, CSS, and JavaScript only.
• No Tailwind, npm, backend, APIs, images, or external assets.
• Must run offline by opening the HTML file.
• No placeholders or incomplete features.
Flow:
1. Welcome screen with title, subtitle, and 'Start Simulation'.
2. Generate a random fictional company (industry, revenue, factories, warehouses, suppliers, inventory days, lead time, countries) displayed as modern cards.
3. Generate one random crisis (factory fire, supplier bankruptcy, port strike, cyberattack, flood, raw material shortage, political conflict, shipping delay) with urgency and business impact.
4. War Room: Present six response actions. The player chooses three. Simulate consequences by updating Cost, Inventory, Profit, Delivery Speed, and Customer Satisfaction using animated progress bars.
5. Negotiation: Branching supplier negotiation with four rounds. Each choice affects Trust, Price, and Lead Time. Display a negotiation score.
6. CEO Boardroom: Five multiple-choice leadership questions. Score executive decision-making.
7. AI Strategy: Let the player choose two AI investments from Demand Forecasting, Inventory Optimization, Supplier Risk Monitoring, Warehouse Vision, and Procurement Copilot. Show expected business impact.
8. Final Dashboard: Display Overall Crisis Score (0-100), Leadership, Negotiation, Resilience, Cost Control, Risk Management, and Customer Satisfaction. Include personalized feedback, biggest mistake, best decision, expert recommendation, and lessons learned.
Design:
• Premium dark theme inspired by enterprise dashboards.
• Responsive.
• Rounded cards.
• Smooth transitions.
• Hover effects.
• Progress bars.
• Modern typography.
• Replay button.
• Every playthrough should randomize companies, crises, values, and outcomes.
Structure the React code into reusable components using useState. Ensure every button works, there are no console errors, and the final response contains only the complete HTML code inside a single code block.

OUTPUT:
<img width="1536" height="1024" alt="29113" src="https://github.com/user-attachments/assets/07adb3bd-83c1-4590-a215-f00abadc4188" />

**Operation Lifeline: Supply Chain Crisis Lab** is ready — 1,263 lines, 81KB, fully self-contained.

Here's what's inside every playthrough:

**7-Step Flow**
1. **Welcome** — clean briefing before you dive in
2. **Company Profile** — randomized corporation (10 names × 8 industries × 5 country sets × randomized metrics)
3. **Crisis Alert** — 1 of 8 crises with animated metric bars showing immediate damage
4. **War Room** — pick 3 of 6 response actions; click Simulate to watch the bars move
5. **Supplier Negotiation** — 4 rounds, 3 choices each, building Trust / Price / Lead Time in real time with expert insight after every pick
6. **CEO Boardroom** — 5 strategic MCQs with explanations whether you're right or wrong
7. **Final Dashboard** — overall score (0–100), grade, 6 sub-scores with animated bars, best decision, biggest gap, AI strategy assessment, and 5 expert lessons

**Design choices made deliberately:**
- Deep navy with a subtle radial gradient — feels like a real ops center, not a game
- No bright acid-green (the AI default) — used a blue/purple palette instead to match enterprise SaaS
- Progress bars are the primary dramatic device: watching them move after simulation is the payoff moment
- Every screen includes a "why does this matter" explanation before you commit to a choice
