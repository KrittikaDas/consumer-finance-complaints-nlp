# consumer-finance-complaints-nlp
NLP analysis of US Consumer Finance Complaints (text cleaning, EDA, sentiment, topic). **Note:** Includes limited attempt to identify insurance complaints via keywords, which may be noisy as the dataset isn't primarily insurance-focused.

# NLP Analysis of US Consumer Finance Complaints (Initial Exploration)

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Overview

This repository contains an initial exploration of the US Consumer Finance Complaints dataset using Natural Language Processing (NLP) techniques. The primary goal was to apply basic NLP methods like text cleaning, Exploratory Data Analysis (EDA), sentiment analysis, and topic modeling to gain preliminary insights from consumer feedback.

**Important Note:** The analysis includes an attempt to identify insurance-related complaints by filtering complaint narratives for relevant keywords. However, this dataset's product categories do not primarily focus on insurance, making this filtering approach potentially noisy and less reliable. A dataset specifically focused on insurance complaints would be more suitable for a targeted analysis of that domain.

## Dataset

* **Name:** US Consumer Finance Complaints
* **Source:** Kaggle ([https://www.kaggle.com/datasets/kaggle/us-consumer-finance-complaints](https://www.kaggle.com/datasets/kaggle/us-consumer-finance-complaints))
* **Description:** This dataset contains consumer complaints about financial products and services submitted to the U.S. Consumer Financial Protection Bureau (CFPB). It includes information about the product, issue, company, complaint narrative, and whether the consumer disputed the resolution.

## Code

* `main.py` (or the downloaded `.py` version of your Colab notebook): This script performs the following steps:
    1.  Loads the US Consumer Finance Complaints dataset.
    2.  Attempts to filter for insurance-related complaints based on keywords in the `consumer_complaint_narrative` column.
    3.  Cleans the complaint text (lowercasing, removing noise, stop words, lemmatization).
    4.  Conducts basic EDA (complaint distribution by product, text length analysis, word frequency).
    5.  Performs a simplified sentiment analysis based on the `consumer_disputed?` column using Logistic Regression.
    6.  Applies Latent Dirichlet Allocation (LDA) for topic modeling on the filtered complaints.

## Usage

1.  **Prerequisites:**
    * Python 3.x
    * pandas
    * nltk
    * scikit-learn
    * matplotlib
    * seaborn
2.  **Installation:**
    ```bash
    pip install pandas nltk scikit-learn matplotlib seaborn
    ```
3.  **Download Dataset:** Download the `us-consumer-finance-complaints.csv` file from the Kaggle link and place it in the same directory as the Python script.
4.  **Download NLTK Stopwords:** Run the following in your Python environment once:
    ```python
    import nltk
    nltk.download('stopwords')
    ```
5.  **Run the script:**
    ```bash
    python main.py
    ```

## Findings (Initial and Limited)

* The keyword-based filtering identified a subset of complaints potentially related to insurance. However, the prevalence of general financial terms in the top words suggests that this filtering is not highly precise.
* The sentiment analysis results are based on a simplified labeling approach and show a class imbalance, limiting their reliability for insurance-specific insights.
* The LDA topics provide a preliminary view of themes within the filtered complaints, but their direct relevance to specific insurance issues is not strongly evident.

**Note:** These findings are preliminary and constrained by the limitations of using a general financial complaints dataset for insurance-specific analysis.

## Further Improvements (Requires a Better Dataset)

To gain more accurate and insightful results for insurance complaints, future work should focus on:

* **Utilizing a dataset specifically focused on insurance reviews or complaints.**
* Employing more advanced NLP techniques for sentiment analysis and topic modeling.
* Analyzing specific types of insurance products if the data allows.

## License

[MIT](LICENSE)

## Author

Krittika Das

## Acknowledgements

* [Kaggle](https://www.kaggle.com/) for providing the US Consumer Finance Complaints dataset.
* The NLTK and scikit-learn libraries for their valuable NLP tools.
* The pandas, matplotlib, and seaborn libraries for data manipulation and visualization.
