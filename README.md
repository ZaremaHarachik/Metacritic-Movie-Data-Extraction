Metacritic Movie Scraper
This project is a Python-based web scraper designed to fetch and organize movie data from Metacritic. It demonstrates the use of Regular Expressions (Regex) for data extraction and pandas for data structuring.  
+1

Features
Web Scrapping: Fetches live HTML content from Metacritic using urllib3 and certifi for secure HTTPS requests.  

Regex Extraction: Efficiently parses movie titles, descriptions, release dates, and Metascores using specific regex patterns.  

Data Cleaning: Automatically handles HTML encoding (converting &#39; to apostrophes) and filters out non-relevant text.  

Structured Output: Compiles extracted data into a dictionary-based list and converts it into a pandas DataFrame for easy analysis.  

Technologies Used
Python 3.x

  
urllib3: For sending HTTP requests.  

certifi: To provide SSL certificates for secure connections.  

re (Regex): For pattern matching and text extraction.  

pandas: For data manipulation and table formatting.  

How It Works
Connection: The script establishes a connection to the Metacritic "All Movies" directory for 2020.  

Extraction: It searches the HTML for patterns such as data-title="(.*?)" and title="Metascore (\d+) out of 100".  

Transformation: The separate lists of titles, scores, and dates are combined into a single structured list of dictionaries.  

Loading: The final data is loaded into a pandas DataFrame, providing a clean preview of the top-rated films.  

Example Output
The scraper retrieves data points for 24 movies, including:  

Title: Small Axe: Lovers Rock

  
Metascore: 95  

Release Date: Nov 27, 2020
