
# COMP6781 Project - BERT-Based Models for Negation Detection in Biomedical Texts

## Overview

This project investigates the role of contextual embeddings in detecting negation and speculation in biomedical texts. Using the BIOSCOPE dataset, the project involves fine-tuning BERT-based models (BERT, BioBERT, ClinicalBERT) for sequence labeling tasks. The tasks include identifying negation cues and scope spans, represented with BIO tags.

### Key Features
- Token-level and span-level evaluations for negation detection.
- Comparative analysis of general-purpose (BERT) and domain-specific (BioBERT, ClinicalBERT) models.
- Evaluation using **Micro F1**, **Span Matching**, and **CRF Suite Metrics**.

## Dataset
The **BIOSCOPE dataset** is used, containing:
- Annotated sentences with cue spans (negation indicators) and scope spans (text affected by negation/speculation).
- Imbalanced data: 12,368 non-negated and 2,094 negated sentences.

Dataset processing steps:
1. Conversion of character spans to word spans.
2. Removal of cue spans from scope spans for better representation.

## Code Structure

The code performs:
- **Preprocessing**: Tokenization and BIO-tag creation.
- **Fine-Tuning**: Training BERT, BioBERT, and ClinicalBERT on labeled data.
- **Evaluation**: Metrics for token-level, span-level, and CRF-based sequence alignment.

### Main Sections:
- **Preprocessing**: Includes data loading, tokenization, and BIO-tagging.
- **Fine-Tuning**: Adapts pre-trained models for the task.
- **Evaluation**: Calculates precision, recall, and F1-scores.

## How to Use

### Prerequisites
1. Python (>= 3.8)
2. Install required libraries:
    ```bash
    pip install -r requirements.txt
    ```
3. Ensure access to the BIOSCOPE dataset.

### Running the Code
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Negation-Cue-and-Scope-Spans-Detection.git
    cd Negation-Cue-and-Scope-Spans-Detection
    ```
2. Run the Jupyter Notebook:
    ```bash
    jupyter notebook COMP6781_Project_Chandrasekar_Ganesh_40256600.ipynb
    ```

## Results
- BERT outperformed BioBERT and ClinicalBERT in both token-level and span-level evaluations.
- Highlighted the challenges of handling rare labels and imbalanced datasets.

## Future Work
Exploring unified training across datasets and attention-based mechanisms to enhance span learning.

## References
- BIOSCOPE dataset: Vincze et al., 2008
- Negation detection techniques: Yoshida et al., 2024

## License
This project is licensed under the MIT License. See `LICENSE` for more details.
