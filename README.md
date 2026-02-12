Titanic Dataset Preprocessing
This notebook performs several data preprocessing steps on the Titanic dataset. The goal is to clean and prepare the data for further analysis or machine learning model training.

1. Data Loading
The dataset Titanic-Dataset.csv was loaded into a pandas DataFrame named df.

2. Handling Missing Values
Missing values in the DataFrame were removed using the dropna() method, specifically dropping rows where any NaN values were present across all columns. After this operation, all columns showed zero null values.

3. Encoding Categorical Features
The following categorical columns were encoded into numerical representations using LabelEncoder from sklearn.preprocessing:

Sex: Converted 'male' and 'female' into numerical labels.
Embarked: Converted 'S', 'C', 'Q' into numerical labels.
Cabin: Converted various cabin identifiers into numerical labels.
4. Scaling Numerical Features
The numerical features 'Age' and 'Fare' were scaled to a range between 0 and 1 using MinMaxScaler from sklearn.preprocessing. This standardization helps in preventing features with larger values from dominating the learning process.

5. Outlier Detection and Removal
Outliers were identified and removed from the numerical columns ('Pclass', 'Sex', 'Age', 'SibSp', 'Parch', 'Fare', 'Cabin', 'Embarked') using the Interquartile Range (IQR) method. Box plots were generated to visualize the data distribution before and after outlier removal. A total of 41 rows identified as containing outliers were removed from the dataset.
