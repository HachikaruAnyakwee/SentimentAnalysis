

# Sentiment Analysis on Mark Carney’s Appointment as Canadian Prime Minister

## Project Overview
This project analyzes public sentiment regarding Mark Carney’s appointment as Prime Minister of Canada. Using data from [Reddit](https://www.reddit.com/), [Google News](https://news.google.com/), and [YouTube](https://www.youtube.com/), we apply sentiment analysis techniques to assess public opinion. We leverage tools like [VADER](https://pypi.org/project/vaderSentiment/) and [TextBlob](https://pypi.org/project/TextBlob/) for this analysis.

## Objective
- Extract and analyze text data from multiple online sources ([Reddit](https://www.reddit.com/), [Google News](https://news.google.com/), [YouTube](https://www.youtube.com/)).
- Perform data cleaning and preprocessing to refine sentiment classification.
- Use [VADER](https://pypi.org/project/vaderSentiment/) and [TextBlob](https://pypi.org/project/TextBlob/) for sentiment scoring.
- Compare sentiment trends across different platforms.
- Identify common keywords and sentiment patterns in political discourse.

## Methodology
1. **Data Collection:** Scraped data from [Reddit](https://www.reddit.com/), [Google News](https://news.google.com/), and [YouTube](https://www.youtube.com/).
2. **Initial Data Cleaning:** Removed duplicate and unnecessary data from each source.
3. **SQL Merging:** Combined cleaned datasets for a unified analysis using [SQL](https://en.wikipedia.org/wiki/SQL).
4. **Preprocessing & Final Cleaning:** Performed tokenization, lemmatization, and additional text normalization.
5. **Sentiment Analysis:** Applied [VADER](https://pypi.org/project/vaderSentiment/) and [TextBlob](https://pypi.org/project/TextBlob/) for classification into positive, negative, or neutral sentiment.
6. **Keyword-Level Sentiment Analysis:** Identified commonly used words in positive and negative sentiment.
7. **Neutral Sentiment Analysis:** Examined the neutral sentiment category for hidden biases.
8. **Visualization & Reporting:** Generated charts and structured insights.

## Project Structure

```
SentimentAnalysis/
├── data/
│   ├── raw/
│   │   └── (Original scraped data)
│   ├── cleaned/
│   │   └── (Cleaned datasets)
│   ├── processed/
│   │   └── (Final preprocessed datasets)
│   ├── sentiment/
│   │   ├── negative_word_frequency.png
│   │   ├── negative_wordcloud.png
│   │   ├── negative_words_analysis.csv
│   │   ├── neutral_word_frequency.png
│   │   ├── neutral_wordcloud.png
│   │   ├── neutral_words_analysis.csv
│   │   ├── positive_word_frequency.png
│   │   ├── positive_wordcloud.png
│   │   ├── positive_words_analysis.csv
│   │   ├── sentiment_analysis_report.txt
│   │   ├── sentiment_analysis.csv
│   │   ├── sentiment_by_source.png
│   │   └── sentiment_distribution.png
│   └── merged/
│       └── (Merged SQL dataset)
│
├── reports/
│   ├── [final_report.pdf](reports/final_report.pdf) (Structured final analysis)
│   └── [thought_process.txt](reports/thought_process.txt) (Raw project journey)
│
├── src/
│   ├── [scrape_reddit.ipynb](src/scrape_reddit.ipynb) (Scraping Reddit comments)
│   ├── [scrape_googlenews.ipynb](src/scrape_googlenews.ipynb) (Scraping Google News comments)
│   ├── [scrape_youtube.ipynb](src/scrape_youtube.ipynb) (Scraping YouTube comments)
│   ├── [data_cleaning.ipynb](src/data_cleaning.ipynb) (Initial data cleaning)
│   ├── [sql_merge.ipynb](src/sql_merge.ipynb) (Merging datasets using [SQL](https://en.wikipedia.org/wiki/SQL))
│   ├── [preprocess_text.ipynb](src/preprocess_text.ipynb) (Text preprocessing & normalization)
│   ├── [clean_final_data.ipynb](src/clean_final_data.ipynb) (Final cleaning after preprocessing)
│   ├── [sentiment_analysis.ipynb](src/sentiment_analysis.ipynb) (Classifying sentiment using [VADER](https://pypi.org/project/vaderSentiment/) and [TextBlob](https://pypi.org/project/TextBlob/))
│   ├── [sentiment_results_analysis.ipynb](src/sentiment_results_analysis.ipynb) (Visualizing sentiment results)
│   ├── [neutral_comments_analysis.ipynb](src/neutral_comments_analysis.ipynb) (Analyzing neutral sentiment)
│   └── [sentiment_keywords_anaysis.ipynb](src/sentiment_keywords_anaysis.ipynb) (Keyword-level sentiment analysis)
│
├── [README.md](README.md)
├── [.gitignore](.gitignore)
└── [requirements.txt](requirements.txt)
```

## Setup Instructions

### **Prerequisites**
Ensure you have Python installed and required libraries available.

### **Installation Steps**
1. Clone the repository:
```
git clone [https://github.com/your-username/SentimentAnalysis.git](https://github.com/your-username/SentimentAnalysis.git)
cd SentimentAnalysis
```

2. Create a virtual environment:
```
python -m venv venv
source venv/bin/activate   #Mac
venv\Scripts\activate      #Windows
```

3. Install dependencies:
```
pip install -r requirements.txt
```

4. Ensure you have an .env file containing necessary [API](requirements.txt) keys.

## Running the Scripts
### **1. Data Collection**
These scripts collect data from different sources. Run them separately:
```
   python [src/scrape_reddit.ipynb](src/scrape_reddit.ipynb)
   python [src/scrape_googlenews.ipynb](src/scrape_googlenews.ipynb)
   python [src/scrape_youtube.ipynb](src/scrape_youtube.ipynb)
```

### **2. Initial Data Cleaning**
Once the data is collected, we perform initial cleaning to remove duplicates and unnecessary text:
```
   python [src/data_cleaning.ipynb](scripts/data_cleaning.ipynb)
```

### **3. Merging Data Using SQL**
After cleaning, we merge the datasets into a single structured database:
```
   [python src/sql_merge.ipynb](scripts/sql_merge.ipynb)
```

### **4. Preprocessing & Final Cleaning**
We preprocess the merged dataset and apply final cleaning:
```
   [python src/preprocess_text.ipynb](scripts/preprocess_text.ipynb)
   [python src/clean_final_data.ipynb](scripts/clean_final_data.ipynb)
```

### **5. Sentiment Analysis**
Now we classify sentiment using [VADER](https://pypi.org/project/vaderSentiment/) and [TextBlob](https://pypi.org/project/TextBlob/):
```
   [python src/sentiment_analysis.ipynb](scripts/sentiment_analysis.ipynb)
```

### **6. Sentiment Result Visualization**
Analyze the sentiment results with visualizations:
```
   [python src/sentiment_results_analysis.ipynb](scripts/sentiment_results_analysis.ipynb)
```

### **7. Neutral Sentiment Deep Dive**
Investigate neutral sentiment to uncover potential biases:
```
   [python src/neutral_comments_analysis.ipynb](scripts/neutral_comments_analysis.ipynb)
```

### **8. Keyword-Level Sentiment Analysis**
Examine the most common words in positive and negative sentiments:
```
   [python src/sentiment_keywords_anaysis.ipynb](scripts/sentiment_keywords_anaysis.ipynb)
```

## Key Findings
 - Public sentiment is highly divided on Carney’s appointment.

 - Neutral sentiment is dominant, but words classified as neutral (e.g., "election") often indicate dissatisfaction.

 - YouTube had the highest negative sentiment, while Reddit had a more balanced mix.

 - Frequent negative keywords: "election," "unelected," "government," "wrong guy."

 - Frequent positive keywords: "leader," "support," "win," "good," "Canada."


## Reports
[Final Report](reports/final_report.pdf): In-depth analysis with charts and insights.
[Thought Process](reports/thought_process.txt): Raw documentation of the entire workflow, challenges, and decisions.

## License
This project is open-source and available under the [MIT License](LICENSE).