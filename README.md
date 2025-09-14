# 🗳️ Political Opinion Analysis in the European Parliament & Beyond  

This repository contains a collection of data-driven analyses on **political statements, debates, and positions** expressed in the European Parliament and in global political discourse. Using NLP (Natural Language Processing), statistical methods, and visualization techniques, the projects aim to uncover **patterns of support, opposition, and polarization** on key international issues.  

---
⚠️ Important! This dataset has an issue with interpreting statements. If a person quotes an opponent, their own statement may be mistakenly classified as supporting the opponent’s position. I try to catch such cases, but it’s impossible to eliminate them completely.


## 📂 Repository Structure  

Each project is organized as a standalone folder with its own dataset(s), notebooks, and results.  

### 🔎 Analyses Included  

- **🇵🇸🇮🇱 Support for Palestine and Israel in the European Parliament**  
  Examines how MEPs position themselves on the Israel–Palestine conflict, including speeches, political group alignments, and country-based patterns.  


- *(More analyses to be added as the project grows.)*  

---

## 📊 Methodology  

Across projects, the general workflow follows a **shared methodology**:  

1. **Data Collection**  
   - Official speeches and statements downloaded from the [European Parliament website](https://www.europarl.europa.eu).  
   - Focused debates/sessions selected for each topic (e.g., Gaza war, Ukraine war, Trump’s influence).  

2. **Preprocessing & Thematic Analysis**  
   - Speech texts cleaned and indexed.  
   - Themes assigned (e.g., *Middle East, Security, Foreign Policy*).  
   - NLP models applied:  
     - **BERT-based Natural Language Inference (NLI)** to classify statements as *supports / opposes / neutral*.  
     - **Entailment scores** (0–1) to measure model confidence.  

3. **Aggregation & Scoring**  
   - Per-MEP stance aggregation with weighted averages.  
   - Neutral statements excluded to focus on clear positions.  
   - Longitudinal tracking of support/opposition intensity.  

4. **Analysis & Visualization**  
   - **Descriptive statistics** (mean, median, variance of support).  
   - **Correlation analysis** between stance and political group, country, or party.  
   - **Visualizations**: bar plots, heatmaps, time series graphs.  
   - (Optional) **Predictive modeling** to estimate positions not explicitly stated.  

---

