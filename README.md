# Canadian Fuze Tea Launch Analysis

This project analyzes Canadian customer sentiment regarding Coca-Cola's Fuze Tea launch, which replaced Nestea in Canada in January 2024. It scrapes Twitter data (via Nitter) to gather public opinions and uses sentiment analysis to understand how the new beverage is being received.

## Table of Contents

- [Project Description](#project-description)
- [Installation](#installation)
- [Usage](#usage)
- [Data Collection](#data-collection)
- [Sentiment Analysis](#sentiment-analysis)
- [Data Analysis](#data-analysis)
- [Contributing](#contributing)
- [License](#license)

## Project Description

This project aims to provide insights into Canadian consumer reception of Fuze Tea following its launch in January 2024. It leverages Twitter data scraped using `ntscraper` to collect tweets related to Fuze Tea and the replacement of Nestea. The data is then processed using `pandas` for data manipulation, and sentiment analysis is performed using `vaderSentiment`. The results are saved to a CSV file for further analysis.

## Installation

1.  **Clone the repository:**

    ```bash
    git clone [repository URL]
    cd [repository directory]
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**

    -   **On Windows:**

        ```bash
        venv\Scripts\activate
        ```

    -   **On macOS and Linux:**

        ```bash
        source venv/bin/activate
        ```

4.  **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

    (Create a `requirements.txt` file with the following content:)

    ```txt
    ntscraper
    pandas
    vaderSentiment
    ```

## Usage

1.  **Run the Python script:**

    ```bash
    python fuze_tea_analysis.py
    ```

    (Replace `fuze_tea_analysis.py` with the actual name of your Python script.)

2.  **The script will:**

    -   Scrape tweets related to Fuze Tea and Nestea.
    -   Filter tweets from January 2024 onwards.
    -   Perform sentiment analysis on the tweet text.
    -   Save the results to a CSV file named `FuzeTea_Canada_tweets.csv` (or the name you designated in the code).
    -   Print the number of tweets and the average sentiment score to the console.

## Data Collection

The script uses the `ntscraper` library to scrape tweets from Nitter, an alternative front-end for Twitter. It searches for tweets using a list of relevant keywords and hashtags.

## Sentiment Analysis

Sentiment analysis is performed using the `vaderSentiment` library. This library analyzes the text of each tweet and assigns a sentiment score, indicating whether the tweet expresses positive, negative, or neutral sentiment. The compound score is used in this analysis.

## Data Analysis

The scraped data is saved to a CSV file, which can be further analyzed using tools like Excel, Google Sheets, or Python libraries like `pandas` and `matplotlib`. Possible analysis steps include:

-   Analyzing the distribution of sentiment scores.
-   Identifying common themes in the tweets.
-   Visualizing the results using charts and graphs.
-   Analyzing changes in sentiment over time.

## Contributing

Contributions are welcome! If you have suggestions for improvements or find any issues, please feel free to open a pull request or submit an issue.

## License

This project is licensed under the [MIT License](LICENSE) (or the license of your choice).
