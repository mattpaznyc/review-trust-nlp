# From Text to Trust: Classifying Unverified Purchases with NLP

## Project Overview
This project addresses the challenge of fake reviews in e-commerce platforms, which affect approximately 4% of online reviews and influence $152 billion in global online spending. Our goal is to enhance trust in online review systems by accurately identifying verified and unverified feedback using Natural Language Processing (NLP) techniques.

## Problem Statement
The ability for anyone to leave a review on e-commerce platforms, regardless of purchase verification, poses significant challenges to trust in online review systems. This project leverages NLP to identify unverified purchases to enhance decision-making and customer trust in e-commerce.

### Key Objectives:
- Restore trust in the review process
- Protect businesses from misleading feedback
- Improve the overall online shopping experience for consumers

## Dataset
- Source: McAuley Lab, focusing on appliances category reviews
- Dataset Size: 200,000 rows (balanced subset through stratified sampling)
- Distribution Variance: ±0.15% between complete and sample sets
- Features: rating, helpful_vote, title, text, and verified_purchase
- Target Variable: verified purchases (0 for verified, 1 for unverified)
- Class Distribution: Originally 96% verified, 4% unverified

## Features
### NLP-Based Features (71% of total features):
- Part-of-speech counts (nouns, adjectives, verbs)
- Named entity recognition for product/brand mentions
- Review sentiment scores
- Text analysis techniques used:
  - Part-of-speech tagging
  - Sentiment analysis
  - NER techniques

### Additional Features:
- Numeric rating (1-5 stars)
- Helpful votes count

## Methodology
### Handling Class Imbalance
- Implementation: Synthetic Minority Oversampling Technique (SMOTE)
- Sampling Strategy: 0.5 (Minority class increased to 50% of majority class)
- Result: Minority class increased by 1052% while maintaining majority class

### Model Selection and Performance
Three models were evaluated:

1. Random Forest (Best Performer):
   - Overall Accuracy: 86%
   - Verified Purchase Metrics: Precision 88%, Recall 91%, F1 89%
   - Unverified Purchase Metrics: Precision 81%, Recall 75%, F1 78%
   - PR-AUC Score: 0.86

2. Decision Tree:
   - Overall Accuracy: 83%
   - Verified Purchase Metrics: Precision 87%, Recall 88%, F1 88%
   - Unverified Purchase Metrics: Precision 76%, Recall 73%, F1 75%
   - PR-AUC Score: 0.78

3. Logistic Regression:
   - Overall Accuracy: 70%
   - Verified Purchase Metrics: Precision 79%, Recall 76%, F1 77%
   - Unverified Purchase Metrics: Precision 55%, Recall 59%, F1 57%
   - PR-AUC Score: 0.66
