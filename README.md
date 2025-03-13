# Dove Sentiment Analysis

## Project Structure
├── 📂 data/                     #Raw & processed datasets
│   ├── raw_tweets.csv           #Raw Twitter data
│   ├── processed_tweets.csv      #Cleaned data
│   ├── reddit_comments.json      #Reddit discussions
│   ├── competitor_data.csv       #Competitor sentiment data
│
├── 📂 notebooks/                #Jupyter notebooks for data exploration
│   ├── 01_X-Scraper.ipynb        #Extracting social media data
│   ├── 02_preprocessing.ipynb    #Cleaning & formatting data
│   ├── 03_sentiment_analysis.ipynb #Analyzing sentiment
│   ├── 04_visualization.ipynb    #Insights & visualization
│
├── 📂 scripts/                  #Python scripts for automation
│   ├── fetch_tweets.py           #Collect tweets using API
│   ├── analyze_sentiment.py       #Run sentiment analysis
│   ├── visualize_results.py       #Generate charts & reports
│
├── 📂 reports/                  #Final insights & documentation
│   ├── summary_report.pdf        #Key findings
│   ├── sentiment_trends.png      #Graphs & charts
│
├── requirements.txt             #Dependencies (Tweepy, VADER, pandas, etc.)
├── README.md                    #Project overview & instructions
├── .gitignore                    #Ignore unnecessary files
