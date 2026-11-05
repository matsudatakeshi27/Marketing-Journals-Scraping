# AI-Related Research Papers in Marketing Journals

## Overview
This project identifies and collects AI-related research papers published between 2022 and 2026 in six leading marketing and management journals:

- Marketing Science (MS)
- Management Science (MGSC)
- Journal of Marketing Research (JMR)
- Journal of Marketing (JM)
- Journal of Consumer Research (JCR)
- Quantitative Marketing and Economics (QME)

The goal is to build a structured dataset of research papers related to artificial intelligence, machine learning, and their applications.

## Data Collection Process

The data collection process consists of three main steps:

### 1. Paper Collection — OpenAlex
OpenAlex API is used to retrieve journal articles published between 2022 and 2026. Initial metadata includes paper titles, publication years, authors, DOIs, and abstracts (when available).

### 2. AI-Related Paper Identification — Keyword Screening
Abstracts retrieved from OpenAlex are reconstructed from their inverted-index format and screened using a predefined list of AI-related keywords.

Papers containing relevant keywords in their abstracts are retained for further review.

### 3. Abstract and Citation Retrieval — Google Scholar
Google Scholar is used to retrieve additional paper information, including abstracts and citation counts.

Papers are searched using their DOIs. Selenium automates browser interactions to collect available information. Results are saved in separate CSV files, with successful retrievals accumulated across multiple rounds. Scraping is performed in separate sessions to manage access limitations.

## Final Dataset

The final dataset combines information from OpenAlex and Google Scholar, including:

- Paper title
- Journal
- Publication year
- Authors
- Abstract
- DOI
- Google Scholar citation count

## Notes
- Abstracts and citation counts may not be available for every paper.
- Google Scholar citation counts are subject to change over time. The data in the file was counted as of 11/04/2026.
- Automated retrieval may encounter access restrictions, so scraping is conducted in separate rounds.
- Keyword screening provides an initial identification of potentially AI-related papers; it does not replace manual relevance review.
