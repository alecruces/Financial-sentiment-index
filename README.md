# Financial Sentiment Index: Text Mining & Sentiment Analysis for Financial Stability Reports

> Developing a Spanish-language financial sentiment dictionary and index to analyze the tone of Chile's Financial Stability Report using text mining and sentiment analysis.

---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [Data Overview](#data-overview)
4. [Methodology](#methodology)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)
10. [Contact](#contact)

---

### About the Project

The purpose of this project is to create a Spanish-language financial sentiment index to assess the tone of the Financial Stability Reports (FSRs) published by the Central Bank of Chile. By employing text mining and sentiment analysis techniques, the project provides two core outputs:

1. **Financial Sentiment Dictionary**: A Spanish lexicon adapted to measure sentiment specifically in financial stability contexts.
2. **Financial Sentiment Index (FSI)**: An index tracking sentiment trends across multiple FSRs over time.

The study’s findings correlate a positive tone in the FSI with strong economic activity, a stable financial market, and reduced uncertainty.

### Key Features

- **Spanish Financial Sentiment Dictionary**: Tailored for analyzing FSRs from Chile, capturing the nuances of the Spanish language.
- **Sentiment Analysis**: Positive and negative sentiment analysis for key terms in financial contexts.
- **Index Calculation**: Quantitative representation of sentiment across time periods.
- **Time-Series Analysis**: Historical trends in sentiment are explored with respect to economic events.

### Data Overview

The project utilizes data from Chile's Financial Stability Reports (FSRs) published semi-annually by the Central Bank of Chile from 2004 onwards. Due to confidentiality, the FSR text data is not included in this repository.

**External Resources**:
- Central Bank of Chile’s reports (available on [Banco Central de Chile’s website](https://www.bcentral.cl))

### 4 Methodology

#### Part 1: Text Preprocessing
1. **Text Extraction**: FSRs are converted from PDF to plain text using `pdftools`.
2. **Text Cleaning**: Removal of non-text elements, numbers, and standard stopwords.
3. **Stopword Filtering**: Custom stopwords relevant to financial stability are added.

#### Part 2: Dictionary Construction
1. **Base Dictionary**: Words from financial stability reports in other languages are translated and adapted.
2. **Sentiment Scoring**: Words are classified as positive, negative, or neutral based on financial stability context.
3. **Bigram and Trigram Adjustments**: Multi-word expressions with contextual sentiment are identified and included.

#### Part 3: Sentiment Index Calculation
The Financial Sentiment Index (FSI) is calculated based on the proportion of positive and negative words across the FSRs. Two methods of calculation are used:
1. **Standard FSI**: Ratio of positive to negative terms.
2. **Normalized FSI**: Adjusted for the total word count in each report, ensuring consistency over time.

### 5 Results
The FSI trends reveal insights into the economic climate over time. Key results include:

A positive sentiment correlates with strong economic indicators, such as higher GDP and reduced market volatility.
Negative sentiment aligns with periods of economic uncertainty and financial instability (e.g., during the 2008 global financial crisis and the 2020 COVID-19 pandemic).

<img width="623" alt="sentiment_index" src="https://github.com/user-attachments/assets/cc60c8c5-3c42-4fe5-a004-8a23820c4eb8">
