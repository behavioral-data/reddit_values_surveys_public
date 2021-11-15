For the past several months I've been studying what aspects of subreddits are most strongly valued by their members, and wanted to share the results and get some feedback.

We have two academic papers on arXiv, the [first describes our methods for creating a taxonomy of values](https://arxiv.org/pdf/2109.05152.pdf), and the [second is a more quantiative analysis of how these values vary from person to person and from subreddit to subreddit](https://arxiv.org/pdf/2111.05835.pdf).

This project was run by researchers at the [Behavioral Data Science Lab](https://bdata.cs.washington.edu/) and the [Social Futures Lab](https://social.cs.washington.edu/) at the [University of Washington](http://cs.washington.edu/).

# Motivation, Methods, and Data
I wanted to work on this project because there is lots of research out there that seeks to make online communities "better." But what does "better" actually mean? While there is relative consensus on certain specific topics (e.g. abuse is bad, misinformation should be minimized), the voices of community members themselves are often exluded from academic research. Furthermore, with so many online communities focused on so many different topics, it seems unlikely that there is a "one size fits all" approach - what is good for one community might be downright harmful to another!

The primary method for this project was online surveys of redditors. We conducted two surveys. The first was a qualitative survey of 39 redditors, which asked them to describe in their own words what they like and dislike about their communities. Using these responses, we developed a taxonomy of 29 community values across 9 major categories.

The second survey was larger and more quantiative, with 2,769 responses. We asked each redditor to list up to 3 subreddits they consider themselves a member of, and then asked about their values for each of those subreddits specifically. Using the taxonomy developed from the first survey, we asked about 3 different dimensions of each value:
1. How important is the value? (1-9 scale)
2. What is the current state of the value (1-11 scale)
3. How would you like the subreddit to change with regards to this value? (-1-+1 scale)

We recruited redditors via reddit advertisements, email lists, and word of mouth. Our study design was approved by the IRB at the University of Washington. 

# Taxonomy of Values

We clustered the responses from the first survey together, and assigned each cluster a name in order to produce our taxonomy of values.

[The resulting taxonomy has 9 major categories: Quality of Content, Community Engagement, Diversity, Size, Participation and Inclusion, Technical Features, Moderation and Moderators, Norms, and Trust.](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/figs/taxonomy_figure.jpg)

Using quantiative responses from the second survey, we then answered 3 research questions:

# What are subreddits' values, and how do they vary across subreddits?

[Figure 1 - The average importance and current state of each value across subreddits.](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/figs/subs_summary.jpg)

By averaging all the responses for each subreddit together, we found that in general, Quality of Content is the most important value, followed by Variety of Content and Trust, while Size and Democracy are generally the least important values. However, there is substantial variation in values from one subreddit to another. For example, while the average subreddit ranks Safety as the 5th most important value, in 171 subreddits, Safety is the most important value, while in another 176 subredits, Safety is the least important value.

[Figure 2 - Differnces in value importance across subreddits of different topics.](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/figs/community_categories.jpg)

Next, we manually categorized the topic of the 120 subreddits for which we recieved the most responses. We found that Trust is most important amongs News and Identity-based (e.g. /r/teenagers) subreddits, and least important amongst Meme subreddits. On the other hand, Meme subreddits place more importance on amount and variety of content, values that are relatively less important to Identity-based subreddits.

# Where is there disagreement over values?

[Figure 3 - Disagreement in perception of importance (a), current state (b), and desired change (c) across subreddits, with axes adjusted for scale width relative to one another.](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/figs/disagreement.jpg)

For each response, we can compute the difference between that response, and the average response within each subreddit. By averaging across these differences (MAD) we can measure the amount of disagreement over each value for each subreddit. We found that in general, there is more consensus on the current state of each subreddit, and more disagreement on the importance of different valus and their desired change. 

There is the greatest disagreement over the importance of Safety, which may be explained by the hypothesis that redditors who have experienced bullying or abuse are more likely to rank Safety as very important than redditors who have not had such experiences.

# How do moderators' values differ from non-moderators?

[Figure 4 - Differences in values between moderators and non-moderators.](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/figs/mod_differences.jpg)

Lastly, we examine how moderators percieve their communities different from non-moderators. Using participants' usernames, we fetched the subreddits that each user moderators from their public profile, and then computed the average difference between moderators' responses and non-moderators' responses within each subreddit. 

We found that moderators believe their communities are less democratic, should be less democratic, and that Democracy is less important, relative to the non-moderator mean in that community. Moderators rank Diversity, Engagement, and Safety as more important to their communities than non-moderator community members.

# Implications

I sincerely hope that these findings offer some insight into what redditors value in their subreddits. As I see it, the key takeaways are:

- Quality and Variety of Content are by far the most important values to most redditors and most subreddits.
- In general, redditors don't care very much about democracy (e.g. involvement in moderation) or the size of their subreddits.
- Safety is a specially tricky value. Just because the majority of redditors don't care very strongly about it doesn't mean that it's unimportant. Often the most vulnerable redditors (women, minorities) are most impacted by safety issues, and their needs are important too.
- Moderators think that their communities' involvement in running the subreddit is less important than non-moderators. As a moderator myself, I am especially curious about this result. Does it improve subreddits in order to have more involvement from the community?

