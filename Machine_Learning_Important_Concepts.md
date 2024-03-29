# Machine Learning Important concepts
- Feature Selection techniques
  - Forward selection
  - Backward Selection
  - Bidirectional Selection
- Feature Reduction Techniques
  - PCA  [Nice Blog](https://towardsdatascience.com/a-one-stop-shop-for-principal-component-analysis-5582fb7e0a9c)
    
    Eigen Vectors of covarince matrix(Z*transpose(Z)): computed as covarince matrix=P*D*inverse(P), P is eigen vector matrix(column wise) and D is eigen value matrix....Eigen value denote importance of corresponding eigen vector. Now transform input feature matrix using these eigen vectors and that transoformed matrix is the one with principal components for our input.
    
- Feature Scaling [what](https://en.wikipedia.org/wiki/Feature_scaling) [Effects of Diffrent Scaling methods on various algos](https://towardsdatascience.com/normalization-vs-standardization-quantitative-analysis-a91e8a79cebf)
  - Min-Max
  - Mean Normalization
  - Standardization (Z-score Normalization)
  - Scaling to unit length
- Sequential Modelling Algorithms
  - HMMs : Generative models - P(X,Y)
  - CRFs: Discriminative models - P(y/x) : (Sequential Version of Logistic Regression) [Link](https://blog.echen.me/2012/01/03/introduction-to-conditional-random-fields/)
    - Linear chain CRFs : Consider only i-1 lable
    - General CRFs
- Generative Models
  - Naive Bayes
  - HMMs
  - EM Algorithm
  - LDA 
    
    How we reassign a word to new topic t, after initial random assignment of words to K(given no) topics, is P(topic t/document d)*P(word/topic t)
- Discriminative Models
  - Logostics/Linear Regression
  - Neural networks
  - Decision Trees
- [Generative Models vs Discriminative Models](https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3)
- Generative Models performs better when there is noise in data as discriminative model in such cases may get overfitted if say data size is less or regularization is not done or due to some other reason. Discriminative Models almost always prform better in classification tasks.
- [joint-probability-vs-conditional-probability](https://medium.com/@mlengineer/joint-probability-vs-conditional-probability-fa2d47d95c4a)
  - RNN 
  - LSTM
  - GRU
- Classical Classification Algorithms
  - Logistic Regression (Its Regression as it outputs probability of class labels)
  - Naive Bayes [Very Nice Blg](https://monkeylearn.com/blog/practical-explanation-naive-bayes-classifier/)
    
    It takes less time in training as just calculates joint probabilities during training
  - SVM (can be used only for classification and it directly predicts class labels on the basis of hyperplanes and support vectors)
    - Linear Kernel
    - RBF Kernel
    - Polynomial Kernel
  - Decision Trees (Regression as well as classification) [Nice Blog](https://medium.com/@rishabhjain_22692/decision-trees-it-begins-here-93ff54ef134)
    - Classification
      - Gini Index
      - Entropy
    - Rgression 
      - Reduction in Variance
  - Bag of classifiers (Bagging)
    - Random Forests
  - Boosting Based classifiers
    - how samples are weighted
      - weighted sampling
      - rejection sampling
    - how decision is made 
      - weighted avergaing (classifiers are weighted on the basis of their performance)
    - XGBoost (Framework known as Xtreme Gradient Boosting) [Blog](https://medium.com/analytics-vidhya/what-makes-xgboost-so-extreme-e1544a4433bb)
      - AdaBoost
      - Gradient Boosting
      - Stochastic Gradient Boosting
      - Regularized Gradient Boosting
  - Bagging Vs Boosting (https://quantdare.com/what-is-the-difference-between-bagging-and-boosting/)
 - Clustering Techniques
   - K-Means [Nice Blog](https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a)
     - No Of Clusters [Nice lecture](https://www.coursera.org/lecture/ml-clustering-and-retrieval/assessing-the-quality-and-choosing-the-number-of-clusters-JVWne)
        - Elbow method (no of clusters vs hetrogeneity (Sum of within cluster distances))
        - Silhouette analysis
     - Initialization algorithms
        - KMeans++ [Nice leacture](https://www.coursera.org/lecture/ml-clustering-and-retrieval/smart-initialization-via-k-means-T9ZaG)
   - K-medoid
   - DBSCAN
   - Agglomerative
   - Divisive
   - Genetic Algorithms
- Regularization
  - L1 regularization
  - L2 Norm
- Similarity measures [Nice blog](https://www.kaggle.com/residentmario/l1-norms-versus-l2-norms)
  - Euclidian distance(L2 Norm)
  - Manhattan Distance(L1 Norm)
- MultiLable classification[Nice blog](https://towardsdatascience.com/journey-to-the-center-of-multi-label-classification-384c40229bff)
- Handling Imbalanced Datasets
  - Undersampling
    - Random
    - Informative
      - Easy Ensemble(learn multiple classifiers such that each of them is exposed to all minority samples but undersampled majority ones)
      - Balance cascade
    
    Disadvantage: Information loss
  - Oversampling
    - Random
    - Informative
    - Synthetic minority oversampling Technique (SMOTE)
    
    Advantage: No Information loss
    
    Disadvantage : Overfitting as we replicate
  - Cost sensitive learning ( More cost for misspredictions of minority class)
- Categorical Feature Encoding[Nice Blog](https://towardsdatascience.com/all-about-categorical-variable-encoding-305f3361fd02)
- Evaluation Metrics
  - Accuracy
  - Precision(Specificity), Recall(Sensitivity), F-Measure
  - multi-class classification
    - macro(class level, balanced class distribution), micro(instance level, class imbalance), weighted precision, recall and F-measure
  - AUC ROC Curve [Blog](https://towardsdatascience.com/understanding-auc-roc-curve-68b2303cc9c5)
  - AUC PR Curve
    - [AUC ROC vs AUC PR](http://www.chioka.in/differences-between-roc-auc-and-pr-auc/)
  - R2 (regression scoring) [check](https://scikit-learn.org/stable/modules/model_evaluation.html#r2-score)
  - bias vs variance [Blog](https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229) [Very Nice Blog](https://towardsdatascience.com/two-important-machine-learning-concepts-to-improve-every-model-62fd058916b)
- How to evaluate
  - cross validation
    - Hold out cv
    - k-fold cv
    - leave one out cv
    
    LOOCV model will have high variance meaning results of LOOCV mzy vary alot if you retrain the model wih same hyperparameter on some other data points for same problem. This happens because train set will have hghest overlap as compared to other CV techniques in LOOCV. [captain_ahab answer](https://stats.stackexchange.com/a/244112/129463)
