# Analyzing-MovieLens-1M-Dataset

![ML-Header](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/movielens-header.png)

## Dependencies (pip install):
```
numpy
pandas
matplotlib
```

## DATA PRE-PROCESSING:

Initially the data was converted to csv format for convenience sake. Using different transformations, it was combined to one file. After combining, certain label names were changed for the sake of convenience. The age attribute was discretized to provide more information and for better analysis. The timestamp attribute was also converted into date and time. The dates generated were used to extract the month and year of the same for analysis purposes. The data was then converted to a single Pandas data frame and different analysis was performed.

## ANALYSIS:

**1) How many movies have an average rating over 4.5 overall?**

![Result-1](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-1.png)

**2) How many movies have an average rating over 4.5 among men? How about women?**

Men on an average have rated 23 movies with ratings of 4.5 and above. Women have rated 51 movies.

**3) How many movies have a median rating over 4.5 among men over age 30? How about women over age 30?**

Considering men and women both, around 381 movies for men and 381 for women have an average rating of 4.5 and above.

**4) Ten most popular movies:

We’ve considered the number of ratings as a measure of popularity. We believe a movie can achieve a high rating but with low number of ratings. Thus, just the average rating cannot be considered as a measure for popularity. Thus, a measure of popularity can be the maximum number of ratings a movie received because it can be considered to be popular since a lot of are talking about it and a lot of people are rating it.

![Result-2](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-2.png)


## CONJECTURES:

<p>
  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-3.png" align="left">

  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-4.png" align="right">
</p>

The age group 25-34 seems to have contributed through their ratings the highest. This implies two things. Firstly, it shows that the younger working generation is active on social networking websites and it can be implied that they watch a lot of movies in one form another. This information is critical. Also, we see that age groups 18-24 & 35-44 come after the 25-34. Hence, these age groups can be effectively targeted to improve sales. For example, we know that the age groups ’25-34’ & ’35-44’ are the working class and data shows they watch a lot of movies. Companies like Netflix can offer executive discounts to this lot of population since they’re interested in watching movies and a discount can drive them towards improving sales. A decent number of people from the population visit retail stores like Walmart regularly. Walmart can tie up with companies like Netflix or theatres and offer discounts to regular or loyal customers, thus improving sales on both sides. Whereas the age group ’18-24’ represents a lot of students. These companies can promote or let students avail special packages through college events and other activities. Also, looking at their average ratings, it shows they’re not very critical and provide open minded reviews. Thus, this class of population is a good target

<p>
  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-5.png" align="left">

  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-6.png" align="right">
</p>

The graph above shows that students tend to watch a lot of movies. Naturally, this habit of students is not surprising since a lot of students’ love watching movies and some of them view this as a social activity to enjoy with your friends. Also, further analysis proves that students love watching Comedy and Drama genres. This gives direction for strategical decision making for companies in the film industry. As stated above, they can offer exclusive discounts to students to elevate their sales.

![Result-7](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-7.png)

Icing on the cake, the graph above shows that college students tend to watch a lot of movies in the month of November. November indicates Thanksgiving break. Thus, targeting audience during family holidays especially during the month of November will benefit these companies.

![Result-8](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-8.png)

The histogram shows the general distribution of the ratings for all movies. The histogram shows that the audience isn’t really critical. A very low population of people have contributed with ratings as low as 0-2.5. Most of the ratings lie between 2.5-5 which indicates the audience is generous. Maximum ratings are in the range 3.5-4. Movies with such ratings can be used to analyze upcoming movies of similar taste and to predict the crowd response on these movies.

Table 1 below represents top 5 genre that were rated by maximum users and Table 2 represents top 5 Genre having 
on an average highest ratings:

<p>
  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-10.png" align="left">

  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-11.png" align="right">
</p>

Genre that were rated by maximum users may not be the true representation of movie ratings as ratings can be given by
users and bots. This represents high bias in the data.
On the other hand, Average rating in table 2 may have sampling biases which means it was rated by few users who rated movies high and ignore ones who rated movies low and that leads to high rating.

To overcome above biased ratings we considered looking for those Genre that show the true representation of 
ratings by considering legitimate users and by considering enough users or samples.

**Count + Rating:**

![Result-12](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-12.png)

The below scatter plots were produced by segregating only those movie ratings who have been rated more than 200 times. The average of these ratings for men versus women was plotted. It shows a similar linear increasing trend as in the scatter plot where ‘number of ratings > 200’ was not considered. Thus, people are like minded (similar) and they like what everyone likes to watch.

**Left Figure:** The below scatter plot shows that the average rating of men and women show a linearly increasing trend. It says that excluding a few movies and a few ratings, men and women tend to think alike.
 
**Right Figure:** Make a scatter plot of men versus women and their mean rating for movies rated more than 200 times.
 
<p>
  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-13.png" align="left">

  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-14.png" align="right">
</p>

### Compute the *correlation coefficent* between the ratings of men and women

![Result-15](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-15.png)

The correlation coefficient shows that there is very high correlation between the ratings of men and women. Thus, indicating that men and women think alike when it comes to movies. A correlation coefficient of 0.92 is very high and shows high relevance.

### Are the ratings similar or not? Support your answer with data!

As we can see from the above scatter plot, ratings are almost similar as both Males and Females follow the linear trend.

**Average Rating overall for men and women:**

| Female  | Male |
| ------- | ---- |
| 3.62036 | 3.568879 |

You can say that average ratings are almost similar. But there may be some discrepancy in above results because as you can see from below results, number of movies rated for men is much higher than women.

**Number of Movies Rated:**

| Female  | Male |
| ------- | ---- |
|  246440 | 753769  |

Though number of average ratings are similar, count of number of movies largely differ. Hence, we cannot accurately predict just on the basis of this analysis. More filtering is required.

### Conjecture under what circumstances the rating given by one gender can be used to predict the rating given by the other gender.


<p>
  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-16.png" align="left">

  <img width="400" height="300" src="https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-17.png" align="right">
</p>


These genres are highly rated by men and women both and on observing, you can see a very slight difference in the ratings. This implies that they are similar and they prove the analysis explained by the scatter plots.
These are some of the special cases where difference in Rating of genre is greater than 0.5. This value is not large enough though. Hence we can use to predict a general trend that if a male viewer likes a certain genre then what is possibility of a female liking it.

![Result-18](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-18.png)

From the crrelation matrix, we can state the relationship between Occupation and Genres of Movies that an individual prefer. For Example: Farmer do not prefer to watch Comedy|Mistery|Thriller and College Student Prefer Animation|Comedy|Thriller.

![Result-19](https://github.com/ddhaval04/Analyzing-MovieLens-1M-Dataset/raw/master/images/result-19.png)

We can find out from the above graph the Target Audience that the company should consider. For Example: College Student tends to rate more movies than any other groups. Moreover, company can find out about the gender Biasness from the above graph. For Example: there are no female farmers who rates the movies



