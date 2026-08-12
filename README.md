


Build a complete beginner-friendly **Prompt Chaining for Summarization** application that demonstrates how a large piece of text can be processed through multiple AI prompts step by step instead of asking the AI to summarize everything in a single prompt.

## Project Objective

The main objective is to create a **multi-step prompt pipeline** for text summarization.

Instead of:

**Input Text → Final Summary**

the application should use:

**Input Text → Extract Key Points → Organize Information → Generate Summary → Improve Summary → Final Summary**

Each step should have a separate prompt and should pass its output to the next step.

---

## Step 1: User Input

Create a simple web interface where the user can enter or paste a large paragraph, article, notes, or document.

Provide:

* Large text box for input
* "Generate Summary" button
* "Clear" button
* Display area for results

Example input:

"Artificial Intelligence is a technology that allows computers to perform tasks that normally require human intelligence. AI is used in healthcare, education, banking, transportation, and many other industries..."

---

## Step 2: Key Point Extraction Agent

Create the first prompt that receives the user's input text.

Its task is to:

* Read the complete text.
* Identify the most important information.
* Extract important facts.
* Extract important concepts.
* Identify important keywords.
* Ignore unnecessary examples and repeated information.
* Do not create the final summary yet.

Example output:

* AI allows computers to perform intelligent tasks.
* AI is used in many industries.
* Healthcare, education, banking, and transportation use AI.
* AI can automate different types of tasks.

Pass this output to Step 3.

---

## Step 3: Information Organization Agent

Create a second prompt that receives the key points from Step 2.

Its task is to:

* Group related information.
* Remove duplicate points.
* Arrange the information logically.
* Identify the main topic.
* Separate important ideas from supporting details.
* Create a structured outline.

Example output:

Main Topic:

* Artificial Intelligence

Important Areas:

* Definition of AI
* Applications of AI
* Benefits of AI
* Industries using AI

Pass this organized information to Step 4.

---

## Step 4: Summary Generation Agent

Create a third prompt that receives the organized information.

Its task is to:

* Generate a concise summary.
* Use only the information provided by the previous step.
* Preserve the original meaning.
* Avoid adding unsupported information.
* Use simple and easy-to-understand English.
* Remove unnecessary repetition.

The summary should normally be around 3–5 sentences.

Pass this summary to Step 5.

---

## Step 5: Summary Improvement Agent

Create a final prompt that receives the generated summary.

Its task is to review and improve the summary.

Check:

* Is the summary clear?
* Is the main idea included?
* Are important points missing?
* Is there unnecessary information?
* Is the grammar correct?
* Is the summary easy to understand?
* Does it preserve the original meaning?

Then generate the final improved summary.

---

## Complete Prompt Chain

The application should follow this exact pipeline:

USER INPUT
↓
KEY POINT EXTRACTION
↓
INFORMATION ORGANIZATION
↓
SUMMARY GENERATION
↓
SUMMARY REVIEW & IMPROVEMENT
↓
FINAL SUMMARY

Each step must use a separate prompt.

---

## User Interface

Create a clean and simple dashboard.

### Input Section

Include:

* Text area
* Character/word counter
* Generate Summary button
* Clear button

### Processing Section

Show each stage separately:

**Step 1: Extracted Key Points**
Display the important points.

**Step 2: Organized Information**
Display the structured information.

**Step 3: Generated Summary**
Display the first summary.

**Step 4: Improved Summary**
Display the final summary.

Use cards or separate sections so that the user can clearly understand how the information changes at every stage.

---

## Technology

Use a beginner-friendly technology stack.

Frontend:

* HTML
* CSS
* JavaScript

Backend:

* Python
* Flask or FastAPI

AI:

* Use an LLM API for generating the responses.

The API key must be stored securely using an environment variable and must not be hardcoded in the source code.

---

## Backend Design

Create separate functions for each prompt:

1. `extract_key_points(text)`
2. `organize_information(key_points)`
3. `generate_summary(organized_information)`
4. `improve_summary(summary)`

Create one main function:

`generate_final_summary(text)`

This function should call the four functions in sequence and pass the output of each step to the next step.

---

## Error Handling

Add basic error handling.

If the user does not enter any text, show:

"Please enter some text to summarize."

If the AI API fails, show a friendly error message.

If one step fails, do not silently continue. Clearly indicate which step failed.

---

## Important Requirement

The main purpose of this project is to **demonstrate prompt chaining**.

Do not create one large prompt that performs all tasks.

Instead, use separate prompts:

Prompt 1 → Extract information
Prompt 2 → Organize information
Prompt 3 → Generate summary
Prompt 4 → Improve summary

The output of one prompt must become the input of the next prompt.

---

## Final Result

The application should allow a user to enter a long text and see how the AI processes it step by step.

Example:

**Input:**
Long article about Artificial Intelligence.

**Step 1:**
Important points extracted.

**Step 2:**
Points organized into categories.

**Step 3:**
Initial summary generated.

**Step 4:**
Summary reviewed and improved.

**Final Output:**
A clear, concise, accurate summary.

Also display a small explanation under each step explaining what that step did.

Make the entire project simple, clean, beginner-friendly, and easy to demonstrate in a college project presentation.

Create a simple **Prompt Chaining for Summarization** system using a multi-step prompt pipeline.

### Pipeline

**Step 1 – Extract Key Points**

* Read the given text.
* Identify the most important facts, ideas, and keywords.

**Step 2 – Organize Information**

* Group the extracted points into logical sections.
* Remove repeated or unnecessary information.

**Step 3 – Generate Summary**

* Create a short and clear summary using the organized information.
* Keep the original meaning.
* Use simple English.

**Step 4 – Improve Summary**

* Check the summary for clarity, correctness, and missing important points.
* Produce the final improved summary.

### Workflow

Input Text → Key Point Extraction → Information Organization → Summary Generation → Final Summary

Create a simple interface where the user can enter text and click **Generate Summary**. Display the output of each step and the final summary.





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
