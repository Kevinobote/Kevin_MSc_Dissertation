# A Novel Kiswahili Audio Processing Pipeline

> An Integrated Approach to Speech Recognition, Sentiment Analysis, and Text Summarization

**Author:** Kevin Omondi Obote  
**Supervisor:** Dr. Betsy Muriithi  
**Institution:** Strathmore University, iLabAfrica  
**Programme:** MSc Data Science and Analytics  
**Date:** January 2026

## Overview

This dissertation presents the design and deployment of an end-to-end Kiswahili audio processing pipeline integrating:

- **Automatic Speech Recognition (ASR)** — Wav2Vec2 fine-tuned for Kiswahili
- **Sentiment Analysis** — Multilingual DistilBERT for transcript-level sentiment classification
- **Abstractive Summarization** — mT5-based summarization of spoken content

## Project Structure

```
├── master-document.tex     # Main LaTeX document (compile this)
├── aimsessay.cls           # AIMS/Strathmore document class
├── chapter1.tex            # Introduction
├── chapter2.tex            # Literature Review
├── chapter3.tex            # Methodology
├── chapter4.tex            # Results and Discussion
├── abstract.tex            # Abstract
├── Declaration.tex         # Declaration of originality
├── acknowledgement.tex     # Acknowledgements
├── abbreviations.tex       # List of abbreviations
├── appendix.tex            # Appendices
├── beamer.tex              # Defence presentation slides
├── references.bib          # Bibliography
├── myabbrvnat.bst          # Custom bibliography style
├── images/                 # Figures and plots
└── code/                   # Source code for the pipeline
```

## Building the Document

### Requirements

- A LaTeX distribution (TeX Live or MiKTeX)
- `pdflatex` and `bibtex`

### Compile

```bash
pdflatex master-document.tex
bibtex master-document
pdflatex master-document.tex
pdflatex master-document.tex
```

Or for the presentation slides:

```bash
pdflatex beamer.tex
```

## Research Objectives

1. Develop a Kiswahili ASR system using self-supervised learning
2. Perform sentiment analysis on speech transcripts
3. Generate abstractive summaries from spoken content
4. Deploy the system as a functional prototype

## Key Results

| Component       | Metric          | Score  |
|-----------------|-----------------|--------|
| ASR             | Best Val. WER   | 0.1068 |
| Sentiment       | F1-score        | 0.0144 |
| Summarization   | ROUGE-L (mT5)  | 0.424  |

## License

This work is submitted in partial fulfillment of the requirements for the Degree of Master of Science in Data Science and Analytics at Strathmore University.
