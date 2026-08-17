# UK Insurance Agent Payroll & Commission Pipeline

## Project Overview
I built this end-to-end Python data pipeline to automate the monthly payroll and commission calculations for an insurance sales team. The system integrates simulated departmental data, calculates volume-based commissions, applies progressive 2026/2027 Scottish Income Tax brackets, and securely distributes encrypted PDF payslips to employees. This modifies a much simpler pipeline I created to generate payslips in Hollard Insurance.

This project demonstrates my ability to transition a raw data processing task into a secure, automated business product.

## Tech Stack & Libraries
* **Core:** Python 3, Pandas
* **Document Generation:** `fpdf`
* **Security:** `pypdf` (AES-128 Encryption)
* **Delivery:** `smtplib`, `email.mime` (SMTP Server Integration)

## Project Evolution & Features

### Version 1.0: Rule-Based Logic & Core Math
* Engineered the foundational mathematical logic using Python dictionaries and custom functions.
* Developed a progressive tax calculator aligned with official Scottish tax bands (Starter, Basic, Intermediate) and National Insurance deductions.
* Built a text-based terminal output to validate the gross-to-net calculations.

### Version 2.0: Pandas ETL Pipeline & PDF Export
* Scaled the script into a robust Extract, Transform, Load (ETL) pipeline using **Pandas**.
* Merged disparate departmental datasets (Sales Administration, Underwriting, and Premium Administration) using SQL-style table joins (`pd.merge`).
* Replaced loop-based calculations with vectorized operations for enterprise-scale data processing.
* Integrated the `FPDF` library to dynamically batch-generate individual, professionally formatted PDF payslips.

### Version 3.0: Data Security & Automated Delivery
* **Security:** Implemented an automated locking mechanism using `pypdf` that applies AES-128 encryption to every generated PDF. The system utilizes each employee's unique Payroll ID as the password, ensuring strict GDPR and data privacy compliance.
* **Delivery:** Engineered an automated distribution system using Python's native `smtplib` to securely log into an SMTP server, draft personalized emails, attach the encrypted payslips, and route them to the respective employee inboxes.

## How to Run
1. Clone the repository to your local machine.
2. Ensure you have the required libraries installed: `pip install pandas fpdf pypdf`
3. Execute the Jupyter Notebook (`UK_Insurance_Payroll_Calculator.ipynb`) sequentially. 
4. *Note: The SMTP email delivery command in V3 is commented out by default to prevent accidental server pings during testing. Generated and encrypted PDFs will be saved to a newly created `/Payslips_Batch` directory.*
