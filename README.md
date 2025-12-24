# 🛒 Customer Segmentation - Online Retail

An unsupervised machine learning project for customer segmentation using K-Means and DBSCAN clustering algorithms.

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![ML](https://img.shields.io/badge/ML-Clustering-purple)
![Status](https://img.shields.io/badge/Status-Complete-success)

## 🎯 Objective

Segment customers into meaningful groups based on their purchasing behavior to:
- Identify high-value customers
- Discover hidden patterns in customer data
- Enable targeted marketing strategies
- Improve customer retention

## 📊 Dataset

Online Retail dataset containing transactional data:

| Feature | Description |
|---------|-------------|
| **InvoiceNo** | Unique invoice number |
| **StockCode** | Product code |
| **Description** | Product description |
| **Quantity** | Quantity purchased |
| **InvoiceDate** | Date of transaction |
| **UnitPrice** | Price per unit |
| **CustomerID** | Unique customer identifier |
| **Country** | Customer's country |

## 🔄 Project Pipeline

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│  Data Loading   │───►│  Preprocessing  │───►│  Feature Eng.   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                                                      │
                                                      ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│    Analysis     │◄───│   Clustering    │◄───│ Feature Scaling │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🛠️ Techniques Used

### Data Preprocessing
- Missing value handling
- Outlier detection and treatment (IQR method)
- Data type conversions
- Removing cancelled transactions

### Feature Engineering (RFM Analysis)
- **R**ecency: Days since last purchase
- **F**requency: Number of transactions
- **M**onetary: Total spending

### Clustering Algorithms

#### K-Means Clustering
- Optimal K selection using Elbow Method
- Silhouette Score analysis
- Centroid-based partitioning

#### DBSCAN Clustering
- Density-based spatial clustering
- Automatic outlier detection
- No need to specify number of clusters

### Visualization
- Cluster distribution plots
- 2D/3D scatter plots
- Customer segment profiles

## 📁 Project Structure

```
online-retail-segmentation/
├── README.md
├── requirements.txt
├── notebooks/
│   └── customer_segmentation.ipynb
├── data/
│   └── .gitkeep (add your data here)
└── outputs/
    └── cluster_profiles.csv
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install -r requirements.txt
```

### Required Libraries

```
pandas
numpy
scikit-learn
matplotlib
seaborn
```

### Usage

1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/online-retail-segmentation.git
cd online-retail-segmentation
```

2. Add your dataset to `data/` folder

3. Open and run the Jupyter notebook
```bash
jupyter notebook notebooks/customer_segmentation.ipynb
```

## 📈 Customer Segments

### Example Segment Profiles

| Segment | Recency | Frequency | Monetary | Description |
|---------|---------|-----------|----------|-------------|
| **Champions** | Low | High | High | Best customers, buy often |
| **Loyal** | Low | Medium | Medium | Regular customers |
| **At Risk** | High | Medium | Medium | Haven't bought recently |
| **Lost** | High | Low | Low | Haven't bought in long time |

## 🔍 Key Findings

1. **Customer Distribution**: Majority fall into 3-4 main segments
2. **High-Value Customers**: ~20% of customers drive ~80% of revenue
3. **Seasonal Patterns**: Purchasing behavior varies by season
4. **Geographic Trends**: Different countries show different patterns


## 💡 Business Applications

- **Personalized Marketing**: Target each segment differently
- **Inventory Management**: Stock based on segment preferences
- **Customer Retention**: Focus on at-risk segments
- **Pricing Strategy**: Offer deals to specific segments

## 📚 Learning Outcomes

This project demonstrates:
- Unsupervised learning techniques
- RFM (Recency, Frequency, Monetary) analysis
- Cluster validation methods
- Business insight generation from data

## 👨‍💻 Author

- IoT & AI Developer @ VoltX
- CS Student @ Helwan University 


---

⭐ Star this repo if you find it useful!
