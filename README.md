# How Many Employees Does a Boba Shop Need? A Business Analytics Consulting Engagement

Decision-support models for a real small business, built around the owner's actual operating constraints: staffing, marketing spend, seasonal inventory and equipment.

**Tools:** Excel (Solver / integer programming, Monte Carlo and queuing simulations via data tables, risk and payoff modeling)
**Type:** Group consulting project

**Team:** Prathiba Reddy, Hanna Teshome, Scarlett Shi, Ananya Jhamb

---

## Context

We interviewed the manager of Beau Tea, a boba and dessert shop in Georgetown, Washington, DC, to understand her budget, staffing, seasonality and risk concerns. We then translated her answers into four quantitative models.

## Models

| Model | Question | Method |
|---|---|---|
| **Staffing** | What is the minimum-cost mix of full-time and part-time employees that still preps all three tea types within a 2-hour window? | Integer linear programming, using actual prep-time data from the manager |
| **Marketing channel** | Which marketing channel minimizes worst-case cost if market conditions and competition don't go as expected? | Cost table across market conditions and competition levels, then minimax regret. The analysis identified TikTok as the channel that minimizes worst-case cost |
| **Seasonal inventory** | How much should the shop produce to maximize expected profit while limiting spoilage? | Monte Carlo simulation: 1,000 demand scenarios each for summer (300-500 cups/week) and winter (about 75 cups/week) |
| **Equipment** | How many boba machines maximize profit? | Queuing simulation of a 480-minute working day, modeling queue length, customer abandonment and machine count |

## Design principle

Every model was built to be reusable. The manager can plug in her own updated numbers (costs, demand, prep times) and get new recommendations, instead of treating the outputs as fixed, one-time answers.

## Repository contents

| File | Description |
|---|---|
| `Business Analytics Final Project (2).xlsx` | Excel workbook with the four models |
| `Business Analytics Project Report.pdf` | Written report |

## How to use

1. Open the workbook in Excel.
2. Each model sits on its own sheet. Input cells hold the shop's assumptions (costs, prep times, demand, etc.), so you can change them to test other scenarios.
3. The staffing model uses Excel Solver. If it isn't enabled, go to File > Options > Add-ins > Solver Add-in.
4. The inventory and queuing models use Excel data tables, so make sure calculation is set to Automatic (Formulas > Calculation Options).

## Notes and limitations

- The models rely on the manager's estimates and on simulated demand, so results are decision aids, not forecasts.
- Monte Carlo and queuing results vary slightly from run to run because they are simulations.

## Author

Prathiba Reddy, MS in Business Analytics & AI, Johns Hopkins Carey Business School
[Portfolio](https://6a38b7b1cee129ca7a613700--comforting-queijadas-d1f251.netlify.app) | [LinkedIn](https://www.linkedin.com/in/)
