1. I decided to run 5 news headlines from CNN into the sarcasm detector. I chose CNN beause personally, this is the news source where I gain most of my information from. Below are my headlines, and what the model classified the headline as: (Note: 1 - Sarcastic, 0 - Not sarcastic)

| Headline  | Classification  |
| ------------- | ------------- |
| Addicted to the high of weed? Its calmer cousin, CBD, may help ease the disorder, study finds  | 0  |
| The rich have one more thing you don't: Better sleep | 1  |
| Inside Brazil's cult of hydroxychloroquine | 1 |
| Zoos struggle to feed animals as pandemic rages on | 0 |
| Congress grilled the CEOs of Amazon, Apple, Facebook and Google. Here are the big takeaways | 0 |

In general, I think the sarcasm detector was pretty accurate. The only thing that could improve is its pedictive probabilites for a headline being sarcastic or not, like for example - the 2nd and 3rd headlines had probabilites around 85%. I was also a little unsure of how the model would react to the first headline. It's not exactly sarastic in my opinion, but weed is usually referred to as "marijuana" in professional news headlinea. The question it poses is a little silly. Thus, I thought it would be interesting to include that headline. The score was interesting. It received a probability of around 40%, which still leans towards not sarcastic.



