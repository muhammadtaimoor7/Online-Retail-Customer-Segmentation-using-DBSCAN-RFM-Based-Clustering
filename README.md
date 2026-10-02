## Dataset
Online Retail Dataset, available at: https://archive.ics.uci.edu/dataset/352/online+retail
(Download the CSV separately and place it in the same directory to run the notebook)
# Online Retail Customer Segmentation using DBSCAN

## Overview
This project applies DBSCAN, a density based clustering algorithm, to segment e-commerce customers based on their purchasing behavior. Raw transaction level data is transformed into customer level RFM metrics (Recency, Frequency, Monetary), and DBSCAN is used to automatically discover natural customer segments while identifying customers with irregular buying patterns as noise, without relying on any predefined labels.

## Dataset
Online Retail Dataset (UCI Machine Learning Repository), containing transaction records including Invoice Number, Stock Code, Description, Quantity, Invoice Date, Unit Price, Customer ID, and Country.

## Workflow
1. Data cleaning: removed missing CustomerID and Description values, removed cancelled orders (Invoice Numbers starting with "C")
2. Feature engineering: built customer level RFM metrics from raw transactions
   - Recency: days since last purchase
   - Frequency: number of unique purchases
   - Monetary: total amount spent
3. Feature scaling with StandardScaler
4. K-distance graph and empirical eps testing to determine the optimal DBSCAN parameters
5. DBSCAN clustering and cluster analysis
6. Visualization of customer segments

This project demonstrates how DBSCAN can uncover both clear customer segments and meaningful outliers directly from raw business data, without relying on any predefined labels.

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
