What is Feature Engineering

Process of creating new features from existing data

Helps ML models learn patterns more effectively

Improves model accuracy and performance

Why Handling Missing Values Matters

ML models cannot handle missing (NaN) values

Missing data can bias predictions if ignored

Proper filling preserves data consistency

Missing Value Treatment Used

Age: Filled with median (robust to outliers)

Embarked: Filled with mode (most frequent category)

Cabin: Dropped due to excessive missing values

New Features Created

FamilySize = SibSp + Parch + 1

IsAlone = 1 if passenger is alone, else 0

Why Encoding is Necessary

ML algorithms work only with numerical data

Categorical text data must be converted to numbers

Prevents model errors and misinterpretation

Encoding Methods Used

Sex: Label Encoding (male = 0, female = 1)

Embarked: One-Hot Encoding

Pclass: Used as numeric feature

Final Outcome

Dataset contains only numerical features

Data is clean and ready for model training
