# 🔗 LEFT JOIN for Tables in Google Sheets (Microproject)

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

- Performs a join between two tables by a shared key column, similar to SQL JOIN. Example:

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
## ⚠️ 4. Possible Errors and Limitations

> **Format mismatch:**  
> Columns must have the same format (number vs plain text) in both tables to avoid errors.  

> **Access restrictions:**  
> Some users might not have permission for certain functions like `IMPORTRANGE`.  

> **Manual copy-paste:**  
> Some repetitive manual work may be needed, but it’s still easier than manual column movement or multiple VLOOKUPs.

> **Raw Data:**  
> Datasets are normally provided clear but sometimes it needs to be clean.

> **Country in Google Sheets**  
> Errors due to location or language, different type of format and logic. 
---
