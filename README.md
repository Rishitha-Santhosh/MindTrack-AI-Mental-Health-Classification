# MindTrack: AI-Powered Mental Health and Daily Activity Correlation

## Overview

MindTrack is an AI-powered mental health classification project that explores the relationship between everyday behavioral patterns and mental well-being.

The project analyzes factors such as:

- Technology usage
- Social media usage
- Screen time
- Sleep duration
- Physical activity
- Age
- Gender

The objective is to investigate whether behavioral and lifestyle patterns can be used to classify different mental health conditions.

The project compares multiple Machine Learning and Deep Learning approaches and evaluates their performance using accuracy, precision, recall, F1-score, confusion matrices, and ROC-AUC.

---

## Project Objective

The main objective of MindTrack is to understand the relationship between daily activities and mental health and build predictive models capable of classifying mental health conditions from behavioral data.

The project demonstrates how AI and machine learning can potentially support mental health analysis by identifying patterns in lifestyle and behavioral data.

---

## Dataset

The dataset contains behavioral, demographic, and mental-health information.

### Features

- User ID
- Age
- Gender
- Technology Usage Hours
- Social Media Usage Hours
- Screen Time Hours
- Sleep Hours
- Physical Activity Hours
- Mental Health Class

### Dataset Size

- Training samples: 48,000
- Testing samples: 12,000
- Target variable: Mental Health Class

The original project documentation states that the data was collected from self-reported surveys, wearable devices, mobile health applications, and Kaggle data sources.

---

## Mental Health Classes

The project initially considered multiple mental-health categories.

After preprocessing and removal of classes with only one sample, the analyzed dataset contained the following classes:

- Severe Depression
- Moderate Depression
- Normal/Healthy
- Mild Anxiety
- Moderate Anxiety
- Mild Depression
- Severe Anxiety

The modeling section also presents the classes in encoded form for classification.

---

# Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the distribution of demographic, behavioral, and mental-health variables.

The analysis included distributions of:

- Age
- Technology usage
- Social media usage
- Screen time
- Sleep duration
- Physical activity
- Mental health classes
- Technology-to-screen-time ratio
- Social-to-technology ratio

The project also examined class distribution and relationships between behavioral variables and mental-health categories.

---

# Data Preprocessing

Several preprocessing and feature-engineering techniques were applied.

## Missing Value Handling

Missing values in important numerical variables such as:

- Screen_Time_Hours
- Social_Media_Usage_Hours
- Sleep_Hours

were handled using median imputation.

Median imputation was selected because it is relatively robust to outliers.

## Feature Engineering

Additional behavioral features were created.

### Technology-to-Screen-Time Ratio

