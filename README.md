## Identifying Fraudulent Transactions using AI

Credit card fraud poses a significant challenge to businesses and consumers, resulting in substantial financial losses annually. Leveraging machine learning techniques offers a promising avenue for detecting fraudulent transactions, albeit complicated by imbalanced datasets, where legitimate transactions vastly outnumber fraudulent ones.

### Overview
This repository evaluates the efficacy of four machine learning algorithms for credit card fraud detection: K-nearest neighbor (KNN), decision tree, random forest, and XGBoost. The evaluation encompasses both real and synthetic datasets characterized by severe class imbalance, with the latter featuring 91.3% legitimate transactions and 8.7% fraudulent transactions.

### Methodology
The algorithms undergo training via four distinct methodologies to ensure robust evaluation: repeated 5-fold cross-validation, stratified 5-fold cross-validation, random oversampling with stratified 5-fold cross-validation, and SMOTE oversampling with stratified 5-fold cross-validation. Performance assessment is conducted using accuracy, precision, F1-score, ROC value, and recall metrics.

### Results
The findings reveal that XGBoost and Decision Tree models yield the highest accuracy (1.00%), F1-score (1.00%), and recall (1.00%) on the synthetic dataset, showcasing their prowess in fraud detection. Notably, both models exhibit exceptional precision (1.00%), striking a balance between identifying fraudulent transactions and minimizing false positives.

However, performance varies when applied to the real dataset. Among the evaluated models, Random Forest and XGBoost emerge as top performers, demonstrating high accuracy, precision, recall, and F1-score values. These models exhibit robust discriminatory capability, as evidenced by ROC values approaching 1.

### Conclusion
This repository underscores the promise of XGBoost and Decision Tree algorithms for credit card fraud detection. Nonetheless, further validation on diverse datasets is imperative to ascertain their generalizability and robustness. Future research should prioritize evaluating these algorithms across multiple real-world datasets to establish their effectiveness and suitability for integration into fraud detection systems.

Below are some screenshots of the web interface that illustrate system performance in identifying fraudulent and non-fraudulent data. The first screenshot shows the system's reaction when entering non-fraudulent data and correctly identifies it as non-fraudulent. Conversely, the second screenshot shows the system's reaction to entering fraudulent data and correctly classifies it as fraudulent. These screenshots serve as visual evidence of the system's effectiveness in distinguishing between fraudulent and non-fraudulent data.

![FDS2](https://github.com/hastikacheddy/Identifying_Fraudulent_Transactions_using_AI/assets/59787014/284d2b8e-7dc2-4d69-b878-88a6c13f5c1f)


![FDS1](https://github.com/hastikacheddy/Identifying_Fraudulent_Transactions_using_AI/assets/59787014/79c17ba4-b015-4c79-938f-11d3bb0dac72)




