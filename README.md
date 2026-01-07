# Multilingual Named Entity Recognition on LitBank

## Overview

This project fine-tunes a multilingual transformer model (XLM-RoBERTa) on English and French LitBank datasets for Named Entity Recognition, enabling multilingual training and cross-lingual transfer evaluation.

## Notebooks

- Data loading and preprocessing: `notebooks/01_data_preprocessing.ipynb`
- Tokenization and model training: `notebooks/02_model_training.ipynb`
- Multilingual evaluation: `notebooks/03_multilingual_evaluation.ipynb`

## Datasets

This project uses multilingual **LitBank** datasets:

### English LitBank
- Literary fiction from Project Gutenberg
- 100 novels with NER annotations (~210,000 tokens)
- Source: [LitBank GitHub](https://github.com/dbamman/litbank)

### French LitBank
- French literary texts with NER annotations
- 18 documents (~235,000 tokens)
- Converted from BRAT format to BIO tagging

## Entity Types

Both datasets use a unified label schema with 7 entity types:

- **PER**: Person (characters, authors)
- **LOC**: Location (cities, regions)
- **GPE**: Geo-Political Entity (countries, states)
- **ORG**: Organization (companies, institutions)
- **FAC**: Facility (buildings, structures)
- **VEH**: Vehicle (ships, cars)
- **TIME**: Time expressions (French only, but included in unified schema)

Note: The TIME entity type appears only in the French dataset but is included in the unified label mapping to enable potential cross-lingual transfer.


