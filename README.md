📱 SMS Spam Detection using NLP

A Natural Language Processing (NLP) project that classifies SMS messages as **Spam** or **Ham (Not Spam)**.

The project demonstrates a complete NLP pipeline, starting from text preprocessing and ending with spam/ham prediction using a machine learning classification model.

---

## 🎯 Project Objective

The main goal of this project is to automatically identify whether an SMS message is:

* 🚨 **Spam** – unwanted, promotional, fraudulent, or suspicious messages
* ✅ **Ham** – normal, legitimate messages

### Example

```text
Input:
"Congratulations! You have won a free iPhone!"

Prediction:
Spam
```

```text
Input:
"Hey, are you coming home for dinner?"

Prediction:
Ham
```

---

## 🧠 NLP Pipeline

The project follows these major steps:

```text
SMS Dataset
     ↓
Text Cleaning
     ↓
Tokenization
     ↓
Stopword Removal
     ↓
Lemmatization
     ↓
Word Embeddings
     ↓
Feature Creation
     ↓
Machine Learning Model
     ↓
Spam / Ham Prediction
```

---

## 📊 Dataset

The project uses an SMS dataset containing messages labeled as:

* `spam`
* `ham`

The dataset is used to train a machine learning model to recognize patterns commonly associated with spam messages.

---

## 🔧 Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Gensim
* Scikit-learn
* Word2Vec
* Jupyter Notebook

---

## 🧹 Text Preprocessing

Raw SMS messages cannot be directly given to most machine learning models.

Therefore, the messages are processed using several NLP techniques.

### 1. Tokenization

The sentence is divided into individual words.

```text
"Congratulations you have won"

↓

["congratulations", "you", "have", "won"]
```

### 2. Stopword Removal

Common words that provide little useful information are removed.

Example:

```text
"you have won a prize"

↓

["won", "prize"]
```

### 3. Lemmatization

Words are converted into their meaningful base form.

Example:

```text
"winning" → "win"
"received" → "receive"
```

### 4. Word Embeddings

The cleaned words are converted into numerical vectors using **Word2Vec**.

Example:

```text
spam → numerical vector
money → numerical vector
offer → numerical vector
```

These numerical representations can then be used by a machine learning model.

---

## 🤖 Model

The processed text is converted into numerical features and passed to a machine learning classification model.

The model learns patterns from the training data and predicts whether a new SMS belongs to:

```text
Spam
or
Ham
```

---

## 🔍 Prediction Example

Example spam message:

```python
new_sms = ["URGENT! You have been selected to receive a cash bonus."]
```

Expected output:

```text
Prediction: Spam
```

Example normal message:

```python
new_sms = ["Hi, I will reach home by 7 pm."]
```

Expected output:

```text
Prediction: Ham
```

---

## 📈 Model Evaluation

The model can be evaluated using common classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

For spam detection, **precision and recall are especially important** because incorrectly classifying legitimate messages as spam can be problematic.

---

## 📁 Project Structure

```text
SMS-Spam-Detection-NLP/
│
├── SMS_Spam_Detection.ipynb
├── spam.csv
├── requirements.txt
├── README.md
├── .gitignore
│
└── images/
    └── confusion_matrix.png
```

> Rename `SMS_Spam_Detection.ipynb` and `spam.csv` to match the actual filenames in your project.

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/nivetha-engineer/SMS-Spam-Detection-NLP.git
```

Move into the project folder:

```bash
cd SMS-Spam-Detection-NLP
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
SMS_Spam_Detection.ipynb
```

Run the notebook cells from beginning to end.

---

## 🧪 Testing New SMS Messages

After training the model, you can test your own messages.

Example:

```python
new_sms = ["Congratulations! You have won a free iPhone!"]
```

The model will process the message and return:

```text
Spam
```

You can also test normal messages:

```python
new_sms = ["Can you call me when you reach home?"]
```

Output:

```text
Ham
```

---

## 💡 What I Learned

Through this project, I practiced:

* Natural Language Processing
* Text preprocessing
* Tokenization
* Stopword removal
* Lemmatization
* Word embeddings
* Word2Vec
* Feature engineering
* Machine learning classification
* Model evaluation
* Real-world text classification

---

## 🚀 Future Improvements

Possible improvements include:

* Compare multiple machine learning algorithms
* Improve feature engineering
* Handle class imbalance
* Add a Flask API
* Build a web application
* Deploy the model
* Add real-time SMS prediction
* Experiment with TF-IDF
* Compare Word2Vec with modern embedding techniques

---

## 👩‍💻 Author

**Nive**

GitHub:
https://github.com/nivetha-engineer

---

## ⭐ If You Like This Project

If you found this project useful, consider giving the repository a ⭐ on GitHub.
