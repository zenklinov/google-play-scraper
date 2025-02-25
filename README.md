# Google Play Reviews Scraper

A Jupyter Notebook script to scrape and analyze Google Play Store app reviews using Python. This script extracts the latest 200 reviews for a specified app, filters relevant data, and presents it in a structured format.

## Features

- **Extract Package Name**: Parses the package name from a Google Play Store URL.
- **Fetch Reviews**: Retrieves the latest 200 reviews, including metadata like content, rating, and timestamp.
- **Data Filtering**: Filters the dataset to retain essential columns (`reviewId`, `content`, `score`).
- **Pandas Integration**: Outputs data as a DataFrame for easy manipulation and analysis.

## Installation

### Dependencies
- Python 3.6+
- `pandas`
- `google-play-scraper`
- `python-dateutil`
- `urllib`

### Setup
1. Install required packages:
   ```bash
   pip install pandas google-play-scraper
   ```
2. Run the Jupyter Notebook (`get.ipynb`).

### Usage
1. Define the App URL:
   ```bash
   url = "https://play.google.com/store/apps/details?id=com.ea.game.pvzfree_row"
   ```
2. Run the Notebook: The script will extract the package name, fetch reviews, and display the filtered DataFrame.

## Example Output

The final DataFrame includes the following columns:

- **reviewId**: A unique identifier for each review.
- **content**: The text content of the review.
- **score**: The rating given by the user (1-5 stars).

| reviewId                                | content                                             | score |
|-----------------------------------------|-----------------------------------------------------|-------|
| ac769863-56f3-4103-85ff-2dd9b2ec8ce8    | "Good"                                              | 5     |
| eb0c29ee-34c9-4ba0-9c94-f0835ba94cb2    | "Ever since I paid for no ads, the app..."          | 4     |

---

## Notes

### Package Name
- Ensure the provided URL includes a valid `id` parameter (e.g., `com.example.app`).
- This `id` corresponds to the app's package name on the platform where reviews are sourced.

### Data Privacy
- All reviews are publicly available, and no sensitive user data is collected or processed.
- The extraction process adheres to ethical guidelines and respects platform terms of service.

### Date Handling
- Timestamps in the example output are illustrative.
- Actual data will reflect real review dates as provided by the source.
