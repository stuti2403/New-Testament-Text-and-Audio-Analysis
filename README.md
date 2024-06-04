# New Testament Text and Audio Analysis

## Project Overview

This project involves the extraction and analysis of text and audio data from the New Testament. Utilizing web scraping techniques and audio analysis methods, we aim to provide a comprehensive exploration of the textual and auditory components of each chapter.
### Dataset 
The data used in this project can be found at [https://www.faithcomesbyhearing.com/audio-bible-resources/bible-is](url)
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

## Key Performance Indicators

### Sentiment Analysis

- **Sentiment Analysis with TextBlob**: 
  - Conducted sentiment analysis using TextBlob on a sample of words.
  - **Key Finding**: Most words in the sample were neutral, indicating a balanced sentiment distribution.

### Audio Properties Analysis

- **Audio File Analysis**: 
  - Analyzed audio files to extract key properties such as duration, sample rates, and channels.
  - **Key Findings**: 
    - Sample rates distribution indicates diversity in audio quality, influencing the accuracy of speech recognition and synthesis.
    - Channels distribution highlights the stereo or mono nature of audio, affecting the spatial perception in TTS and STT applications.

### Text Properties Analysis

- **Text File Examination**: 
  - Examined text files to understand text lengths and word counts.
  - **Key Findings**: 
    - Around 25 files have lengths between 2000-4000 words.
    - Maximum of 750 words in a file.

### Alignment Between Text and Spoken Content

- **Alignment Analysis**: 
  - A higher frequency in a specific range of ratios may indicate common patterns or challenges in aligning text with audio in TTS or STT applications.

### Outlier Detection

- **Z-Score Analysis**: 
  - Utilized Z-score analysis to detect outliers in audio durations.
  - **Key Finding**: Two files detected as outliers, providing insights into anomalous audio files that may require special handling or preprocessing steps for improved TTS and STT performance.

### Amplitude Analysis

- **Mean Amplitude Distribution**: 
  - The plot visualizes the distribution of mean amplitudes across all audio files.
  - **Key Finding**: Mean amplitude is 3600 for more than 20 audio files, providing insights into the overall loudness or intensity of the audio files, which can be crucial for understanding speech clarity and quality in TTS and STT applications.

### Silence Detection

- **Silent Interval Analysis**: 
  - Analyzed the presence and distribution of silent intervals in the audio.
  - **Key Finding**: Silence of around 4 seconds is found to be present maximum times, which can be important for analyzing pauses, speech cadence, and overall audio structure in TTS and STT applications.

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
