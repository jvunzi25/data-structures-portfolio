# How strongly does daily nightly screen time affect an individual's average night's sleep duration? 
---
## Introduction
In life, sleep is one of the most essential factors influencing overall well-being, mood, and daily productivity. Not getting enough sleep can raise risk of disease, disorders, low mental health and even strokes and heart diseases (National Institutes of Health, 2021) . Studies show that people should have 7 - 9 hours of sleep. However, this time people use their hours of sleep on their phone doomscrolling. Doomscrolling is spending an excessive amount of time on your phone scrolling through social media. Doomscrolling causes higher levels of stress, anxiety, and emotional burnout. It can also lead to headaches, tight muscles, high blood pressure, and trouble sleeping. The goal of my project is to find out how strongly does daily nightly screen time affect an individual's average night's sleep duration? Predicting an individual's total nightly sleep duration based on their nightly screen time and habit data. My target variable is the sleep hours they get(y) and night screen time(x). This is definitely a regression problem because I'm predicting numeric variables. Students and people that work really would benefit from this prediction to better manage their bedtime habits. 

## Data Description
To find the results to my research question I went on Kaggle to see if there were some surveys or anything that correlates to my question. I found a data set called: [Sleep & Doomscrolling Habits Dataset](https://www.kaggle.com/datasets/harpartapsingh13/sleep-and-doomscrolling-habits-dataset/data) where they surveyed 1000 people asking about their nightly screen time hours, how many hours do they sleep, which serve as my features.Each row in the dataset represents an individual survey respondent's daily habits and sleep metrics. A potential feature that I actually use is their sleep quality. Another potential feature is their age. The data collection relies on self reported survey responses so I could introduce potential biases. Some individuals may underestimate their screen time and overestimate their sleep duration.

## Data Visualization and Understanding

<img width="563" height="454" alt="099d90ad-9c03-4b08-9a9c-bcfde454c343" src="https://github.com/user-attachments/assets/160f1e30-5908-4a8f-b18a-abf88dd4936f" />

As you can see I made a linear regression of the sleep hours per night and bedtime screen time in minutes. In this data we see that in the 0 - 50 minutes of bedtime screetime majority of the plots have a high sleep hours per night, but the more nightly screentime the less sleep they get. That means it's more right skewed heavy. There could be a potential outlier on the plot that has more that 200 screen time minutes 

<img width="769" height="469" alt="db950c5a-7903-41e2-8b6f-34251717e170" src="https://github.com/user-attachments/assets/d94190cb-1bae-4b06-8f89-a030519c21b7" />

I made a logistic regression using the best screen time and a potential feature, their sleep quality. This uses their probability on how good their sleep is based on their screentime. 

The linear regression really helped me with the correlation between the variables and their potential relationships with the target. Exploring scatter plots revealed a clear negative correlation between nightly screen time and sleep duration, confirming screen time as a key feature to retain.


## Data Preparation
There weren't any missing values in this data set which was very good but I didn't really have to deal with outliers because the outlier that was in the data really made my prediction better so I just left the outlier. One main thing I had to deal with was unnecessary columns. So I made a variable called “needed_columns” where I added the necessary columns I needed and used “df = df[needed_columns]” to only put the columns that I needed into my dataframe. I did encode a categorical variable(“sleep_quality_category”)to make the  logistic regression model and turned the variable into a probability variable. No features directly encode or indirectly reveal the target variable.

## Model description
The models I trained were logistic regression and linear regression. The baseline I established was to predict the mean sleep duration for every respondent in the dataset. These models were appropriate to my prediction problem because both predicted how damaging doomscrolling is for your sleep; my linear regression was trained to predict continuous sleep duration based on the bedtime screen time and my logistic regression was trained to classify whether an individual sleep quality was based on their screen time. In my models I did not tune any model settings or hyperparameters. I ensured the models were compared fairly because i didnt use the individual's age because based on the internet the younger you are the more sleep you should get but I only used the 7 - 9 range. 

MAE and RMSE are appropriate because they measure average prediction error in the same units as the outcome. Also R2 is useful for explaining how much variance is explained. There’s no explicit baseline model reported, however the only performance evidence is the regression line appears to track the scatter plot trend and the logistic probability curves show how predicted class probabilities change with screen time. I selected my linear regression model because it describes my prediction question more than my logistic regression. The tradeoffs during my final approach was that linear regression is easy to interpret and my logistic regression is ideal for classification and probability estimation.

The model learned a negative linear relationship between bedtime screen time and total sleep duration.Specifically, the model's regression coefficient indicates that for every additional 30 minutes of nightly screen time, predicted sleep duration decreases by approximately 45 minutes. The feature that appeared the most influential is definitely the bedtime screentime how I used it in both models and the large negative regression demonstrates that relationship with sleep hours. The model performs well between the 20 and 90 minutes where the screen time usage was moderate until it turned into a consistent downward trend. "Analyzing the regression coefficients shows that bedtime screen time has a negative slope confirming that screen time reduces sleep duration. Analyzing the regression residuals indicates that while screen time is a major contributor to sleep loss, extreme sleep deprivation is likely influenced by additional unmeasured factors. The conclusion that can be drawn for the model is that bedtime screen time and doomscrolling does have a strong inverse relationship with sleep duration; screen time can predict sleep hours for average users. What cannot be drawn from this is that we cannot state screen time as the only predictor of lack of sleep, it's possible for people who suffer from something like insomnia starts doomscrolling because they cannot sleep.

## Limitations, Ethics, and Reflection
There's definitely biases in this dataset that I mention, like people underestimate their screen time and overestimate their sleep duration and also people have a condition like insomnia that they end up doomscrolling because they cannot sleep. Incorrect predictions can affect many people who overestimate/underestimate sleep; they might experience unnecessary anxiety about their sleep hygiene if I predict that they should get more sleep which they don't or someone might doomscroll more if I predict that they should get less sleep which they don't. Those examples can have false positive and false negative consequences. This model would and wouldn't be appropriate for real-world decision-making. It's not appropriate because people could have insomnia and it could be appropriate as an informal, educational feature inside a wellness app or habits tracker to raise user awareness about bedtime habits. If I did have more time I would explode their caffeine intake and if they did have a condition. Users should understand that Reducing screen time alone might not automatically cure sleep issues if health conditions are present and this model predicts population averages, not guaranteed personal outcomes. 

--- 
Code:
Click here to access my code for this project

Reference and transparency:
Dataset: Singh, H. (2024). Sleep & doomscrolling habits dataset [Data set]. Kaggle. https://www.kaggle.com/datasets/harpartapsingh13/sleep-and-doomscrolling-habits-dataset/data 


National Institutes of Health. (2021, April). Good sleep for good health. NIH News in Health. https://newsinhealth.nih.gov/2021/04/good-sleep-good-health 

Ai tool: i used copilot to help me with both of my models and i used google gemini to help me out with essay and to problem solve for my visuals. 
