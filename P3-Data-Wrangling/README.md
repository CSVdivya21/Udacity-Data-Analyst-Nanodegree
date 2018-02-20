# Wrangle and Analyze Data 

## Introduction

Real-world data rarely comes clean. This project on ‘Data Wrangling’ involves 3 main steps namely:- 
1. Gathering 
2. Assessing 
3. Cleaning
Throughout this project several python libraries will be used to gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it.

## The Dataset

The dataset that i will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people’s dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because “they’re good dogs Brent.” WeRateDogs has over 4 million followers and has received international media coverage. WeRateDogs  downloaded their Twitter archive and sent it to Udacity via email exclusively for you to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. 

## Data Wrangling

1. Gathering 
There are 3 data files (obtained from 3 different sources) used in this project :- 
* Enhanced Twitter Archive  
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column  of the archive does contain though: each tweet's text, which is used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." The 5000+ tweets have been filtered for tweets with ratings only (there are 2356). This is downloaded manually and then stored as ‘twitter_archive.csv’ file. 
* Image Predictions File   
This file is full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images). This file is downloaded programmatically using the Requests library and the following URL: 
https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-
predictions.tsv and then saved as ‘image_pred.tsv’ . 
* Additional Data via the Twitter API  
This file contains 2 columns - retweet count and favorite count which are gathered by querying Twitter's API using tweet_ids from twitter_archive file . Then its stored as a text file called  ‘tweet_json.txt’ . Then this .txt file is read line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count. 
2. Assessing 
This step involves assessing the 3 datasets collected above (from 3 different sources) both 
visually and programmatically and find out quality and tidiness issues.
3. Cleaning 
The cleaning step has 3 steps :-
* Define
* Code
* Test