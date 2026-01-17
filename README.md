# Multilingual Named Entity Recognition on LitBank

## Overview

This project fine-tunes a multilingual transformer model (XLM-RoBERTa) on English, French and Italian LitBank datasets for Named Entity Recognition (literary texts), enabling multilingual training and cross-lingual transfer evaluation.

## Notebooks

- Data loading and preprocessing: `notebooks/01_data_preprocessing.ipynb`
- Tokenization and model training: `notebooks/02_model_training.ipynb`
- Multilingual evaluation: `notebooks/03_multilingual_evaluation.ipynb`

## Datasets

This project uses three separate **LitBank** datasets that follow roughly the same annotation schema:

### English LitBank
- 100 novels with NER annotations (~210'000 tokens)
- Available from Hugging Face datasets
- Source: [LitBank GitHub](https://github.com/dbamman/litbank)

### French LitBank
- 17 novels with NER annotations (~235'000 tokens)
- Converted from BRAT format to BIO tagging
- Source: [fr-litbank](https://github.com/lattice-8094/fr-litbank/tree/main)

### Italian LitBank
- 87 works with NER annotations (~260'000 tokens)
- Converted from BRAT format to BIO tagging
- Source: [Italian LitBank](https://github.com/maxdgen/italian-litbank/)

## Entity Types
All datasets use a unified label schema with 7 entity types:

- **PER**: Person (characters, authors)
- **LOC**: Location (cities, regions)
- **GPE**: Geo-Political Entity (countries, states)
- **ORG**: Organization (companies, institutions)
- **FAC**: Facility (buildings, structures)
- **VEH**: Vehicle (ships, cars)
- **TIME**: Temporal and historical references (morning, Christmas day)

Note: Some of the additional entity types in the French dataset with respect to the other datasets were mapped (e.g. NO_PER -> PER) or dropped if considered irrelevant or too rare. The TIME entity type, which also includes the mapped HIST tags (both temporal references) appears only in the French dataset but is included in the unified label mapping to enable potential cross-lingual transfer. 


