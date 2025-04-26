Project Document: Local AI for Tableau Server Log Analysis

Overview

This project aims to build a local, privacy-focused ML/AI application that:

Analyzes Tableau Server logs.

Detects anomalies and errors.

Generates Root Cause Analysis (RCA) summaries.

Recommends troubleshooting steps.

Presents results via a secure, tabbed web chat interface.


The solution runs entirely offline to ensure data privacy and security.


---

Architecture

Flow:

[Logs Input] -> [Parser] -> [Preprocessing] -> [ML Engine (Anomaly Detection)] -> [RCA Generator] -> [Web UI Tabs Display]

Components:

Log Parser: Ingests and normalizes various Tableau Server logs.

Preprocessor: Cleans and extracts relevant information.

Anomaly Detector: Uses ML models to find unusual patterns.

RCA Generator: Summarizes causes and proposes troubleshooting.

Knowledge Base: Maps known errors to fixes.

Web Chat UI: Displays results across multiple tabs.



---

Component Breakdown


---

Technology Stack


---

Web Interface (UI Structure)

Chat Input ("Ask about logs")

Tabs:

Errors and Warnings

Anomalies Detected

RCA Summaries

Suggested Fixes

Raw Extracted Data




---

Flow Diagram

[Upload Logs / Auto-ingest]  
        ↓
[Parse and Preprocess]  
        ↓
[Anomaly Detection ML Model]  
        ↓
[RCA Generator + KB Lookup]  
        ↓
[Tabbed Web Chat Display]


---

Prototype POC (Quick Setup)

Dependencies:

pip install streamlit pandas scikit-learn pyod faiss-cpu transformers

Run App:

streamlit run app.py

Input: Upload a Tableau Server log zip or directory.

Outputs:

List of anomalies.

Top 5 Errors.

RCA summaries per anomaly.

Suggested troubleshooting based on KB.



---

Testing Approach

Use real Tableau ziplogs bundles.

Validate parsing (no crashes on missing or weird log files).

Validate anomalies detected (manual inspection).

Validate RCA summaries (compare against manual RCA).

Validate troubleshooting steps (KB lookup accuracy).



---

Future Enhancements

Add Graphs (error trends over time).

Add auto-scheduler (periodic monitoring of logs folder).

Add Alerting (local email/SMS when critical errors detected).

Add CLI tool for server admins.

Expand to cover Tableau Prep and CRM Analytics logs.

Integrate with internal JIRA or ServiceNow ticket creation.



---

End of Document


---

(Next Step: Architecture Diagram + Prototype Code coming up!)

