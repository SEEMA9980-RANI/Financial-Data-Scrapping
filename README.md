**Stock Market Data Scraper (Python, Web Scraping, Data Processing)**  
*Developed an automated Python-based tool to scrape real-time stock prices from Google Finance for multiple companies and export the data in CSV format.*

### Project Description:
- **Objective:**  
  Created a web scraping tool that retrieves live stock price data for multiple companies from Google Finance using stock ticker symbols as input. The tool automates the data collection process, enabling users to extract and analyze stock data in real-time.

### Key Features:
- **Multi-Stock Scraping Capability:**  
  The script allows scraping stock prices for multiple companies by accepting a list of stock ticker symbols. For each stock, it dynamically constructs the appropriate URL to retrieve its financial data.
  
- **Web Scraping with BeautifulSoup:**  
  Utilized the `requests` library to send HTTP GET requests to Google Finance URLs for specific stock tickers. Parsed the HTML response using `BeautifulSoup`, targeting specific HTML elements (`div` tags with class identifiers) to extract stock prices.

- **Robust Error Handling:**  
  Implemented error handling mechanisms to ensure the script gracefully handles missing elements or unexpected errors during the scraping process. For instance, when the stock price is not found, the script returns a meaningful error message rather than failing unexpectedly.

- **Delay Mechanism for Server-Friendliness:**  
  Incorporated a customizable delay between scraping requests using `time.sleep()`. This ensures that the script doesn’t overwhelm Google Finance servers, adhering to web scraping best practices and reducing the risk of being blocked or throttled.

- **Data Handling with Pandas:**  
  The scraped data for each stock, including the ticker symbol and the current stock price, is compiled into a structured dictionary format. This data is then converted into a `Pandas` DataFrame, allowing easy manipulation and export. The final output is saved as a CSV file for further analysis or storage.

- **Browser Emulation:**  
  Set HTTP headers to include a user-agent string that mimics a real browser request. This helps prevent the requests from being blocked by the target website, as many sites reject automated requests that don’t come from browsers.

### Skills Demonstrated:
- **Python Programming:**  
  Wrote modular, efficient Python code to handle web requests, parse HTML, process data, and manage files.
  
- **Web Scraping:**  
  Demonstrated the ability to scrape data from websites by identifying relevant HTML structures and extracting target elements, in this case, stock prices from Google Finance.

- **Data Processing with Pandas:**  
  Showcased the use of `Pandas` to store scraped data in a tabular format, enabling easy manipulation and export to CSV for further analysis in tools like Excel or Python’s own data analysis libraries.

- **HTTP and Requests Management:**  
  Managed HTTP requests effectively by handling headers and using error codes to diagnose issues, such as 404 Not Found or 403 Forbidden responses. This ensured reliable communication with the server during the scraping process.

- **File I/O:**  
  Used Python’s built-in file handling capabilities to save the scraped data as a CSV file. This provides a portable and user-friendly way to share or store the results for future use.

### Example of Usage:
The script takes in stock symbols like `AAPL` (Apple), `GOOGL` (Google), and `MSFT` (Microsoft), scrapes the current stock prices from Google Finance, and outputs the data in a CSV file (`google_stock_data.csv`) in a tabular format, with columns for each stock's symbol and its current price.

### Technologies Used:
- **Languages & Libraries:** Python, BeautifulSoup, Requests, Pandas
- **Concepts:** Web Scraping, Data Extraction, HTTP Request Handling, Error Handling, Data Processing
- **Tools:** Python environment (IDE), CSV file handling.
