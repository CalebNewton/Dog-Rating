# Dog-Rating

Data from 2356 of the 5000+ tweets from the @dog_rates twitter account that were published between November 15, 2015 and August 1, 2017 are included in the WeRateDogs Twitter archive. This information consists of dog ratings that were extracted from the tweet's text together with the dog's name and stage, if they were given. I had to obtain this additional information from the twitter account using the tweet ID from the archive because the retweet count and favorite count for each tweet were not included in the improved archive. I obtained an image predict file from Udacity servers that had the top 3 dog breed predictions based on the photographs from the tweets together with the Twitter data.

# Data Wrangling of Quality & Tidiness Issues

## Quality issues
* Dogs without names, but given names of "a" or "an" instead of "None"
* incorrect datatype in columns 'rating numerator', 'rating denominator', source and timestamp should be fixed.
* Tweet_id has a wrong datatype in all the 3 data files
* Some rows possess redundant retweets
* Some rating_denominator do not equal 10
* Some columns aint needed for our analysis hence, drop in_reply_to_status_id, in_reply_to_user_id, expanded_urls and img_num columns from image_predict column
* Since source column contains over 90% duplicates, the column should be dropped
* The text column contains a url which should be removed

## Tidiness issues
* 4 columns in twitter_archive data exist as dog stages i.e doggo, floofer, pupper and puppo
* The json_data file should be combined with the twitter_archive file

## Questions to Investigate

* 10 Most Popular Dog breeds
* 10 Least Popular Dog breeds
* Dog breeds with over 50000 likes and retweets
* Most Common Dog stages

## Summary of Findings

* Golden retriever was the most popular dog breed
* Malamute was the least most popular amongst the top 10. About 8 dogs were the least popular breeds
* A total of 113 unique breeds existed. Wire-haired_fox_terrier and Australian_terrier were the most popular amongst the 10 least poular breeds
* Puppies are referred to as "pupper" or "puppo", older puppies as "doggo", and older doggo as "floofer". People love puppies, as analysis and visualization have shown. The most liked and retweeted of all were puppies.
