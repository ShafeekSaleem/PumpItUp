# Pump it Up, Data Mining the Tanzania Water Table

## Data pre-processing and feature engineering

I used PandasProfiling to explore all of the columns in the data. The data had a few columns with a large amount of missing values. I imputed some of the columns with mean values and I chose to immediately drop few columns, due to the high volume of missing values. Imputing data or filling missing values would've altered the data too much. I converted boolean columns to strings and categorical columns to integers using LabelEncoder(). Also, I replaced NaN values with explicit 'nan' string format for ease of use in the later part.

Looking further into the data, there was also a decent amount of columns that were very similiar to one another. I examined these columns using value counts. If the columns were too similar, I chose to keep whichever one I thought was better and drop the other. Some columns were completely identical. This would help later on when I needed to make dummy variables for my classification models. Finally I normalized all the data columns using StabdardScaler(). Luckily from there, the data was pretty clean and I was comfotable to start running some models.

## Training

I used different models with different parameter space to compare the results. Ensemble based models gave better results. Both Random forest and XGBoost gave similar results and wwas able to achieve an accuracy of 81% on test dataset and 80.96% accuracy on the final leaderboard. I also plotted the feature importance graph to see which feature influenced the model most. 
