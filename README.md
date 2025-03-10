# Taskml
1. Preprocessing Steps and Rationale

Data Handling:

              Missing Values: Imputed using the median of each feature.

              Normalization: StandardScaler was applied to ensure all features had zero mean and unit variance.

Data Visualization:

              Spectral Reflectance Visualization: Line plots helped explore trends across wavelengths.

              Heatmaps: Provided insights into correlations between spectral bands.

2. Dimensionality Reduction Insights

             PCA:

              Used to reduce dimensionality while preserving variance.

              Top 2 principal components explained a significant portion of variance, revealing patterns in spectral data.

             t-SNE:

              Used for nonlinear dimensionality reduction.

              Showed clustering patterns that indicated spectral similarities in samples.

3. Model Selection, Training, and Evaluation

                Models Implemented:

                Random Forest Regressor (Baseline model)

                Transformer-based Regressor (with attention mechanism)

                Training Details:

                Train-Test Split: 80% training, 20% testing.

                Random Forest: 100 trees, default hyperparameters.

                Transformer: 2-layer encoder, 64 hidden units, 4 attention heads.

                Optimizer: Adam (learning rate = 0.001)

                Loss Function: Mean Squared Error (MSE)

Model Evaluation:

Model                 Random Forest              Transformer

MAE                      0.24                       0.21

RMSE                     0.36                       0.33

R² Score                 0.82                       0.85

           The Transformer model outperformed Random Forest in all metrics.

           Visualization: Scatter plots showed Transformer predictions were closer to actual values.

4. Key Findings and Suggestions for Improvement

        Key Findings:

              Spectral data effectively predicts DON concentration.

              Transformer-based models captured long-range dependencies better than Random Forest.

       Future Improvements:

              Hyperparameter tuning: Optimize Transformer architecture further.

              More Data: Include additional spectral bands or preprocessing techniques.

              Alternative Models: Explore CNNs or LSTMs for sequence-based spectral data.




Project Overview:

This project predicts DON concentration in corn samples using hyperspectral imaging data. It includes:

Data preprocessing and visualization

Dimensionality reduction (PCA, t-SNE)

Machine learning models (Random Forest, Transformer)

