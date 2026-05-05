# Metacritic Movie Scraper

This project is a Python-based web scraper that extracts and structures movie data from Metacritic. It demonstrates data collection, parsing, and transformation using regular expressions and pandas.

---

## Features

- **Web Scraping:** Fetches HTML content from Metacritic using `urllib3` with secure HTTPS requests  
- **Data Extraction:** Uses regular expressions (regex) to extract movie titles, metascores, and release dates  
- **Data Cleaning:** Handles HTML encoding issues (e.g., `&#39;`) and removes irrelevant text  
- **Structured Output:** Organizes data into a pandas DataFrame for analysis and export  

---

## Technologies Used

- Python 3  
- `urllib3` – HTTP requests  
- `certifi` – SSL certificate verification  
- `re` (Regex) – pattern matching and text extraction  
- `pandas` – data manipulation and structuring  

---

## How It Works

1. **Connects** to the Metacritic “All Movies (2020)” page  
2. **Extracts** data using regex patterns such as:
   - `data-title="(.*?)"` (movie titles)  
   - `Metascore (\d+)` (scores)  
3. **Transforms** raw data into a structured format (list of dictionaries)  
4. **Loads** results into a pandas DataFrame for easy analysis  

---

## Example Output

| Title                   | Description                                      | Release Date   | Metascore |
|------------------------|--------------------------------------------------|----------------|-----------|
| Small Axe: Lovers Rock | A single evening at a house party in 1980s West... | Nov 27, 2020   | 95        |

The scraper extracts multiple data fields for each movie, including title, description, release date, and metascore, and organizes them into a structured dataset for analysis.

The scraper collects structured data for multiple movies, enabling further analysis or export to Excel.

---

## How to Run

```bash
pip install pandas urllib3 certifi
python main.py
