### **Wine Quality Prediction: Regression Analysis**  
📊 **Predicting Wine Quality Using Regression Models**  

## **Overview**  
This project analyzes the factors influencing wine quality using regression techniques, such as **Ordinary Least Squares (OLS)** and **ElasticNet**. We explore how different chemical properties impact wine quality scores and assess the effectiveness of interaction terms in improving model performance.  

## **Dataset**  
The dataset contains physicochemical properties (e.g., acidity, alcohol content, sulfur dioxide levels) of wine samples, along with expert-rated quality scores ranging from 3 to 8. Given the imbalance in the quality distribution, two models were performate: one, without altering the data, and the other merging quality scores 3 and 4, and 8 and 7.  

## **Objective**  
- Identify key factors influencing wine quality  
- Compare **OLS and ElasticNet** regression models  
- Evaluate the impact of **interaction terms**  
- Evaluate the impact of **merging the quality score**  

## **Key Findings**  
- **Alcohol and Sulphates** are the strongest predictors of wine quality.  
- Adding the **alcohol × sulphates interaction term** improves predictive power.  
- **ElasticNet regression provides a balance** between Ridge and Lasso but does not always outperform simpler models.  
- **Merging quality labels** does not significantly alter model performance but slightly reduces MSE.   

## **Model Performance Summary** 

| Model | Training R<sup>2</sup> | Holdout R<sup>2</sup> | Training MSE | Holdout MSE | 
|-------------|------------|------------|--------------|--------------|
| Baseline               |
| OLS<sup>*</sup>        |   0.370    |   0.446    | 0.411        | 0.353        |  
| Interaction Term|            |              |              | 
| OLS<sup>*</sup>        | 0.376      | 0.455      | 0.350        | 0.404        |  
| ElasticNet  | 0.382      | 0.453      | 0.346        | 0.406        |  
| Interaction Term + Imbalance Adjustment              |   
| ElasticNet  | 0.385      | 0.443      | 0.321        | 0.382        | 

<sup>*</sup> Variables manually selected.

## **Setup & Installation**  
1. **Clone the repository:**  
   ```bash
   git clone https://github.com/Darirad/Wine-Quality-Prediction.git
   ```  
2. **Install dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```  
3. **Run the analysis:**  
   ```bash
      jupyter notebook RedWineQuality.ipynb 
   ```
   or   
   ```bash
      jupyter lab RedWineQuality.ipynb 
   ```
## **Dependencies**  
- Python 3.12  
- pandas, numpy, scikit-learn  
- statsmodels, matplotlib, seaborn  

## **Future Improvements**  
- Explore **non-linear models** (e.g., decision trees, random forests).  
- Consider **classification approaches** for wine quality prediction.  
