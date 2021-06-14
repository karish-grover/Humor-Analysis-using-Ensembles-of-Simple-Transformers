# HAHA@IberLEF2021

This is the offical repository for the paper **HAHA@IberLEF2021: Humor Analysis using Ensembles of Simple Transformers** by team **Jocoso**.

This paper describes the system submitted to the Humor Analysis based on Human Annotation (HAHA) task at IberLEF 2021. This system achieved the highest results in the main task of binary classification(Task 1) and was based on an ensemble of pre-trained **multilingual BERT**, pre-trained Spanish BERT i.e. **BETO**, a variation of **BETO** finetuned for sentiment analysis, **RoBERTa**, and a naive **Bayes** classifier. Our models achieve the winning F1 Score of **0.8850** in the Binary Classification task, the second place macro F1 Scores of **0.2916** and **0.3578** in Multi-class Classification and Multi-label Classification tasks respectively, and the third place RMSE score of **0.6295** in the Regression task. 

## Competition Details and Data: https://www.fing.edu.uy/inco/grupos/pln/haha/


# Task 1: Binary Classification

The baseline provided bythe organizers for this task uses Naive Bayes with TFIDF features for BinaryClassification of tweets. It achieves an F1 score of **0.6619** over the testing corpus.In the final solution, we tried a series of ensembles of pre-trained models. The model used in the final solution is an ensemble of 5 models.

| **Ensembles Used**                           | **Ensemble ID**     |
| ---------------                              | ---------------     |
| sBERT + mBERT + BETO + RoBERTa + NB          | Jocoso<sub>[1]</sub>|
| sBERT + mBERT + ALBERT + BETO + NB + RoBERTa | Jocoso<sub>[2]</sub>|
| sBERT + mBERT + BETO + NB                    | Jocoso<sub>[3]</sub>|
| sBERT + mBERT +ALBERT + BETO + NB            | Jocoso<sub>[4]</sub>|
| mBERT + BETO + sBERT + DeBERTa               | Jocoso<sub>[5]</sub>|
| mBERT + BETO + ALBERT + sBERT                | Jocoso<sub>[6]</sub>|

### Task 1 Results

| **Ensembles**.        | **F1**     | **Precision**     | **Recall**     | **Accuracy**     |
| ---------------       | ------     | -------------     | ----------     | ------------     |
| Jocoso<sub>[1]</sub>  | **0.8850**     | 0.9198            |** 0.8526**         | **0.8891**           |
| Jocoso<sub>[2]</sub>  | 0.8826     | 0.9194            | 0.8486         | 0.8871           |
| Jocoso<sub>[3]</sub>  | 0.8822     | 0.9157            | 0.8509         | 0.8863           |
| Jocoso<sub>[4]</sub>  | 0.8791     | 0.9176            | 0.8436         | 0.8840           |
| Jocoso<sub>[5]</sub>  | 0.8777     | **0.9221**            | 0.8373         | 0.8833           |
| Jocoso<sub>[6]</sub>  | 0.8758     | 0.9215            | 0.8343         | 0.8816           | 
| Second Place          | 0.8716     |                   |                |                  |
| Third Place           | 0.8700     |                   |                |                  |
| BETO                  | 0.8687     | 0.9044            | 0.8356         |0.8736            |
| mBERT                 | 0.8561     | 0.9137            | 0.8053         |0.8646            |
| Baseline              | 0.6619     |                   |                |                  |
