# part-1-neural-network-analysis
Domain: Telecom - Customer Churn Prediction
Overview
This project builds a neural network to predict whether a telecom customer will churn or stay. The model is trained on structured customer data with 16 features and uses TensorFlow and Keras.
Dataset
File: customer_churn_nn.csv
Total records: 2000
Target variable: churn where 1 means churned and 0 means retained
Churn rate: 1.55 percent
Features include region, plan type, contract type, payment method, tenure, monthly charges, satisfaction score, and more.
Tasks Completed
Task 1: Dataset understanding including shape, types, missing values, and target distribution
Task 2: Data preprocessing including one hot encoding, standard scaling, train test split, and class weights
Task 3: Neural network model built with Dense layers, BatchNormalization, Dropout, and Sigmoid output
Task 4: Model trained and evaluated with confusion matrix, ROC curve, and classification report
Task 5: Five hyperparameter experiments comparing architecture size, activation functions, learning rate, and batch size
Task 6: Written reflection on weights, biases, activation functions, learning rate effects, and overfitting
Model Architecture
Input Layer with 25 features
Hidden Layer 1 with 64 neurons ReLU activation BatchNorm and Dropout 0.3
Hidden Layer 2 with 32 neurons ReLU activation BatchNorm and Dropout 0.3
Output Layer with 1 neuron and Sigmoid activation
Loss function: Binary Crossentropy
Optimizer: Adam with learning rate 0.001
Class weights applied to handle severe class imbalance
Early stopping monitors validation AUC with patience of 12
Hyperparameter Experiments
Config 1 is a Small Network with architecture 32 and 16, ReLU activation, learning rate 0.001, batch size 32
Config 2 is the Baseline Medium with architecture 64 and 32, ReLU activation, learning rate 0.001, batch size 32
Config 3 is a Deeper Network with architecture 128, 64, and 32, ReLU activation, learning rate 0.0005, batch size 32
Config 4 uses tanh Activation with architecture 64 and 32, tanh activation, learning rate 0.001, batch size 64
Config 5 uses High Learning Rate with architecture 64 and 32, ReLU activation, learning rate 0.01, batch size 128
Key Findings
Severe class imbalance of 1.55 percent churn makes ROC-AUC and Recall the critical metrics and not just accuracy. Class weights significantly improve the model ability to detect churners. Asignificantly improve the model ability to detect churners. A medium depth network with moderate dropout performs best overall. A very high learning rate leads to unstable training and lower recall.
How to Run
Install dependencies using: pip install -r requirements.txt
Open notebook using: jupyter notebook notebook.ipynb
Run all cells from top to bottom
Requirements
tensorflow 2.13 or higher
numpy 1.24 or higher
pandas 2.0 or higher
scikit-learn 1.3 or higher
matplotlib 3.7 or higher
seaborn 0.12 or higher
