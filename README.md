# Hacker News Pipeline

## Project Overview

This project involves building a data processing pipeline to analyze Hacker News posts from 2014. The goal is to filter, clean, aggregate, and summarize data to identify the top 100 keywords discussed in the tech community during that year.

## Dataset

- **Source:** The data is sourced from a Hacker News (HN) API, which returns JSON data of the top stories in 2014.
- **File:** The dataset is stored in a file named `hn_stories_2014.json`.
- **Content:** Each post contains keys such as `created_at`, `url`, `objectID`, `author`, `points`, `title`, and `num_comments`.

## Project Steps

### 1. Loading the JSON Data
- Extracted stories from the JSON file using Python's `json` module.

### 2. Filtering the Stories
- Filtered stories to include only those with more than 50 points, more than 1 comment, and titles not starting with "Ask HN".

### 3. Converting to CSV
- Transformed the filtered stories into a CSV format for consistent data processing.

### 4. Extracting Title Column
- Extracted the title column from the CSV file for further analysis.

### 5. Cleaning the Titles
- Cleaned the titles by converting them to lowercase and removing punctuation.

### 6. Creating the Word Frequency Dictionary
- Built a word frequency dictionary, excluding common stop words, to identify key terms.

### 7. Sorting the Top Words
- Sorted and identified the top 100 keywords based on frequency.

## Results

- The analysis revealed popular keywords such as "bitcoin," "google," "programming," and "python," providing insights into the tech topics discussed in 2014.

## Next Steps

- Implement file output for each task to enable task checkpointing.
- Use the `nltk` package for more advanced natural language processing tasks.
- Convert to CSV before filtering to retain all stories from 2014 in a raw file.
- Fetch data directly from the Hacker News JSON API for real-time analysis.

## Requirements

- Python 3.x
- JSON
- CSV
- String
- Datetime
- Custom modules: `pipeline`, `stop_words`

## Usage

1. Clone the repository.
2. Ensure the `hn_stories_2014.json` file is in the project directory.
3. Run the Python script to process the data and identify top keywords.

## Conclusion

This project demonstrates the use of a data processing pipeline to extract meaningful insights from large datasets, showcasing skills in data extraction, transformation, and natural language processing.
