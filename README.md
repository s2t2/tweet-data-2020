# Research Data (Shared)

This repository contains data used in conjunction with the paper ["Bots, Disinformation, and the First Trump Impeachment"](https://arxiv.org/abs/2204.08915) by Michael Rossetti and Tauhid Zaman.

The data is stored here separately for sharing purposes, while the code can be found [here](https://github.com/s2t2/tweet-analysis-2020).

If you are a researcher interested in using our data, we would be happy to invite you to access the full dataset in our shared Google BigQuery data environment.

## User Details

Data Dictionary for the "user_details_20210806.csv" file:


column_name | datatype | description
--- | --- | ---
user_id	| INTEGER | unique identifier for each user in our "impeachment 2020" dataset
created_on	| DATE | date the user was created
screen_name_count	| INTEGER | number of screen names used
screen_names	| STRING | all screen names used
is_bot	| BOOLEAN | whether or not we classified this user as a "bot" / automated account
bot_rt_network	| INTEGER | for bots, which retweet network (0:anti-trump, 1:pro-trump) -- DON'T USE THIS!!
is_q	| BOOLEAN | whether or not this user is classified as a Q-anon promoter (i.e. pro-Trump users who used Q-anon language / hashtags in their profiles)
q_status_count	| INTEGER | the number of tweets with Q-anon language / hashtags
status_count	| INTEGER | number of total tweets authored by this user (in our "impeachment 2020" dataset only)
rt_count	| INTEGER | number of total retweets authored by this user (in our "impeachment 2020" dataset only)
avg_score_lr	| FLOAT | avergage opinion score from our Logistic Regression model (0:anti-trump, 1:pro-trump)
avg_score_nb	| FLOAT | avergage opinion score from our Naive Bayes model (0:anti-trump, 1:pro-trump)
avg_score_bert	| FLOAT | avergage opinion score from our BERT Transformer model (0:anti-trump, 1:pro-trump)
opinion_community	| INTEGER | binary classification of average opinion (0:anti-trump, 1:pro-trump) -- THIS IS THE PARTISANSHIP LABEL!!
follower_count	| INTEGER | number of followers (in our "impeachment 2020" dataset only)
follower_count_b	| INTEGER | ... who are bots
follower_count_h	| INTEGER | ... who are humans
friend_count	| INTEGER | number of friends (in our "impeachment 2020" dataset only)
friend_count_b	| INTEGER | ... who are bots
friend_count_h	| INTEGER | ... who are humans
avg_toxicity	| FLOAT | average "toxicity" score from the Detoxify model
avg_severe_toxicity	| FLOAT | average "sever toxicity" score from the Detoxify model
avg_insult	| FLOAT | average "insult" score from the Detoxify model
avg_obscene	| FLOAT | average "obscene" score from the Detoxify model
avg_threat	| FLOAT | average "threat" score from the Detoxify model
avg_identity_hate	| FLOAT | average "identity hate" score from the Detoxify model
fact_scored_count	| INTEGER | number of tweets with URL domains that we have rankings for
avg_fact_score	| FLOAT | average fact score of links shared (1: fake news, 5: mainstream media)
