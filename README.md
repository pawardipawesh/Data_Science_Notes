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
  - HMMs
  - CRFs [Link](https://blog.echen.me/2012/01/03/introduction-to-conditional-random-fields/)
  - RNN 
  - LSTM
  - GRU
- Classical Classification Algorithms
  _ Logistic Regression (Its Regression as it outputs probability of class labels)
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
  
# Deep Learning Important Concepts
- Deep Neural Networks
- Activation Fuctions
  - Sigmoid
  - Tanh
  - Relu
  - Leky Relu
  - softmax 
- Optimization Algorithms
  - Gradient Descent
  - Stochastic Gradient Descent
  - Momentum
  - RMSProp
  - Adam
- Loss functions
  - binary cross entropy loss
  - mean square error
  - Categorical cross entropy
- Regularization
  - Dropout
- Sequential learning
  - Recurrent Neural Networks
  - Long Short Term Memory Networks (LSTMs)
  - Gated Recurrent Unit (GRU)
  - Concepts cum Applications
    - Word2Vec
      - CBOW
      - Skipgram
        - Hierarchial Softmax
        - Negative Sampling
    - Glove
- Encoder Decoder Architecture
- Attention Mechanism [Nice Blog]{https://towardsdatascience.com/attn-illustrated-attention-5ec4ad276ee3}
- AutoEncoders
      
# Important Questions
- Why not approach classification through regression [Link](https://stats.stackexchange.com/questions/22381/why-not-approach-classification-through-regression)
- Linear vs Logistic regression ?
- What is maximum likelihood estimates?
- What is Expectation-Maximization algorithm (EM Algorithm)? Can it be used for regressiona or classification ? Does it always converge?
- How SVM work? What are kernels in SVM
- Decision Tree globally or locally optimal? How to avoid overfitting in decision trees[good blog](https://www.edupristine.com/blog/decision-trees-development-and-scoring)
- MultiCollinearity ? Why bad ? How to detect? How to handle? [Link](https://www.edupristine.com/blog/detecting-multicollinearity)
- L1 vs L2 regularization. What are differences? Which is better ? Can they be termed as feature selection or reduction techniques? [Nice Blog](https://towardsdatascience.com/intuitions-on-l1-and-l2-regularisation-235f2db4c261#15c2)
- Optimizations functions in Deep learning ?
- When to use which feature scaling ?
- Similarity measures in Machine learning [Nice blog](https://dataaspirant.com/2015/04/11/five-most-popular-similarity-measures-implementation-in-python/)
- Need of Negative sampling and hierarchial softmax in skip gram based word2vec [Nice Video1](https://www.coursera.org/lecture/nlp-sequence-models/word2vec-8CZiw?authMode=login) [Nice Video2]{https://www.coursera.org/lecture/nlp-sequence-models/negative-sampling-Iwx0e}
- Why Weight initialization ways are important in DNN? Vanishing Gradients and Exploding gradients ?
- Why high dimensionality is a curse?
- what is advantage of higher grams and what is their disadvantage? probability of finding higher grams in test set is less.
- Are features also sampled in Random Forest ? what makes them better than Decision trees?
- How to reduce overfitting without regularization(by processing data)
- startegies to handle imbalanced data
- What happens when no. of features are greter than no. of samples?
- Is random weight assignment better than assigning same weights to the units in the hidden layer?
