# Transformer-based Named Entity Recognition on LitBank

## Overview

This project fine-tunes a multilingual transformer model (XLM-RoBERTa) on the LitBank dataset for Named Entity Recognition, then evaluates its performance on cross-lingual transfer tasks. This branch contains the baseline test of training a pre-trained transformer model on the English LitBank dataset to obtain first results (to compare with the results of BiLSTM training with the same dataset)

## Notebooks

- Data loading and preprocessing: `notebooks/01_data_preprocessing.ipynb`
- Tokenization and model training: `notebooks/02_model_training.ipynb`
- Evaluation: `notebooks/03_multilingual_evaluation.ipynb`

## Dataset

This project uses the **LitBank** dataset:
- Literary fiction from Project Gutenberg
- ~100 novels with NER annotations (~200'000 tokens)
- Download: [LitBank GitHub](https://github.com/dbamman/litbank)



