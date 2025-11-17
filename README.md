# Goodreads Books Exploration

A compact exploratory data analysis (EDA) of a 3,045-row Goodreads books dataset that captures each title’s ranking, authorship, text complexity, and rating metadata. The notebook focuses on understanding what separates consistently well-rated books from the rest and which textual/series attributes correlate with popularity.

## Dataset

- **Location:** `datasets/goodreads_books_dataset.csv`
- **Shape:** 3,045 books × 20 columns (9 numeric, 7 categorical, 4 boolean)
- **Key fields:** `rank`, `percentile_rank`, `book_id`, `title`, `author`, `rating`, `rating_category`, `rating_tier`, `title_length`, `word_count`, `author_count`, `title_complexity`, `title_type`, `estimated_popularity`, `has_series_info`, `has_subtitle`
- **Data quality highlights:**
  - `series_number` is missing for ~61 % of records, reflecting standalone titles; encode “no series” explicitly rather than imputing arbitrary numbers.
  - `rating_category` has only two nulls; they can be back-filled from the numeric rating or dropped with negligible effect.
- **Distribution takeaways (from the notebook):**
  - Ratings are tightly clustered around 4.0 (mean = 4.06, median = 4.07) with very few poorly rated books.
  - Title lengths are right-skewed (mean ≈ 32.6 chars) due to verbose titles/subtitles.
  - Rating labels are dominated by “Excellent” and “Good”, so analyses should be interpreted as “top-shelf” Goodreads titles rather than the full catalog.
  - Frequent authors include Agatha Christie, Stephen King, Brandon Sanderson, Terry Pratchett, and Isaac Asimov.

## Environment Setup

```powershell
# 1. Create and activate a virtual environment
python -m venv .venv
.\.venv\Scripts\activate   # (Use `source .venv/bin/activate` on macOS/Linux)

# 2. Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install pandas numpy matplotlib seaborn jupyter

# 3. Launch Jupyter
jupyter notebook Books.ipynb
