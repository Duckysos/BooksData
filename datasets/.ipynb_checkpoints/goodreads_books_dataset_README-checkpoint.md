# Goodreads Books Dataset Dataset

## Overview
This dataset contains book data scraped from Goodreads.

## Dataset Information
- **Total Records**: 3,045
- **Columns**: 20
- **File Size**: 0.99 MB
- **Created**: 2025-10-08

## Columns Description

| Column | Type | Description |
|--------|------|-------------|
| rank | int | Book ranking position |
| book_id | str | Unique Goodreads book identifier |
| title | str | Book title |
| author | str | Book author(s) |
| rating | float | Average rating (0-5 scale) |
| rating_category | str | Rating category (Poor/Fair/Good/Excellent) |
| title_length | int | Number of characters in title |
| author_count | int | Number of authors |
| goodreads_link | str | URL to Goodreads book page |
| cover_url | str | URL to book cover image |
| source | str | Data source (Goodreads) |
| scraped_at | datetime | Timestamp when data was scraped |

## Statistics
- **Average Rating**: {info['rating_stats']['mean']:.2f}
- **Rating Range**: {info['rating_stats']['min']:.2f} - {info['rating_stats']['max']:.2f}
- **Most Common Rating Category**: {max(info['rating_distribution'], key=info['rating_distribution'].get)}

### Top 10 Authors by Book Count
- Agatha Christie: 20 books
- Stephen        King: 19 books
- Brandon Sanderson: 12 books
- Terry Pratchett: 11 books
- Isaac Asimov: 10 books
- C.S. Lewis: 9 books
- Sarah J. Maas: 9 books
- Holly Black: 9 books
- Lee Child: 9 books
- David Eddings: 8 books


## Data Quality
- **Missing Values**: 1853 total missing values
- **Completeness**: 97.0%

## Usage
This dataset is suitable for:
- Data analysis and visualization
- Machine learning projects
- Recommendation system development
- Statistical analysis
- Academic research

## License
This dataset is provided for educational and research purposes. Please respect the terms of service of the original data sources.

## Citation
If you use this dataset in your research, please cite:
```
Goodreads Books Dataset Dataset. Created: 2025-10-08. 
Source: Goodreads web scraping.
```
