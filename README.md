# Movie Spoiler Analysis
#### Dataset
IMDB Spoiler Dataset (https://rishabhmisra.github.io/publications/)

  - 573,913 records
  - 150,924 spoiler reviews

#### Technology Stack
  - Pandas
  - SKLearn
  - NLTK
  - Matplotlib
  - Seaborn
  - IMBLearn
#### Process
  - EDA
  - Data Cleaning: We first used a ReGex-based cleaner to translate each review into a list of individual words we could then lemmatize and tokenize. We were able to improve this process with a "cleaner" function utilizing python's built-in .isalpha() method, among others.
  - Modeling: Naive Bayes models outperformed Logistic Regression and Random Forest classifiers every time.
  - Model Mutations: We went through four main mutations of our model. We can up with an initial baseline and then tweaked our cleaner function to collect a cleaner/better collection of words. We then experimented by adding custom stop words as well as bigrams. This was the third attempt at our model. We noticed the bigrams actually decreased the performance of our model however and removed them for the next model. The fourth model kept the custom stop words. For this model we also wanted to dig deeper into feature engineering and decrease the amount of processesing power required. We subsampled our data to a collection of 10,000 Spoiler and 10,000 Non-Spoiler. We added 'Review Length' as a new feature to the model because we concluded the average individual review length of the two groups was statistically different.
  
   
#### Results
Model Four does a good job of what we originally intented. It's accuracy is not ideal, however, the recall on the Spoilers group is 91%. Our model would prevent a potential viewer from read the vast majority of reviews that contain spoilers but it would also unfortunately falsely label a number of Non-Spoilers as the Spoiler group.

#### Conclusions/Moving Foward
Our next steps would be:
- Implement Neural Network/Deep Learning so the model would be able to better understand the actual meaning of the words and thus make better decisions.
- Conduct an analysis of the false negatives to understand why non-spoilers were mislabeled.
