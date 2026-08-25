# 🧠 Practical Text Analytics: Automotive Review Sentiment Classification

### CE807 – Practical Text Analytics | University of Essex

A Natural Language Processing (NLP) project for classifying sentiment in automotive product reviews using **unsupervised** and **discriminative** machine learning approaches.

---

## 📌 Project Overview

This project was completed as part of **CE807 – Practical Text Analytics** at the **University of Essex**.

The project investigates **sentiment classification of automotive reviews from an e-commerce dataset**. The aim is to develop and evaluate two different approaches for identifying whether a review expresses positive or negative sentiment.

The project focuses not only on building classifiers, but also on understanding and evaluating:

- Text preprocessing
- Text representation
- Feature extraction
- Model selection
- Hyperparameter selection
- Model performance
- Validation-based evaluation
- Comparison between different classification approaches
- Error analysis
- Comparison with existing approaches

The project follows a complete NLP workflow from raw text through preprocessing, model training, validation, testing, and analysis.

---

## 🎯 Objective

The main objective of the project is:

> **To develop and evaluate NLP-based sentiment classifiers for automotive product reviews and determine which approach provides the strongest performance on the provided dataset.**

The project uses two complementary classification approaches:

### 1. 🔵 Unsupervised Classifier

An unsupervised sentiment classification approach is used to predict sentiment without directly training on the labelled training data.

### 2. 🟣 Discriminative Classifier

A discriminative machine learning approach is trained using labelled examples to learn the relationship between textual features and sentiment labels.

The two approaches are evaluated using the validation data before producing predictions for the unseen test dataset.

---

# 🔬 NLP Pipeline

The overall workflow can be summarised as:

```text
                 Automotive Reviews
                         │
                         ▼
                ┌─────────────────┐
                │ Data Loading    │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Text            │
                │ Preprocessing   │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Text            │
                │ Representation  │
                └────────┬────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
      ┌───────────────┐     ┌────────────────┐
      │ Unsupervised  │     │ Discriminative │
      │ Classifier    │     │ Classifier     │
      └───────┬───────┘     └───────┬────────┘
              │                     │
              └──────────┬──────────┘
                         ▼
                ┌─────────────────┐
                │ Validation &    │
                │ Model Selection │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Test Prediction │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Performance &   │
                │ Error Analysis  │
                └─────────────────┘
```
# 📊 Dataset

The project uses the **provided automotive review dataset** supplied for the CE807 assignment.

The dataset is divided into three components:

| Dataset | Purpose |
|---|---|
| `train.csv` | Used to train the discriminative model |
| `valid.csv` | Used for model selection and parameter tuning |
| `test.csv` | Used to generate final predictions |

The training and validation datasets contain sentiment labels, while the test dataset is used for generating the final model predictions.

The test set is kept separate from model selection and parameter tuning to avoid using unseen test information during development.

---

# 🧹 Text Preprocessing

Text preprocessing is an important part of the classification pipeline.

Depending on the modelling approach, preprocessing may include operations such as:

- Text cleaning
- Tokenisation
- Normalisation
- Removal of unnecessary characters
- Stop-word handling
- Feature extraction
- Transformation of text into numerical representations

The preprocessing strategy is selected according to the requirements of the classification models.

---

# 🔤 Text Representation

Since machine learning models cannot directly process raw text, the reviews are transformed into numerical representations.

The project investigates how different text representations affect classification performance.

The representation of the text is considered alongside the classifier and preprocessing strategy when selecting the final models.

---

# 🤖 Classification Approaches

## 🔵 Unsupervised Sentiment Classification

The first approach uses an **unsupervised sentiment classification method**.

The objective is to estimate the sentiment of a review without directly learning from the labelled training examples.

This provides a useful baseline for understanding how sentiment can be inferred from textual information without conventional supervised training.

---

## 🟣 Discriminative Classification

The second approach uses a **discriminative classifier** trained using labelled examples from the training dataset.

The model learns patterns in the textual features that distinguish between sentiment classes.

The validation set is used to investigate model settings and identify the strongest configuration before applying the selected model to the test dataset.

---

# ⚙️ Model Selection

Model selection is based on experimental evaluation rather than simply choosing a model in advance.

The project considers:

- Classification performance
- Preprocessing choices
- Text representation
- Model parameters
- Validation performance
- Computational considerations
- Generalisation to unseen data

