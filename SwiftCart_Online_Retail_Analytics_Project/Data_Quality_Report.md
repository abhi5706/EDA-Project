# SwiftCart Data Quality Report

## Raw Dataset Profile
- Rows: **31,047**
- Columns: **21**
- Exact duplicate rows: **0**
- Missing values occur in `index`, `Order ID`, `Cust ID`, `Gender`, `Age`, `Age Group`, `Date`, and `Month`.
- `Age` contains non-numeric placeholders and impossible high values.
- `Date` contains invalid serial values outside the observed 2022 range.
- `ship-state` contains **72** values with trailing whitespace.

## Cleaning Decisions
1. Removed `index` because it is a non-unique row-index artifact.
2. Stripped whitespace from text fields.
3. Converted `Cust ID` to numeric with `pd.to_numeric(..., errors="coerce")`.
4. Converted `Age` to numeric; invalid text and ages outside 18–100 were treated as missing.
5. Converted postal code to string because it is an identifier.
6. Converted valid Excel serial dates to datetime; invalid date serials were treated as missing.
7. Filled missing `Month` only when a valid `Date` supplied the month.
8. Retained all exact non-duplicate records and all valid positive quantity/amount observations.

## Before vs After
| Check | Raw | Cleaned |
|---|---:|---:|
| Rows | 31,047 | 31,047 |
| Columns | 21 | 20 |
| Exact duplicate rows | 0 | 0 |
| Missing Age | 1,085 | 1,114 |
| Missing Date | 465 | 488 |
| Missing Month | 465 | 8 |

## Validation
- No zero or negative quantities.
- No zero or negative amounts.
- Main categorical values are standardized.
- Valid dates fall in 2022.
- Remaining missing values are documented rather than fabricated.
