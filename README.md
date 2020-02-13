# Movie Spoiler Analysis
#### Dataset
IMDB Spoiler Dataset (https://rishabhmisra.github.io/publications/)

  - 573913 records
  - 150924 spoiler reviews

#### Technology Stack
  - Pandas
  - SKLearn
  - NLTK
  - Matplotlib
  - Seaborn
  - IMBLearn
#### Process
  - EDA
  - Data Cleaning
  - Modeling  
  - Model Mutations: We went through four main mutations of our model. We can up with an initial baseline and then tweaked our cleaner function to collect a cleaner/better collection of words. We referred to this model as M1. We then added custom stop words as well as bigrams.This model was known as M3. We noticed the bigrams actually decreased the performance of our model however and removed them for the next model. M4 kept the custom stop words. For this model we also wanted to dig deeper into feature engineering and decrease the amount of processesing power required we subsampled our data to a collection of 10,000 Spoiler and 10,000 Non-Spoiler. We added Review Length as a new feature.
  
   
#### Results
M4 does a good job of what we originally intented. It's accuracy is not ideal, however, the recall on the Spoilers group is 91%. Our model would prevent a potential viewer from read the vast majority of reviews but it would also unfortunately falsely label a large amount of Non-Spoilers as the Spoiler group.

#### Conclusions/Moving Foward
Neural Network/Deep Learning so the model can understand the actual meaning of the words.
