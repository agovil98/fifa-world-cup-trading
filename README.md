# FIFA World Cup 2026 Fair Value Trading Calculator

An advanced, interactive single-page React application designed for traders and coordinators in a World Cup 2026 point-payoff trading game. The application instantly computes the mathematical **Fair Price** of all 48 countries based on custom-assigned points for group stage finishes and knockout round eliminations, combined with complex probability distributions.

## Tournament Context & Format
The FIFA World Cup 2026 features **48 teams** divided into **12 groups of 4**:
- Teams finish **1st, 2nd, 3rd, or 4th** in their respective groups.
- All 1st and 2nd place teams (24 teams) plus the **8 best 3rd-place teams** advance to the **Round of 32**.
- From the Round of 32 onwards, the tournament operates on a **single-elimination knockout bracket**, including a 3rd/4th place playoff for the semifinal losers.

## Core Mathematical Formula
Points are strictly additive. The Fair Price of a country represents its expected point payoff:
$$\text{Fair Price} = \sum (\text{Prob of Group Position} \times \text{Points for that Position}) + \sum (\text{Prob of Knockout Elimination} \times \text{Points for that Elimination})$$

## Features
1. **Glassmorphic UI**: Ultra-premium dark theme designed with modern CSS filters, responsive dashboard cards, and animated transitions.
2. **Dual Payoff Matrix Dashboard**: Real-time adjustable sliders and inputs for:
   - **Group Stage**: 1st, 2nd, 3rd, 4th positions.
   - **Knockout Stage**: R32, R16, QF, Finished 4th (losing 3rd-place match), Finished 3rd (winning 3rd-place match), Runner-Up, and Winner.
3. **Instant Engine**: Modifying points instantly updates all 48 teams in real-time ($< 5\text{ms}$).
4. **Smart CSV Import**: Clean drag-and-drop file panel and paste textarea supporting Excel/CSV format with error validation.
5. **Interactive Leaderboard**: Sort by country or Fair Price, filter by name, and view individual visual probability breakdowns.
6. **Data Export**: One-click download of computed values as a clean CSV file.

## Getting Started
Since this application is written as a fully client-side React single-page app using CDN libraries, **no installation, Node.js, or server is required**.

1. Double-click the `index.html` file inside this directory to open it in Google Chrome, Safari, or Firefox.
2. Adjust the points matrix in the left sidebar to see all prices recalculate instantly.
3. Paste or drop your own custom probability model CSV to update the dataset.
