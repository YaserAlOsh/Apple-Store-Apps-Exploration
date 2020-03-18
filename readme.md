# Apps Features that affect ratings on the Apple Store
## by (Yaser Haitham AlOsh)


## Dataset

> The data set is of Apple Store apps, it contains many features or variables for each app. 
I got the data from Kaggle. https://www.kaggle.com/ramamet4/app-store-apple-data-set-10k-apps
Features are documented in the same page.
There are 7197 rows. I removed two duplicate apps that had different versions, to end up with 7195 unique apps.
Data Wrangling I have done:
- Rename column names
- Remove to duplicate apps (two rows)
- Remove useless columns 
- Convert columns to appropriate types where needed.
- Convert size_bytes column values to megabytes

## Summary of Findings

> I have found that a larger percentage of Paid apps have got high ratings (above 4.0) than Free apps.
 I have also noted that as Paid apps get pricier their average ratings get better, 
 and their total ratings count also decrease,since less users would buy pricy apps.
 I thought at first that the increase in average ratings was only because the total ratings were less, 
 but further investigation showed that as the total ratings increase, the average ratings get better, 
 which negates what I have presumed.
 Also, prices seldom went above 30-35$. And when examining prices per Genre, 
 I noted that most genres had apps priced less than 10$, while lots of games go up to 35$. 
 Continuing my per genre investigation, it was shown that some Educational, Utilities,
 and Work related genres had more Paid apps than Free.
 Initial observations suggested making Paid apps for those genres, since you would have better chance of success. 
 But with multivariate exploration of genres and ratings (Both average and total), 
 I was surprised to know that these specific genres actually had better average ratings for their free apps, 
 while all other genres (e.g. Games, Entertainment..) had better ratings for their Paid apps.
 Further investigation pointed out that almost all genres have more total ratings for Free apps, 
 which means a much larger % of users would use Free apps over Paid apps, up to 10x for Utilities and 5x for Educational apps. 
This explains how looking at one measure only can be misleading. 
Looking at the following variables at once: average ratings, total ratings, per Genre for Free vs Paid apps, through one plot, 
revealed important insights for developers to know which type is best for each genre, Free or Paid:
Specific genres have better support for Paid apps, mainly those which are niche and have a small audience. 
If one is creating a game app, it can be Free or Paid  and it would produce similar resuls as per ratings.
Other genres have a strong competition and you can hardly succeed with a Paid app, such as Social Networking.

Other features of interest proved helpful; I discovered that most apps with large sizes 
are spread out on the higher levels of ratings. And that apps that support more than 4 languages
 usually had high ratings. Furthermore, those apps with larger sizes or wider support of languages weren't pricier,in fact,
 a lot of them were below 5$.
 One last variable, number of supported devices, seemed to have a weak negative relationship with the ratings; 
 more support of devices could introduce more stability issues for old devices thus attracting bad reveiws.
 
I explored relations between features that weren't about the ratings. 
Notably, Productivity, Social Networking and Photo & Video apps had more support for languages than other genres.
I have also found that Games had the largest sizes, followed by Educational apps. 
On the other side, Utilities and Social Networking apps had the smallest sizes.
About the support of devices, it seemed that all genres support the same amount of different devices,
which is probably why the number of suported devices variable didn't have a strong effect.

Another categorical variable which had a small effect is the content rating. Apps with content rating '17+' 
had  worse ratings distribution than any other content rating. That's probably because there is a 
relatively small number of '17+' apps, which makes the distribution quite inaccurate.

## Key Insights for Presentation

> I present factors that have large effect on an app ratings. Which are: Price, number of supported Languages,
 apps sizes and genres. I also present key differences between Paid and Free apps and how those 
 differences affect ratings and prices across genres.
 
 I start with introduction to our main feature,average ratings, presenting its distribution through a histogram.
 Then I show the first observation through a plot of average ratings vs price, and total ratings vs price, 
 followed by explaining useful insights.
 To introduce genres I present the frequency per genre, 
  followed by a box plot of average ratings per genre,
  showing how some genres have better ranking distributions than others.
 To explain which combinations of app sizes and languages are better, 
  I plot a 2d histogram for average ratings vs app sizes and vs languages.
 Drifting a little bit away from the main quest, and to show how this may differ across genres, 
 I plot a violin plot and a bar plot,
 showing average app sizes and average number of supported langauges per genre, respectively.
 Lastly, to end my investigation of genres effect, I plot a bar chart for each genre and hue the bars by the 
 Type (Paid or Free).
 Putting the total ratings on one side and the average ratings on the other side, helps in understanding
	whether Free or Paid apps are better for certain genres.
	
 After each plot, I try to draw conclusions and derive insights labeled as Tips for developers or Takeaways.


## Resources
This blog post helped me: https://nik-davis.github.io/posts/2019/steam-data-exploration/

 
 