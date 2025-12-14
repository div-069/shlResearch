# Grammar Scoring Engine – SHL Intern Hiring Assessment 2025

This project implements an end-to-end grammar scoring engine for spoken English audio as part of the SHL Intern Hiring Assessment 2025 Kaggle competition. The objective is to predict a continuous grammar score between 0 and 5 for each audio sample based on the perceived grammatical quality of speech.

The dataset consists of spoken audio recordings with durations between 45 and 60 seconds. The training set contains 409 audio samples with ground truth grammar scores, while the test set contains 197 audio samples without labels. All audio files are provided in WAV format, and accompanying CSV files contain audio filenames and labels for training.

As a preprocessing step, all audio files are loaded and resampled to a sampling rate of 16 kHz to ensure consistency across samples. Mel Frequency Cepstral Coefficients (MFCCs) are extracted from each audio file to capture important acoustic and speech characteristics relevant to grammar and fluency. A total of 40 MFCC features are computed per audio sample, and temporal mean pooling is applied to obtain a fixed-length feature representation.

A regression-based modeling approach is used to predict grammar scores. A Random Forest Regressor is trained on the extracted MFCC features due to its robustness and ability to model non-linear relationships in small to medium-sized datasets. Model performance is evaluated using Root Mean Squared Error (RMSE), which is mandatory for the competition, and Pearson correlation, which aligns with the leaderboard evaluation metric. Relevant evaluation results and visualizations are included in the notebook for interpretability.

The final submission is a CSV file containing predicted grammar scores for all test audio samples in the required format with a header and exactly 197 rows. This project focuses on building a clean, interpretable, and reproducible baseline solution that satisfies the competition requirements and hiring evaluation criteria.

