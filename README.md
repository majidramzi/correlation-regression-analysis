# correlation-regression-analysis

This repository is used for completing exercises for the "Applied Analytics and AI" course, and all its contents are public.

## Correlation and regression analysis

### [Combined cycle power plant - Dataset & Prediction](https://www.kaggle.com/datasets/aagmandeep/combined-cycle-power-plant-dataset-and-prediction)

Prediction of the Output Power of a Combined Cycle Power Plant using ML

### About Dataset

**Predicting Electrical Energy Output of Combined Cycle Power Plant**

**Background:**
Single-cycle gas turbine power plants generate electricity using natural gas and compressed air. Combining gas and steam turbines in combined cycle power plants enhances efficiency by capturing waste heat, resulting in up to 50% more power generation. Predicting full load electrical power output is crucial for efficient operation.

**Data Description:**
The dataset comprises 9568 hourly average ambient environmental readings from sensors at a Combined Cycle Power Plant. Variables include Temperature (T), Ambient Pressure (AP), Relative Humidity (RH), Exhaust Vacuum (V), and Net hourly electrical energy output (PE).

**Data Source:**
The dataset was sourced from:

- Pınar Tüfekci, International Journal of Electrical Power & Energy Systems, 2014
- Heysem Kaya, Pınar Tüfekci, Sadık Fikret Gürgen, Proceedings of ICETCEE 2012, Dubai

**Special Mentions:**
We extend gratitude to Pınar Tüfekci and her co-authors for providing the dataset, facilitating research in power plant efficiency prediction.

**The Problem:**
Predict the net hourly Electrical Energy Output (EP) of a power plant.

**Why it's great:**
- It features clean, real thermodynamic variables: Ambient Temperature (T), Ambient Pressure (AP), Relative Humidity (RH), and Exhaust Vacuum (V).
- **Regression Challenge:** It is highly realistic and has almost no missing data. Temperature and Exhaust Vacuum have a very high negative correlation with energy output (as it gets hotter, thermodynamic efficiency drops). This is an ideal benchmark dataset for standard Multiple Linear Regression.


## Recommended Workflow for Your Analysis:
- **Correlation Analysis:** Load the dataset, filter for numerical columns, and plot a **Correlation Heatmap** (e.g., using Python's ```python sns.heatmap(df.corr(), annot=True)```). Look for variables with the strongest positive or negative correlation to your target variable.
- **Scatter Plots:** Plot the strongest predictors against the target variable to verify the linearity assumption.
- **Regression Analysis:** Fit the model and evaluate the **R² score** (explanatory power) and individual variable **p-values** (statistical significance).

## Quick Tip for Engineering Data
When working with these datasets, always check the **VIF (Variance Inflation Factor)** or run a correlation heatmap first. In physics and engineering, variables are frequently dependent on each other (like Temperature and Pressure via the Ideal Gas Law), meaning you will likely need to deal with **multicollinearity** before finalizing your regression coefficients
