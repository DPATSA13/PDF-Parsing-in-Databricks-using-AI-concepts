# 📄 AI-Powered Resume Parser in Databricks

This project parses resume PDFs to extract structured information such as contact details, skills, companies, roles, and durations using NLP and regex techniques. Built entirely on **Databricks** using **Python**, **PyMuPDF**, **spaCy**, and **RapidFuzz**.

## 🚀 What It Does

Given a PDF resume (uploaded to DBFS or workspace volume), the parser extracts:

- 👤 **Name**
- 📧 **Email**
- 🔗 **LinkedIn**
- 📞 **Phone Number**
- 🛠️ **Skills**
- 🎯 **Roles**
- ⏱️ **Duration**
- 🏢 **Companies Worked With**

All extracted data is:
- Printed in a clean format (line-by-line)
- Written to a CSV file in overwrite mode
- Ready for use in dashboards or Delta Lake tables

## 🛠️ Tech Stack

- 🧠 **spaCy** (NER for organizations)
- 📄 **PyMuPDF (`fitz`)** (to read PDF content)
- 🧪 **Regex** for pattern extraction
- 🧠 **RapidFuzz** for fuzzy company name matching
- 🧾 **Pandas + CSV I/O**
- ☁️ **Databricks File System (DBFS)** for file storage

## 📁 Folder Structure

```
.
├── notebooks/
│   └── resume_parser.ipynb         # All code with explanation
├── data/
│   └── sample_resume.pdf           # Your sample resume(s)
├── output/
│   └── parsed_resume_clean.csv     # CSV output with extracted fields
├── README.md
```

## ⚙️ How to Use

1. Upload your PDF resume to `/FileStore/pdfs/` in Databricks.
2. Run the notebook. It will:
   - Read the resume
   - Parse all fields
   - Print results
   - Write output to `/FileStore/parsed_resumes/parsed_resume_clean.csv`
3. Download or query the output file.

## ✅ Sample Output

```
Name     : DURGA PRASAD PATSA
Email    : durgaXXXXXXX@gmail.com
LinkedIn : https://linkedin.com/in/durga-prasad-patsa-1a0335bb
Phone    : 309-XXX-XXXX

Skills:
 - Azure Databricks
 - Delta Lake
 - Power BI
 ...

Companies:
 - BP
 - AT&T
 - Microsoft
 - Nationwide Insurance
```

## 🧠 Future Enhancements

- Process multiple resumes in batch
- Build search engine using Elasticsearch
- Serve as an API with Flask/FastAPI
- Feed parsed data into ML pipelines for recommendation or ranking

## 🤝 Acknowledgements

- `fitz` (PyMuPDF) for PDF parsing
- `spaCy` for NER
- `rapidfuzz` for intelligent text matching
- Inspired by real-world recruiting needs and resume analytics use cases

## 📬 Contact

👤 **Prasad Patsa**  
📧 [durgapatsa.p@gmail.com](mailto:durgapatsa.p@gmail.com)  
💼 [LinkedIn Profile](https://www.linkedin.com/in/durga-prasad-patsa-1a0335bb)

> 🎯 Showcase this project during Data Architect interviews — it proves your strength in NLP, automation, AI-enhanced ETL, and real-world problem solving.
