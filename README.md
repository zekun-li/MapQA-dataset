
# Open-domain Geospatial Question Answering on Map Data
<img width="434" alt="logo1" src="https://github.com/user-attachments/assets/e6c75371-1c7e-42df-a9f1-ecdb5ca8f27c" />



## Overview
This dataset is designed for geospatial question answering (QA) tasks and contains data for two different approaches:
1. **Retrieval-based approach** (stored in the `retrieval/` directory)
2. **Large Language Model (LLM)-based approach** (stored in the `llm/` directory)

Each approach includes data for two study regions: **California** and **Illinois**.

## Dataset Structure
```
github-dataset/
│── llm/
│   ├── california_full/
│   │   ├── question-answer/
│   │   │   ├── adjacent_dataset.csv
│   │   │   ├── adjacent_dataset.json
│   │   │   ├── amenities-around-specific.csv
│   │   │   ├── amenities-around-specific.json
│   │   │   ├── amenities_around_dataset.csv
│   │   │   ├── amenities_around_dataset.json
│   │   │   ├── amenities_dataset.csv
│   │   │   ├── amenities_dataset.json
│   │   │   ├── compare-closer.csv
│   │   │   ├── compare-closer.json
│   │   │   ├── direction_nearest_dataset.csv
│   │   │   ├── direction_nearest_dataset.json
│   │   │   ├── distance_dataset.csv
│   │   │   ├── distance_dataset.json
│   │   │   ├── intersection_dataset.csv
│   │   │   ├── intersection_dataset.json
│   │   │   ├── nearest_amenity_dataset.csv
│   │   │   ├── nearest_amenity_dataset.json
│   │   ├── amenities.csv
│   │   ├── entities.csv
│   ├── illinois_test/
│   │   ├── question-answer/
│   │   ├── amenities.csv
│   │   ├── entities.csv
│
│── retrieval/
│   ├── california/
│   │   ├── train/
│   │   │   ├── train_socal_dpr_cased_amenity.json
│   │   │   ├── train_socal_dpr_cased_entity.json
│   │   ├── test/
│   │   │   ├── test_socal_dpr_cased_adjacent.json
│   │   │   ├── test_socal_dpr_cased_amenities.json
│   │   │   ├── test_socal_dpr_cased_amenities_around.json
│   │   │   ├── test_socal_dpr_cased_amenities_around_specific.json
│   │   │   ├── test_socal_dpr_cased_compare_closer.json
│   │   │   ├── test_socal_dpr_cased_direction_nearest.json
│   │   │   ├── test_socal_dpr_cased_nearest_amenity.json
│   ├── illinois/
│   │   ├── test/
│   │   │   ├── test_il_dpr_cased_adjacent.json
│   │   │   ├── test_il_dpr_cased_amenities.json
│   │   │   ├── test_il_dpr_cased_amenities_around.json
│   │   │   ├── test_il_dpr_cased_amenities_around_specific.json
│   │   │   ├── test_il_dpr_cased_compare_closer.json
│   │   │   ├── test_il_dpr_cased_direction_nearest.json
│   │   │   ├── test_il_dpr_cased_nearest_amenity.json
```


## Contents
### LLM-Based Approach (`llm/`)
- **question-answer/**: Contains multiple CSV and JSON files with geospatial QA pairs categorized into nine different types.
- **amenities.csv**: Contains a list of amenities relevant to the study region.
- **entities.csv**: Contains a list of geospatial entities relevant to the study region.

### Retrieval-Based Approach (`retrieval/`)
- **train/**: Contains training data formated for the retrieval-based approach, the question-answer pairs are the same as in the `llm` folder.
- **test/**: Contains test data used to evaluate the retrieval-based approach.

## Statistics
The final dataset consists of 3,154 question-answer pairs categorized into 9 types. For the Southern California region, which includes 2,206 pairs, we divide 80% of them into training samples and 20% into testing samples. During model training, the training samples were further split into train and validation sets with an 80/20 ratio. The Illinois region serves as the zero-shot learning evaluation set, containing a total of 948 samples.

