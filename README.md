# WeRateDogs Tweets - Wrangling
## by Monique van den Berg

## Dataset

This project is focused on the act of data wrangling the tweet archive of the Twitter account WeRateDogs. Data wrangling consists of gathering data from multiple sources, assessing the data for quality and tidiness issues and finally cleaning the data.

The WeRateDogs account rates and humorously comments about people's dogs. The ratings are mainly a score out of 10 or multiples of 10 if there are multiple dogs. Because "they're good dogs" the numerators are frequently a value larger than 10.

Three pieces of data were gathered for this wrangling project. The first piece was provided by WeRateDogs as a csv archive which consisted of basic tweet data. The second piece was a tsv file hosted on servers which needed to be programmatically downloaded using pythons request library. The tsv file contained the top three image predictions for the breed of dog shown in the tweet. The third piece of data was gathered by querying Twitter’s API named Tweepy. Using the tweet ids and Tweepy the retweet count and favorite count was gathered for each tweet in the csv archive.

After all three pieces of data were gathered the data was assessed visually by viewing all three pieces of data in their entirety. And programmatically with pandas to determine 8 or more quality issues and 2 or more tidiness issues. The following quality issues were detected: missing values, erroneous data types and wrong data. The following tidiness issues were detected: each variable didn’t form a column and each observational unit didn’t form a table.  

In order to clean the issues discovered during the assessment a copy was made of each piece of data and the define-code-test framework was used to guide the cleaning process. Cleaning was performed on the copied data pieces and consisted of removing some row entries and columns, converting wrong data types, merging pieces of data and determining the correct values. The cleaning process resulted in a tidy master dataset which was stored in a csv file.

## Summary of Findings

Insights:
1. Lucy is the most popular dog name and was mentioned in 10 tweets.
2. Pupper was mentioned 223 times and is the most mentioned dog stage.
3. Tweet with tweet id: 822872901745569793 and text: "Here's a super supportive puppo participating in the Toronto  #WomensMarch today. 13/10 https://t.co/nTz3FtorBc" is the tweet with the highest favorite count of 132810.
4. Tweet with tweet id: 666102155909144576 and text: "Oh my. Here you are seeing an Adobe Setter giving birth to twins!!! The world is an amazing place. 11/10 https://t.co/11LvqN4WLq" is the tweet with the lowest favorite count of 81.
5. Tweet with tweet id: 744234799360020481 and text: "Here's a doggo realizing you can stand in a pool. 13/10 enlightened af (vid by Tina Conrad) https://t.co/7wE9LTEXC4" is the tweet that has been retweeted the most number of times 79515.
6. Tweet with tweet id: 666102155909144576 and text: "Oh my. Here you are seeing an Adobe Setter giving birth to twins!!! The world is an amazing place. 11/10 https://t.co/11LvqN4WLq" is the tweet that has been retweeted the least number of times, only 16.
7. The tweet with the lowest favorite count and lowest retweet count is the same tweet with tweet id: 666102155909144576.
8. Tweet with tweet id: 749981277374128128 and text: "This is Atticus. He's quite simply America af. 1776/10 https://t.co/GRXwMxLBkh" is the tweet with the highest rating of 1776/10.
9. Tweet with tweet id: 835152434251116546 and text: "When you're so blinded by your systematic plagiarism that you forget what day it is. 0/10 https://t.co/YbEJPkg4Ag" is the tweet with the lowest rating of 0/10.
