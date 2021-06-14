# HAHA@IberLEF2021: Humor Analysis using Ensembles of Simple Transformers

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
| Jocoso<sub>[1]</sub>  | **0.8850** | 0.9198            |**0.8526**      | **0.8891**       |
| Jocoso<sub>[2]</sub>  | 0.8826     | 0.9194            | 0.8486         | 0.8871           |
| Jocoso<sub>[3]</sub>  | 0.8822     | 0.9157            | 0.8509         | 0.8863           |
| Jocoso<sub>[4]</sub>  | 0.8791     | 0.9176            | 0.8436         | 0.8840           |
| Jocoso<sub>[5]</sub>  | 0.8777     | **0.9221**        | 0.8373         | 0.8833           |
| Jocoso<sub>[6]</sub>  | 0.8758     | 0.9215            | 0.8343         | 0.8816           | 
| Second Place          | 0.8716     |                   |                |                  |
| Third Place           | 0.8700     |                   |                |                  |
| BETO                  | 0.8687     | 0.9044            | 0.8356         |0.8736            |
| mBERT                 | 0.8561     | 0.9137            | 0.8053         |0.8646            |
| Baseline              | 0.6619     |                   |                |                  |


# Task 2: Regression

Similar to task 1, we use the Simple Transformers classification model,Clas-sificationModelfor this task. However, unlike Task 1, we use it with a regres-sion head i.e. we set the parameterregression = True. We used 6 pretrainedmodels  in  our  final  solution:-  Multilingual  Base  cased  BERT(**mBERT**),**ALBERT** base v2, **RoBERTa** base, **DistilBERT** base cased, **BETO** and **XLNet** base cased model. All these models were fine tunes on the trainingdata for 2 epochs without any preprocessing.

### Task 2 Results

| **Ensembles**.        | **RMSE**   |  
| ---------------       | ------     |
| First Place Solution |  0.6226 | 
| Second Place Solution | 0.6246 | 
| mBERT+ ALBERT + RoBERTa + DistilBERT + BETO + XLNet | **0.6295**|
| BETO + mBERT + ALBERT |  0.6378|
| BETO + DistilBERT | 0.6397|
| BETO + ALBERT |  0.6391|
| BETO + XLNet | 0.6400 |
| BETO + mBERT |  0.6412|
| Fourth Place Solution | 0.6587|
| Baseline | 0.6704|


# Task 3: Multi-class Classification

Our model, with a Macro F1 score of **0.2916**, utilizes BETO to solve thisproblem of multi-class classification. We fine-tuned our model over the trainingcorpus which comprises of approx 4800 tweets for this task.

### Task 3 Results

| **Ensembles**.        | **Macro F1**   |  
| ---------------       | ------     |
| First Place Solution |  0.3396 | 
| BETO - Cased | **0.2916**|
| BETO - Cased + BETO - Uncased | 0.2636|
| Third Place Solution |  0.2522|
| Baseline | 0.1001|


# Task 4: Multi-Label Classification

Our  system  comprises  a  pre-trained  **Spanish  BETO**  cased  model  which  is fine-tuned  for  4  epochs  on  approximately  2000  tweets.  Various  ensembles  andtheir results are listed in the above table.

### Task 4 Results

| **Ensembles**.        | **RMSE**   |  
| ---------------       | ------     |
| First Place Solution | 0.4228 | 
| BETO - Cased, Not Preprocessed  |**0.3578** | 
| BETO - Cased, Preprocessed | 0.3569 | 
| Third Place Solution | 0.3225 | 
| Baseline | 0.0527 |

