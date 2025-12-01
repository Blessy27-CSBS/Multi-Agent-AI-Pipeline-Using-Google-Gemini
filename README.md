![Uploading ChatGPT Image Dec 1, 2025, 04_27_31 PM.png…]()

# Multi-Agent AI Pipeline Using Google Gemini — Research, Analysis, Writing & Evaluation System

**Capstone project (Google Agents Intensive)** — This notebook implements a complete multi-agent pipeline that automates web research, analysis, long-form report writing, and evaluation. The system demonstrates key concepts from the Agents course: multi-agent coordination, tools, sessions & memory, long-running operations (pause/resume), observability, and LLM integration (Google Gemini 2.5).

## Project overview
- **Researcher Agent**: runs parallel web searches and stores results in a persistent memory bank.  
- **Analyzer Agent**: synthesizes research notes using the Gemini LLM.  
- **Writer Agent**: performs long-running report generation with pause/resume (checkpoint).  
- **Evaluator Agent**: scores the final report for clarity and completeness.

## Key files (outputs)
- Final report: `/kaggle/working/final_report.txt`  
- Memory bank: `/kaggle/working/agents_memory.json`  
- Writer checkpoint: `/kaggle/working/writer_checkpoint.json`

## How to run (quick)
1. Run the cells in order (imports → tools → memory → call_llm → agents → pipeline).  
2. Run the pipeline: `state = run_pipeline("<your topic>")`  
3. Resume writer & evaluate: run the resume/evaluate cell; final report will be saved to the path above.

## Notes
- The notebook uses the Google Gemini API. Make sure your `GOOGLE_API_KEY` is stored in **Kaggle Add-ons → Secrets**.  
- If web scraping returns empty results, try richer queries or add manual text to memory to seed the analyzer.

