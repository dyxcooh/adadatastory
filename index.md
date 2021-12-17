## Welcome to GitHub Pages

### Abstract

Quotes, as you know them, are a reference to a person’s words: they are found in a wide range of contexts, be it in research articles, in novels, or even in news articles!

Indeed, quotes are a short way of summarizing the essence of a person’s opinion, input, comments or description in regard to a topic. They can be used to relay decisions, emotions, which makes them all the more impactful! This explains their frequent use in news articles.

Quotes enclose much more than the sentences they are. Through their repeated use in news articles, they can show how relevant a speaker is in a given field. The more times a quote is re-shuttled across articles, the more impactful it is! The same goes for quote length, highlighting the complexity/thoughtfulness of a speaker’s insight!

Adding in further details from the speaker, such as gender and occupation, we find ourselves with valuable information for analyzing news trends in speaker representation.

Let’s start the data story!

### Quotebank

Quotebank is a collection of 178 million quotes culled from 162 million English news items published between 2008 and 2020. We focused our study on the years 2015 to 2020 because this portion of the dataset is already quite substantial and representative. The quotebank dataset enables us to relate quotes to their respective speakers and their information, with QIDs mapping to Wikipedia entries such as speaker identity, gender and occupation.

### Reserch questions

From the informative potential held within quotes, what do we want to uncover?

We focused on two facets: gender parity and relevance of speakers. 

Indeed, we started by asking ourselves: is there a gender more quoted than the other? Are there fields in which the voices of males or females resonate more?

As we go further in our study, we realized we could extend this to more broadly look at the relevance of speakers in regards to where they are quoted, which could give us insights on the reliability of media in general.

### Why this is important

We live in a century where news has become so overwhelming that we have the impression that they are from everywhere and are about everything. We rarely suffer from the lack of information, but rather the inability to manage and process it. However, on the other hand, the decisions we make depend on the information we receive. And the news provides a lot of information that shapes our reasoning. It is intriguing to deploy data analysis tools to have a global view of the speakers in news and try to learn more about them. Which people are influencing us? Are some of them really relevant to the topic if they always speak in areas that are not related to their profession? This allows us to keep the critical mind facing the media and be aware of the identities behind the authoritative words.

### Our approach

After some statistical analysis on the number and the length of the quotes. We decide to classify the quotes into four general categories: politics, art, science and sport, by manipulating the URL of the corresponding articles with the help of a NLP pipeline. We choose to retrieve the topic from the URLs instead of directly from the quotes, because we observed that a URL often contains the title of the article and its category, assigned by the website or by the authors themselves. We believe that this information is a more accurate indicator of the theme and the context than the quote itself, since a quote can be used in a figurative way and the real subject may not appear in the quote at all.

On the other hand, we also assign one of the four categories mentioned above to every speaker’s occupation. This enables us to compare the subjects of the quotes and the expertise domain of the speakers, as they are on the same set of categories. 

### What we found

First of all, we look at a global image of the relation between professions and quotes. We choose to examine the data one year after another to observe a potential evolution over years.

Let’s look at the number of quotes per category of professions depicted by the barplots on the right column: the scientists seem to be least represented and have a decreasing number of quotes. For the majority of years, we see that politicians are the most quoted ones, and this trend is particularly evident for 2020, maybe due to the presidential election of the USA. For the years 2015 and 2016, people involved in sports have a comparable number of quotes, this could probably be explained by the existence of sport stars and the popularity of sports in general. We are a bit surprised to see that in 2017, artists have the most quotes, but knowing that some celebrities can be classified in the category of art, this is not too strange.

![fig big](https://user-images.githubusercontent.com/61227389/146612087-f5570d7f-d309-4ec9-ae07-b70f1fd20489.png)

As for the length of quotes, we plot the quote length distribution for every year per category, while distinguishing the different genders by color. We witness heavy tail distributions: most quotes have a short length, the peak value is often around 50 characters. However, it is not rare to see very long quotes having 200 to 300 characters. In science and sports, there are slightly more quotes of medium lengths, and less of very short length than others. We think this is because science-related speakers tend to be more precise and give more details, and sportsmen when describing the situation of a match have longer quotes to give all the context.
For all four categories, females are less quoted than males. This disparity is most noticeable when the speakers’ occupation belongs to the sports category, and less obvious for the art domain, which corresponds to our expectation. It is also interesting to point out that we can hardly see non-binary gender people being quoted, especially for a small representation in art.

**Themes and Occupations in 2020**

Now that we’ve seen these statistics, what are the quotes actually about? Let’s take a closer look at the data of 2020 and classify them according to their theme, that is, the main context of the articles in which they occur. For all the 2.3 millions quotations we considered, 45% of them are about politics, 21% about sport, 17% and 13% about art and science respectively.

![fig stat-thème](https://user-images.githubusercontent.com/61227389/146603894-7906ba75-0d4e-483e-a0e5-8e7b4266c5bb.png)

We finally arrive at the question we asked at the beginning: Do speakers talk about subjects related to their domain? Looking at the data, we can see that when someone in the news expresses themselves about sports, it is likely that they are relevant. However, this is less the case for other topics: the worst one is science, in which politicians and artists are more quoted than actual scientists. This is likely a result of the Covid-19 pandemic, which impacted everyone and became a public health issue. Many celebrities, classified in the Art categories, and politicians have been outspoken about healthcare-related items such as vaccines and masks, thus skewing the distribution. We can also imagine that the media chooses to highlight the speech of some famous people in order to drive the attention of the public, since scientists are often unknown to the commun readers, they are less visible in the news. Still, it is very interesting to see the opinions of politicians outweigh in number the scientific category, and it is an important indicator that people should be wary of misinformation from subjects in this category.

We tend to observe the same trend for both females and males in occupations across topics, but there are a few things of note: Most notably in Sport, where there’s almost as many quotes coming from the Art category than Sport themselves for female speakers. We think this is because most directly sport-related roles, like coach, player, trainer, ect are overwhelmingly men, and less directly-related occupations like reporter, presenter, ect have a better parity, thus leading to the gap between Art and Sport to be much narrower for females.

![fig topic-job](https://user-images.githubusercontent.com/61227389/146612245-7bf34827-03ee-4572-9f8b-87c0fcebdf46.png)

And what about the distribution of topics for people with different occupations? We have an interesting discovery that except for athletic people, all the others are more likely to be quoted for political topics, no matter whether their expertise domain is politics or not.

If we look at the artists more closely, we can see that even though female artists are also slightly more heard for their political statements than for art subjects, this phenomenon is much more evident for male artists: there exists twice as many quotes about politics compared to the art ones.

![fig per job2](https://user-images.githubusercontent.com/61227389/146612261-a6331365-8592-4e60-bb98-a9875ff3a19b.png)

### Conclusion

One of the most glaring takeaways is that women are less quoted in almost every regard compared to their male counterparts. We need to give them more visibility on the news in the future. Despite that, the trends in topic and occupation for each genders were very similar, and women were just as relevant as men in most cases.

Speaking of relevance, there were some surprising results here too: for instance, the influence of politics across the board, and reciprocally most people tend to be quoted in a political context, despite their occupations. But most notably, in the scientific topic, people should be careful of misinformation, and should check the credentials of speakers. 

