# 🇵🇸🇮🇱 Support for Palestine and Israel in the European Parliament

## Short Description
This project analyzes the positions of Members of the European Parliament (MEPs) regarding Palestine and Israel. The goal is to understand patterns of support or opposition across parties, countries, and political groups.

---

## Context & Motivation
The European Parliament is a key arena for international politics. Understanding how MEPs position themselves on issues related to Israel and Palestine can reveal political alignments, ideological trends, and the influence of party affiliation or country of origin.

---

## Dataset Description

The project uses two main prepared datasets:

### `prepared/speeches_prepared.csv`
Contains individual speeches by MEPs.  
**Columns**:  
- `person_id`: Unique identifier of the MEP  
- `first_name`, `last_name`: Name of the MEP  
- `speech_index`: Identifier of the speech within the dataset  
- `theme_name`: Thematic category assigned to the speech (e.g., Gaza war, Middle East, etc.)  
- `entailment_score`: Confidence score (float 0–1) from the NLI model  
- `classification`: Position of the speech (`supports`, `opposes`, or `neutral`)  
- `speech_title`: Title of the session or debate  
- `speech_link`: Link to the original statement on the EP website  
- `group_code`: Political group of the MEP (e.g., EPP, S&D, Greens/EFA)  
- `country`: Country of the MEP  

### `prepared/persons_prepared.csv`
Contains aggregated information about MEPs’ positions across themes.  
**Columns**:  
- `person_id`: Unique identifier of the MEP  
- `first_name`, `last_name`: Name of the MEP  
- `theme_name`: Thematic category  
- `classification`: Aggregated position of the MEP (`supports`, `opposes`, or `neutral`)  
- `group_code`: Political group of the MEP  
- `country`: Country of the MEP  

**Notes**:  
- `classification` indicates the stance derived from BERT-based NLI analysis.  
- `entailment_score` reflects the model’s confidence in assigning support or opposition.  
- Neutral positions were later excluded from the analysis to focus on clear stances.

---

---

## Methodology

- **Data Collection**:  
  - Statements of MEPs were downloaded from the European Parliament website.  
  - Focused sessions were selected, covering Middle East issues and the Gaza war.  
  - Every statement by each MEP was saved for analysis.

- **Feature Engineering & Thematic Analysis**:  
  - Each statement was analyzed using a BERT-based Natural Language Inference (NLI) model.  
  - Statements were classified across several thematic categories (full list provided in the table below).  
  - For each theme, statements were categorized as `supports`, `opposes`, or `neutral`.  
  - Neutral statements were removed from the dataset to focus on clear positions.

- **Aggregation & Scoring**:  
  - Support/opposition scores were aggregated per MEP over time using weighted averages, capturing the intensity and frequency of positions.  

- **Analysis Techniques**:  
  - Descriptive statistics (mean, median support) to summarize positions across parties, countries, and political groups.  
  - Correlation analysis between political group/country/party and stance on Israel or Palestine.  
  - Visualizations including bar plots, heatmaps, and time series graphs to identify trends.  

- **Optional Advanced Step**:  
  - Predictive modeling using linear regression or classification techniques to estimate MEP positions not explicitly stated in the dataset.

---
