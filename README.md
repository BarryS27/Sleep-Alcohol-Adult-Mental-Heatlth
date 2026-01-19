# 🧠 Sleep, Alcohol, and Mental Health
### An Exploratory Analysis of CDC BRFSS Data

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue)
![Dataset](https://img.shields.io/badge/Dataset-CDC%20BRFSS-green)
![Status](https://img.shields.io/badge/Status-Completed-orange)

---

### 📖 Project Background
The **Behavioral Risk Factor Surveillance System (BRFSS)** is the nation's premier system of health-related telephone surveys. It collects state data about U.S. residents regarding their health-related risk behaviors, chronic health conditions, and use of preventive services.

> **Research Question:**
> *How do lifestyle choices—specifically sleep duration and alcohol consumption—interact with an individual's reported mental well-being?*

### 🔬 Research Hypotheses
* **Hypothesis 1 (Sleep):** 📉 Individuals experiencing **sleep deprivation (<6 hours)** will report a significantly higher number of poor mental health days.
* **Hypothesis 2 (Alcohol):** 🍷 **Drinkers** may exhibit greater volatility in mental health outcomes compared to non-drinkers.

---

### 🧹 Data Cleaning & Dictionary
To prepare the raw survey data for analysis, specific coding values were transformed into analytical metrics:

| Variable Name | Original Feature | Raw Code Meaning | Data Transformation Strategy |
| :--- | :--- | :--- | :--- |
| **MentalHealth** | `MENTHLTH` | `88` = "None" (0 days) | Replaced `88` with **`0`**; Treat `77`/`99` as `NA`. |
| **AlcoholDrinking**| `ALCDAY5` | `888` = "No alcohol" | Categorized `888` as **`Non-drinker`**; Others as **`Drinker`**. |
| **SleepTime** | `SLEPTIM1` | Hours (1-24) | Filtered outliers (>15h) for realistic analysis. |

---
