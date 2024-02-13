# Detecting Phishing Websites: Machine Learning Approaches for Classification and Feature Extraction

## Contributors:
- Nick Bohm
- Simon Burke
- Yonathan Daniel
- Lara Karacasu
- Vansh Murad Kalia

## Introduction
Phishing attacks are a prevalent issue in the digital age, posing significant threats to internet users worldwide. Our project aims to tackle this issue by utilizing machine learning techniques to distinguish between phishing and genuine websites based on various website characteristics. This README outlines our approach, methodology, data analysis, and the results of our models.

## Data
The `PhishingWebsites` dataset from OpenML.org, originally sourced from the UC Irvine Machine Learning Repository, forms the foundation of our analysis. It encompasses over 11,000 observations with 31 features, including but not limited to the presence of IP addresses, URL length, and SSL certificates. This dataset is balanced across phishing and non-phishing classifications, aiding in the development of an unbiased model.

## Methodology
Our approach involves constructing and evaluating four distinct models:
1. **Decision Tree**
2. **Random Forest**
3. **XGBoost**
4. **Convolutional Neural Network (CNN)**

Each model underwent rigorous training, hyperparameter tuning, and testing to optimize for recall without neglecting overall accuracy. The decision-making process factored in the high cost of false negatives (misidentifying phishing sites as non-phishing), prioritizing recall in our evaluation metrics.

## Model Results

### Decision Tree
Achieved a 96% accuracy and 96% recall on the test set. The model's effectiveness was confirmed through hyperparameter tuning, with SSLfinal_State, URL_of_Anchor, and Links_in_tags emerging as the most critical features.

### Random Forest
Enhanced to mitigate overfitting observed in the Decision Tree model, our Random Forest model demonstrated robust performance with 98% accuracy and recall, emphasizing the importance of SSLfinal_State, URL_of_Anchor, and web_traffic as pivotal features.

### XGBoost
Our XGBoost model, after a detailed hyperparameter optimization, reported a 97% accuracy, with the top predictive features being SSLfinal_State, URL_of_Anchor, and Prefix_Suffix. A subsequent model focusing on the seven most influential features showed a slight decrease in accuracy, underscoring the complexity of feature relationships.

### Convolutional Neural Network (CNN)
The CNN, designed with two 1D convolutional layers followed by max pooling and dropout layers to prevent overfitting, achieved a 95% accuracy on the test set. This model slightly favored precision over recall, aligning with our strategic emphasis on minimizing false negatives.

## Conclusion
Our exploration reveals the Random Forest model as the standout, combining high accuracy with significant recall. The consistency of SSLfinal_State and URL_of_Anchor as top features across models provides valuable insights for future phishing detection efforts. This project not only demonstrates the applicability of machine learning in cybersecurity but also lays groundwork for further research into phishing prevention strategies.