```text
Tech_to_Screen_Ratio =
Technology_Usage_Hours / Screen_Time_Hours
Social_to_Tech_Ratio =
Social_Media_Usage_Hours / Technology_Usage_Hours

Feature Scaling

Numerical features were normalized using StandardScaler.

Scaling brings numerical variables to a comparable scale and helps improve the performance of models that are sensitive to feature magnitude.

Class Balancing

Class distributions were analyzed during preprocessing.

Resampling techniques were used to address class imbalance and improve the representation of the mental-health categories during model training.

Dimensionality Reduction

Principal Component Analysis (PCA) was used to visualize the processed dataset.

The PCA visualization was used to examine how the different mental-health classes were distributed across the principal components.

Machine Learning Models

The following Machine Learning models were evaluated:

Random Forest
Gradient Boosting
XGBoost
Multilayer Perceptron (MLP)
Random Forest

Random Forest was used as an ensemble classification model based on multiple decision trees.

Reported performance:

Training Accuracy: approximately 99.87%
Testing Accuracy: approximately 98.65%
Training ROC-AUC: 1.0000
Testing ROC-AUC: 0.9965

The model produced strong precision, recall, and F1-scores across the evaluated classes.

Gradient Boosting

Gradient Boosting was evaluated as another ensemble learning approach.

Reported performance:

Training Accuracy: approximately 98.69%
Testing Accuracy: approximately 98.75%
Training ROC-AUC: 0.9983
Testing ROC-AUC: 0.9979

The model achieved strong classification performance across the evaluated mental-health categories.

XGBoost

XGBoost was evaluated as a gradient-boosting classification model.

Reported performance:

Training Accuracy: approximately 98.91%
Testing Accuracy: approximately 98.78%
Training ROC-AUC: 0.9998
Testing ROC-AUC: 0.9981

XGBoost was identified as the best Machine Learning model in the project, achieving approximately 99% accuracy.

Multilayer Perceptron (MLP)

A Multilayer Perceptron neural network was also evaluated.

The project used an MLP architecture containing a hidden layer with 100 neurons.

Reported performance:

Training Accuracy: approximately 98.68%
Testing Accuracy: approximately 98.70%
Training ROC-AUC: approximately 0.9985
Testing ROC-AUC: approximately 0.9988
Deep Learning Models

The project evaluated multiple Deep Learning architectures:

LSTM
GRU
LSTM with Batch Normalization
Deeper Neural Network
LSTM

Long Short-Term Memory (LSTM) was evaluated as a recurrent neural network architecture.

The model achieved approximately:

Accuracy: 99%
Macro F1-score: approximately 0.98
Weighted F1-score: approximately 0.99

The confusion matrix demonstrated strong classification performance across the evaluated categories.

GRU

Gated Recurrent Unit (GRU) was evaluated as another recurrent neural network architecture.

The model achieved approximately:

Accuracy: 99%
Macro F1-score: approximately 0.98
Weighted F1-score: approximately 0.99
LSTM with Batch Normalization

An LSTM architecture incorporating Batch Normalization was evaluated to investigate the effect of additional normalization during model training.

The model demonstrated strong classification performance across the evaluated classes.

Deeper Neural Network

A deeper neural network architecture was also evaluated.

Reported performance:

Accuracy: approximately 99%
Macro F1-score: approximately 0.98
Weighted F1-score: approximately 0.99

The Deeper Neural Network was identified as the best Deep Learning model in the project.

Model Evaluation

The models were evaluated using multiple performance metrics.

Accuracy

Measures the overall proportion of correctly classified samples.

Precision

Measures how many samples predicted as a particular class were actually members of that class.

Recall

Measures the ability of the model to correctly identify samples belonging to a class.

F1-Score

Provides a balance between precision and recall.

Confusion Matrix

Confusion matrices were generated to analyze correct and incorrect predictions for each mental-health category.

ROC-AUC

One-vs-rest ROC curves were used to evaluate multiclass classification performance.

Model Comparison
Model	Approx. Test Accuracy	Approx. Test ROC-AUC
Random Forest	98.65%	0.9965
Gradient Boosting	98.75%	0.9979
XGBoost	98.78%	0.9981
MLP	98.70%	0.9988
LSTM	~99%	~0.99
GRU	~99%	~0.99
LSTM + Batch Normalization	~99%	~0.99
Deeper Neural Network	~99%	~0.99
Best Models
Best Machine Learning Model

XGBoost

XGBoost was identified as the best Machine Learning model, achieving approximately 99% accuracy.

Best Deep Learning Model

Deeper Neural Network

The Deeper Neural Network was identified as the best Deep Learning model, also achieving approximately 99% accuracy.

Key Findings

The project demonstrates that behavioral and lifestyle variables contain useful predictive patterns associated with mental-health categories in the dataset.

The analysis focused on:

Technology usage
Social media usage
Screen time
Sleep duration
Physical activity
Age
Gender

Multiple Machine Learning and Deep Learning approaches achieved high classification performance.

Project Workflow
                         Raw Dataset
                              |
                              v
                       Data Cleaning
                              |
                              v
                  Missing Value Handling
                              |
                              v
                       Outlier Analysis
                              |
                              v
                     Feature Engineering
                              |
                              v
                       Feature Scaling
                              |
                              v
                 Exploratory Data Analysis
                              |
                              v
                      Class Balancing
                              |
                              v
                       Train/Test Split
                              |
                 +------------+------------+
                 |                         |
                 v                         v
        Machine Learning            Deep Learning
                 |                         |
                 v                         v
           Random Forest                LSTM
           Gradient Boosting            GRU
           XGBoost                      LSTM + Batch Norm
           MLP                          Deeper Neural Network
                 |                         |
                 +------------+------------+
                              |
                              v
                       Model Evaluation
                              |
                              v
          Accuracy / Precision / Recall / F1
                       ROC-AUC
                              |
                              v
                       Model Comparison
                              |
                              v
                        Best Models
Visualizations

The project includes several visualizations:

Feature distributions
Mental-health class distribution
Outlier analysis using boxplots
Technology-to-screen-time ratio
Social-to-technology ratio
Sleep-quality distribution
PCA visualization
Confusion matrices
ROC curves
Training vs. testing accuracy
Training vs. testing loss
Training and validation accuracy
Training and validation loss
Technologies Used
Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost
TensorFlow
Keras
Project Achievement

🏆 2nd Place – Team No. 014

The MindTrack project was developed as Team No. 014 and achieved 2nd place in the project/competition evaluation.

Future Work

Possible future improvements include:

Expanding the dataset with real-time behavioral data
Incorporating additional real-time data sources
Exploring additional ensemble-learning methods
Improving model generalization
Investigating deployment for real-world applications
Evaluating the models on larger and more diverse datasets
Limitations

The project is based on the available dataset and its associated behavioral and mental-health labels.

The results should therefore be interpreted within the context of the dataset and experimental setup.

Further validation using larger, diverse, and independently collected datasets would be necessary before considering real-world deployment.

Disclaimer

This project is intended for educational and research purposes.

The predictions generated by the models should not be considered medical diagnoses or a replacement for professional mental-health assessment.

References
F. Mustač et al., "How to maintain mental health in turbulent times: Can mobile applications be a part of the solution?", 2021 6th International Conference on Smart and Sustainable Technologies (SpliTech), 2021.
C. Zhang et al., "AI Chatbots for Mental Health: A Scoping Review," Applied Sciences, vol. 14, no. 13, 2022.
World Health Organization, "Artificial intelligence in mental health research: New WHO study on applications and challenges," 2021.
S. Banerjee et al., "Mental Health Applications of Generative AI and Large Language Modeling in the United States," International Journal of Environmental Research and Public Health, 2024.
M. Huang and Y. Lin, "Exploring the Role of AI in Mental Health Support During COVID-19: A Review," Journal of Affective Disorders, 2022.
T. Smith et al., "Machine Learning Approaches to Predict and Prevent Mental Health Disorders," Psychiatry Research, 2023.
A. Davis and J. Roy, "AI-Based Assessment of Mental Health: Advances, Opportunities, and Ethical Challenges," Frontiers in Psychiatry, 2021.
L. Patel et al., "Personalized Mental Health Interventions with Machine Learning and Wearables," Computers in Biology and Medicine, 2022.
R. Gupta and S. Patel, "The Use of AI for Mental Health Monitoring in Adolescents," Healthcare, 2022.
Y. Zhao et al., "Natural Language Processing in Mental Health: Applications and Emerging Trends," PLoS ONE, 2022.

