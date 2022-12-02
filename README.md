# Twitter-erlang  
# 1. group members  
Xin Li, Yuhao Tian  
# 2. Project definition  
Implementing a Twitter Clone and a client tester/simulator  
# 3. Project requirements  
## 1) Implement a Twitter-like engine with the following functionality:  
  1. Create an account.  
  2. Post a tweet. Tweets can include mentions(@) and hashtags(#).  
  3. Follow a user's tweets Retweets.  
  4. Allow searching through tweets you've subscribed to, tweets using certain hashtags, and tweets that mention you (my mentions).  
  5. Deliver the aforementioned categories of tweets live if the user is connected.  
## 2) Use a tester to test the aforementioned  
  1. Reproduce as many users as we can.  
  2. Users' live connection and disconnect times will be simulated.  
  3. On the basis of the subscriber count, simulate a Zipf distribution. Increase tweet output for accounts with large subscriber bases. Retweet a few of these messages.  
# 4. How to operate  
  Init -> server:init_database()  
  Launch ->server:main()  
  Register -> server:log_up_api(username,password)  
  Login -> server:log_in_api(username,password)  
  Logout -> server:log_off_api(username)  
  Subscribe -> server:subscribe_api(Tweeter)  
  Release -> server:send_tweet_api(Owner)  
  Query -> hashtag & mention ->server:lookup_hashtag_or_mentions(Content)  
  Zipf -> server:zipf(Sender,Owner,Exp)  
# Performance(intel i7 12th gen, core - 16GB ram))
  Max users tested - 12,000.    
    |Users|Tweets|Time Taken(ms)|
  |---|----|----|
  |2000|16,873|12073|
  |6000|77,408|37669|
  |12000|241,937|98348|
  

  

