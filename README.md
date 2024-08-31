# Conflict_Model_Predictor
# Background 
Since the 1990s, conflicts in Africa have evolved from civil wars, such as in Rwanda and Liberia, to insurgencies driven by groups like Boko Haram and Al-Shabaab. Communal violence, political unrest, and terrorism have further destabilized regions, with ethnic tensions and resource competition fueling conflicts in places like South Sudan, Ethiopia, and the Sahel. These conflicts have shifted towards asymmetric warfare, targeting civilians, and expanding across borders. A conflict predictor using ACLED data would help governments, security agencies, and humanitarian organizations anticipate violence, allocate resources effectively, and design informed peacebuilding strategies, enabling proactive intervention and crisis prevention.
ACLED Dataset Overview

The ACLED (Armed Conflict Location & Event Data) dataset above provides detailed information on conflict events, including the following key columns:

- **Event ID**: Unique identifier for each event.
- **Event Date**: Date when the event occurred.
- **Event Type**: Category of the event (e.g., battles, protests, riots, explosions).
- **Sub-event Type**: Detailed event type description (e.g., armed clashes, peaceful protests).
- **Actor 1**: Primary actor involved (e.g., government forces, rebel groups).
- **Actor 2**: Opposing or secondary actor (if applicable).
- **Inter1 & Inter2**: Codes representing actor types (e.g., state forces, civilians).
- **Country**: Country where the event took place.
- **Region**: Geographic region (e.g., East Africa, Southern Africa).
- **Location**: Specific city or area where the event occurred.
- **Latitude & Longitude**: Coordinates for mapping the event.
- **Fatalities**: Number of deaths reported due to the event.

![image](https://github.com/user-attachments/assets/6c78c215-e486-4ea4-b246-d63a98f52162)

![image](https://github.com/user-attachments/assets/51ffcbe0-8698-4da6-8dc2-efffe5a35e3a)

Insights
The bar chart shows regional disparities in the number of events across Africa. Eastern Africa has the highest count, nearing 120,000, indicating the most activity, followed by Western and Northern Africa with around 80,000 events each. Middle Africa shows moderate activity with just over 60,000 events, while Southern Africa has the lowest at approximately 40,000. This suggests Eastern Africa requires more focus, while Southern Africa might be under-represented or less active.
![image](https://github.com/user-attachments/assets/cd5e3409-32ee-4780-ae85-8badc0f9aedc)
Comparison of Logistic Regression vs Polynomial Feature Improvement:
Accuracy:

Logistic Regression: 0.71
Polynomial Features: 0.56
Recommendation: The logistic regression model has significantly better accuracy (0.71 vs. 0.56), making it more reliable for overall predictions.
Class-wise Precision, Recall, and F1-scores:

Riots:

Logistic Regression: Precision = 0.62, Recall = 0.80, F1-score = 0.70
Polynomial: Precision = 0.50, Recall = 0.80, F1-score = 0.62
Recommendation: Both models have similar recall, but logistic regression has better precision and F1-score, making it preferable for this class.
Battles:

Logistic Regression: Precision = 0.38, Recall = 0.02, F1-score = 0.03
Polynomial: Precision = 0.24, Recall = 0.01, F1-score = 0.02
Recommendation: Both models perform poorly here, but logistic regression has slightly better precision and F1-score.
Strategic Developments:

Logistic Regression: Precision = 0.85, Recall = 0.92, F1-score = 0.89
Polynomial: Precision = 0.68, Recall = 0.88, F1-score = 0.77
Recommendation: Logistic regression outperforms polynomial features significantly, especially in precision and F1-score.
Violence Against Civilians:

Logistic Regression: Precision = 0.64, Recall = 0.22, F1-score = 0.33
Polynomial: Precision = 0.33, Recall = 0.13, F1-score = 0.18
Recommendation: Logistic regression performs much better in precision and recall, making it preferable for this class.
Protests:

Logistic Regression: Precision = 1.00, Recall = 1.00, F1-score = 1.00
Polynomial: Precision = 0.00, Recall = 0.00, F1-score = 0.00
Recommendation: The polynomial model fails entirely for this class, while logistic regression handles it perfectly.
Explosions/Remote Violence:

Logistic Regression: Precision = 0.62, Recall = 0.73, F1-score = 0.67
Polynomial: Precision = 0.54, Recall = 0.54, F1-score = 0.54
Recommendation: Logistic regression again outperforms polynomial features, especially in recall and F1-score.

Random forest is a powerful capture of complex and non-linear relationships between features, which is especially helpful when the relationship between the conflict types. Additionally, it can help with feature importance by identifying factors most influential in predicting conflict types. Most importantly, it aids with multiclass flexibility, which benefits this classification problem with multiple conflict types.
