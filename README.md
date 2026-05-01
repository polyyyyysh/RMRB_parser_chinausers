# People.cn News Parser (人民日报新闻爬虫)

A web scraper for collecting news articles from the People's Daily search engine (`search.people.cn`) by keyword. Designed to work in China where Google services are blocked. The scraper uses Selenium to obtain cookies and then `requests` to fetch article metadata and full texts via the search API.

## Features

- Collects: title, URL, source (main/local), publication date, full article text.
- Filters by date range (min_date / max_date).
- Deduplication by normalized URL and (title + day).
- Saves results to Excel (`.xlsx`).

## Requirements

- Python 3.8+
- Google Chrome browser installed
- Manual download of `chromedriver.exe` (see below)
- Download chromedriver.exe from a mirror (e.g., https://chromedrive.cn/) matching your Chrome version.
- Place the file in the same folder as the notebook/script.

## Installation

1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt

## Usage
Open the Jupyter notebook parser_analysis.ipynb and run cells sequentially.
You can change keyword and max_pages inside the notebook.

## Notes
Google’s official ChromeDriver sources are blocked in China; use a local mirror.

Add time.sleep() delays to avoid IP blocking.

Some articles may fail to load (e.g., due to image‑heavy pages) – they are skipped with a log message.

## Repository structure
parser_analysis.ipynb – main notebook with scraping.

requirements.txt – list of Python packages.

README.md – this file.
