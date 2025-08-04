# 🏀 Task 05 – Descriptive Statistics with LLM Evaluation

This project analyzes the 2023–2024 season data for Syracuse University Women’s Basketball. It evaluates how well a Large Language Model (LLM) — specifically **GPT-4o** by OpenAI — can understand and reason about structured sports statistics using natural language prompts.

---

## 📊 Dataset

- **Source**: [Syracuse Women's Basketball](https://cuse.com)
- **Type**: Season-level stats (PDF)
- **Scope**:
  - Player statistics (overall + conference)
  - Team-level performance
  - Game results
- **Note**: The dataset was extracted from PDF and not included in this repo (per assignment guidelines).

---

## 📁 Project Structure

```
.
├── data/                        # PDF dataset (not uploaded to GitHub)
├── extracted_csv/              # Cleaned player-level CSVs
│   ├── players_overall.csv
│   └── players_conference.csv
├── prompts/
│   └── basketball_prompts.md   # Natural language questions for LLMs
├── results/
│   ├── descriptive_summary.json  # Ground-truth stats from Python
│   └── llm_testing_results.json  # GPT-4o responses + validation
├── scripts/
│   ├── data_extractor.py         # Extract structured data from PDF
│   ├── descriptive_stats.py      # Compute top scorer, rebounder, etc.
│   └── llm_evaluator.py          # Save/test LLM responses
└── README.md
```

---

## 🧠 LLM Used

- **Model**: `gpt-4o`
- **Provider**: OpenAI (May 2024 release)
- **Reason for Use**:
  - Advanced reasoning on structured text
  - Higher context limit and multimodal capabilities
  - Faster and more accurate than GPT-4-turbo
- **Platform**: ChatGPT Web (chat.openai.com)

---

## 🔍 Sample Prompts Asked

- Who was the top scorer for the team?
- Which player had the best field goal percentage?
- Who grabbed the most total rebounds?
- Who had the best assist-to-turnover ratio?
- Should the coach focus on offense or defense to win 2 more games?

> See: [`prompts/basketball_prompts.md`](./prompts/basketball_prompts.md)

---

## ✅ Accuracy Summary

| Question Type             | Status |
|--------------------------|--------|
| Basic Player Stats       | ✅ Accurate |
| FG% / Efficiency         | ✅ Accurate |
| Rebounds / AST/TO        | ✅ Accurate |
| Coaching Insight Prompts | 🔄 Deferred (future period) |

All tested prompts were correctly answered by GPT-4o and validated against Python results.

---

## 🔜 Future Work (Next Period)

- Add visualizations (e.g., PPG bar chart, radar plots)
- Compare responses across other models like **Claude**, **Gemini**, **Copilot**
- Use advanced prompt engineering for strategic reasoning
- Automate prompt injection via OpenAI API

---

## 🧾 Submission Notes

- Author: **Harshad Hirde**
- Status: ✔️ Phase 1 complete
