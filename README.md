# DecisionTree_titanic
## Conclusion

This project explored survival prediction on the Titanic dataset using a Decision Tree classifier and demonstrated how feature engineering affects both performance and interpretability.

### Key Findings

- **Sex, Age, and Travel Class (Pclass)** are the strongest predictors of survival — consistent with historical “women and children first” evacuation policy.
- Adding **FamilySize** improves interpretability but does **not improve** performance for a Decision Tree model.
- Adding **Title** extracted from the passenger name introduces additional social-status information, which **increases model accuracy**.

| Model Version | Best Accuracy | Best Depth |
|--------------|:-------------:|:----------:|
| Baseline features | **0.8156** | Unrestricted |
| + FamilySize | 0.7993 | 4 |
| + Title | **0.8213** | 4 |

### Interpretation

- Decision Trees already capture family-structure information through **SibSp** and **Parch**, making FamilySize redundant.
- **Title** successfully encodes multiple important characteristics at once:
  - gender
  - social status and class
  - age category (e.g., “Master” for young boys)
  - special roles (e.g., officers)

As a result, adding Title improves both predictive power and historical interpretability.

### Final Takeaways

- Thoughtful **feature engineering** can outperform deeper or more complex models.
- Enhanced feature sets allow shallower trees to perform competitively → better generalization.
- Model behavior aligns well with real Titanic survival dynamics.

### Next Steps

- Try more advanced models (Random Forest, Gradient Boosting, Logistic Regression).
- Perform hyperparameter search and cross-validation.
- Expand domain features (ticket group size, cabin-deck extraction, marital status, etc.).

