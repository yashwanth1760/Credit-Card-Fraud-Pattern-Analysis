# Credit-Card-Fraud-Pattern-Analysis
# 💳 Credit Card Fraud Detection Analysis

A comprehensive data analysis project to identify fraudulent credit card transactions using statistical methods and pattern recognition.

## 📊 Project Overview

This project analyzes credit card transaction data to detect fraud patterns and develop actionable detection rules. The analysis reveals that **86.2% of fraud occurs during night hours (10PM-6AM)** and fraudulent transactions are **7.9x larger** than legitimate ones.

## 🎯 Problem Statement

Credit card fraud causes significant financial losses for both customers and financial institutions. The challenge is to:
- Identify fraudulent transactions in real-time
- Minimize false positives that frustrate legitimate customers
- Develop practical detection rules based on data patterns

## 📁 Dataset Information


- **Total Transactions:** 1,296,675
- **Fraudulent Cases:** 7,506 (0.58%)
- **Unique Customers:** 983
- **Time Period:** 2015-2017
- **Features:** Transaction amount, timestamp, merchant info, customer details, location data

## 🔍 Key Findings

### 1. Time-Based Patterns
- **86.2%** of fraud occurs between 10PM-6AM
- Night-time transactions are **14.5x riskier** than daytime
- Peak fraud activity around 2AM

### 2. Amount Patterns
- Average fraud transaction: **$531**
- Average legitimate transaction: **$67**
- Fraud amounts are **7.9x larger**

### 3. Optimal Detection Threshold
- **$250 threshold** catches 95% of fraud cases
- 14.6% fraud detection rate in flagged transactions
- Best balance between detection and false positives

### 4. Z-Score Analysis
- Z-score > 3 identifies unusual customer behavior
- Catches **42.4%** of fraud cases
- Only flags **1.4%** of total transactions

### 5. Combined Rules
- Amount > $250 + Night time = **32.7% fraud rate**
- Z-score > 3 + Amount > $250 + Night time = **37.3% fraud rate**
- Combined approach: 1 in 3 flagged transactions is actual fraud

### 6. Merchant Risk
- New merchants: **1.32%** fraud rate
- Existing merchants: **0.48%** fraud rate
- **2.8x higher risk** with new merchants

## 📈 Visualizations

### Average Z-Score by Hour
![Z-Score by Hour](images/chart1.png)
*Fraud activity spikes dramatically during night hours while legitimate transactions remain flat.*

### Z-Score vs Transaction Amount
![Z-Score vs Amount](images/chart2.png)
*Clear clustering of fraud in high Z-score and high amount quadrant.*

### Z-Score Distribution
![Distribution](images/chart3.png)
*Fraud and legitimate transactions show distinct distribution patterns with Z=3 as effective separator.*

## 💡 Recommended Solutions

### Tier 1: Auto-Decline
**Rule:** Block transactions > $1,000 during 10PM-6AM
- Highest risk transactions
- Customer can verify via phone

### Tier 2: Verification Required
**Rules:**
- Amount > $250 during 10PM-6AM
- Z-score > 3 during 10PM-6AM
- New merchant with amount > $100

**Action:** Send SMS for confirmation within 10 minutes

### Tier 3: Flag for Review
**Rules:**
- Amount > $500 anytime
- Moderate risk scores (7-12)

**Action:** Allow transaction, manual review within 2 hours

## 📊 Business Impact

### Current State
- 7,506 fraudulent transactions
- ~$4M total fraud losses
- Detection happens after the fact

### Expected Improvement
- ✅ **95% real-time fraud detection**
- ✅ **~$3.8M saved annually**
- ✅ **<2%** of customers need verification
- ✅ Minimal customer friction

## 🛠️ Technologies Used

- **Python/SQL** - Data analysis and processing
- **Pandas** - Data manipulation
- **Matplotlib/Seaborn** - Data visualization






## 📝 Key Analysis Steps

1. **Data Preprocessing**
   - Handle missing values
   - Feature engineering (time extraction, Z-score calculation)
   - Data normalization

2. **Exploratory Data Analysis**
   - Temporal pattern analysis
   - Amount distribution analysis
   - Customer behavior profiling

3. **Statistical Analysis**
   - Z-score calculation per customer
   - Threshold optimization
   - Rule combination testing

4. **Visualization**
   - Time-based fraud patterns
   - Amount vs risk scatter plots
   - Distribution comparisons

## 📊 Results Summary

| Metric | Value |
|--------|-------|
| Fraud Detection Rate | 95% |
| False Positive Rate | <5% |
| Annual Savings | ~$3.8M |
| Customer Impact | <2% need verification |
| Best Rule | $250 + Night time |
| Best Accuracy | 37.3% (combined rules) |

## 👤 Author

**Yashwanth CH**

- GitHub: [Yashwanth Chalamalla](https://github.com/yashwanth1760/)
- LinkedIn: [yashwanth-chalamalla]([https://linkedin.com/in/yourprofile](https://www.linkedin.com/in/yashwanth-chalamalla/))

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.




⭐ **If you found this project helpful, please consider giving it a star!**
