<!-- Project overview + problem statement.

Setup instructions (conda / pip install -r requirements.txt).

Usage examples (input/output JSON).

Architecture diagram.

Reproducibility notes. -->


# 🏥 ADEGuard

ADEGuard is an AI-powered system designed to detect Adverse Drug Events (ADEs) from free-text patient reports, cluster symptom variants with age and modifier awareness, and classify their severity. The project is part of a broader health-tech initiative by CureviaAI, focusing on real-world problems in drug safety, patient care, and clinical decision support.

Project Background

Since the COVID-19 pandemic, mass vaccinations have led to a surge in reported ADEs, ranging from mild reactions to severe, life-threatening complications. While large-scale surveillance systems like the Vaccine Adverse Event Reporting System (VAERS) collect structured symptom codes and free-text notes, the free-text entries remain noisy, unstandardized, and lack severity or age-specific context.

ADEGuard aims to bridges this gap by leveraging NLP and AI to transform unstructured patient narratives into actionable insights for hospitals, regulators, and pharmaceutical companies, helping improve drug safety, optimize response times, and prevent critical complications.

### Problem Statement

Free-text ADE reports are rich but unstructured.

Existing structured data lack context, such as intensity, duration, or age-specific patterns.

Timely insights into ADEs are critical for healthcare decision-making and patient safety.

### Task Overview

As part of the ADEGuard project, the AI system is designed to:

Create Gold Data: Manually annotate ADE and DRUG spans in patient narratives.

Use Weak Supervision: Generate weak labels from existing report data.

NER Extraction: Detect ADE and DRUG entities using BioBERT or similar biomedical NER models.

Modifier-Aware & Age-Specific Clustering: Group ADE symptoms based on modifiers (mild/moderate/severe) and patient age groups.

Label Severity Levels: Determine severity using rules, manual labels, and model-based predictions.

Visualization & Explainability: Streamlit or Gradio UI for token-level highlights, clustering plots, and explainable AI visualizations using SHAP or LIME.

### Key Features

NER for ADEs and Drugs using biomedical transformer models.

Weak Supervision & Rule-Based Methods to scale annotations.

Data Augmentation to enhance model performance on limited labeled data.

Modifier & Age-Aware Clustering using HDBSCAN and Sentence-BERT embeddings.

Severity Classification combining rules, manual labels, and model predictions.

Interactive Visualizations for explainable insights.

### Technology Stack

Python – Core programming language

BioBERT / SciSpacy – Biomedical embeddings & NER

HuggingFace Transformers – Model fine-tuning and classification

Label Studio / Prodigy – Data annotation

HDBSCAN + Sentence-BERT – Symptom clustering

Streamlit / Gradio – Interactive UI for exploration

SHAP / LIME – Explainable AI

### Future Goals

Expand ADE detection to broader datasets beyond VAERS.

Enhance severity scoring and clustering algorithms.

Deploy the system for real-time pharmacovigilance support.

### Contact

Developed by Joe Raymond