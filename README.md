# DSE511 Project

---

# Vietnamese Pentagram Poem Generation

## Overview
This project demonstrates a **Text Generation** system for creating **Ngũ ngôn poetry** (Vietnamese pentagram poems), using Transformer-based model to generate poetic lines based on an initial prompt.

---

## Features
- **Input**: A pentagram poem phrase consisting of 5 words.
- **Output**: N subsequent lines of poetry, where N is configurable.
- **Applications**:
  - Poetry composition
  - Creative writing assistance
  - Vietnamese NLP exploration

---

## Project Pipeline

![image](https://github.com/user-attachments/assets/5ecd5d39-06b9-447c-9552-9a879a79e5f2)

1. **Data Collection**: Web scraping Vietnamese pentagram poems from [Thivien.net](https://www.thivien.net) using Selenium. Including:
   - Identify target data location

![image](https://github.com/user-attachments/assets/f655039f-779b-411b-9c88-85685cc627fb)
 
   - Create driver

![image](https://github.com/user-attachments/assets/22a498bf-9361-4ed9-ba2a-8a5a8c874360)

   - Access to datatable 
   - Take poem data

2. **Data Preprocessing**:
   - Text normalization (lowercasing, punctuation removal, adding `<start>` and `<end>` tokens).
   - Tokenization and padding.
   - Preparing input-output pairs for training.
3. **Model Implementation**:
   - Transformer architecture with encoder-decoder components.
4. **Training and Evaluation**:
   - Loss: Masked loss to handle padding.
   - Metrics: Masked accuracy, BLEU score, and perplexity.
5. **Inference**: Generate poetry using the trained model.

---

## Training and Evaluation
- **Split**: Training (70%), validation (20%), and test (10%).
- **Optimizer**: Adam with custom learning rate scheduling.
- **Metrics**:
  - **Perplexity**: Evaluates the uncertainty of generated text.
  - **BLEU Score**: Assesses text generation quality by comparing outputs with ground truth.

---

## Prerequisites
- Python 3.8+
- Required Libraries:
  - TensorFlow
  - Selenium
  - Pandas
  - Matplotlib
  - nltk

