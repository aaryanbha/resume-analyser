# GenAI Resume Analyzer

## Overview
An AI-powered application that analyzes resumes and provides actionable feedback to improve ATS compatibility and overall quality.

## Key Features

### Web UI Mode
Users can:

- Upload Resume PDF
- Paste any Job Description
- Run AI analysis instantly
- View:

  - Score
  - Category
  - Matched Skills
  - Missing Skills
  - AI Recommendation

---

It performs:

- Resume parsing from PDF
- Skill extraction
- Job description matching
- Candidate scoring
- Matched vs Missing skills detection
- Explainable AI recommendations
- Candidate ranking support

---

# Tech Stack

## Frontend
- React.js

## Backend
- FastAPI
- Python

## AI / LLM
- LangChain
- Groq (LLaMA 3.3)

## PDF Processing
- PyPDF

---

# Features

## Dynamic Resume Analysis
Upload a PDF resume and paste any Job Description for analysis.

## Skill Matching
Detects:

- Matched Skills
- Missing Skills

## Hybrid Candidate Scoring
Generates realistic candidate score:

0–100

Based on:
- Skill Match
- Experience
- Penalties for skill gaps

## Candidate Classification
- STRONG
- AVERAGE
- WEAK

## Explainable AI
Returns:
- Strengths
- Weaknesses
- Recommendation

## Batch Processing (CLI)
Add multiple resumes into:

```text
resumes/
```

and run:

```bash
python main.py
```

Automatically evaluates all resumes.

## Web UI
Upload Resume + Paste Job Description + Analyze instantly.

---

# Architecture

```text
Resume PDF
   ↓
Extraction
   ↓
Matching
   ↓
Scoring
   ↓
Explanation
   ↓
UI / CLI Output
```

# Web UI Usage

1. Upload Resume PDF

2. Paste Job Description

3. Click Analyze

4. Get:

- Score
- Category
- Matched Skills
- Missing Skills
- AI Recommendation

---

# Sample API Response

```json
{
 "score":85,
 "category":"STRONG",
 "matched_skills":[
   "React",
   "Node.js",
   "MongoDB"
 ],
 "missing_skills":[
   "Docker"
 ]
}
```

---

# Scoring Logic

| Factor | Weight |
|--------|--------|
| Skill Match | 60% |
| Experience | 30% |
| Penalties | Applied |
