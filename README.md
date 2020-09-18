# Student Performance Prediction

Analysis on the UCI Machine Learning Student Performance Dataset (https://archive.ics.uci.edu/ml/datasets/Student+Performance#).<br>
The dataset contains students' achievements collected in two Portuguese Secondary schools, _Gabriel Pereira_ and _Mousinho da Silveira_. There are information related to Mathematics and Portuguese classes.<br>
Binary classification is performed to predict students' outcome at the end of the year (_pass_ or _fail_).<br>

## Analysis steps
1. Before applying the classification algorithms, the data was preprocessed:<br>
  1.1 **Features encoding** to translate textual values into numerical ones and categorical attributes into boolean ones. Zero-one and one-hot encodings were used.<br>
  1.2 **Feature scaling**: data was standardized, according to the estimates of mean and standard deviation computed with the bootstrap method.<br>
  1.3 **Dimensionality Reduction** with **PCA** to decrease the number of features describing the dataset, retaining 90\% of its cumulative variance.<br>
  1.4 **Oversampling with SMOTE** to balance the data sets, which were imbalanced on the negative class.<br>
2. Hyperparameters tuning with **5-Fold Cross Validation**
3. Training and testing with different classification techniques<br>
  3.1 Logistic Regression<br>
  3.2 K-Nearest Neighbors<br>
  3.3 Support Vector Machines (linear and RBF kernel)<br>
  3.4 Decision Trees<br>
  3.5 Random Forests<br>

Models were trained on both oversampled and non-oversampled training sets. Results were evaluated in terms of accuracy and F1-score and then compared to the state-of-the-art (https://www.researchgate.net/publication/228780408_Using_data_mining_to_predict_secondary_school_student_performance).
