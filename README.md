# 📰 Smart Fake News Detection System

### An NLP and Machine Learning Based News Classification Platform

## 📌 Project Overview

The **Smart Fake News Detection System** is a machine learning-based web application developed to identify whether a given news article is likely to be fake or real.

The system uses Natural Language Processing (NLP) techniques and machine learning algorithms to analyze news headlines and article content. It applies TF-IDF (Term Frequency–Inverse Document Frequency) for text feature extraction and uses trained classification models to generate predictions.

The application provides an interactive dashboard where users can enter news content, analyze articles, view prediction results, check confidence scores and maintain prediction history.

## 🎯 Project Objectives

- Develop a machine learning system for fake news detection.
- Analyze news headlines and article content.
- Perform text preprocessing and cleaning.
- Convert textual data into numerical features using TF-IDF.
- Train and evaluate multiple machine learning algorithms.
- Identify the best-performing classification model.
- Build an interactive web application using Streamlit.
- Display prediction results and confidence scores.

## ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Machine learning algorithms |
| TF-IDF | Text feature extraction |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Streamlit | Interactive web application |
| Joblib | Saving and loading trained models |

## 📂 Dataset

**Dataset Name:** WELFake Dataset

The WELFake dataset is used to train and evaluate the fake news classification models.

- Original records: 72,134
- Cleaned records: 63,673
- Training records: 50,938
- Testing records: 12,735
- Target column: `label`
- Label 0: Fake News
- Label 1: Real News

The dataset contains news titles, article text and corresponding labels.

**Note:** The dataset is not included in this GitHub repository because of its large file size.

To train the model again, place the dataset inside:

`data/WELFake_Dataset.csv`

## 🧹 Data Preprocessing

The following preprocessing steps are performed:

1. Loading the dataset.
2. Handling missing values.
3. Removing duplicate records.
4. Combining news headlines and article text.
5. Preparing input features and target labels.
6. Splitting the dataset into training and testing sets.

## 🧠 Machine Learning Algorithms

Two machine learning algorithms are implemented and evaluated.

### 1. Logistic Regression

Logistic Regression is used to classify news articles into fake and real categories. It achieved the best performance and was selected as the final model.

### 2. Multinomial Naive Bayes

Multinomial Naive Bayes is implemented as a second classification algorithm for comparison.

### TF-IDF Feature Extraction

TF-IDF converts news text into numerical features that machine learning algorithms can understand.

Maximum features used: **15,000**

## 📊 Model Performance

The models were evaluated using accuracy, precision, recall and F1-score.

| Evaluation Metric | Logistic Regression | Multinomial Naive Bayes |
|---|---:|---:|
| Accuracy | 95.52% | 86.31% |
| Precision | 94.93% | 83.95% |
| Recall | 95.21% | 86.31% |
| F1 Score | 95.07% | 85.11% |

### Best Performing Model

**Logistic Regression** was selected as the final model because it achieved the highest accuracy and F1-score among the evaluated models.

Final Test Accuracy: **95.52%**

## 📈 Exploratory Data Analysis and Visualizations

The project generates the following visualizations:

- Fake and real news label distribution.
- Logistic Regression confusion matrix.
- Multinomial Naive Bayes confusion matrix.
- Model performance comparison chart.

These visualizations help understand the dataset distribution and compare the performance of the classification algorithms.

## 🌟 Application Features

The Streamlit web application includes the following features:

### 1. Dashboard
- Project overview.
- Model information.
- Performance metrics.
- System workflow.

### 2. News Detection
- Enter a news headline.
- Paste the complete news article.
- Load sample news.
- Analyze news using the trained model.
- View prediction results.

### 3. Prediction Results
- Likely Fake News or Likely Real News classification.
- Model confidence percentage.
- Prediction details.

### 4. Prediction History
- View previously analyzed articles.
- Check prediction results.
- Download prediction history as a CSV file.
- Clear prediction history.

### 5. About Project
- Project objectives.
- Machine learning algorithms.
- Technology stack.
- Dataset information.

## 🔄 System Workflow

1. User enters a news headline and article.
2. The application combines the text.
3. TF-IDF transforms the text into numerical features.
4. The trained Logistic Regression model processes the features.
5. The model predicts the news category.
6. The application displays the prediction and confidence score.

## 📁 Project Structure

```text
Smart_Fake_News_Detection/
│
├── app.py
│
├── train_model.py
│
├── requirements.txt
│
├── README.md
│
├── model_comparison.csv
│
├── data/
│   └── WELFake_Dataset.csv
│
├── models/
│   └── fake_news_model.joblib
│
└── screenshots/
    ├── label_distribution.png
    ├── logistic_regression_confusion_matrix.png
    ├── multinomial_naive_bayes_confusion_matrix.png
    └── model_comparison_bar_chart.png
```

## 🚀 Installation and Execution

Follow these steps to run the project locally.

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Smart-Fake-News-Detection.git
```

### Step 2: Open the Project Folder

```bash
cd Smart-Fake-News-Detection
```

### Step 3: Create a Virtual Environment

```bash
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

### Step 4: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 5: Run the Application

```bash
streamlit run app.py
```

The application will open in your browser.

### To Retrain the Model

Make sure the WELFake dataset is available at `data/WELFake_Dataset.csv`, then execute:

```bash
python train_model.py
```

The trained model will be saved inside the `models` folder.

## 📦 Requirements

The project requires the following Python libraries:

- streamlit
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- joblib

## 🔮 Future Enhancements

- Integrate advanced NLP techniques and transformer-based models.
- Explore deep learning approaches for improved classification.
- Add explainable AI techniques to understand model predictions.
- Integrate reliable external fact-checking sources.
- Support multilingual news classification.
- Deploy the application for public access.

## ⚠️ Disclaimer

This project is developed for academic and educational purposes. The model identifies patterns learned from its training dataset and provides predictions based on textual content.

A prediction does not establish whether a news article is factually true or false. Users should verify important information through reliable news organizations and independent fact-checking sources.

## 👩‍💻 Project Information

**Project Title:** Smart Fake News Detection System

**Domain:** Artificial Intelligence and Machine Learning

**Technologies:** Python, NLP, Machine Learning and Streamlit

**Project Type:** Final Year Major Project

---

⭐ If you find this project interesting, feel free to explore the repository and its implementation.

**Developed as an academic project using Python and Machine Learning.**
