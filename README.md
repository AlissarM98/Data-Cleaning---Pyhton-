# Data-Cleaning---Pyhton-
Python workflows for cleaning messy clinical data from hospital records — handling duplicates, inconsistent formats, and healthcare-specific data quality issues.
# Cleaning Clinical Data with Python
### A Practical Guide to Hospital Record Data Workflows

> A hands-on guide for healthcare analysts and data scientists who work with 
> messy, real-world clinical data from hospital records.

---

## 📖 About This Book

Hospital records are notoriously messy — inconsistent formats, missing values, duplicate patient entries, ambiguous codes, and free-text fields that resist 
automation. This book walks through practical Python workflows to tackle these challenges head-on.

Diagnosis entries are often non-standardized entries, a single "diabetes Type 2" Diagnosis for example could be entered anywhere from "Diabetes Mellitus T2" , "Diab Mellitus Type 2" "Diabetes Type 2" and so on. Including case deifferences and free spaces, a single dagnosis may be found in about 20 entries. 
When dealing with large data sets with all kinds od diagnoses, this could render a dataset that is impossible to work with or handle on any PC. 


This data was aimed to be operable computationally in this REQUIRED FORM: 

Patient ID       ......... Diagnosis 1       Diagnosis 2     Diagnosis 3 ..........etc
0000001                        0                 1              0               
0000002                        1                 1              0

Where 1 means the existance of this diagnosis and 0 means its absence.

With standardized entries, exploding the "Diagnosis" data form one column into individual ones would have been quite approachable with several lines of code. 
But with entries such as described above, the dataframe was impossible to work with, and even when possible, the analysis and interpretion would be quite challenging.

This dataframe held about 300k entries with patient's vitals measurements and prescriptions along with the diagnosis. To have the diagnosis in the required form, The dataframe would render with size 300 000 x 100 000 — a completely unworkabe size. 

**Deleting redundant entries, clustering diagnosis in categories, and keeping the relevant-data only in this dataset i was able to reduce the size to 
The final dataframe;s size was [139305 rows x 187 columns]

Note: There may be some codes that are study-specific and can be deleted or changed as required
---


## 📚 Table of Contents

1. Diag_Prep: Since Diagnoses were a major problem, I extracted the "Diagnoses" column and worked with it on a seperate python book to have as much memory as possible. I then appended them to the original dataframe.
2. Main_DataFrame
---

## 🛠️ Tools & Libraries Used

- `pandas` 
- `numpy`
- `re` — regular expressions 
- `collections` 


---


## ⚠️ A Note on Data Privacy

There is no dataset uploaded, as the work dataset is completely confiential. I am ready to try this workflow on a demo dataset or on your specific dataset. 
The file names, terms included and paths are all synthetic. 

---

## 📄 License

This book is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE).  
You are free to share and adapt it with attribution.

---

## 🤝 Contributing

Found a type or want to add a workflow? Or even have suggestions for better coding? I am learning and always like to learn more! 
Please open an issue or submit a pull request.
