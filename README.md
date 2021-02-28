Group 48 Data Science Project
----------
Project Title : Movie Rating Prediction
----------
**Student names:** <br />
Thushal Babukumar - 46154469 <br />
Pratik Dipak Raut - 46147888 <br />
Daryll Ralph D’Costa - 45841217 <br />
Saurav Anil Dubey - 45835551 <br />

***Movie Rating Predictions***

The digital revolution (also known as Third Industrial Revolution) is the shift from mechanical and analogue electronic technology to digital electronics. Nowadays, we hardly see people renting physical copies of movies. We are currently living in a world of instant gratifictaion. With a click of button, or a tap on a screen, media consumers are given their desired entertainment within seconds after requesting it. Movie Rating Predictions may help as a deciding factor whether to watch an upcoming movie or not. Prediction Systems is generally used for estimation of some variable of interest at some specified future date. Usually it is based on statistical and time series forecasting method. The science of prediction systems can generate future insights with a significant degree of precision. As several movie release every year, there are lots of data to study and analyze.

***Project Goal***

-  To predict the rating of a movie, that may help as a deciding factor for a user.

The outcome of this project can be applied in various social media applications, web applications, mobile applications in order to improve recommendation system. 

***Data Source and Background***

We used datasets from TMDB. The website provides various API to retrieve useful information for our movies. We used available API's to retrieve information such as cast & crew, vote count, genres, production countries, productions companies, language, release date and runtime.
Ratings corresponding to our 45000+ movies is retrieved from MovieLens. The two datasets had common Movie ID's which made it easier to merge. There are multiple data files namely:
- links.csv - Contains movieId, imdbId and tmdbId. (Used to link ratings, movies_metadata and credits)
- ratings.csv - Contains userId, movieId, rating of a movie.
- movies_metadata.csv - Contains movie budget, movie title, movie genre, imdbId, revenue, runtime, vote average, vote count, popularity of a movie, etc.
- credits.csv - Contains information about cast, crew and id of a movie.

Data source links: <br />
TMDB: https://www.themoviedb.org/documentation/api <br />
GroupLens: https://grouplens.org/datasets/movielens/latest/ <br />

***Data Format***

We downloaded a zip file containing various csv files: credits.csv, movies_metadata.csv, ratings_small.csv, links.csv, etc.

***Notebook Contents***

The notebook contains the folder 'data' which holds all the .csv files. Since the data files are too large, the contents are cut down and uploaded. <br />
The file finaladddf which contains movies_metadata and ratings merged together. <br />
The file Data-Cleaning where all the cleaning techniques are used to filter out raw data and get necessary data for analysis. <br />
The file Data-Analysis where evlauation and modelling is done. <br />
The .ppt file of our video presentation.


***Data Cleaning***

**> Extracting necessary data**

The first step commenced by extracting the main actors and directors from credits.csv. The extacted information is merged with movies_metadata. Next, the Id colunms of movies_metadata is made consistent using links.csv. Once the Id colunm is consistent, ratings.csv is merged with the movies_metadata giving the required data for analysis. 

**> Duplicate and missing values**

There were several duplicate records in the datasets which would have caused problems during modeling or plotting. For instance, the possibility that same people watch different genres of movies or rate the same movie twice. All duplicate values were dropped using the drop function.
Many cells in the columns were aslo empty. These cells were also discarded.

***Data Analysis***

**> Relationships**

The analysis is carried out by evaluating different relationships. We explore the features that affect the ratings and profits of a movie. Using bar plots we first examine the number of movies released in a month and in particular days. Using this information we analyse the profits generated as a result of particular day. We then use scatter plots to analyse the correlation between vote count and vote averge. Further, we observe the correlation between the runtime and profits of a movie. We also explore the profits and ratings with respect to the runtime of a movie. Effects of features like budget and genre on the profits and ratings of a movie are summarised.

A brief comparison of the relationship between average movie ratings and profits is studied. A correlation plot between average ratings, runtime, revenue, budget, profit and number of votes is visualised to have a better understanding. Various other relationships are also explored and visualised in the notebook.

**> Modelling**

Recursive Feature Estimation (RFE) is used to extract the best features. It is observed that there are nine major features. These features are used in various classification models to predict the rating of a movie. The accuracy score, RMSE, R2 score and MAE are calculated for each model. A plot visualising the outcome of each classifier is created. The SVM model is chosen as it has the highest accuracy of about 70%. Finally, t-test is performed to find statistical significance.
