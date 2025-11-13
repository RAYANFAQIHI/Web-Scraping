# Web Scraping with Python & BeautifulSoup 

This project is a simple web scraper written in Python that collects movie data
(title, rating, and vote count) from the IMDb Top Chart page using `requests`
and `BeautifulSoup`.

---

## Features

- Send HTTP requests using `requests`
- Parse HTML using `BeautifulSoup`
- Extract:
  - Movie title
  - IMDb rating
  - Vote count
- Combine multiple lists (titles, ratings, votes) using a `for` loop / `zip`
- Optionally export the scraped data to a CSV file

---

## Technologies

- Python 3.x  
- Requests  
- BeautifulSoup4  
- (Optional) CSV module (built-in)  

---

## Installation

1. Clone the repository:

    git clone (https://github.com/RAYANFAQIHI/Web-Scraping)
  

2. (Optional) Create and activate a virtual environment:

    python -m venv venv  

    On Windows:

    venv\Scripts\activate  

    On macOS / Linux:

    source venv/bin/activate

3. Install dependencies:

    pip install requests beautifulsoup4 lxml

---

## How It Works

1. Send a GET request to the IMDb Top Chart URL.
2. Parse the HTML response using `BeautifulSoup`.
3. Use `find_all` to collect:
   - all title elements
   - all rating elements
   - all vote count elements
4. Loop over the lists (with `for` + `zip`) and build a list of dictionaries
   containing `title`, `rating`, and `votes`.
5. Print the results and/or save them to a CSV file.

---

## Run the Project

### Jupyter Notebook

1. Open `Web_Scraping.ipynb` in Jupyter or Google Colab.
2. Run all cells.
3. Check the printed output and generated files (e.g. `movies.csv`).

### Python Script

1. Put the main scraping code in `main.py`.
2. Run:

    python main.py

---

## Export to CSV (Optional)

The scraped data can be saved as `movies.csv` using `csv.DictWriter`, where each
row represents one movie with columns:

- `title`
- `rating`
- `votes`
