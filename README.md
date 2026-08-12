# Insurance Sales Agent Payroll Calculator 🧮

## Business Context
In the insurance sector, sales agents typically earn a baseline salary augmented by a complex, product-specific commission structure. This project is a rule-based Python pipeline designed to automate these calculations and generate accurate net-pay figures.

## Project Value & Features
* **Automated Commission Logic:** Maps raw sales volume to tiered product payouts (Life, Health, Home/Auto).
* **UK Tax Localization:** Integrates progressive 2026/2027 Scottish Income Tax bands and National Insurance deduction logic to calculate true net take-home pay.
* **Modular Design:** Built with isolated configuration dictionaries to allow business users to update tax bands and commission rates annually without rewriting core logic.

## Technical Stack
* **Language:** Python 3
* **Environment:** Jupyter Notebook
* **Concepts:** Control flow, dynamic dictionaries, custom functions, progressive mathematical modeling.

## Next Steps (Version 2.0 Pipeline)
Currently scaling this script into a full enterprise ETL pipeline using **Pandas** to merge disparate departmental data (Underwriting sales, Premium Administration conversion rates, and HR employee rosters).
