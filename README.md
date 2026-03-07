# Boston Police Department Journal Scraper

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![Project Status: Abandoned – Initial development has started, but there has not yet been a stable, usable release; the project has been abandoned and the author(s) do not intend on continuing development.](https://www.repostatus.org/badges/latest/abandoned.svg)](https://www.repostatus.org/#abandoned)

Scraping Boston Police Journal pdfs, provided (roughly) daily on https://bpdnews.com/.

Running:

1. Save your OpenCage API key in a file called `.env` with contents `OPENCAGE=yourapikeygoeshere`

2. Run `scrape_rss.py` to download the PDF files

3. Run `scrape_reports.py` to parse and geocode the PDF files into CSV fles

4. Run `clean_csvs.py` to clean the addresses into a geocodable format

5. Run `consolidate_csvs.py` to consolidate all CSVs into a single one (`output.csv`)

6. Run `geocode_csv.py` to geocode your consolidated CSV

7. Finally, run `fuzzy_match.py` to join the CSV file `/outputs/police_journal.csv` with the officer and district data. You will have a `outputs/incidents.geojson` you can open in your favorite GIS program
