# Deep Learning Important Concepts
- Deep Neural Networks
- Activation Fuctions[Derivative Graph](https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6) , [Comaprison](https://en.wikipedia.org/wiki/Activation_function) , [sigmoid Vs Tanh Vs Relu](https://towardsdatascience.com/exploring-activation-functions-for-neural-networks-73498da59b02)
  - Sigmoid/Logit
  - Tanh
  - Relu
  - Leky Relu
  - softmax [Blog1](https://developers.google.com/machine-learning/crash-course/multi-class-neural-networks/softmax) [Blog2](https://medium.com/data-science-bootcamp/understand-the-softmax-function-in-minutes-f3a59641e86d)
- Optimization Algorithms[Very Nice Blog](https://towardsdatascience.com/understanding-rmsprop-faster-neural-network-learning-62e116fcf29a)
  - Gradient Descent
  - Stochastic Gradient Descent
  - GD with Momentum
  - RProp (Does not work well with mini batches)
  - RMSProp(Divide with explonential weighted avraged gradient and multiple with current gradient)
  - Adam
- Loss functions [Nice Blog](https://heartbeat.fritz.ai/5-regression-loss-functions-all-machine-learners-should-know-4fb140e9d4b0)
  - Regression
    - Mean,ordinal,Least Square loss/L2 loss/Quadratic loss (Less robust to outliers)
    - Mean Absolute loss/L1 Loss (More robut to outliers)
    - Huber loss/Smooth Mean Absolute Error (Combination of MSE and MAE with a thresold)
    - Log cosh loss
  - Classification [Blog](https://machinelearningmastery.com/loss-and-loss-functions-for-training-deep-learning-neural-networks/)
    - Cross Entropy(log loss) [Nice Blog](https://towardsdatascience.com/understanding-binary-cross-entropy-log-loss-a-visual-explanation-a3ac6025181a)
     Distance between two distributions. Entropy is measure of uncertainty in a distribution.
      - binary cross entropy loss
      - Categorical cross entropy
    - KL Divergence
      -  [Nice Blog](https://www.countbayesie.com/blog/2017/5/9/kullback-leibler-divergence-explained) 
- Batch Normalization vs Layer Normalization(Normalize hidden layer input)[Nice Blog](https://www.pinecone.io/learn/batch-layer-normalization/#:~:text=Batch%20Normalization%20vs%20Layer%20Normalization&text=Batch%20normalization%20normalizes%20each%20feature,effective%20for%20small%20batch%20sizes.)
  - How : standard Normalization with Learnable parameters
  - Why : if input distribution changes a lot(coveriate shift), retraining is needed. To avooid this and make netwrk more robust Batch Normalization.
  - Whats the difference between input normalization vs batch normalization.
  - Is batch normalization applied mean and standard deviation across features or independently for each feature
  - Which mean and standard dev are used while scroing for normalization
  - Whats the difference between batch and layer norm ?
  - What are learnable parameters used in batch norm ? How they are set for first batch ?
  - Where does batch norm is used and where layer norm is used ?
- Regularization
  - Dropout
  - Batch Normalization 
  - Early Stopping
  - Weight constraint
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
- Vanishing Gradient Problem
  - why : In sigmoid, Tanh activations, drivative ranges from 0-0.25 and 0-1 with normal distribution, derivative is very small after some -ve and +ve values. Also as we go in earlier layers gradients become even smaller due to multiple multiplications.
  - how to handle : Relu Activation....TBPTT....Careful Weight initialization
- Exploading gradient problem
  - why: gradient accumalate, must be happening mostly with Relu, and explode as they pass towards input layers. causes overflow and hence NANs
  - How to handle: gradients clipping, careful weight initialization
  
- Encoder Decoder Architecture
- Attention Mechanism [Nice Blog](https://towardsdatascience.com/attn-illustrated-attention-5ec4ad276ee3)
- BERT
  - Tokenizer [Blog](https://www.analyticsvidhya.com/blog/2021/09/an-explanatory-guide-to-bert-tokenizer/)
- AutoEncoders (Feature Reduction, Selection) [Blog](https://towardsdatascience.com/autoencoders-bits-and-bytes-of-deep-learning-eaba376f23ad)
- Can we train LSTMs without padding or tructating?
  - Yes. However, to do so we will have to have batch size=1. This is because, when batch size>1, forward propagation happens in paralell. With diffent timesteps for samples in same batch we won't be able tp process in paralell. So, we can train LSTMs with varying timesteps samples, However we will have to keep batch size=1. This will hamper training time a lot. Hence, most of the time padding with masking is preferred.
- Evaluation metrics for ranking system [FAISS](https://engineering.fb.com/2017/03/29/data-infrastructure/faiss-a-library-for-efficient-similarity-search/)
  - 1-Recall@1
    - Recall: Recall is a common evaluation metric in information retrieval and ranking systems. It measures the ability of a system to retrieve relevant items from a given set of items. In this case, it assesses how well the ranking system is at finding the relevant items.
      @1: The "@1" part of the metric specifies the cutoff point for evaluating recall. It means that you are only considering the performance of the system
      at the top-ranked item (the first item). In other words, you are interested in whether the ranking system was able to find the most relevant item and
      place it at the very top of the list.
      1-recall@1: This term indicates that you are calculating the recall at the top position, i.e., whether the most relevant item is found at the first
      rank. Subtracting this value from 1 gives you the "1-recall@1," which essentially tells you how often the most relevant item is missed at the top
      position. So, if the 1-recall@1 value is 0.2, it means that the most relevant item was missed at the top position 20% of the time.
      In summary, 1-recall@1 is a measure of how often the ranking system fails to place the most relevant item at the very top of the list. It is a critical
      metric when the highest-ranked item is of utmost importance, such as in cases where users typically only view or interact with the top result, like in
      web search engines.
  - 10-intersection
  - Precision@K
  - Recall@K
- FAISS : [Blog](https://www.pinecone.io/learn/series/faiss/faiss-tutorial/)
- Contrastive Learning : [Blog](https://www.baeldung.com/cs/contrastive-learning)
