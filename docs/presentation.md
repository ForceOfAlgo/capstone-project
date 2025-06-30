# Presentation Notes

## Executive Summary
- This project forecasts e-payment transaction growth across 20 economic sectors in Bahrain, segmented by credit and debit card types.
- It extends my dissertation work from June 2024 by incorporating real transaction data from 2022-2024 to predict 2025 outcomes.
- The analysis supports decision-makers in assessing expected growth or decline in specific sectors.

---

## Overview of the Final ML Model and Its Parameters
- Selected model: **Random Forest (oversampled)**, with best performance on validation data.
- Final tuned hyperparameters:
  - `n_estimators`: 300
  - `max_depth`: 30
  - `min_samples_split`: 2
  - `min_samples_leaf`: 1
  - `bootstrap`: True
- Multi-class classification was implemented to handle predictions across 20 sectors.

---

## Model Performance Summary
- Training accuracy: **100%** (oversampled)
- Validation accuracy: **90.6%**, with a manageable gap indicating good generalization.
- Precision, recall, and F1-scores confirmed robust performance, especially important given the class imbalance.
- Oversampling effectively addressed sector imbalance, leading to more reliable forecasts.

---

## Results Highlights
- Predicted transaction values for 2025 segmented by sector and card type (credit and debit).
- Calculated expected growth percentages to pinpoint sectors with highest predicted increases:
  - **Education**: +321.7% forecasted growth.
  - **Miscellaneous Goods & Services**: +506.4% forecasted growth.
  - **Transportation**: +228.6% forecasted growth.
- Identified sectors with expected declines, allowing for proactive strategy adjustments.

---

## Conclusion
### Summary of Achievements
- Built a reliable forecasting model using real data from Bahrain.
- Extended prior research with detailed card-type forecasts.
- Achieved high accuracy through careful preprocessing, balancing, and hyperparameter tuning.

### Future Improvements
- Integrate time-series modeling for monthly/quarterly forecasts.
- Include additional features such as macroeconomic indicators.
- Explore deep learning models for potential performance gains.

### Lessons Learned
- Data balancing is essential for multi-class classification across many categories.
- Feature engineering, including card type and CPI, was key to improving accuracy.
- Regular model evaluation prevents overfitting and supports more trustworthy forecasts.

---

## Notes
- This script serves as a guide for presenting the project during meetings, demos, or sharing on GitHub.
- Replace sector-specific or proprietary details if making the repository public.

