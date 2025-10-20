# Netflix-data-Cleaning
# Task 1 — Netflix Data Cleaning & Preprocessing

**Dataset:** Netflix Movies and TV Shows  
**Tool:** Microsoft Excel

## Files submitted
- netflix_titles_raw.xlsx (original)
- netflix_titles_work.xlsx (working copy)
- netflix_titles_cleaned.xlsx (final cleaned)
- README.md

## Summary of cleaning steps
1. Converted CSV to Excel table for safe editing.
2. Removed 12 exact duplicate rows (Excel → Remove Duplicates).
3. Trimmed extra spaces and removed non-printable characters from text columns (TRIM, CLEAN).
4. Standardized text:
   - `type`: standardized to "Movie" / "TV Show"
   - `rating`: standardized to uppercase (e.g., "TV-MA")
   - `country`: standardized to Proper case
5. Handled multi-value cells:
   - `listed_in` split into rows using Power Query (split by comma → into rows)
   - `cast` split into columns (cast_1, cast_2, cast_3) using Text to Columns
6. Converted `date_added` to Excel Date type and formatted to `dd-mm-yyyy`. Blank/invalid dates: Y left as blank / replaced with "Unknown".
7. Ensured `release_year` is numeric.
8. Replaced blank values in `director`, `cast`, `country` and `rating` with "Unknown" (where appropriate).
9. Final dataset size: Rows = __, Columns = 12

## Notes / Decisions
- Kept original raw file unchanged (`netflix_titles_raw.xlsx`).
- Used Power Query to expand genres into separate rows for easier genre-level analysis.
- Replaced only non-critical missing values with "Unknown"; left critical missing dates blank and documented them.

