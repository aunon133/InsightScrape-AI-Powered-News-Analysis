## **News Scraper and Analyzer**

This project, **News Scraper and Analyzer**, is developed as part of the Python Intern Final Assessment Task. It involves scraping data from a specified news portal, processing and structuring it according to a Django model, and generating insights using a language model.

## Project Overview

The main objectives are:
1. **Scraping and Filtering**: Extract news article URLs from a given category on a news portal.
2. **Data Extraction**: Retrieve relevant information for each article according to the Django `News` model structure.
3. **Insight Generation**: Use an open-source language model (LLM) to determine:
   - The importance score of the news article.
   - Sentiment analysis of the content.
   - Whether the article is internationally relevant.
4. **JSON Output**: Save the extracted and generated data into a JSON file.

## Repository Contents

- `article_analysis.json`: A JSON file containing analyzed articles with fields matching the Django `News` model structure.
- `demo.ipynb`: A Jupyter notebook containing code for scraping, analyzing, and processing the articles. The notebook includes data extraction logic and LLM-based analysis steps.

## Django Model Structure

The project utilizes a Django `News` model with fields such as:

- **url**: URL of the article.
- **title**: Title of the article.
- **meta_description**: Meta description for SEO.
- **news_type**: Main category of the article (e.g., Sports, Politics, Tech).
- **news_subcategory**: Sub-category within the main category.
- **media_type**: Media format (e.g., TV, Newspaper, Online).
- **image_urls**: URLs of associated images.
- **published_date** and **updated_date**: Publication and last update timestamps.
- **keywords**: Auto-generated keywords if unavailable on the page.
- **source**: Source of the article.
- **last_scraped**: Timestamp of the scraping event.
- **international**: Boolean, `True` if globally relevant.
- **old**: Boolean, `True` if older than 3 days.
- **sentiment**: Sentiment classification (positive, neutral, negative).
- **views, news_score, rating, engagement**: Various default values.
- **author**: Name of the author.
- **content**: Full text content of the article.


## Libraries Used

- **Django**: For defining the data model.
- **Requests**: To fetch web pages.
- **BeautifulSoup**: For HTML parsing and data extraction.
- **HuggingFace Transformers** or **similar LLM API**: For sentiment analysis and scoring.

## License

This project is licensed under the MIT License.
