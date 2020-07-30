1. I decided to run 5 news headlines from CNN into the sarcasm detector. I chose CNN beause personally, this is the news source where I gain most of my information from. Below are my headlines, and what the model classified the headline as: (Note: 1 - Sarcastic, 0 - Not sarcastic)

| Headline  | Classification  |
| ------------- | ------------- |
| Addicted to the high of weed? Its calmer cousin, CBD, may help ease the disorder, study finds  | 0  |
| The rich have one more thing you don't: Better sleep | 1  |
| Inside Brazil's cult of hydroxychloroquine | 1 |
| Zoos struggle to feed animals as pandemic rages on | 0 |
| Congress grilled the CEOs of Amazon, Apple, Facebook and Google. Here are the big takeaways | 0 |

In general, I think the sarcasm detector was pretty accurate. The only thing that could improve is its pedictive probabilites for a headline being sarcastic or not, like for example - the 2nd and 3rd headlines had probabilites around 85%. I was also a little unsure of how the model would react to the first headline. It's not exactly sarastic in my opinion, but weed is usually referred to as "marijuana" in professional news headlinea. The question it poses is a little silly. Thus, I thought it would be interesting to include that headline. The score was interesting. It received a probability of around 40%, which still leans towards not sarcastic.

2.

## OUTPUT #1:

ROMEO: my master?

DUKE VINCENTIO:
Youth, e'en drums, boy! of after whose honour fly?
Finds she shall she be full out win: and live root
To whom bad address? pracies upt thou, a pair,
You love your huse sIEN GRUY:
Go too; your words, sride, princess we may not from the love of this.

CAPULET:
Marry, see tho way. Come, so, Andevio.
And now:
Call't in this winds with winding;
And so his conditian to the field?

RIVERS:
A most genreanct who,
And for himself and endment my Romans.
Nortake, as then sits falsehood of men, and greet it, I'll
Stinking his faced friend.

DUKE VINCENTIO:
The floters of your adriace will not polserve;
Ruphing his victory and with the city,
And fright foul fight and poor, time look upon, well-saged,
We said 'swear't.

CLARENCE:
Are you that he hath doth pripof against thee I had;
More such a howide king, my
heart. Seliong, have been a fearful
dreamsure Rativen, none doth no softle must come.
Farewell, as not your grace hath from the world
mad
For corn guilt on him in suc

## Output #2

ROMEO: hearing she's mean upon: the
trust I did Addimar and the offences be
Name to succeed: hirse is obedient George.
Grumio! Read me another musical:
Give me thy son, hid yet we may proceed!
Master, you are prepured living shrew,
To savive you bear thyself see which dish himely word,
That, his sons she wanton closesur. A vilgar,
And, undergone be you bled runame my friends,
In hild. Prithee, seek thee you think for this.

First Mercutio,
I desire myself like a trodouch cried 'O:
'Tis sulents.

AUTOLWIUS:
For, fellow! Phant weeping how the most noble lords,
You have done but a bord: leave heir that your fire--

EGLARES:
Good brame, what I saw speedy.

ANTONIO:
While impoilt it hath some him. You'll lacufe too issue.

WARWICK:
True, learn all Jucury: cried it shrew'd.

HORTENSIO:
Madam, my friends out of that substance on mysure,
And now Minoladues, piled, with an appreehions. Away with it your consul! and, and scarce with the gods
Would prove as this puplishining and en hine:
Consastreme; we

## Analysis

It's interesting to see how different these texts are after running generate.text() twice. The model is essentially learning a piece of literature, and generating a different output of text every time. It's not 100% accurate and I do see some issues within the text, but pretty amazing considering the short literature it was trianed on and the fact that only 10 epochs of training were utilized. 

3. translate(u'hace mucho frio aqui.')
  output: it s too cold
  
  translate(u'esta es mi vida.')
  output: this is my life
  
  translate(u'¿todavia estan en casa?')
  output:  are you still at home ?
