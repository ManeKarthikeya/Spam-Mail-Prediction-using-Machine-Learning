# Spam Mail Prediction using Machine Learning

## 📖 Project Overview

This project implements a Machine Learning classifier to automatically detect and filter spam emails. Using Natural Language Processing (NLP) techniques and Logistic Regression, the system can accurately distinguish between legitimate emails ("ham") and unsolicited spam messages.

This is a practical application of text classification that demonstrates how machine learning can solve real-world problems in email security and content filtering.

## 🧠 Algorithms & Techniques Used

- **Logistic Regression**: A robust classification algorithm that works well for binary text classification tasks.
- **TF-IDF Vectorization**: Converts raw text into meaningful numerical features by analyzing term frequency and inverse document frequency.
- **Text Preprocessing**: Includes lowercasing and stop words removal to clean and prepare the text data.

## 📊 About the Dataset

The dataset consists of email messages labeled as either "spam" or "ham" (non-spam).

### Dataset Structure:

- **Message**: The actual content/text of the email
- **Category**: The label classifying the email as either:
  - **spam (0)**: Unsolicited, promotional, or malicious emails
  - **ham (1)**: Legitimate, personal, or important emails

- **Dataset Size**: Contains thousands of email samples for training and evaluation.

## 🛠️ Implementation Steps

The project follows a complete machine learning pipeline for text classification:

1. **Data Loading & Cleaning**: Loads the dataset and handles missing values
2. **Label Encoding**: Converts categorical labels ('spam'/'ham') to numerical values (0/1)
3. **Train-Test Split**: Divides data into training (80%) and testing (20%) sets
4. **Feature Extraction**: Uses TF-IDF vectorization to transform text into numerical features
5. **Model Training**: Trains a Logistic Regression classifier on the processed text features
6. **Model Evaluation**: Assesses performance using accuracy metrics on both training and test sets
7. **Prediction System**: Implements a functional spam detection system for new emails

## 📈 Performance Metrics

The model's effectiveness is measured using:

- **Training Accuracy**: How well the model learns from the training data
- **Test Accuracy**: How effectively the model generalizes to unseen email data

*(Note: Actual accuracy percentages will be displayed when you run the code with your dataset.)*

## 🚀 How to Use this Project

1. **Clone the repository**:
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
```

2. **Navigate to the project directory**.

3. **Install required dependencies**:
```bash
pip install numpy pandas scikit-learn
```

4. **Prepare the dataset**:
   - Download a spam/ham email dataset (commonly available as CSV)
   - Update the file path in the code: `raw_mail_data = pd.read_csv('path/to/your/spam_dataset.csv')`

5. **Run the Python script**:
```bash
python spam_mail_prediction.py
```

## 💡 Making Predictions

To classify a new email as spam or ham, provide the email text to the `input_mail` variable:

**Example:**
```python
input_mail = ["Congratulations! You've won a $1000 Walmart gift card. Click here to claim your prize now!"]
```

The system will output:
- **'Ham mail'** - Legitimate email (Prediction: 1)
- **'Spam mail'** - Spam email (Prediction: 0)

## 📁 Repository Structure

```
├── spam_mail_prediction.py       # Main Python script
├── mail_data.csv                 # Email dataset
└── README.md                     # Project documentation (this file)
```

## 🔧 Key Features

- **Efficient Text Processing**: Uses TF-IDF for effective feature extraction from email content
- **High Accuracy**: Logistic Regression provides reliable performance for spam detection
- **Easy Integration**: Simple interface for classifying new emails
- **Scalable**: Can be extended with more advanced models or larger datasets

## 🎯 Potential Applications

- Email client spam filters
- Message filtering in chat applications
- Content moderation systems
- Educational tool for understanding NLP and classification
