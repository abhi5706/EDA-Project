# SwiftCart Outlier Analysis

## Findings
- Raw Age includes **23** numeric values above 100 and six non-numeric placeholders. These are invalid for age analysis and were set to missing.
- Quantity ranges from **1 to 20**, with no zero or negative quantities. High quantities were retained because they are valid positive purchases.
- Amount ranges from **₹229 to ₹3,036**, with no zero or negative amounts. High values were retained because they are valid sales observations.
- 23 Date serials were outside the valid observed range and were treated as missing.

## Decision
Do not delete valid high-value or high-quantity transactions merely because they are uncommon. Remove/transform only demonstrably invalid values.
