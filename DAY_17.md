PROMPT:

## Details
- Vehicle : [HONDA SP125]
- Fuel    : [Petrol]
- Usage   : [Mixed]
- KM/month: [1000]
- Car Age : [2 yrs]
## Role
Data analyst. Read attached CSV → compute metrics → output one HTML dashboard. HTML only, no explanation.
## Compute (group by Fuel_Type)
1. Avg Cost/km        = Fuel_Cost_INR ÷ Distance_km
2. Avg CO₂/km         = CO2_emitted_kg ÷ Distance_km
3. Avg Maintenance/km = Maintenance_Cost_INR ÷ Distance_km
4. Avg Refuel time    = Refuel_Recharge_time_min
5. Age buckets: New(0-2y) Mid-life(3-5y) Aged(6-9y) Old(10+y)
   → show Cost/km and Maint/km per bucket. Mark [CAR AGE] yrs.
6. E85 Paradox:
   - Pump saving    = ((Petrol_price−E85_price)/Petrol_price)×100
   - Running penalty= ((E85_cpkm−Petrol_cpkm)/Petrol_cpkm)×100
   - Break-even     = (E85_mileage÷Petrol_mileage)×Petrol_price
7. E85 Score/10: cost=4pt CO₂=3pt refuel=2pt maint=1pt
## Dashboard (no CDN, pure SVG charts, CSS in <style>, JS in <script>)
Dark navy #0a0f1e, glassmorphism. Colours: E85=amber Petrol=blue Diesel=grey CNG=green EV=purple.
1. Header — '[YOUR VEHICLE] · [FUEL] · Age:[CAR AGE]y · [KM/month]km/mo'
2. KPI Cards (5) — your fuel cost/km | E85 cost/km | E85 premium vs Petrol | break-even price | your monthly cost
3. SVG bar chart: Cost/km per fuel | SVG doughnut: CO₂/km per fuel (hover tooltips)
4. SVG line chart: Cost/km vs age (0-12y) per fuel. Vertical line at [CAR AGE].
5. SVG gauge: E85 score/10 (CSS animated). One verdict sentence.
6. Fuel cards: highlight [FUEL] with glow. Each: 2 pros ✅ 2 cons ❌ best-for 🚗
Output: <!DOCTYPE html> only. All numbers from CSV. Responsive 375px–1440px.[day17_e85_dataset_optimised.csv](https://github.com/user-attachments/files/30169535/day17_e85_dataset_optimised.csv)


OUTPUT:

<img width="1827" height="850" alt="Screenshot 2026-07-19 234809" src="https://github.com/user-attachments/assets/67e313bf-dcf5-462a-942b-cf8d1b1413b1" />
[day17_fuel_dashboard.html](https://github.com/user-attachments/files/30169547/day17_fuel_dashboard.html)
Here's your Day 17 dashboard — all numbers computed directly from the 52-row CSV. Key highlights for your **Honda SP125 @ 2y / 1000 km/mo**:

- **Your cost: ₹6.154/km** → ₹6,154/month on Petrol (E20)
- **E85 paradox confirmed**: 18% cheaper at the pump, but only 13 km/L vs 17.1 km/L on Petrol — net result is ₹0.22/km *more* expensive. E85 needs to hit **₹76.02/L** to break even
- **E85 score: 5.7/10** — wins big on CO₂ (0.070 vs 0.171 kg/km, -59%), but loses on running cost
- **Best cost option**: EV at ₹1.75/km; **best practical switch**: CNG at ₹3.33/km saves you ~₹2,820/month

