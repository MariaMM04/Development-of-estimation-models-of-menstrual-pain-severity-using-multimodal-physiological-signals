# Development-of-estimation-models-of-menstrual-pain-severity-using-multimodal-physiological-signals
Bachelor's Thesis focused on the classification of menstrual pain intensity using physiological and hormonal variables through statistical analysis and machine learning techniques.

##Repository structure
### Dataset
- `master_tripel_cramps_dataset.csv`: Final dataset used throughout the project.
### Exploratory analysis

#### Box-Whisker Graphs

Box-Whiskers graphs of every studied variable

- Glucose
  - `Glucose Global.ipynb`: Box-Whiskers diagrams for each individual participant presented sequentially, as well as Box-Whisker diagrams of each variable grouped by menstrual phase across all participants
  - `Glucose per id and day.ipynb`: Individual time-series Box-Whisker diagrams showing the values of the specific variable for every participant throughout the study period

- Heart Rate
  - `Heart Rate Global.ipynb`
  - `Heart Rate per id and day.ipynb`
- Menstrual Cycle Hormones: Only has the first type of file since it each individual has only a value per day
  - `Hormones Global.ipynb`
- Temperature
  - `Temperature Global.ipynb`
  - `Temperature Diff from Baseline per id and day.ipynb`

#### Correlation Matrix

Correlation analyses between physiological variables and their p values.

- `correlation_summary_complete_dataset.csv`
- `correlation_summary_menstrual_dataset.csv`

### Supervised machine learning models

All classification experiments are located in the `notebooks` folder.

#### Complete Dataset

- `Complete 6 levels_V2.ipynb`: Six levels pain classification.
- `Complete 3 levels_V2.ipynb`: Three levels pain classification.
- Binary Classification: Two levels pain classification.
  - `README.md`
  - `outer_splits_binary.pkl`: First dataset split (outter split) into five folds with train 80% and test 20%. Used to ensure identical train/test partitions across all evaluated classification schemes and models, allowing a fair comparison of results. 
  - `Complete binary_V2.ipynb`: Binary pain classification without balancing approach
  - `Complete binary_SMOTE_0.3_V2.ipynb`: First balancing approach with SMOTE at 0.3
  - `Complete binary_SMOTE_0.3_Undersampling_0.7_V2.ipynb`: Second balancing approach with SMOTE at 0.3 and undersampling at 0.7
  - `Complete binary_SMOTE_0.3_Undersampling_1.0_V2.ipynb`: Second balancing approach with SMOTE at 0.3 and undersampling at 1.0
  - `Other SMOTE configurations`: Previous approaches with different SMOTE ratios

#### Menstrual Dataset

- `outer_splits_menstrual_binary.pkl`: First dataset split (outter split) into five folds with train 80% and test 20%. Used to ensure identical train/test partitions across all evaluated classification schemes and models, allowing a fair comparison of results.
- `Menstrual binary_V2.ipynb`: Binary pain classification without balancing approach
- `Menstrual binary_SMOTE_V2.ipynb`: First balancing approach with SMOTE at 1.0
- `Mesntrual binary_SMOTE_Undersampling_V2.ipynb`: Second balancing approach with SMOTE at 0.9 and undersampling at 1.0

## Reproducing Machine Learning Models for the Complete dataset

1. Load `master_tripel_cramps_dataset.csv`.
2. Load `outer_splits_binary.pkl`
3. Execute the notebooks inside `notebooks/Complete dataset`
4. Results reported in the thesis can be reproduced from these notebooks.

## Reproducing Machine Learning Models for the Menstrual dataset

1. Load `master_tripel_cramps_dataset.csv`.
2. Load `outer_splits_menstrual_binary.pkl`
3. Execute the notebooks inside `notebooks/Menstrual dataset`
4. Results reported in the thesis can be reproduced from these notebooks.
