# Automated Amazon Price Tracker

The goal of this project is to build an automated web scraper that monitors product prices on Amazon. The script extracts data directly from the webpage, logs it into a structured CSV file over time, and triggers email notifications when the price drops below a target threshold.



### Project Structure

* `Amazon Web Scraping Using Python.ipynb`: The core Python script detailing the scraping pipeline:
    * **Web Scraping**: Utilizing `BeautifulSoup` and `requests` to parse HTML and extract the product's title and exact price.
    * **Data Cleaning**: Stripping raw text to isolate the numerical price and formatting it for data logging.
    * **Time-Series Logging**: Appending the extracted price and a daily timestamp (`datetime`) to an external `AmazonWebScraperDataset.csv` file.
    * **Process Automation**: Wrapping the extraction logic inside a `check_price()` function and using a `while(True)` loop with `time.sleep()` to automate daily data collection without manual intervention.
    * **Email Alert System**: Implementing `smtplib` to automatically send an SSL-encrypted email alert to the user when the targeted item goes on sale.

### Skills Demonstrated
* **Web Scraping**: Extracting unstructured HTML data.
* **Automation**: Scheduled background tasks.
* **Python Built-ins**: Advanced use of standard libraries like `csv`, `datetime`, and `smtplib`.

### Use Case
This architecture can be scaled to track multiple competitors' prices simultaneously, creating a live market-monitoring dataset for retail analytics.
