# Spam-Email-Detection
Detect spam mail from data using statistical analysis and machine learning modeling. Spam detection is crucial for protecting inboxes from harmful content and improving productivity. These emails often carry advertisements, scams, or phishing attempts and can be a nuisance or even harmful to users.
## DataSet
The data set contains two columns
- Category: Classify the messages as either ham or spam
- Message: Column contains the text of each message

<img width="274" alt="head" src="https://github.com/user-attachments/assets/ac24ec71-22a9-41fa-b0b7-0d9347827cde">

## Steps
- Data Pre-processing
- Data Cleaning
- Label Encoding
- Exploratory Data Analysis (EDA)
- Feature Selection
- Spam Filter Algorithm
- Data Modeling
- Confusion Matrix
- Accuracy
- Testing Phase

### 1-Data Pre-processing
- In this step, download the dataset from Kaggle and load it using Python libraries like pandas in Jupyter Notebook.
- Inspecting the structure of the dataset to understand its columns and rows.
### 2-Data Cleaning
- Remove null & Empty rows
- Remove duplicate data
- Remove Special Character
### 3-Label Encoding
- Using the LabelEncoder() library to encode **Category** column & convert into numeric values for analysis or model building
- Convert ham into 0 and spam into 1
- Converting to lowercase.
- Removing punctuation and special characters.
- Removing stopwords.
- Tokenization and lemmatization 
### 4-Exploratory Data Analysis
- Count the number of rows by Category
- Data set contains ham mail more than 4000 & spam mail less than 1000
<img width="444" alt="cont" src="https://github.com/user-attachments/assets/8d07607b-4328-4f62-aa3c-fc267e2f71d1">

### 5-Feature Selection
- Applied feature extraction on text messages to find frequency matrix for data modeling
- Using the CountVectorizer library and selecting a feature from the Message column
### 6-Spam Filter Algorithm
- In this phase, splitting the data into training and testing sets using train_test_split from scikit-learn
- Split the dataset with 70% of the data as the training set and 30% as the test set
### 7-Data Modeling
- used GaussianNB, MultinomialNB, and LogisticRegression algorithms to detect spam emails from the data.

### 8-Confusion Matrix
The confusion matrix for the **GaussianNB model** shows 1200 true negatives, 190 false positives, 24 false negatives, and 180 true positives, providing insights into spam email classification performance.

<img width="410" alt="image" src="https://github.com/user-attachments/assets/79e92783-0a6e-47f2-be70-f27ec5bb1678">

The confusion matrix for the **MultinomialNB model** shows 1300 true negatives, 21 false positives, 16 false negatives, and 190 true positives, providing insights into spam email classification performance.

<img width="416" alt="image" src="https://github.com/user-attachments/assets/411eb39f-8547-4e3b-88b1-30186a81a062">

The confusion matrix for the  **LogisticRegression model** shows 1300 true negatives, 1 false positive, 45 false negatives, and 160 true positives, providing insights into spam email classification performance.

<img width="411" alt="image" src="https://github.com/user-attachments/assets/0cb1f8e3-b048-4bc1-9068-8c74b14c3754">

### 9-Accuracy
- GaussianNB Accuracy: 0.8636950904392765
- MultinomialNB Accuracy: 0.9760981912144703
- Logistic Regression Accuracy: 0.9702842377260982

The Accuracy Score of the MultinomialNB model and Logistic Regression is almost the same but the precision score of Logistic Regression is high. The dataset contains imbalanced values so select the logistic regression model for testing. It indicates that the Logistic Regression model performs better than the MultinomialNB & GaussianNB model.
