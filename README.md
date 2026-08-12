# Prompt Chaining for Summarization Lab

An interactive web application demonstrating a 4-step multi-prompt pipeline for document summarization.

## 🔗 Pipeline Architecture

`Input Text` ➔ `Step 1: Key Point Extraction` ➔ `Step 2: Information Organization` ➔ `Step 3: Draft Summary Generation` ➔ `Step 4: Final Summary Audit`

### Steps Breakdown:
1. **Step 1 – Extract Key Points**: Reads input text and identifies core facts, statistical metrics, claims, and keywords as bullet points.
2. **Step 2 – Organize Information**: Groups extracted points into logical sections and strips redundant information.
3. **Step 3 – Generate Summary**: Drafts a concise summary in simple English while keeping original meaning intact.
4. **Step 4 – Improve Summary**: Audits draft for clarity, correctness, and missing points to produce final summary.

## 🚀 How to Run Locally

```bash
python server.py
```
Open `http://localhost:8000` in your browser.
