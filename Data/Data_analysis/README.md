### Exploratory Data Analysis (EDA) — Fake News Dataset

The goal of this analysis is to understand the structure, quality, and characteristics of the dataset before building machine learning models for fake news detection.

#### Dataset Overview

The dataset consists of two main classes:

- Fake news (label = 0)

- Real news (label = 1)

Each record contains:

- title: headline of the article

- text: full article content

- label: classification target

The datasets were merged into a single dataframe for further analysis.

#### Data Quality

No critical missing values were observed in the key columns (text, label)

Data appears relatively clean, but further preprocessing (e.g., removing special characters, normalization) will be required

#### Class Distribution

The dataset is relatively balanced between fake and real news

This is beneficial for model training and reduces the risk of bias

#### Text Length Analysis

A new feature text_length was created to measure article length

The distribution shows:

- most articles are short to medium length

- there is a long tail of very long articles (outliers)

- some texts exceed tens of thousands of characters

  <img width="589" height="455" alt="Length analysis graph" src="https://github.com/user-attachments/assets/3fe5eb3c-57aa-479d-89e7-040888fb2a07" />

#### Implications for Modeling

Transformer-based models (e.g., BERT) have input size limitations (typically 512 tokens)

Long articles will need to be truncated or split into smaller chunks

Failure to handle this may negatively impact model performance.

#### Observations from Sample Texts

Fake news articles often contain:

- emotionally charged language

- sensational wording

Real news articles tend to be:

- more structured

- more formal and neutral


#### Additional Observations

Text data is unstructured and varies significantly in length and style

Feature engineering may improve baseline models (e.g., TF-IDF)

Deep learning models will benefit from contextual embeddings


