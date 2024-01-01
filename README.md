# Ensembling-Correlation
## Ensembling with Correlation Guidance - ECG

<img src="https://cdn-images-1.medium.com/max/1000/1*-IcaYVgZf-0uErY9Lkt9NA.png">

Usually, at the very beginning of the calculations, a part of the training data is separated for the validation data. Validation data has important applications in calculations. Tuning of hyperparameters is done with the help of validation data and it can even be used to determine Ensembling coefficients. But in many cases (for example, Kaggle challenges, etc.) when we want to Ensembling the results of two or more independent calculations, only the results themselves and the score (public score) of each of them are available. So, determining Ensembling coefficients in this case should be based on previous experiences and trial and error method. Even when we want to Ensembling them based on the score (public score), i.e. give more weight to the better scores, we fail very quickly and then in the dark we have to try different coefficients so that we might be lucky and the score Be better than before.

So just as finding the right coefficient for Ensembling is not methodical, even finding two results whose Ensembling can improve the score is also not methodical. That is, for example, Ensembling the best scores is not always successful, and in most cases only by Ensembling some results, the score improves. When the number of answer columns is more than one, the darkness increases. Because it is not known that after finding the right coefficient for Ensembling the first columns, the same coefficient is optimal for Ensembling the next columns.

In other words, in many cases, we are looking for an optimal coefficient for the linear combination of two lists (a pair of lists). But to combine two pairs of lists, we should logically look for two coefficients. That is, for thousands of pairs of lists, we should no longer expect a coefficient to be the best coefficient and the optimal coefficient. Although it is possible to use only two or three coefficients to combine thousands of pairs of lists. Recently, the “Open Problems — Single-Cell Perturbations challenge” was held in Kaggle, which includes the prediction of more than eighteen thousand columns. That is, the issue of Ensembling in these cases becomes very complicated, because if a coefficient is chosen for Ensembling the first column, it cannot be sure that the same coefficient is optimal for more than eighteen thousand other Ensembling. For example, a notebook may have predicted ten thousand columns very well, but not predicted other columns (for any reason) well. When we want to use the results of this notebook for Ensembling, it might be better to use at least two different coefficients.

In this article, we want to share with you the experience of using correlation for Ensembling. Knowing the correlation value of the columns, when you want to Ensembling them, is like the light of a candle in the dark, which can help you to some extent to reach your destination. This article was written in January 2024 by Somayeh Gholami and Mehran Kazeminia.

- You can read this article at the following address:

- https://medium.com/@mehrankazeminia/ensembling-correlation-66605cc0a06d


