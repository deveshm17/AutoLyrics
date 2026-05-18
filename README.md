# AUTOLYRICS

AI-powered Singing Voice Transcription using ASR + LoRA Fine-Tuning

---

## Overview

Standard Automatic Speech Recognition (ASR) systems are primarily optimized for spoken language and often perform poorly on singing audio because of:

- Pitch variations
- Prolonged phonemes
- Background instrumentation
- Rhythm and melody distortions

**AUTOLYRICS** transforms an open-source ASR Transformer model into a system capable of generating more accurate lyrics transcriptions from singing audio.

The project improves transcription quality using lightweight fine-tuning techniques such as **LoRA (Low-Rank Adaptation)** and evaluates performance against the original pre-trained baseline.

---

## Features

- Singing voice transcription from short music clips
- LoRA-based parameter-efficient fine-tuning
- HuggingFace Transformer integration
- Audio preprocessing and dataset handling
- Evaluation using WER (Word Error Rate) and CER (Character Error Rate)
- Interactive Gradio demo interface
- Support for custom audio inference

---

## Tech Stack

### Machine Learning
- Python
- PyTorch
- Torchaudio

### Transformers & Fine-Tuning
- HuggingFace Transformers
- HuggingFace Datasets
- PEFT (LoRA)
- BitsAndBytes

### Evaluation & Deployment
- Jiwer
- Gradio

---

## Dataset

The project uses the **SLT Lyrics Audio Dataset** available on Hugging Face:

- https://huggingface.co/datasets/gmenon/slt-lyrics-audio

The dataset contains:
- Singing audio clips
- Corresponding lyric transcriptions
- Audio-text pairs suitable for ASR fine-tuning

The dataset is used for:
- Training
- Validation
- Inference testing
- Evaluating transcription quality using WER/CER metrics

---

## Project Pipeline

1. Load and preprocess singing audio datasets
2. Convert audio into model-compatible features
3. Fine-tune ASR Transformer model using LoRA
4. Evaluate model using WER/CER metrics
5. Run inference on custom music clips
6. Deploy interactive transcription demo using Gradio

---

## Model Training

The notebook includes:

- Dataset preparation
- Audio preprocessing
- Tokenization
- Transformer model loading
- LoRA adapter configuration
- Fine-tuning pipeline
- Evaluation metrics
- Inference testing
