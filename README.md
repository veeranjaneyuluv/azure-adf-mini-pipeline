

# 📌 Azure Data Factory – Metadata-Driven ETL Pipeline

## 🔹 Project Overview

This project demonstrates how to use **Azure Data Factory (ADF)** to build a metadata-driven ETL pipeline. The pipeline copies data from a raw folder in **Azure Data Lake Storage Gen2**, extracts metadata, loops through multiple files, and applies conditional logic for dynamic execution.

---

## 🔹 Architecture

```
Azure Data Lake Gen2 (Raw)
        │
        ▼
  Azure Data Factory Pipeline
   ├── Copy Data (CSV → ADLS)
   ├── Get Metadata (file properties)
   ├── ForEach (loop over files)
   └── If Condition (branch execution)
        │
        ▼
Azure Data Lake Gen2 (Processed)
```

---

## 🔹 Features Implemented

1. **Copy Data Activity**

   * Moves CSV files from **raw** container to **processed** container.
   * Configured dataset with dynamic parameters for file path.

2. **Get Metadata Activity**

   * Extracts file names, size, and last modified date.
   * Helps to validate file existence before processing.

3. **ForEach Loop**

   * Iterates over multiple files in the folder dynamically.
   * Ensures all incoming data files are processed automatically.

4. **If Condition**

   * Adds branching logic based on metadata (e.g., file exists or not).
   * Skips or processes accordingly.

---

## 🔹 Tools & Technologies

* Azure Data Factory
* Azure Data Lake Storage Gen2
* CSV (Delimited Text) Datasets
* JSON (for pipeline export)

---

## 🔹 Screenshots

*(Add your screenshots here)*

* Pipeline overview
* Copy Data activity
* Get Metadata activity
* ForEach loop
* If Condition

---

## 🔹 How to Reproduce

1. Upload sample CSV files into **ADLS Gen2 raw container**.
2. Create datasets in ADF (DelimitedText).
3. Build pipeline with:

   * Copy Data → Get Metadata → ForEach → If Condition.
4. Publish and trigger the pipeline.
5. Output files appear in **processed container**.


