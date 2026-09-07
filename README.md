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

