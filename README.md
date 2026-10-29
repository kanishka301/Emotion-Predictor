# Emotion Prediction System

A deep learning-based NLP project that predicts emotions expressed in text using a trained **Bidirectional GRU (BiGRU)** model and FastAPI.

## Features

- Classifies text into six emotions: sadness, joy, love, anger, fear, and surprise.
- Performs text preprocessing, tokenization, and sequence padding.
- Compares RNN, LSTM, GRU, and BiGRU architectures.
- Achieves **92.1% test accuracy** with the BiGRU model.
- Integrates the trained model with FastAPI for emotion prediction.
- Returns predicted emotions and confidence scores.

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow, Keras
- **NLP:** Text preprocessing, tokenization, sequence padding
- **Backend:** FastAPI
- **Libraries:** NumPy, Pydantic, Uvicorn
- **Frontend:** HTML, CSS, JavaScript

## Project Structure

```text
Emotion-Predictor/
├── Artifacts/
│   ├── BiGRU_Model.keras
│   └── tokenizer.pkl
├── static/
│   ├── index.html
│   ├── script.js
│   └── style.css
├── main.py
├── notebook.ipynb
├── requirements.txt
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/kanishka301/Emotion-Predictor.git
cd Emotion-Predictor
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the FastAPI server

```bash
uvicorn main:app --reload
```

Open the API documentation in your browser:

`http://127.0.0.1:8000/docs`

## Model Development

The project follows these steps:

1. Text preprocessing and tokenization.
2. Conversion of text into padded numerical sequences.
3. Training and evaluation of RNN, LSTM, GRU, and BiGRU architectures.
4. Selection of BiGRU based on model evaluation.
5. Integration of the trained model and tokenizer with FastAPI for inference.

## Model Performance

| Metric | Result |
|---|---:|
| Test Accuracy | 92.1% |
| Number of Emotion Classes | 6 |

## Future Improvements

- Improve generalization across different text styles and domains.
- Perform detailed per-class precision, recall, and F1-score analysis.
- Add automated tests for prediction endpoints.
- Deploy the model for online inference.
