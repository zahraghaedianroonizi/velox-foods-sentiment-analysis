# 🍽️ Velox Foods | Restaurant Review Sentiment Analysis

![Python](https://img.shields.io/badge/Python-Data%20Analysis-00AEEF?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-FF8C00?logo=jupyter&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-Cloud%20LLM-22C55E)
![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-9B59B6)
![NLP](https://img.shields.io/badge/NLP-Sentiment%20Analysis-FF4F9A)

## 📌 Project Overview

This project evaluates cloud-based and locally hosted large language models for **aspect-based sentiment analysis of restaurant customer reviews**.

Developed during a Data Analytics and AI training program, the project compares **Groq (cloud-based)** with **Ollama (locally hosted)** to determine which approach is more suitable for Velox Foods.

The evaluation focuses on sentiment prediction accuracy, coverage, consistency, processing speed, estimated costs, and privacy considerations.

## 🎯 Project Objectives

- Analyze customer reviews across five sentiment aspects: **Overall, Food, Service, Price, and Environment**.
- Compare model predictions against manually annotated human ground truth.
- Evaluate prediction quality using **Mean Absolute Error (MAE)**, error variability, and coverage.
- Assess processing speed and estimated operating costs.
- Recommend a suitable approach for restaurant review analysis.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data processing and analysis |
| Pandas | Data manipulation and evaluation |
| Jupyter Notebook | Analysis and documentation |
| Groq API | Cloud-based language model inference |
| Ollama | Local language model inference |
| Google Sheets | Manual review annotation |
| Git & GitHub | Version control and project documentation |

## 🔬 Methodology

### 1. Human Annotation

The four-person team manually annotated **200 restaurant reviews**, with each member responsible for **50 reviews** in Google Sheets.

The annotations were combined into a shared human-labeled dataset for model evaluation.

### 2. Independent Sentiment Analysis

Using the complete set of 200 annotated reviews, I independently performed the subsequent analysis and evaluation, comparing predictions from the Groq cloud model and the locally hosted Ollama model.

### 3. Model Evaluation

The comparison considered:

- **Accuracy:** Mean Absolute Error against human annotations
- **Consistency:** Standard deviation of prediction errors
- **Coverage:** Proportion of reviews receiving usable aspect predictions
- **Speed:** Estimated processing time for larger workloads
- **Cost:** Estimated cloud API expenses
- **Qualitative findings:** Mixed reviews, missing predictions, and potential ground-truth inconsistencies

## 📊 Key Findings

| Evaluation Dimension | Groq (Cloud) | Ollama (Local) |
|---|---|---|
| Prediction accuracy | Lower MAE across all five aspects | Higher MAE |
| Error consistency | Lower variability | Higher variability |
| Aspect coverage | Stronger overall coverage | More missing values, especially for Environment |
| Estimated time for 5,000 reviews | **18.6 minutes** | **5.2 hours** |
| Estimated API cost for 5,000 reviews | **$2.09** | No external API charges |

*Processing times and API costs are estimates extrapolated from the experiment, not measurements of an actual 5,000-review run. Local computing costs are not included.*

### Interpretation

The cloud-based approach performed better on the main evaluation dimensions. Both approaches encountered challenges with mixed or contradictory reviews, while some extreme prediction errors suggested possible inconsistencies in human labels, particularly for Price and Environment.

## ✅ Final Recommendation

**Groq was the preferred approach for Velox Foods** based on its stronger prediction accuracy, consistency, coverage, and processing speed.

**Ollama remains a relevant alternative** where local processing, privacy, or avoiding external API charges is a higher priority.

## 👩‍💻 My Contribution

This was a **four-member group project** with an initial collaborative annotation stage.

My individual contribution included:

- Manually annotating 50 restaurant reviews.
- Combining the team's annotations into a 200-review evaluation dataset.
- Independently performing the subsequent model analyses using the complete dataset.
- Comparing cloud and local model predictions.
- Evaluating accuracy, coverage, consistency, speed, and estimated costs.
- Interpreting the results and developing the final recommendation.

## 📁 Repository Structure

```text
velox-foods-sentiment-analysis/
├── notebooks/
│   ├── restaurant_groq_analysis.ipynb
│   ├── restaurant_ollama_analysis.ipynb
│   ├── restaurant_local_vs_cloud_evaluation.ipynb
│   └── Copy_of_2_ollama_and_reviews.ipynb
├── environment.yml
├── .gitignore
└── README.md
```

The original analysis data and generated CSV files are not included in this repository.

## 🔐 Security & Reproducibility

API credentials are not included in the repository. Local environment files are excluded through `.gitignore`.

The notebooks document the original analytical workflow. Reproducing all results requires access to the underlying review data, a suitable local Ollama setup, and a valid Groq API key for cloud inference.

## 📚 Project Context

Completed as part of a **Data Analytics and AI training program**, combining collaborative ground-truth annotation with independently conducted model analysis and evaluation.
