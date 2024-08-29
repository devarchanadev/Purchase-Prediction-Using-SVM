# Purchase Prediction Using SVM

---
## 🚀 Project Overview

In this project, I set out to predict the variable **"Purchase"** using the OJ dataset from the ISLR package. I evaluated various Support Vector Machines (SVMs) with different kernel functions—linear, radial, and polynomial—to identify the optimal cost parameters for each model and achieve the best prediction accuracy.

- [Data Preparation](#-data-preparation)
- [Methodology](#-methodology)
- [Performance Analysis](#-performance-analysis)
- [Business Impact](#-business-impact)
- [Insights and Recommendations](#-insights-and-recommendations)
- [Passion and Relevance](#-passion-and-relevance)
- [Conclusion](#-conclusion)
- [Key Takeaways](#-key-takeaways)
- [Statistical Significance](#-statistical-significance)
- [Importance for Data Scientists](#-importance-for-data-scientists)
- [Tools and Packages Used](#-tools-and-packages-used)
- [Installation Steps](#-installation-steps)
- [Dataset Source](#-dataset-source)
- [Further Reading and Links](#-further-reading-and-links)

---

## 🧹 Data Preparation

### 📊 Splitting the Data

I began by dividing the OJ dataset into a training set and a test set. I selected one-third of the data as the test set, with the remaining two-thirds forming the training set. This approach ensured that the model could be trained and tested on separate data, providing a reliable measure of its performance.

---

## 🔬 Methodology

### Support Vector Classifier with a Linear Kernel

**Approach:**  
```r
library(e1071)

# Fit SVM with linear kernel
fit <- svm(Purchase ~ ., data = training, kernel = "linear", cost = costs[i])
```
Optimal Cost Identified: 1

<img width="527" alt="Screenshot 2024-08-29 184110" src="https://github.com/user-attachments/assets/21a86e2c-37b5-4ee4-a834-de307cf48bf4">

### Support Vector Machine with a Radial Kernel

**Approach:**
```r
library(e1071)

# Fit SVM with radial kernel
fit <- svm(Purchase ~ ., data = training, kernel = "radial", cost = costs[i])
```
Optimal Cost Identified: 0.81

<img width="499" alt="Screenshot 2024-08-29 184139" src="https://github.com/user-attachments/assets/e802c68e-f411-4b92-8933-744fc78f4568">

### Support Vector Machine with a Polynomial Kernel

**Approach:**
```r
library(e1071)

# Fit SVM with polynomial kernel
fit <- svm(Purchase ~ ., data = training, kernel = "polynomial", degree = 2, cost = costs[i])
```
Optimal Cost Identified: 6.21

<img width="500" alt="Screenshot 2024-08-29 184203" src="https://github.com/user-attachments/assets/f849dcdf-1033-4564-b493-b062e20712f5">

## 📈 Performance Analysis

### Accuracy Comparison

| Kernel       | Accuracy |
|--------------|----------|
| **Linear**   | 81.18%   |
| **Radial**   | 81.18%   |
| **Polynomial** | 82.30%   |

### Test Error Comparison

| Kernel       | Test Error |
|--------------|------------|
| **Radial**   | 0.1854     |
| **Linear**   | 0.1882     |
| **Polynomial** | 0.1910     |

---

## 💼 Business Impact

Selecting the right SVM kernel can significantly impact model performance and business decisions. Accurate predictions of customer purchases can optimize marketing strategies, improve sales forecasting, and enhance customer segmentation.

---

## 💡 Insights and Recommendations

- **Linear Kernel:** Suitable for simpler, linearly separable data.
- **Radial Kernel:** Best for capturing complex data patterns, with the lowest test error.
- **Polynomial Kernel:** Provides the highest accuracy but with a slight trade-off in generalization.

---

## ❤️ Passion and Relevance

Understanding and applying different SVM kernels enhances predictive modeling capabilities. Effective model selection and tuning are crucial for deriving actionable insights and making data-driven decisions.

---

## 🏆 Conclusion

The analysis shows that while the polynomial kernel achieved the highest accuracy, the radial kernel showed better generalization performance with the lowest test error. Balancing accuracy and generalization is key for effective predictive modeling.

---

## 🗝️ Key Takeaways

- **Model Selection:** Balance complexity and performance.
- **Generalization:** Radial kernel offers better performance on unseen data.
- **Accuracy vs. Error:** Higher accuracy does not always imply better generalization.

---

## 📊 Statistical Significance

Optimizing the kernel and cost parameter balances training accuracy and generalization error, which is crucial for developing robust predictive models.

---

## 🔍 Importance for Data Scientists

Careful model selection and tuning ensure predictive models fit training data well and generalize to new data, leading to reliable insights and better decision-making.

---

## 🛠️ Tools and Packages Used

- **R Libraries:** ISLR2, ROCR, e1071, tidyverse, caret
- **Software:** R

---

## 🧑‍🔬 Installation Steps

1. Install R from [CRAN](https://cran.r-project.org/)
2. Install required packages using R:
   ```r
   install.packages(c("ISLR2", "ROCR", "e1071", "tidyverse", "caret"))

## 📥 Dataset Source

- **OJ Dataset:** Available in the ISLR2 package.

---

## 🔗 Further Reading and Links

- [ISLR2 on CRAN](https://cran.r-project.org/web/packages/ISLR2/index.html)

---

## 🌐 Visit My Repository

- [🔗 View Project Repository](https://github.com/devarchanadev/Purchase-Prediction-Using-SVM)

---

## 📥 Download Dataset

- [🔗 Download OJ Dataset](https://cran.r-project.org/web/packages/ISLR2/index.html)

---

Thank you for exploring this project! If you have any questions or need further details, please visit my [GitHub Repository](https://github.com/devarchanadev/Purchase-Prediction-Using-SVM).

---
