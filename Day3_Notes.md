DAY 3 — Exploratory Data Analysis (EDA) & Visualization

Dataset: Titanic Dataset

🔍 1. Basic Inspection

Performed initial data inspection using:

df.shape → Dataset dimensions

df.columns → Feature names

df.info() → Data types & missing values

df.describe() → Statistical summary

This helped understand dataset structure and quality.

🧹 2. Missing Values Handling

Identified missing values using df.isnull().sum()

Age: Missing values filled using median (robust to outliers)

Cabin: Dropped due to excessive missing data

Embarked: Filled using mode

Decision based on data importance and missing percentage.

🧮 3. Feature Types
Categorical Features:

Sex

Embarked

Pclass

Survived

Numerical Features:

Age

Fare

SibSp

Parch

This separation helps in choosing correct visualization and preprocessing techniques.

📊 4. Data Visualization

Created 6 mandatory plots using Matplotlib & Seaborn:

Survival count plot

Gender vs Survival

Passenger Class vs Survival

Age distribution

Fare distribution

Correlation heatmap (numeric features only)

Visualization helped reveal hidden patterns and relationships.

🧠 5. Key Insights

Females had a significantly higher survival rate than males due to evacuation priority.

1st class passengers survived more compared to 2nd and 3rd class.

Children showed better survival chances than adults.

Higher fare passengers had higher survival probability.

Passenger class negatively correlated with survival, while fare showed positive correlation.

✅ Conclusion

EDA revealed that gender, passenger class, and fare were the most influential factors in survival prediction.
