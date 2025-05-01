# Advanced Company Profiling and Data-Validation

## Overview

This project profiles, cleanses, enriches, and validates contact information from a sample UK company dataset.  
Using the Companies House API, company records were matched, deduplicated, and enriched with official metadata.  
Smart enrichment logic prioritized API data with fallback to original values for completeness.

## Steps Completed

- 🔍 Data profiling & null analysis
- 🧹 Data cleaning (column names, types, casing, nulls)
- 🔗 API integration using Company Number
- ✅ Field-by-field validation (fuzzy match & exact match)
- 📊 Reporting on match rates
- 📁 Export of final enriched file

## Deliverables

- `task_solution.ipynb`: Complete notebook with logic and outputs
- `final_enriched.csv`: Exported enriched dataset
- `README.md`: This file

## Notes

- Matching was primarily done using `company_number` for high accuracy
- Validation used fuzzy matching for name/address and exact matching for identifiers
- Match rate visualisation 

## Requirements

- Python 3.8+
- Libraries: `pandas`, `matplotlib`, `re`, `requests`, `difflib`

---

## Acknowledgements

- Companies House API (https://developer.company-information.service.gov.uk)

---


