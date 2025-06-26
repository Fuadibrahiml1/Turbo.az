# Turbo.az Web Scraping Project

This project is a thorough and advanced web scraping solution for [Turbo.az](https://turbo.az), the largest car marketplace in Azerbaijan. It collects highly detailed data about every car listing, including technical details, pricing, and more, and saves the results in a structured CSV format.

## Features

- **Most Detailed Data Extraction**:  
  Scrapes comprehensive details from each car listing, including:
  - Brand, model, price, currency, and production year
  - Engine size, horsepower, fuel type
  - Mileage, color, body type, transmission, drive type
  - Number of seats, owners, vehicle condition, city, market, and more

- **Automatic Pagination Handling**:  
  The script automatically determines the number of pages to scrape (or defaults to 5 if undetectable).

- **Resilient and Informative**:  
  - Uses Selenium to robustly navigate and extract data from dynamically loaded content.
  - Provides console output for each step, including progress, errors, and summary.

- **Gentle to Source**:  
  Includes delays between requests to minimize server load and reduce the risk of being blocked.

## Usage

### Requirements

- Python 3.7+
- [Selenium](https://pypi.org/project/selenium/)
- [Geckodriver](https://github.com/mozilla/geckodriver/releases) (for Firefox)
- Firefox browser installed

Install Python dependencies:
```bash
pip install selenium
```

### How to Run

1. Download and install [Geckodriver](https://github.com/mozilla/geckodriver/releases) and ensure it is in your system PATH.
2. Make sure Firefox browser is installed.
3. Run the scraper notebook or script:
   - You can use the `Turbo.azWebscap.ipynb` Jupyter Notebook, or convert it to a Python script.
   - The script will navigate Turbo.az, collect detailed data, and save it into `data.csv`.

### Output

- All car data is saved in `data.csv` in the project directory.
- Columns include:  
  Brand, Model, Price, Currency, Year, Engine Size, Horsepower, Fuel Type, Distance, Color, Body Type, ProdYear, Transmission, Drive Type, New, Seats, Owners, Condition, Market, City.

Example output row:
```
BMW, 530, 36000, USD, 2018, 3.0 L, 249, Petrol, 120000 km, White, Sedan, 2018, Automatic, AWD, No, 5, 1, Used, Europe, Baku
```

## How it Works

- The scraper loads listing pages, discovers all car links, and then visits each car detail page to extract structured data.
- Handles dynamic content and pagination with Selenium and Firefox in headless mode.
- Data is parsed and written to CSV after every car to minimize data loss on errors.

## Legal & Ethical Notice

- This code is for educational and research purposes only.
- Respect the [Turbo.az terms of service](https://turbo.az/pages/rules) and their robots.txt.
- Avoid running the scraper too aggressively. Use for personal, non-commercial analysis only.
- The authors are not responsible for any misuse.

## Author

Fuad Ibrahimli

## License

MIT License

---

**Disclaimer:**  
This project is not affiliated with or endorsed by Turbo.az. All trademarks and data belong to their respective owners.
