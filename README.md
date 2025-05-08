# Telugu ASR Cross-Validation Study

## Overview  
We compare two speech-to-text models on Telugu data using $k$-fold cross-validation ($k=2,3,4,5$):  
- **Wav2Vec2.0 XLSR-53-large**  
- **Whisper-small**  

Each experiment is encapsulated in a notebook (with input code and output cells) that fine-tunes the model, logs training/validation loss, WER, CER, and generates plots.

## Experiments  
- Base model (no CV)  
- $k$-fold CV for $k=2,3,4,5$  
- Metrics: WER, CER, evaluation loss  

## Usage  
1. Install dependencies (PyTorch, Transformers, Datasets, NumPy, Matplotlib, Jupyter).  
2. Open the desired notebook (`wav2vec_k*.ipynb` or `whisper_k*.ipynb`) in JupyterLab.  
3. Run all cells end-to-end to reproduce training logs, tables, and figures.

## Key Results  
| Model                      | Base WER/CER | Best CV WER/CER ($k=5$) |
|----------------------------|--------------|-------------------------|
| Wav2Vec2.0 XLSR-53-large   | 0.2567/0.0453| 0.2362/0.0412           |
| Whisper-small              | 0.2776/0.0515| 0.2867/0.0548           |

A combined bar chart (`base_vs_best.pdf`) illustrates side-by-side comparison of base vs.\ best-fold errors.

## Contributing  
Suggestions and issues are welcome—feel free to propose new folds, models, or enhancements to the analysis.
  
