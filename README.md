# Insurance Sales Agent Payroll Calculator 🧮

## Business Context
In the insurance sector, sales agents typically earn a baseline salary augmented by a complex, product-specific commission structure. This project is a rule-based Python pipeline designed to automate these calculations and generate accurate net-pay figures.

## Project Value & Features
* **Automated Commission Logic:** Maps raw sales volume to tiered product payouts (Life, Health, Home/Auto).
* **UK Tax Localisation:** Integrates progressive 2026/2027 Scottish Income Tax bands and National Insurance deduction logic to calculate true net take-home pay.
* **Modular Design:** Built with isolated configuration dictionaries to allow business users to update tax bands and commission rates annually without rewriting core logic.

## Technical Stack
* **Language:** Python 3
* **Environment:** Jupyter Notebook
* **Concepts:** Control flow, dynamic dictionaries, custom functions, progressive mathematical modelling.

## Version 2.0 Update: Enterprise ETL Pipeline & Automated Reporting
The initial rule-based script has been successfully scaled into a full Pandas-driven ETL pipeline with automated PDF generation. 
* **Extract:** Ingests simulated departmental datasets representing Sales Administration, Underwriting, and Premium Administration using Pandas DataFrames.
* **Transform:** Utilises SQL-style joins (`pd.merge`) and vectorised operations to calculate validated sales based on conversion rates, handle missing data (`NaN`), and aggregate total commissions.
* **Load:** Integrates the custom Scottish progressive tax logic across the entire DataFrame using `.apply(lambda)`, processing bulk payroll seamlessly.
* **Reporting:** Integrates the `FPDF` library to dynamically batch-generate individual, professionally formatted PDF payslips for every agent in the master payroll table.

## Next Steps (Version 3.0)
Currently working on securing the pipeline by implementing `pypdf` for AES-128 password encryption (using unique Agent IDs) and `smtplib` for automated email delivery of the locked payslips.
