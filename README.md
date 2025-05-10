# Advanced Company Profiling and Data Validation

## 🚀 Overview

This project demonstrates an end-to-end data engineering solution that profiles, cleanses, validates, enriches, and visualizes a sample of UK company records.  
It combines original company data with external enrichment from the **Companies House API** and **Postcodes.io**, prioritizing high-quality, validated registered contact information.

## 📊 Objectives

- Clean and standardize messy business records
- Match company details via `company_number`
- Enrich missing fields using authoritative APIs
- Validate enrichment using fuzzy and exact logic
- Visualize match effectiveness and enrichment coverage

---

## 🛠️ Workflow Summary

1. **Profiling**: Dataset inspection and null analysis

2. **Cleaning**:
   - Dropped columns with >90% missing values
   - Renamed and converted fields to snake_case
   - Standardized text casing and formats
   - Deduplication

3. **Enrichment**:
   - **Companies House API**: Enriched fields like name and registered address
   - **Postcodes.io API**: Fetched city, county, and country based on postcode
   - Prioritized API values using `combine_first()` logic

4. **Validation**:
   - Applied fuzzy matching for names and addresses using `difflib`
   - Used exact string match for structured fields
   - Counted and visualized match rates

5. **Caching**:
   - Implemented local caching to avoid redundant API calls

6. **Visualization**:
   - Compared original vs enriched fields
   - Displayed match rates by column using bar charts

---

## 📁 Deliverables

- `task_solution.ipynb`: Main Jupyter Notebook with logic and outputs
- `final_enriched.csv`: Final enriched dataset with validated fields
- `README.md`: This documentation

---

## 📊 Integration Workflow

![Data Workflow](https://github.com/user-attachments/assets/4d61352e-c42a-4ddb-95a6-5ba99415837f)

---

## 🔍 Validation Logic

- `company_number`: used for precise record matching
- Fuzzy match: for `company_name`, `address_line_1`, `address_line_2`
- Exact match: for `post_code`, `city`, `county`, `country`
- Match statistics were computed per column and visualized

---

## 🧰 Technologies Used

- Python 3.8+
- `pandas`, `matplotlib`, `re`, `requests`, `difflib`

- APIs:
  - [Companies House](https://developer.company-information.service.gov.uk)
  - [Postcodes.io](https://postcodes.io/)

---

## 📦 How to Run

1. Clone this repo and open `task_solution.ipynb`
2. Install required packages (if needed):

   ```bash
   pip install pandas requests matplotlib
   
3. Add your Companies House API key where indicated in the notebook
4. Run each cell in order

## 🙏 Acknowledgements

- Companies House API
- Postcodes.io API
- CluedIn for the use case task
