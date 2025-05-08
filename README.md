# Marketplace Price Analysis

## Overview
This repository contains an anonymized Python script designed to extract advertised product prices from a marketplace using a web scraping API, transform the data into a structured format, and compare prices against a reference price list to identify discrepancies. The script automates the generation of an Excel report with hyperlinks, enabling stakeholders to analyze pricing trends and make data-driven decisions. Developed as part of my work as an SAP Master Data Analyst, this project demonstrates skills in data pipeline development, ETL processes, and business intelligence (BI) reporting.

## Purpose
The `MarketplacePriceAnalysis` script supports business stakeholders (e.g., product or category managers) by providing actionable insights into marketplace pricing. It showcases my expertise in:

- Web scraping and API integration for data ingestion.
- JSON data transformation into DataFrames for analysis.
- Automated reporting with Excel outputs for stakeholder decision-making.
- Data pipeline optimization, mirroring workflows in SAP master data management and BI reporting.

This project is relevant to roles requiring data pipeline development, data analysis, and stakeholder collaboration in data engineering and analytics.

## Technologies
### Python
Core programming language for scripting and data processing.

### Libraries
- `requests`: For API data fetching.
- `pandas`: For DataFrame creation and data manipulation.
- `openpyxl`: For Excel file handling and hyperlink integration.
- `json`: For parsing API responses.
- `datetime`: For timestamped file naming.

### APIs
Generic web scraping API (placeholder; replace with actual API, e.g., a retail-focused API).

### Output
Excel file with sorted price differences and seller hyperlinks.

## Functionality
The script performs the following tasks:

1. **Data Extraction**: Fetches offer data (prices, sellers, conditions) for a list of product identifiers using a web scraping API.
2. **Data Transformation**: Parses JSON responses into a pandas DataFrame, extracting key fields (e.g., price, seller, condition).
3. **Data Integration**: Merges the fetched data with a reference price list (CSV) to align advertised prices with Minimum Advertised Prices (MAP).
4. **Price Comparison**: Calculates price differences (advertised price minus minimum advertised price from price list) and sorts results to highlight discrepancies.
5. **Reporting**: Exports the results to a timestamped Excel file, adding hyperlinks to seller links for stakeholder analysis.

## Anonymization
The code has been anonymized to protect sensitive information, ensuring it is safe for public sharing. Specific details, such as the API key, product identifiers, API endpoint, and company-specific references, have been replaced with placeholders (e.g., `YOUR_API_KEY`, `SAMPLE_ID_1`, `https://api.example.com`). The functionality remains intact, demonstrating web scraping, ETL, and reporting capabilities applicable to various marketplaces and datasets.

## Setup and Usage
### Prerequisites
- Python 3.7+
- Install required libraries: `pip install requests pandas openpyxl`
- A valid API key for a web scraping service (placeholder: `YOUR_API_KEY`).
- A price list CSV file (e.g., `resources/price_list.csv`) with columns: `MaterialID`, `ProductID`, `Description`, `MAPPrice`.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/gmmarsh/MarketplacePriceAnalysis.git
   cd MarketplacePriceAnalysis
   ```

### Create and Activate a Virtual Environment
- **On Windows**:
  ```bash
  python -m venv venv
  .\venv\Scripts\activate
  ```
- **On macOS/Linux**:
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### Install Dependencies
Install the required libraries within the virtual environment:
```bash
pip install requests pandas openpyxl
```

### Prepare the Environment
1. Place your price list CSV in the `resources/` directory.
2. Update the `API_KEY` variable in the script with your actual API key.
3. Replace the placeholder `product_ids` list with your product identifiers.
4. Update the API endpoint and domain as needed (e.g., replace `https://api.example.com/request` with the actual service).

### Running the Script
Execute the script:
```bash
python price_analysis.py
```

The script will:
- Fetch offer data for the specified product IDs.
- Generate a text file (`YYYY-MM-DD_offers_list.txt`) with raw JSON data.
- Produce an Excel file (`YYYY-MM-DD_marketplace_analysis.xlsx`) with sorted price differences and seller hyperlinks.

## Example Output
The Excel output includes the following columns:
- **ProductID**: Unique product identifier.
- **ItemCode**: Marketplace item code.
- **Price**: Advertised price.
- **MAPPrice**: Reference price from the price list.
- **PriceDifference**: Difference between advertised and MAP price.
- **Seller**, **SellerLink**, **ConditionTitle**: Seller details and product condition.

The file is sorted by `PriceDifference` to highlight significant pricing discrepancies, with clickable `SellerLink` hyperlinks for stakeholder review.

## Relevance to Data Engineering
This project aligns with key data engineering and BI tasks:
- **Data Pipeline Development**: Ingests and transforms marketplace data, similar to data lake ingestion processes.
- **ETL Processes**: Extracts (API), transforms (JSON to DataFrame), and loads (Excel) data.
- **BI Reporting**: Delivers stakeholder-focused insights.
- **Stakeholder Collaboration**: Supports business decision-making.

## Future Enhancements
- Integrate with visualization tools for advanced price trend analysis (in progress, aligning with my Microsoft Certified: Fabric Data Engineer Associate study).
- Add support for multiple marketplaces or APIs.
- Implement automated alerts for significant price discrepancies.
- Enhance error handling for API rate limits or missing data.

## Contact
For questions or feedback, reach out via:
- **Email**: gmmarsh@gmail.com
- **LinkedIn**: [linkedin.com/in/marshgraham](https://linkedin.com/in/marshgraham)
- **GitHub**: [github.com/gmmarsh](https://github.com/gmmarsh)

Explore my other projects on GitHub, including Crypto Clustering, for additional examples of my data analysis and machine learning skills.