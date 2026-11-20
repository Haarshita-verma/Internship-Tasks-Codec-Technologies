# Customer Churn Prediction

Data Analytics Internship · Project 01

## Run locally

From this folder, create a Python 3 environment and run:

```bash
python -m pip install -r requirements.txt
jupyter lab Customer_Churn_Prediction.ipynb
```

The notebook includes executed cells and charts. Use **Run All Cells** to reproduce the analysis. The bundled sample CSV comes from [IBM](https://github.com/IBM/telco-customer-churn-on-icp4d/blob/master/data/Telco-Customer-Churn.csv). See the upstream repository license in `data/IBM-LICENSE`.

## Results

Stratified 80/20 train/test split, random seed 42, positive class = customer churn.

| Model | Accuracy | Recall | Precision | ROC-AUC |
| --- | ---: | ---: | ---: | ---: |
| Majority baseline | .735 | .000 | .000 | .500 |
| Logistic Regression | .806 | .559 | .657 | .842 |
| Random Forest | .796 | .497 | .650 | .837 |

In the training sample, churn was 42.7% for month-to-month customers and 2.9% for two-year contracts. Logistic Regression scored highest across the reported test metrics. At the default threshold it still missed about 44% of churners. Test a retention offer and validate the model on newer data before using it to prioritize outreach.
