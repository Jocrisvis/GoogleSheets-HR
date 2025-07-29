# ✅ Google Sheets Formula: Row-by-Row Comparison

This formula checks whether values in **Column A** match those in **Column B**, row by row, and flags mismatches for review.

---

## What It Does

- Returns `✓` if values in the same row **match**
- Returns `Needs Attention` if they **do not match**
- Returns blank if the cell in Column # is empty *(avoids clutter)*

---

## Formula

```
=ARRAYFORMULA(IF(A2:A="", "", IF(A2:A = B2:B, "✓", "Needs Attention")))
```
## Example


| A (Expected) | B (Actual) | C (Result)      |
| ------------ | ---------- | --------------- |
| Apple        | Apple      | ✓               |
| Orange       | Banana     | Needs Attention |
| Grape        | Grape      | ✓               |
|              | Watermelon |                 |
| Mango        |            |                 |
| Mango        | Mango      | ✓               |
| Kiwi         | Papaya     | Needs Attention |
