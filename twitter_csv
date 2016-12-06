#loading tweets from twitter with search ketword and store in csv file.
#if library does not exist, please uncomment below code
#install.packages(twitterR)
#install.packages(tm)

library(twitteR)
library(tm)

#get api key,secret,token from http://dev.twitter.com
api_key<-"<your twitter development api key>"
api_secret<-"<your twitter development api secret>"
access_token<-"<your twitter development access token>"
access_token_secret<-"<your twitter development access token secret>"
#Twitter authentication with R
setup_twitter_oauth(api_key,api_secret,access_token,access_token_secret)
keyword <- "<search keyword"
Tweets <- userTimeline(keyword, n=100)
dataframe <- do.call("rbind", lapply(Tweets, as.data.frame))
#dim(df)
write.csv(dataframe,'D:\\tweetdata\\tweet.csv')
