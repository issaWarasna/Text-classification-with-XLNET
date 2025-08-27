# Text Classification with XLNet

This project demonstrates how to **classify text into emotions** using a **pre-trained XLNet model**. The model is fine-tuned on a custom dataset to predict **four emotions**: **anger, fear, joy, and sadness**.

## Project Overview

The goal is to **analyze text** and determine the underlying emotion.  
We use **XLNet**, a state-of-the-art transformer model, pre-trained on large amounts of text and fine-tuned for classification tasks.  

The workflow includes:
1. **Data preprocessing**: Cleaning text (removing mentions, special characters, etc.)  
2. **Label encoding**: Converting emotion labels to numeric IDs for the model  
3. **Dataset balancing**: Ensuring each emotion has an equal number of examples  
4. **Tokenization**: Converting text into token IDs that XLNet can process  
5. **Model fine-tuning**: Training XLNet on your dataset with HuggingFace `Trainer`  
6. **Evaluation**: Measuring accuracy on unseen validation data  
7. **Prediction**: Using a ready-to-use pipeline to classify new text samples  

## Model Details

- **Model**: `XLNetForSequenceClassification`  
- **Pre-trained checkpoint**: `xlnet-base-cased`  
- **Number of classes**: 4 (anger, fear, joy, sadness)  
- **Tokenizer**: `XLNetTokenizer` (cased)  
- **Framework**: PyTorch with HuggingFace Transformers  

## Usage

1. Prepare and preprocess your dataset.  
2. Split your dataset into **train, validation, and test sets**.  
3. Tokenize the text using XLNet tokenizer.  
4. Fine-tune XLNet using HuggingFace `Trainer`.  
5. Evaluate model accuracy on validation/test sets.  
6. Use the trained model to predict emotions for new text.  

## Summary

This repository provides a complete pipeline for **emotion detection in text** using a transformer model. It’s suitable for experiments, fine-tuning on custom datasets, or as a baseline for NLP emotion classification tasks.
