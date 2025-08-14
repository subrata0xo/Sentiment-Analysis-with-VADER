#Sentiment Analysis of Product Reviews using VADER

## **Project Overview**

This project performs sentiment analysis on a dataset of product reviews to classify them as **positive, negative, or neutral**. The analysis is done using the **VADER (Valence Aware Dictionary for sEntiment Reasoning)** sentiment analysis tool from the NLTK library, which is particularly effective for short texts such as social media posts or reviews. The goal is to understand customer opinions, visualize trends, and identify the overall sentiment distribution.

---

## **Steps in the Project**

### **1. Importing Libraries**

* **pandas, numpy** → For data handling and manipulation.
* **matplotlib, seaborn** → For data visualization.
* **WordCloud** → To generate word clouds for positive and negative reviews.
* **nltk (VADER)** → For sentiment analysis.

---

### **2. Loading and Cleaning Data**

* Dataset (`Reviews.csv`) is loaded into a pandas DataFrame.
* Selected relevant columns such as `Id`, `ProductId`, `UserId`, `Score`, `Time`, `Summary`, and `Text`.
* Removed duplicate reviews and rows with missing values.
* Converted `Time` from UNIX timestamp to human-readable datetime format.

---

### **3. Exploratory Data Analysis (EDA)**

* **Rating Distribution:** A count plot shows how reviews are distributed across rating scores.
* **Trend Over Time:** A line plot shows the number of reviews per year, helping identify growth patterns in customer engagement.

---

### **4. Sentiment Analysis with VADER**

* Downloaded the `vader_lexicon` for sentiment scoring.
* Defined a function `sentiment_analysis()` to classify review text:

  * **Positive** if compound score ≥ 0.05
  * **Negative** if compound score ≤ -0.05
  * **Neutral** otherwise
* Applied the function to the `Text` column to create a new `Sentiment` column.
* Visualized sentiment distribution using a bar plot.

---

### **5. Word Cloud Visualization**

* Generated separate word clouds for **positive** and **negative** reviews.
* Positive reviews often feature words like *“love”, “great”, “best”*, while negative ones include words like *“bad”, “disappointed”, “waste”*.

---

### **6. Key Insights**

* Most reviews are **positive**, suggesting general customer satisfaction.
* Certain years show a spike in review volume, possibly due to product launches or promotions.
* Word clouds provide a quick understanding of common themes in customer opinions.

---

## **Conclusion**

This project demonstrates how **VADER Sentiment Analysis** can be used to process and interpret large volumes of product reviews efficiently. Businesses can leverage such analysis to monitor customer satisfaction, track changes over time, and improve their products or services.


