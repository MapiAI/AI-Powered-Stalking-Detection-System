# AI-Powered-Stalking-Detection-System
Building AI course project

##Summary
Develop an AI system to identify stalking messages (potentially expandable to mobbing and bullying) and generate alerts to notify authorities or guardians. It functions similarly to spam detection algorithms, applying logistic regression or other methods to accurately identify stalking messages.

## 1. Background
**Problem**: Stalking, mobbing, and bullying are pervasive issues affecting individuals' mental health and safety. The lack of automated systems to detect such messages on popular messaging platforms like WhatsApp exacerbates the problem.

**Prevalence**: These issues are alarmingly common, with millions of cases reported globally each year.

**Motivation**: Personal safety and mental well-being are critical. An effective detection system could help protect vulnerable individuals by providing timely alerts.

**Importance**: Creating an automated alert system can significantly reduce harm by prompting timely interventions.

## 2. Data and AI Techniques
**Data Sources**: Utilizes data from messaging platforms, pre-labeled datasets of stalking, mobbing, and bullying messages. These sources need to be carefully curated to ensure data quality and representativeness.

**Techniques**:
- **Logistic Regression**: Suitable for binary classification problems.
- **Natural Language Processing (NLP)**: For text analysis and feature extraction.
- **Machine Learning Models**: Potential use of models like Random Forest, SVM, etc.

**Example Code**:

```python
from sklearn.linear_model import LogisticRegression
from sklearn.feature_extraction.text import TfidfVectorizer

# Example data
messages = ["I'm watching you", "Meeting at 5", "I know where you live"]
labels = [1, 0, 1]  # 1 = stalking, 0 = non-stalking

# Vectorization
vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(messages)

# Model
model = LogisticRegression()
model.fit(X, labels)
```

## 3. Use Case and Target Audience
**Context**: Implementation as an add-on service for messaging platforms like WhatsApp.

**Users**: Individuals at risk, guardians of minors, educational institutions, and law enforcement agencies.

## 4. Challenges
**Limitations**:
**False positives/negatives**: Need for high precision and recall.

**Data privacy concerns**: Ensuring user data is handled ethically.

**Dynamic language**: Adapting to evolving language and slang used in stalking.

## 5. Future Directions
**Expansion**:

Broaden scope to include mobbing and bullying.

Integration with more platforms.

Continuous model improvement with real-time feedback and updates.
