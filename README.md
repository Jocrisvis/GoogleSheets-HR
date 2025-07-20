# 🔗 LEFT JOIN for Tables in Google Sheets

This formula improves processes in the HR and EHS departments.  
It can be applied elsewhere, but its main goal is to increase efficiency in HR workflows.

---

##  1. Objective

- Merge two tables using a specific key column  
- Avoid errors common with VLOOKUP/XLOOKUP  
- Reduce the number of manual steps when combining data

---

##  2. Method

- Uses only **formulas** in Google Sheets (no scripts needed)  
- Designed for simplicity and ease of use

---

##  3. Overview

Performs a join between two tables by a shared key column, similar to SQL JOIN. Example:

**Table 1: Employees**  
| ID | Name  |  
|----|-------|  
| 1  | Alice |  
| 2  | Bob   |  

**Table 2: Departments**  
| ID | Department      |  
|----|-----------------|  
| 1  | HR Department   |  
| 2  | EHS Department  |  

**Result (Join by ID):**  
| ID | Name  | Department     |  
|----|-------|----------------|  
| 1  | Alice | HR Department  |  
| 2  | Bob   | EHS Department |
---
## 4. Solution in Google Sheets

```
=QUERY({HR!A1:K1 , Survey!A1:D1 ; HR!A2:K , ARRAYFORMULA(IF(HR!A2:A="", ,(VLOOKUP(HR!A2:A , {Survey!A2:A , Survey!A2:D}, SEQUENCE(1,COLUMNS(Survey!A2:D), 2),FALSE))))}, "SELECT Col1, Col2, Col3, Col4, Col5, Col11, Col12, Col13", 1)
```
`SEQUENCE` is used to generate the headers from both worksheets.

``VLOOKUP`` helps match values between the tables based on a common key.

``QUERY`` lets us select and organize the final columns for the output table.

The exact structure depends on your sheet names, dimensions, and selected columns.

---

##  5. Possible Errors and Limitations ⚠️
>**Format mismatch:**
>
> Columns must have the same format (number vs plain text) in both tables to avoid errors.

>**Access restrictions:**
>
> Some users might not have permission for certain functions like IMPORTRANGE.

>**Manual copy-paste:**
>
> Some repetitive manual work may be needed, but it’s still easier than manual column movement or multiple VLOOKUPs.

>**Raw Data:**
>
> Datasets are normally provided clear but sometimes it needs to be clean.

>**Country in Google Sheets:**
>
> Errors due to location or language, different type of format and logic.
