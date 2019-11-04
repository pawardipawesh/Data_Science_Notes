# Machine Learning Important concepts
- feature Selection techniques
  - Forward selection
  - Backward Selection
  - Bidirectional Selection
- Feature Reduction Techniques
  - PCA
- Feature Scaling [Link](https://en.wikipedia.org/wiki/Feature_scaling)
  - Min-Max
  - Mean Normalization
  - Standardization (Z-score Normalization)
  - Scaling to unit length
- Sequential Modelling Algorithms
  - HMMs : Generative models - P(X,Y)
  - CRFs: Discriminative models - P(y/x) : (Sequential Version of Logistic Regression) [Link](https://blog.echen.me/2012/01/03/introduction-to-conditional-random-fields/)
    - Linear chain CRFs : Consider only i-1 lable
    - General CRFs
  - RNN 
  - LSTM
  - GRU
- Classical Classification Algorithms
  - Logistic Regression (Its Regression as it outputs probability of class labels)
  - Naive Bayes
  - SVM (can be used only for classification and it directly predicts class labels on the basis of hyperplanes and support vectors)
    - Linear Kernel
    - RBF Kernel
    - Polynomial Kernel
  - Decision Trees (Regression as well as classification)
  - Bag of classifiers (Bagging)
    - Random Forests
  - Boosting Based classifiers
    - XGBoost (Framework known as Xtreme Gradient Boosting)
      - AdaBoost
      - Gradient Boosting
      - Stochastic Gradient Boosting
      - Regularized Gradient Boosting
 - Clustering Techniques
   - K-Means
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
- Evaluation Metrics
  - Accuracy
  - Precision(Specificity), Recall(Sensitivity), F-Measure
  - AUC ROC Curve [Blog](https://towardsdatascience.com/understanding-auc-roc-curve-68b2303cc9c5)
  - AUC PR Curve
# Deep Learning Important Concepts
- Deep Neural Networks
- Activation Fuctions[Derivative Graph](https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6) , [Comaprison](https://en.wikipedia.org/wiki/Activation_function) , [sigmoid Vs Tanh Vs Relu](https://towardsdatascience.com/exploring-activation-functions-for-neural-networks-73498da59b02)
  - Sigmoid/Logit
  - Tanh
  - Relu
  - Leky Relu
  - softmax [Blog1](https://developers.google.com/machine-learning/crash-course/multi-class-neural-networks/softmax) [Blog2](https://medium.com/data-science-bootcamp/understand-the-softmax-function-in-minutes-f3a59641e86d)
- Optimization Algorithms
  - Gradient Descent
  - Stochastic Gradient Descent
  - Momentum
  - RMSProp
  - Adam
- Loss functions [Nice Blog](https://heartbeat.fritz.ai/5-regression-loss-functions-all-machine-learners-should-know-4fb140e9d4b0)
  - Regression
    - Mean,ordinal,Least Square loss/L1 loss/Quadratic loss (Less robust to outliers)
    - Mean Absolute loss/L2 Loss (More robut to outliers)
    - Huber loss/Smooth Mean Absolute Error (Combination of MSE and MAE with a thresold)
    - Log cosh loss
  - Classification [Blog](https://machinelearningmastery.com/loss-and-loss-functions-for-training-deep-learning-neural-networks/)
    - Cross Entropy 
    
     Distance between two distributions. Entropy is measure of uncertainty in a distribution.
      - binary cross entropy loss
      - Categorical cross entropy
- Regularization
  - Dropout
- Sequential learning
  - Recurrent Neural Networks
    - BPTT, TBPTT [Nice answer](https://stats.stackexchange.com/questions/219914/rnns-when-to-apply-bptt-and-or-update-weights)
  - Gated Recurrent Unit (GRU)
  - Long Short Term Memory Networks (LSTMs)
  
    GRU and LSTMs helps in capturing long term dependency(vanishing gradient problem) which RNN can not.
  - Concepts cum Applications
    - Word2Vec
      - CBOW
      - Skipgram
      - Implemented using Hierarchial Softmax, Negative Sampling
    - Glove
- Encoder Decoder Architecture
- Attention Mechanism [Nice Blog](https://towardsdatascience.com/attn-illustrated-attention-5ec4ad276ee3)
- AutoEncoders (Feature Reduction, Selection) [Blog](https://towardsdatascience.com/autoencoders-bits-and-bytes-of-deep-learning-eaba376f23ad)
      
# Important Questions
- Why not approach classification through regression [Link](https://stats.stackexchange.com/questions/22381/why-not-approach-classification-through-regression)
- Linear vs Logistic regression ?
- CRF Vs HMMs?
- What is maximum likelihood estimates?
- What is Expectation-Maximization algorithm (EM Algorithm)? Can it be used for regressiona or classification ? Does it always converge?
- How SVM work? What are kernels in SVM
- Decision Tree globally or locally optimal? How to avoid overfitting in decision trees[good blog](https://www.edupristine.com/blog/decision-trees-development-and-scoring)
- MultiCollinearity ? Why bad ? How to detect? How to handle? [Link](http://www.sfu.ca/~dsignori/buec333/lecture%2016.pdf)
- L1 vs L2 regularization. What are differences? Which is better ? Can they be termed as feature selection or reduction techniques? [Nice Blog](https://towardsdatascience.com/intuitions-on-l1-and-l2-regularisation-235f2db4c261#15c2)
- Optimizations functions in Deep learning ?
- When to use which feature scaling ?
- Similarity measures in Machine learning [Nice blog](https://dataaspirant.com/2015/04/11/five-most-popular-similarity-measures-implementation-in-python/)
- Need of Negative sampling and hierarchial softmax in skip gram based word2vec [Nice Video1](https://www.coursera.org/lecture/nlp-sequence-models/word2vec-8CZiw?authMode=login) [Nice Video2](https://www.coursera.org/lecture/nlp-sequence-models/negative-sampling-Iwx0e)
- Why Weight initialization ways are important in DNN? Vanishing Gradients and Exploding gradients ? [Blog](https://www.dlology.com/blog/how-to-deal-with-vanishingexploding-gradients-in-keras/)
- Why high dimensionality is a curse?
- what is advantage of higher grams and what is their disadvantage? probability of finding higher grams in test set is less.
- Are features also sampled in Random Forest ? what makes them better than Decision trees?
- How to reduce overfitting without regularization(by processing data)
- startegies to handle imbalanced data
- What happens when no. of features are greter than no. of samples?
- Is random weight assignment better than assigning same weights to the units in the hidden layer?
- Integer encoding vs one hot encoding vs dumy encoding. When to use which?[Blog](https://towardsdatascience.com/one-hot-encoding-multicollinearity-and-the-dummy-variable-trap-b5840be3c41a)
- Why we use exponentiation in softmax activation funcion instead can we not just divide logit  by sum of logits?[check why](https://medium.com/data-science-bootcamp/understand-the-softmax-function-in-minutes-f3a59641e86d)
- Why softmax is computationally complex?
- Which is easy Regression or Classification? Why?
- Decision boundry in decision tree?
- Where we can not apply K-means ?
- How to approach classification problem where target variable is ordinal?
- when to choose which optimizer?

# Links To nice resources
- [Google guide] https://developers.google.com/machine-learning/guides
- [Machine Learning Glossary] https://developers.google.com/machine-learning/glossary
