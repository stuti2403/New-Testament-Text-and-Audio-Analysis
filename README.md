# New Testament Text and Audio Analysis

## Project Overview

This project involves the extraction and analysis of text and audio data from the New Testament. Utilizing web scraping techniques and audio analysis methods, we aim to provide a comprehensive exploration of the textual and auditory components of each chapter.

## Methodology

### Web Scraping with Selenium

- **Dropdown Menu Extraction**: 
  - Utilized Selenium to dynamically open the dropdown menu for all chapters in the New Testament.
  - Extracted relevant HTML tags to retrieve the links for each chapter and stored them in a list.

### Iterating Through Chapter Links

- **Text Extraction**: 
  - Iterated through the list of chapter links and extracted text content from each chapter's webpage.
  - Encountered an issue where some indices were missed during text extraction due to the speed of scraping.
  - Overcame this by introducing delay statements between scraping actions to ensure the webpage loaded completely before extracting text.

### Extracting Audio Links

- **Audio Tag Identification**: 
  - Used Beautiful Soup to find audio tags on each chapter's webpage.
  - Audio links were located in a dropdown menu, dynamically extracted from the dropdown.
  - Encountered errors with repeated webpage opening for audio extraction; resolved by introducing delays to prevent overload.

### Downloading Audio Files

- **Audio File Extraction**: 
  - Extracted parameters for downloading audio files from the audio links.
  - Downloaded audio files using the extracted parameters.

### Combining Text and Audio

- **Data Combination**: 
  - Combined each chapter's text with its corresponding audio link for analysis.
  - Printed the combined data for further examination.

### Exploratory Data Analysis (EDA)

- **Text Cleaning**: 
  - Removed numbers and different symbols from text for cleaner analysis.
- **Linguistic Analysis**: 
  - Identified bigrams and trigrams in the text for linguistic analysis.
- **Audio Analysis**: 
  - Analyzed audio properties such as amplitude, silence detection, frequency spectrum, anomalies, duration distribution, and sample rates.

## Challenges Faced and Solutions

- **Dynamic Dropdown Menu**: 
  - Used webdriver with Selenium to scrape dynamic links that were not showing up with BeautifulSoup.
- **Missed Indices in Text Extraction**: 
  - Addressed by introducing delay statements to allow sufficient time for webpage loading before scraping.
- **Repeated Webpage Opening for Audio Extraction**: 
  - Solved by adding delays between webpage accesses to avoid server overload and errors.
- **Cleaning Text Data**: 
  - Removed numbers and symbols from text to ensure accurate analysis and visualization.
- **Audio Analysis**: 
  - Used various techniques like amplitude analysis, silence detection, and frequency spectrum analysis for comprehensive audio insights.
