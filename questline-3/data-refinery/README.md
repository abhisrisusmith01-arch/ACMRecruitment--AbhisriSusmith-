# Questline 2: From Chaos to Clarity
## Task: Data Refinery

### Overview
The goal of this task was to clean up the raw `StudentsPerformance.csv` dataset into a clean, organized data.

---
**STEPS:**

1. **Loaded the Data:** Opened the CSV file using Python's `pandas` library.
2. **Checked for Empty Spaces (Missing Values):** Ran a check to see if any test scores or student details were missing.
3. **Checked for Repeated Rows (Duplicates):** Scanned the dataset to make sure no student's row was accidentally copy-pasted or entered twice. 
4. **Double-Checked the data:** Ran quick test commands (`assert`) to prove that there were zero missing values and zero duplicates left in the final dataset.
5. **Saved the Clean Version:** Saved this freshly verified dataset as a new file named `cleaned_students_performance.csv`.

---

### Observations:

While cleaning and inspecting the dataset, here is what I observed about the data:

* **Data Completeness:**
   The dataset is already complete, so no rows or columns had to be deleted or filled in.
* **Row Uniqueness:**
  . Every single entry represents a unique student record with no accidental copy-pastes.
* **Data Reliability:**
   Because the raw dataset had zero null values and zero duplicate rows, running our data refinery script successfully verified and saved a 100% clean output file (`cleaned_students_performance.csv`) that is ready for reliable analysis.

---
