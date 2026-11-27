# Experimental Reproducibility

## Dataset

This research uses the TON_IoT network dataset.

Dataset source: https://research.unsw.edu.au/projects/toniot-datasets

The dataset is not distributed with this repository.

## Environment Setup

Install the required Python dependencies:

`pip install -r requirements.txt`

A CUDA-compatible GPU is recommended for language model inference.

## Model Configuration

| Component | Model |
|---|---|
| Intrusion detector | LightGBM |
| Drift monitor | ADWIN |
| SLM | Qwen/Qwen3-1.7B |
| LLM | Qwen/Qwen3-8B |
| LLM quantization | 4-bit NF4 |
| Random seed | 42 |
| Window size | 1,000 records |
| Label delay | One window |
| Confidence threshold | 0.80 |
| LLM invocation budget | 3 |

## Running the Experiments

1. Download the TON_IoT network dataset.
2. Install the required dependencies.
3. Open the research Jupyter notebook.
4. Update dataset and output paths for your environment.
5. Execute the notebook cells sequentially.
6. Compare the generated results with the recorded experimental CSV files.

## Evaluation Protocol

The experiments employ prequential evaluation with delayed label feedback. Adaptation decisions use only previously available labeled observations.

The dataset ordering represents controlled sequential distribution changes rather than verified chronological concept drift.

## Reproducibility Notes

Execution times may vary depending on hardware, software versions, and computational resources. Exact reproduction of the reported results has not yet been independently verified.
