# Budget-Aware SLM–LLM Collaboration for Adaptive IIoT Intrusion Detection Under Concept Drift

## Overview

This research investigates a budget-aware collaboration framework between Small Language Models (SLMs) and Large Language Models (LLMs) for adaptive Industrial Internet of Things (IIoT) intrusion detection under concept drift.

The proposed framework integrates conventional machine learning, continuous error monitoring, dynamic security evidence generation, and selective language model escalation to support resource-efficient adaptation decisions.

## Proposed Framework

- LightGBM-based network intrusion detection
- ADWIN-based error-change monitoring
- Dynamic contextual security evidence generation
- Qwen3-1.7B as the primary adaptation agent
- Qwen3-8B as the selective adaptation reviewer
- Budget-aware escalation and adaptation execution
- Prequential evaluation with delayed label feedback

## Experimental Dataset

The experiments utilize the TON_IoT network dataset.

- Total records: 211,043
- Training records: 84,417
- Validation records: 21,104
- Evaluation records: 105,522
- Predictive features: 30
- Sequential evaluation windows: 106

The evaluation uses controlled sequential distribution changes rather than verified chronological traffic evolution.

## Experimental Results

| Method | Accuracy | F1-score |
|---|---:|---:|
| Frozen LightGBM | 87.89% | 92.63% |
| Deterministic Controller | 96.64% | 97.84% |
| SLM-Only | 98.82% | 99.23% |
| LLM-Only | 88.39% | 92.92% |
| Proposed SLM–LLM | 99.21% | 99.49% |
| SLM + Rule Reviewer | 99.21% | 99.49% |

### Key Findings

- 99.21% overall detection accuracy.
- 99.49% F1-score.
- 2.75% false positive rate.
- 33.09% reduction in classification errors compared with SLM-only adaptation.
- 93.33% reduction in LLM invocations compared with LLM-only adaptation.
- 54.06% reduction in measured adaptation time compared with LLM-only adaptation.

The deterministic reviewer ablation achieved identical predictions with lower measured adaptation time, motivating further investigation of when LLM-based review provides additional value.

## Repository Contents

| File | Description |
|---|---|
| Jupyter Notebook | Research implementation and experimental workflow |
| configuration.json | Experimental configuration |
| final_performance.csv | Comparative detection performance |
| final_computational_cost.csv | Computational efficiency results |
| all_predictions.csv | Recorded experimental predictions |
| *_adaptation.csv | Adaptation operation logs |
| *_decisions.csv | Adaptation decision records |
| *_windows.csv | Window-level evaluation results |
| figures/ | Experimental visualizations |

## Technologies

Python, LightGBM, River, PyTorch, Hugging Face Transformers, Qwen3, NumPy, Pandas, Scikit-learn, Matplotlib, and Jupyter Notebook.

## Reproducibility

The repository contains the experimental implementation, recorded results, configurations, and decision logs. Reproduction requires access to the TON_IoT dataset and a suitable computational environment for language model inference.

## Author

**Faisal Popalzai**  
University of Regina  
Regina, Saskatchewan, Canada

## Research Status

Research manuscript and experimental implementation. Publication and citation details will be updated when available.
