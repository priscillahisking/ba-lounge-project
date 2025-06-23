# British Airways Lounge Eligibility Model

This project provides a flexible, data-driven approach to estimate the proportion of passengers eligible for British Airways' lounges at Heathrow Terminal 3. The model is designed to support high-level planning (e.g., lounge capacity forecasts) without relying on specific flight numbers or aircraft types.

## 📌 Project Goal

✅ Build a lookup table that estimates lounge eligibility (Tier 1: Concorde Room, Tier 2: First Lounge, Tier 3: Club Lounge)  
✅ Group flights logically by route type, time of day, and region  
✅ Apply percentage assumptions to estimate lounge demand  
✅ Enable easy reuse on future flight schedules

---

## 🛫 Groupings & Assumptions

We grouped flights into the following categories:

- **Route Type:** Short-haul vs. Long-haul  
- **Time of Day:** Early Morning, Mid-Day, Evening  
- **Region:** Europe, North America, Asia, Other

### Estimated lounge eligibility per category:

| Category                        | Tier 1 (Concorde Room) | Tier 2 (First Lounge) | Tier 3 (Club Lounge) |
|----------------------------------|-----------------------|----------------------|---------------------|
| Long-haul, North America         | 5%                    | 15%                   | 30%                  |
| Long-haul, Asia                  | 5%                    | 15%                   | 30%                  |
| Long-haul, Other regions         | 5%                    | 15%                   | 30%                  |
| Short-haul, Europe               | 1%                    | 5%                    | 10%                  |

💡 *Note:* These assumptions are estimates based on typical passenger mix and can be adjusted as more data becomes available.

---

## 🗂 Project Files

- **`ba_lounge_analysis.ipynb`** → Jupyter notebook with code to load the flight schedule, apply groupings, and generate the lookup table.
- **`ba_lounge_lookup_table.csv`** → The generated lookup table showing estimated lounge eligibility for each flight in the sample schedule.
- **`README.md`** → Project documentation (this file).

---

## ⚙ How to Use

1️⃣ Clone the repo:
```bash
git clone https://github.com/your-username/ba-lounge-project.git
cd ba-lounge-project
