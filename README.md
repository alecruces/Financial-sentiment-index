# Financial Sentiment Index: NLP for Chile’s Financial Stability Reports

> Harnessing Natural Language Processing (NLP) techniques to create a financial sentiment index and analyze the tone of Chile's Financial Stability Reports.

![cover_image](https://github.com/user-attachments/assets/ad062e81-7eb2-4abd-84fb-0338867f1c1a)

---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [Data Overview](#data-overview)
4. [NLP Methodology](#nlp-methodology)
5. [Results](#results)
6. [Screenshots and Graphs](#screenshots-and-graphs)
7. [Contributing](#contributing)
8. [License](#license)
9. [Contact](#contact)


### About the Project

This project applies **Natural Language Processing (NLP)** to develop a Spanish-language financial sentiment index. Using text mining techniques, the tone of Chile’s Financial Stability Reports (FSRs) is assessed, providing insights into economic sentiment trends over time.

Two main outputs of the project are:
1. **Financial Sentiment Dictionary**: An NLP-powered Spanish lexicon tailored for financial stability contexts.
2. **Financial Sentiment Index (FSI)**: A numerical representation of sentiment trends across multiple FSRs.

The findings suggest that positive sentiment in FSRs correlates with economic strength and stability, while negative sentiment aligns with financial uncertainty.


### Key Features

- **NLP-Powered Sentiment Analysis**: Utilizing tokenization, lemmatization, and sentiment scoring to process financial texts.
- **Custom Financial Sentiment Dictionary**: Built specifically for Spanish-language financial contexts, capturing nuances in FSRs.
- **Sentiment Index Calculation**: Quantitative representation of sentiment using natural language data.
- **Time-Series Sentiment Trends**: Analyzing sentiment dynamics across years of financial reports.

### Data Overview

The project leverages **Chile’s Financial Stability Reports (FSRs)**, published semi-annually by the Central Bank of Chile from 2004 onwards. Due to confidentiality, FSR text data is not included in this repository.

**External Resources**:
- [Banco Central de Chile - Financial Stability Reports](https://www.bcentral.cl)


### NLP Methodology

#### Part 1: Text Preprocessing
1. **PDF Text Extraction**: Using tools like `pdftools` for converting FSRs to plain text.
2. **NLP Pipeline**:
   - Tokenization: Breaking text into individual words and phrases.
   - Lemmatization: Reducing words to their base forms for consistent analysis.
   - Stopword Removal: Filtering out irrelevant or frequently occurring words.
3. **Custom Stopwords**: Adding financial domain-specific stopwords to refine text analysis.

#### Part 2: Sentiment Dictionary Construction
1. **Word Scoring**: Annotating financial terms as positive, negative, or neutral based on their context in FSRs.
2. **Bigram and Trigram Handling**: Accounting for multi-word expressions with specific financial connotations.

#### Part 3: Sentiment Index Calculation
1. **NLP-Based Sentiment Scoring**:
   - Positive Score: Count of positive terms.
   - Negative Score: Count of negative terms.
2. **Financial Sentiment Index (FSI)**:
   - **FSI Formula**:  
     FSI = (Positive Words - Negative Words) / Total Words
     
3. **Time-Series Trends**: Sentiment index values are plotted over time to reveal long-term trends.


### Results

The **Financial Sentiment Index (FSI)** captures sentiment dynamics over time. Key findings include:

- **Positive Sentiment**: Correlated with strong economic activity, reduced uncertainty, and stable financial markets.
- **Negative Sentiment**: Linked to economic crises (e.g., 2008 financial crisis, 2020 COVID-19 pandemic).

**Example Sentiment Trends**:
- The sentiment index saw a sharp decline during global economic downturns, signaling financial instability.
- Recovery periods showed a gradual increase in positive sentiment.


### Screenshots and Graphs

1. **Construction of the Dictionary by Correa et al. (2017)**  

  <p align="center">
  <img width="702" alt="process" src="https://github.com/user-attachments/assets/ec12990b-a4c5-4e35-9d17-9663e9268fd0">
  </p>

Note: Flowchart by Correa et al. (7) for the development of the Financial Stability dictionary. It collects FSRs from different countries, processes them, and discards words based on various criteria. First by frequency, then by the context of Financial Stability, and finally by tone, positive or negative.

2. **Standardized FSI and Eventss**  

  <p align="center">
  <img width="702" alt="isef_events" src="https://github.com/user-attachments/assets/2202eb40-ab84-431f-ae7a-0095575aa41a">
  </p>

Note: Each bar represents the tone of the FSR in a given period. The ZISEFt is significant when it is less than -1 or greater than 1. When it is greater than 1, it has a negative tone or sentiment; when it is less than -1, it has a positive tone or sentiment. The dotted lines represent significant economic events for the Chilean economy.

  
