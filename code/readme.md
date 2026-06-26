
# Kiswahili Audio Processing Pipeline  
**An Integrated System for Speech Recognition, Sentiment Analysis, and Text Summarization**

## Overview
This repository contains the complete implementation of the dissertation research project:

**A Novel Kiswahili Audio Processing Pipeline: An Integrated Approach to Speech Recognition, Sentiment Analysis, and Text Summarization**

The project presents an end-to-end pipeline that transforms raw Kiswahili audio into structured insights using Automatic Speech Recognition (ASR), Sentiment Analysis, and Automatic Text Summarization. The system is designed with modularity, ethical responsibility, and deployability in mind, particularly for low-resource language settings.

## Research Objectives
- Design an end-to-end Kiswahili audio processing pipeline
- Transcribe speech using transformer-based ASR models
- Perform sentiment analysis on transcribed text
- Generate abstractive summaries from long-form speech
- Analyze errors, biases, and ethical implications
- Provide an API-ready architecture for deployment

---

## System Pipeline
The complete data flow of the system is as follows:

```

Raw Audio
↓
Validation
↓
Chunking (if required)
↓
Automatic Speech Recognition (ASR)
↓
Text Processing & Normalization
↓
Sentiment Analysis & Summarization
↓
Aggregation
↓
Structured JSON Response

```

---

## Repository Structure
```

.
├── data/
│   ├── raw/                  # Raw audio inputs
│   ├── processed/            # Cleaned and resampled audio
│   └── metadata/             # Speaker demographics and annotations
│
├── notebooks/
│   ├── exploratory_analysis.ipynb
│   ├── demographic_bias_analysis.ipynb
│   └── error_analysis.ipynb
│
├── src/
│   ├── audio_preprocessing.py
│   ├── asr.py
│   ├── text_processing.py
│   ├── sentiment.py
│   ├── summarization.py
│   ├── aggregation.py
│   └── utils.py
│
├── api/
│   ├── main.py               # FastAPI entry point
│   ├── schemas.py            # Pydantic data models
│   └── routes.py
│
├── experiments/
│   ├── asr_evaluation.py
│   ├── sentiment_evaluation.py
│   └── summarization_metrics.py
│
├── requirements.txt
├── README.md
└── LICENSE

````

---

## Models Used

### Automatic Speech Recognition (ASR)
- Transformer-based pretrained speech model
- Multilingual training with Kiswahili support
- Evaluated using Word Error Rate (WER)

### Sentiment Analysis
- Multilingual DistilBERT fine-tuned on English sentiment data
- Applied via cross-lingual transfer learning
- Outputs sentiment polarity and confidence scores

### Text Summarization
- Transformer-based abstractive summarization
- Chunk-based summarization for long transcripts
- Evaluated using ROUGE metrics

---

## Evaluation Metrics

### Word Error Rate (WER)
\[
\text{WER} = \frac{S + D + I}{N}
\]
Where:
- \(S\) = Substitutions  
- \(D\) = Deletions  
- \(I\) = Insertions  
- \(N\) = Total reference words  

### Summarization Metrics
- ROUGE-1
- ROUGE-2
- ROUGE-L

### Sentiment Analysis
- Prediction distribution
- Confidence score analysis
- Qualitative error inspection

---

## Ethical Considerations
- Dataset demographic imbalance
- Socio-linguistic bias risks
- Cross-cultural sentiment interpretation limitations

The study emphasizes transparency, bias awareness, and responsible deployment in real-world systems.

---

## Installation

### Requirements
- Python ≥ 3.9
- FFmpeg
- CUDA-enabled GPU (recommended)

### Setup
```bash
git clone https://github.com/your-username/kiswahili-audio-pipeline.git
cd kiswahili-audio-pipeline
pip install -r requirements.txt
````

---

## Running the Pipeline

### Local Execution

```bash
python src/audio_preprocessing.py
python src/asr.py
python src/sentiment.py
python src/summarization.py
```

### API Deployment

```bash
uvicorn api.main:app --host 0.0.0.0 --port 8000
```

Example API response:

```json
{
  "transcription": "…",
  "sentiment": "Positive",
  "summary": "…",
  "confidence": 0.87
}
```

---

## Reproducibility

* Fixed random seeds
* Version-controlled scripts
* Documented preprocessing and evaluation steps
* Deterministic experiment setup

---

## Limitations

* Demographic bias in speech data
* Cross-lingual sentiment transfer constraints
* Reduced performance on long-form audio

These limitations are discussed extensively in the dissertation.

---

## Citation

```bibtex
@mastersthesis{Obote2025,
  title={A Novel Kiswahili Audio Processing Pipeline: An Integrated Approach to Speech Recognition, Sentiment Analysis, and Text Summarization},
  author={Obote, Kevin Omondi},
  year={2025},
  school={Strathmore University}
}
```

---

## Author

**Kevin Obote Omondi**
MSc Data Science and Analytics
Strathmore University

**Supervisor:** Dr. Betsy Muriithi

---

## License

This project is released for academic and research use. See the `LICENSE` file for details.
