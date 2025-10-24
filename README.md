# IITM_Deep-Learning_seq2seq-model
Character-level Seq2Seq model for transliterating words from Roman script to Indian languages using the Aksharantar dataset.

# Seq2Seq Transliteration Project

This project implements a character-level sequence-to-sequence (Seq2Seq) model to transliterate words from Roman script (e.g., chat-style typing) to various Indian scripts using a subset of the Aksharantar dataset released by AI4Bharat.

## Features
- Character-level embedding for input Roman script.
- Flexible encoder-decoder architecture (RNN, LSTM, GRU).
- Teacher forcing during training.
- Predicts one character at a time for accurate transliteration.
- Easily adjustable to different Indian languages in the dataset.

## Dataset
- The project uses samples from the Aksharantar dataset.
- Each language folder contains:
  - Training, validation, and test CSVs.
  - Two columns:
    - `transliterated` → Romanized word (source).
    - `original` → Word in target script (target).

## Model Architecture
- Encoder: 1-layer RNN/LSTM/GRU (configurable).
- Decoder: 1-layer RNN/LSTM/GRU (configurable).
- Embedding size: 64 (configurable).
- Hidden state size: 128 (configurable).
- Loss: CrossEntropyLoss.
- Optimizer: Adam.

## Usage
1. Load the dataset from a language folder (e.g., `tam` or `ori`).
2. Preprocess data to create character-level vocabulary.
3. Train the Seq2Seq model.
4. Transliterate new words using the trained model.

```python
# Example usage
transliterate_word("ghar")  # Output depends on target language
```
