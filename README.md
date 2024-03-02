## Model Development: 

Various deep learning architectures were investigated, including convolutional neural networks (CNNs). These models were chosen for their effectiveness in capturing both local and sequential features within textual data, which is crucial for offensive language detection.

## Model 1: Offensive Tweet Identification (Dense Layer)
**Task:** Identify offensive language in tweets.   
**Approach:** This model utilizes a single dense layer directly on the input features (e.g., word embeddings, character n-grams) to perform classification.   
**Performance:** Achieved an F1-score of 0.75.   
**Limitations:**   
**Limited feature learning:** A single dense layer lacks the capability to capture complex relationships within the data compared to models with deeper architectures like CNNs and LSTMs.   
**Potential overfitting:** With a limited number of parameters, the model might be prone to overfitting the training data, leading to reduced performance on unseen data.    

## Model 2: Offensive Tweet Identification (1D CNNs + Dense Layer)   
**Task:** Identify offensive language in tweets.
**Approach:** Leverages one-dimensional convolutional neural networks (1D CNNs) to capture local patterns within tweets, followed by a dense layer for classification.   
**Performance:** Achieved an F1-score of 0.74.   
**Comparison:** While Model 2's F1-score of 0.74 is lower than Model 3 (0.78), it offers potential advantages such as   
- Interpretability: 1D CNNs can sometimes provide insights into specific words or phrases contributing to offensive language detection.   
- Efficiency: 1D CNNs might be computationally less expensive compared to pre-trained models like the Universal Sentence Encoder used in Model 3.   


## Model 3: Offensive Tweet Identification (Universal Sentence Encoder + Dense Layer)   
**Task:** Identify offensive language in tweets.   
**Approach:** Utilizes a pre-trained Universal Sentence Encoder to extract semantic embeddings from tweets, followed by a dense layer for classification.   
**Performance:** Achieved an F1-score of 0.78.    
