# HAHA@IberLEF2021

This is the offical repository for the paper **HAHA@IberLEF2021: Humor Analysis using Ensembles of Simple Transformers**.

This paper describes the system submitted to the Humor Analysis based on Human Annotation (HAHA) task at IberLEF 2021. This system achieved the highest results in the main task of binary classification(Task 1) and was based on an ensemble of pre-trained **multilingual BERT**, pre-trained Spanish BERT i.e. **BETO**, a variation of **BETO** finetuned for sentiment analysis, **RoBERTa**, and a naive **Bayes** classifier. Our models achieve the winning F1 Score of **0.8850** in the Binary Classification task, the second place macro F1 Scores of **0.2916** and **0.3578** in Multi-class Classification and Multi-label Classification tasks respectively, and the third place RMSE score of **0.6295** in the Regression task. 

## Competition Details and Data: https://www.fing.edu.uy/inco/grupos/pln/haha/

| Ensembles Used | Ensemble ID |
| sBERT + mBERT + BETO + RoBERTa + NB | Jocoso_{[1]} |

\textbf{Ensembles Used} & \textbf{Ensemble ID}\smallskip\\ % inserts table
%heading
\hline% inserts single horizontal line
Jocoso_{[1]} \, & sBERT + mBERT + BETO + RoBERTa + NB  \\
Jocoso_{[2]} \, & sBERT + mBERT + ALBERT + BETO + NB + RoBERTa \\
Jocoso_{[3]} \, & sBERT + mBERT + BETO + NB \\
Jocoso_{[4]} \, & sBERT + mBERT +ALBERT + BETO + NB \\
Jocoso_{[5]} \, & mBERT + BETO + sBERT + DeBERTa\cite{he2021deberta} + NB \\
Jocoso_{[6]} \, & mBERT + BETO + ALBERT + sBERT  \\ % inserting body of the table
% 2 & 47  \\[0.5ex]
% 3 & 31 \\[0.5ex]
% 4 & 35  \\[0.5ex]
% 5 & 45 \\ [0.5ex] % [1ex] adds vertical space
\hline %inserts single line
\end{tabular}
\label{table:nonlin} % is used to refer this table in the text
\end{table}
