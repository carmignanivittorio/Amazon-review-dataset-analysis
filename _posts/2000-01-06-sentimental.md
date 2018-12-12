---
title: "Sentimental Analysis"
bg: purple
color: black
---

<br>
## Sentimental Analysis
{: .center}

Here, We will explore the sentiment of the reviews. In order to accomplish this task we are going to use the word list provided by SentiWords ([***Page link***](https://hlt-nlp.fbk.eu/technologies/sentiwords); [***References***](http://hltdistributor.fbk.eu/license.php?licenseId=f99f59c080464addad699f91bd8c190e)). This list contains **150'000** words (which include collocations). Moreover, We changed the interval of values from [-1,1] to [0,100].

<br>

### Categories vs Star rating
We want to see if the headline better catches the sentiment of the review comparing with the body, as resulted in tf-idf body vs headline (star rating). We have plotted 2 graphs, which show the same data, to have a more clear overview of the outcomes.
{: .left}

![line charts](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20charts.png)
{: .center}

<br>

![newheatmap](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/new_heatmap.png)
{: .center}

* From both graphs, it is verified the fact that the sentiment grows together with the star rating for all the categories.
* As we imagined, the headline better catches the sentiment. In fact, the headlines' interval has a range of values approximately doubled respect to the body's one; [48,65] vs [50,59].
* Another fact worth noticing in the graph is that, the general reviews sentiment is more than 50. Since 50 represents the neutral value, it means that the reviews are almost always "happy" (if "happy" is considered above 50) but they do not exceed. This behaviour could be explained by the fact that people try to be impartial in the process of reviewing. The interesting thing is represented by fact that people are equitable "only" with low rating. In contrast, they are more willing  of writing "happy" words if the products satisfied their need (more stars). This is strange in the sense that, generally, it is easier to "judge".
* The Baby's reviews with 5 stars seems to be the happiest. This is reasonable, in the sense that the category Baby is the "cuteness" among these categories.
* In contrast, all the technological equipment (Video, Camera, Video Games, ...) contains sadder reviews in general.
{: .left}

<br>

### Best Categories
{: .center}

Let's understand which are the happiest/saddest categories. Then, let's see the categories' sentiment distribution.
{: .left}
<br>
![categories sentiment distribution](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/categories%20sentiment%20distribution%20new.png)
{: .center}

<br>
***Plot explanation*** : in this plot, there is a lot of information which will be explained. Firstly, the plot shows the sentiment distribution for each category. Each box has a different shape based on how the review's sentiment is distributed. Secondly, the black line which can be found in each box represents the average. As you can see, the categories are plotted in order respect to this value. All the boxes have approximately the same shape, width, and height. It does not mean that they have the same number of reviews but, the distribution is normalized based on the own values. To see the difference in the number of values, the grey things over the boxes were plotted. Specifically, each point is a review and its position is based on its sentimental value. In fact, you can see that Music and DVD have a lot of reviews comparing to Shoes. Moreover, it can be seen that in the tails appear fewer points (because they represent exceptions in terms of sentiment).

**Outcomes**:
* From this plot we can say that there are not many differences between the distributions.
* Video and Baby are the "happiest" category with an average sentiment value about 63.
* In contrast, Music and Watches are the "saddest" with an average sentiment value about 55, which is still a "happy" value.
* It is reasonable to think that this data is biased by the large presence of "5-star reviews". Since this plot does not show the distribution "in details", an additional "more classic" graph will be created.
{: .left}
<br>
<br>
![joy plot](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/joy%20plot.png)
{: .center}
<br>
This graph is more detailed. In particular, it can be observed that most of the distributions present 2 peaks, approximately in 50 and in 65. As we said before, this is probably due to the fact that the distribution of the reviews (in terms of star rating) is not uniform. Interpreting these peaks, it is logical to think that the reviews are either neutral (50) or relative happy (65). These abnormalities are more visible in _MobileApps_ and _Video_. This behavior was not captured by the previous graph. In our opinion, it was due to the fact that the 2 peaks were contained in the "main box" for each category. In addition, looking at the tails, it seems that _MobileApps_ has significant numbers of "haters", with values near 25, and "lovers", with values near 85.
{: .left}
<br>

### Funny measurements
{: .center}
<br>

In the notebook we performed some funny measurements like: worst/best product, happiest/saddest reviewer, best days/months. We report here the graphs about the best days:
{: .left}
<br>
![sentiment headlines](https://raw.githubusercontent.com/carmignanivittorio/SocialGraphProject/master/img/sentiment%20headlines.png)
{: .center}

* Most of the times, the sentiment has risen together with the year. This is probably because people got used to buying and review products. Therefore they feel more comfortable throughout the years.
* There are no many variations looking at the days among the different categories. There are some exceptions. For example in Video, Wednesday is a really good day; in contrast, Sunday is not.
{: .left}