The objective is to select the best-performing configuration based on the **validation dataset**, while keeping the test dataset unseen during development.

---

# 📈 Evaluation

The models are evaluated using appropriate classification metrics.

Depending on the experiments, these can include:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

The evaluation is used to compare the unsupervised and discriminative approaches and understand where each model performs well or poorly.

> **Note:** The numerical results reported in this repository are based on the experiments conducted for the project. No performance values are stated here unless they are directly supported by the experimental results.

---

# 🔎 Error Analysis

Beyond overall performance, the project examines individual examples from the validation data.

The analysis considers examples where:

- Both models correctly classify the review
- Both models make an incorrect prediction
- One model is correct while the other is incorrect
- The models show different levels of confidence

Examining individual examples helps explain **why** the models behave differently rather than relying only on a single performance score.

## 🧪 Experimental Evaluation

The project follows an experimental approach to compare different modelling choices.

The evaluation investigates how changes in:
```text

Preprocessing
      +
Text Representation
      +
Model Configuration
      │
      ▼
Validation Performance
      │
      ▼
Best Configuration
      │
      ▼
Final Test Predictions
```

This provides a systematic basis for selecting the final models and generating the final test predictions.

## 📁 Repository Structure

```text
NLP-Text-Analysis/
│
├── README.md
│
├── data/
│   └── Dataset files
│
├── notebooks/
│   └── NLP analysis and modelling notebooks
│
├── report/
│   └── Project report
│
├── presentation/
│   └── Presentation slides
│
├── .gitignore
│
└── .gitattributes
```
### 📂 `data/`

Contains the dataset used for the NLP experiments.

### 📓 `notebooks/`

Contains the Jupyter/Google Colab notebooks used for NLP analysis, preprocessing, experimentation, and model development.

### 📄 `report/`

Contains the written academic report describing the methodology, experiments, results, analysis, and conclusions.

### 🎥 `presentation/`

Contains the presentation slides and supporting material prepared for the project.

## 🚀 Running the Project

### 1. Clone the Repository

Clone the repository using Git:

```bash
git clone https://github.com/zeinabdastmozd/NLP-Text-Analysis.git
cd NLP-Text-Analysis
```
### 2. Install the required Python packages

If a requirements.txt file is provided:
```bash
pip install -r requirements.txt
```
### 3. Prepare the dataset

Place the required dataset files inside the appropriate data/ directory.

The expected dataset structure is:
```bash
data/
├── train.csv
├── valid.csv
└── test.csv
```
### 4. Run the notebook

Open the notebook located in:
```bash
notebooks/
```
The notebook contains the data processing, modelling, evaluation, and analysis workflow.

# 📊 Project Outputs

The project produces outputs associated with:

- **Text preprocessing**
- **Feature representation**
- **Model training**
- **Validation experiments**
- **Sentiment predictions**
- **Model comparison**
- **Error analysis**
- **Final test predictions**

The final test predictions follow the required output structure for the **CE807 assessment**.

---

# 💡 Key Learning Outcomes

This project provided practical experience in:

- Designing NLP classification systems
- Working with real-world text data
- Cleaning and preprocessing textual data
- Transforming text into machine-readable features
- Comparing supervised and unsupervised approaches
- Selecting models using validation data
- Evaluating classification performance
- Analysing model errors
- Justifying modelling decisions experimentally
- Communicating technical findings through a research report and presentation

---

# 🎓 Academic Context

This project was completed as part of:

**CE807 – Practical Text Analytics**

**School of Computer Science and Electronic Engineering**  
**University of Essex**

The project was designed to provide practical experience in developing, evaluating, and scientifically analysing text classification systems.

# 📚 Research Areas

This project sits at the intersection of:
```text

Natural Language Processing
            │
            ▼
      Text Analytics
            │
     ┌──────┴──────┐
     ▼             ▼
Sentiment       Machine
Analysis        Learning
     │             │
     └──────┬──────┘
            ▼
      Text Classification
```
# ⚠️ Academic Note

This repository represents an academic project completed as part of university study.

Any datasets, external resources, libraries, algorithms, or code adapted from external sources should be appropriately acknowledged according to the relevant academic and licensing requirements.

# 👩‍💻 Author

Zeinab Dast Mozd

MSc Artificial Intelligence

Interests
Artificial Intelligence
Machine Learning
Natural Language Processing
Large Language Models
AI Evaluation
Data Science
Human-AI Interaction
