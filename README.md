# EduVerse

Awarded 2nd Place Overall at NUS LifeHack 2025.

EduVerse is an adaptive learning management platform that keeps teachers in control of lesson design and question curation while personalising student revision using Knowledge Tracing models.

## Overview

Many educational platforms either rely on static worksheets or hand full control over to generative models without teacher oversight. EduVerse bridges that gap:

- Teacher-led curriculum design: Teachers structure lesson plans, define prerequisite links between topics, and curate the exact questions assigned to students.
- Multimodal revision materials: Teachers attach notes, worked examples, and media directly to topic nodes so students can revise actively while attempting questions.
- Adaptive Knowledge Tracing (`kt_models`): A Python and PyTorch backend models each student's per-topic mastery over time and routes targeted revision material where gaps appear.

## Architecture

- Frontend: Next.js and TypeScript web application providing separate teacher authoring and student practice views.
- ML Backend (`kt_models/`): Python service running Knowledge Tracing inference to estimate mastery probabilities across linked curriculum topics.

## Getting Started

### 1. Start the Knowledge Tracing model service

```bash
cd kt_models
python -m venv venv
# On macOS / Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate.bat

pip install -r requirements.txt
python main.py
```

### 2. Start the web application

In a separate terminal from the repository root:

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.
