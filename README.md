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

## Setup and Processing

### Processing French Data

If you need to reprocess the French dataset:

```bash
python process_french_data.py
```

This script:
- Loads French LitBank from CSV format
- Splits into train/dev/test (80/10/10)
- Converts to JSON format matching English data
- Creates unified label mapping

### Updating Label Mappings

To ensure both datasets use the same label IDs:

```bash
python update_english_labels.py
```


