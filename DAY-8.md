INPUT-

Act as a Senior Data Analyst, Environmental Researcher, UX Designer, and Frontend Dashboard Developer.
Create a Claude Artifact called:
🌍 Personal Environmental Health Analyzer
DATA RULES
If a dataset is provided, use it. If no dataset is provided, automatically search the web for the latest AQI and water-quality data for the user's current city/location. If location is unavailable, ask for the city name first. Use the most recent available data, cite sources, clean the data, handle missing values, and validate quality before analysis.
ANALYSIS
Generate: cleanest city, most polluted city, highest AQI city, lowest AQI city, average AQI, number of cities analyzed, trends, anomalies, most surprising observation, executive summary.
INTERACTIVE DASHBOARD
Create a fully interactive Claude Artifact with:
📊 Key Metrics: average AQI, highest AQI city, lowest AQI city, number of cities analyzed, environmental health score.
📈 Visualizations: AQI comparison chart, PM2.5 comparison chart, PM10 comparison chart, city ranking chart, AQI distribution chart.
🎛 Interactive Filters: city selector, AQI range filter, pollutant selector, health-risk filter, date filter (if available), city comparison mode.
📋 City Detail Cards: AQI, PM2.5, PM10, air-quality category, health score, water-quality score.
🚦 AQI Categories: Good (Green), Satisfactory (Light Green), Moderate (Yellow), Poor (Orange), Very Poor (Red), Severe (Dark Red).
ENVIRONMENTAL HEALTH ANALYSIS
For the selected city explain AQI impact on lungs, sleep, energy levels, exercise performance, long-term health, and water-quality impact on hair fall, hair dryness, scalp health, skin dryness, acne, and sensitive skin.
Use risk indicators: 🟢 Low, 🟡 Moderate, 🔴 High.
PERSONAL REPORT CARD
Generate an Environmental Health Score (0–100) with breakdowns for Air Quality Score, Water Quality Score, and Overall Environmental Score.
Assign grades for Air Quality (A–F), Water Quality (A–F), Hair Risk, and Skin Risk.
INSIGHTS PANEL
Include: top 3 cleanest cities, top 3 most polluted cities, biggest anomaly, most surprising observation, recommended actions.
PERSONALIZED RECOMMENDATIONS
Provide: daily actions, indoor air improvements, outdoor activity guidance, hair-care recommendations, skin-care recommendations, water-quality improvement suggestions.
DESIGN
Modern, professional, mobile responsive, dark theme, smooth animations, premium UI, clean typography, dashboard-style layout, highly visual, colourful, LinkedIn-shareable.
OUTPUT
Generate a complete downloadable HTML application that is fully responsive and ready to save as index.html.
IMPORTANT
Do not provide code snippets. Create a complete interactive Claude Artifact with working charts, filters, cards, insights, report cards, and dashboards that users can interact with directly.


OUTPUT-

Your **🌍 Personal Environmental Health Analyzer** is complete and fully interactive. Here's what's packed inside, built on real data:

---

**📡 Data Sources Used**
- AQI readings from aqi.in as of July 10, 2026: Delhi 87, Mumbai 57, Bengaluru 62, Chennai 89–113, Kolkata 90, Hyderabad 64, Pune 58, Ahmedabad 69
- Additional AQI cross-referenced from aqicn.org: Jaipur 153, Lucknow 144
- IQAir confirms Ghaziabad historically at 115 µg/m³ PM2.5 annually (AQI ~179)
- Ghaziabad groundwater data: pH 7.35–9.05, hardness 170–335 mg/L, TDS 514–549 mg/L
- Hyderabad water TDS ~1,207 mg/L — above BIS limit of 500 mg/L
- Hard water city context: Chennai TDS above 1,000 ppm from seawater intrusion

---

**What's built — all 7 tabs:**

| Tab | What you get |
|-----|-------------|
| 📊 Overview | 5 live metrics + AQI bar chart + 3 quick-insight panels |
| 📈 Charts | 5 interactive charts with filter bar (city, AQI range, risk category) |
| 🏙️ City Cards | 11 clickable city cards with AQI, PM2.5, PM10, TDS, Hardness, scores |
| 🫁 Health Analysis | Air + Water impact analysis (10 health factors) per selected city |
| 📋 Report Card | Animated score ring, 5 score bars, 4 grade cards (Air/Water/Hair/Skin) |
| 💡 Insights | Anomaly detection, the North–South paradox, full executive summary |
| ✅ Recommendations | 6 personalised action cards for Ghaziabad's specific conditions |

[index.html](https://github.com/user-attachments/files/29914570/index.html)

