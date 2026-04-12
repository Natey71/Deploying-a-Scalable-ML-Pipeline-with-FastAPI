# Model Card

For additional information see the Model Card paper: https://arxiv.org/pdf/1810.03993.pdf

## Model Details

This model uses Random Forest classifier from scikit-learn.
The purpose of this supervised learning model is to predict wheter and individual salary is more than 50k per year, and is trained locally using Python 3.10. The model is saved in `model/model.pkl` folder of this repository.

## Intended Use

**This model should be used purely for educational purposes and not for any production environment or real world decision making.**

It shows how to build a machine learning pipeline that includes data processing, cleaning, model traiing and automated CI/CD pipelines using GitHub Actions. API's are built using FastAPI to access the model and data within this repository. 

## Training Data

The model is trained on *Census Income Dataset*, that included demographic and employment data. 

Information in dataset
- Workclass
- Education
- Occupation
- Race
- Sex
- Salary
- Martial Status

## Evaluation Data

Using 20% of the dataset for testing against the other 80% that the model was trained on for accuracy. The evaluation includes both overall performance across individual categories such as sec, race, occupation.

## Metrics
_Please include the metrics used and your model's performance on those metrics._
- Percision: 0.7419
- Recall: 0.6384
- F1 Score: 0.6863

Examples of slice performance
- **Sex: Male** Males had higher recall compared to female
- **Workclass = Private** Individuals that worked in private sectors, had moderate precision
- **Education** Had a huge impact on training and individuals income

## Ethical Considerations

Census data contained demographic information and may reflect historical biases, and training on the data can aplify these biases. 

## Caveats and Recommendations

- Data could be outdated and doesn't reflect current demographics or populations
- Model is for learning purposes only
- This model was not tuned or optimized, using parameters that are default to Random Forest Classification