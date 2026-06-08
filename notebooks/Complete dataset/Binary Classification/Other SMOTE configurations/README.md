# Other SMOTE configurations

Before selecting the final balancing strategies, for the complete dataset, reported in the thesis, several additional SMOTE configurations were evaluated to assess the influence of different balancing ratios on model performance. These experiments were exploratory and are included in the repository for completeness and reproducibility.

## SMOTE ratios

- `Complete_binary_SMOTE_1.0_V2.csv`:
  A fully balanced approach where synthetic samples were generated for the minority class (High Pain) until it reached the same number of observations as the majority class (Low Pain), resulting in a 1:1 class ratio.

- `Complete_binary_SMOTE_0.4_V2.csv`:
  This configuration increased the minority class size to 40% of the majority class size. It was evaluated to determine whether a stronger oversampling strategy than the final selected ratio (0.3) could improve classification performance. However, the obtained results were slightly worse than those achieved with SMOTE 0.3.

## SMOTE with undersampling

- `Complete_binary_SMOTE_0.9_Undersampling_1.0_V2.csv`:
  Following the same balancing strategy later applied to the menstrual dataset, SMOTE was first used to increase the minority class size to 90% of the majority class size. Random undersampling was then applied to the majority class until both classes contained the same number of observations (1:1 ratio).
