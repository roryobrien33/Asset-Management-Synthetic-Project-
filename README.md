# Asset Lifecycle Analytics & Forecasting (Synthetic Data)

# Project Background

This project was originally developed as part of a real-world asset management case study for a major UK retailer.  
The initial analysis was performed on the client’s asset register, applying lifecycle modelling, criticality scoring, and investment forecasting across a large multi-site portfolio.

For data protection and confidentiality, **all client-identifiable information has been fully removed**.  
The dataset included in this public repository has been **reconstructed using synthetic values** that preserve the structure, category distribution, lifecycle patterns, and analytical behaviour of the original data — while containing **no real facility names, locations, system paths, asset identifiers, or commercial information**.

The notebook and workflow remain faithful to the original analytical methodology, allowing this repository to demonstrate the full end-to-end process without exposing sensitive client data.


# Project Overview

- **Data Ingestion & Pseudonymisation**  
  Importing a raw asset register and anonymising sensitive fields using synthetic replacements for facilities, locations, system paths, and asset identifiers.

- **Data Cleaning & Standardisation**  
  Removing non-essential fields, normalising categories, correcting inconsistent text, and handling missing or malformed data.

- **Criticality Mapping & Scoring**  
  Applying a rule-based mapping table to classify system criticality and calculate associated scores.

- **Condition & Expiry Modelling**  
  Creating derived fields such as revised expiry years, condition scores, combined risk scores, and priority rankings.

- **Investment Analysis (2025–2034 Window)**  
  Aggregating lifecycle costs across revised asset descriptions and inspecting distribution of spend inside/outside the key forecasting period.

- **Exporting Cleaned Outputs**  
  Saving intermediate and final datasets to the `/data-processed/` folder for further analysis or reporting.

All data used in this repository is **synthetic and non-identifiable**, ensuring complete privacy and compliance.

---

# Repository Structure

asset-lifecycle-portfolio/
│
├── notebooks/
│ └── Asset_Management_Synthetic_Project_A.ipynb # Main analysis notebook
│
├── data-raw/
│ ├── asset_lifecycle_public_synthetic.xlsx # Anonymised input data
│ ├── Asset Criticality.xlsx # Mapping reference file
│ └── other_raw_files.xlsx # (if any)
│
├── data-processed/
│ ├── asset_mapping_cleaned.xlsx # Clean mapping outputs
│ ├── df_assets_final.xlsx # Final cleaned dataset
│ └── system_full_path_mapping.xlsx # Unique path mappings
│
├── data-external/
└── (empty or supporting documentation)


This layout follows a standard, reproducible data science folder pattern.

# How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/asset-lifecycle-portfolio.git

2. Open the project folder: cd asset-lifecycle-portfolio

3. Launch Jupyter Notebook or JupyterLab

4. notebooks/Asset_Management_Synthetic_Project_A.ipynb

# Data Privacy
The project contains:

no client addresses

no facility names

no personal identifiers

All sensitive columns were removed or pseudonymised using:

stable synthetic mappings (e.g., FAC_0001, SITE_0003)

generated location names (e.g., Town A, Town B)

synthetic asset codes (ASSET_0001234)

This ensures the analysis is realistic but fully safe to publish.

# Key Skills Demonstrated
This project highlights practical data engineering and analytics skills:

Reproducible folder structure and relative path management

Complex data cleaning, deduplication, and standardisation

Custom pseudonymisation logic tailored to sensitive asset data

Criticality scoring and lifecycle prioritisation

Scenario analysis using 2025–2034 investment windows

Production-grade notebook organisation

Exporting clean, structured datasets for downstream analysis

# Example Outputs
The notebook produces:

Cleaned and categorised asset registers

Criticality and condition scoring tables

Ranking outputs for asset renewal programmes

Aggregated 2025–2034 lifecycle investment totals

Quality checks for data completeness and logic consistency

# License
This repository is released under the MIT License, allowing others to view and reuse the workflow while maintaining attribution.

# Contributions
This is a public, learning-focused project. PRs and suggestions are welcome for improving workflow structure, scoring logic, or data pseudonymisation techniques.

**Contact
If you have feedback, questions, or ideas for improvements, feel free to open an issue or contact the repository owner through GitHub.
