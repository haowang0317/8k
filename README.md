# Automated Financial Event Identification Pipeline for SEC 8-K Filings

## 1. Project Context and Role

This project was developed to automate the critical pre-processing stages of quantitative financial research at NTU.

| Detail | Specification |
| :--- | :--- |
| **Role** | Non-dedicated Research Assistant (RA) |
| **Supervisor** | **Prof. Yiling Wu (吳儀玲教授)** |
| **Institution** | **National Taiwan University (NTU)** |
| **Period** | Second Half of 2025 (2025 H2) |

---

## 2. Project Goal

The primary objective is to streamline the professor’s research workflow by automating the entire process, from targeted data acquisition to final structured output, ensuring high efficiency and data consistency.

## 3. Core Workflow: Three-Step Automation

The application executes a robust, three-stage data pipeline designed specifically for event-driven studies:

### Step 1: Targeted Data Acquisition

* **Input:** Utilizes the professor’s proprietary **Excel file** (containing target identifiers).
* **Action:** Initiates focused web crawling against the SEC EDGAR database to retrieve specific 8-K financial filings.
* **Output:** Stores the raw filing data to the local disk.

### Step 2: Keyword Filtering and Isolation (Refining the Dataset)

* **Input:** The locally stored raw 8-K filings (full text files saved from Step 1) and keywords file provided by professor.
* **Action:** Scans the entire text of all local filings, applying predefined research lexicons or keyword lists to identify the presence of specific events (e.g., M&A, leadership changes).
* **Output:** Generates a separate, filtered repository containing **only** those 8-K reports in which the targeted keywords were identified, isolating the relevant dataset for Step 3.

### Step 3: Structured Reporting (HTML Output)

* **Action:** Organizes the identified reports and their associated metadata (e.g., filing date, company name, keyword context).
* **Output:** Generates a professional and easily reviewable **HTML table** format, strictly adhering to the professor’s exact layout specifications (as per the required `result_example` specification).

---

