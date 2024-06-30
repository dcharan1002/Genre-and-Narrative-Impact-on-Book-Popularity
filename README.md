# Genre-and-Narrative-Impact-on-Book-Popularity
This project explores how genre and narrative structure impact the popularity of English-language fiction using Project Gutenberg metadata. By analyzing Kullback-Leibler divergence (KLD) measures and applying LASSO regression, it identifies key predictors of book downloads, offering insights to enhance reader engagement and increase downloads.

To do this, please find attached two files from Project Gutenberg. In metadata.csv, you’ll find book IDs and book-level attributes, including download counts. In KLDscores.csv, you’ll find book IDs and corresponding “narrative revelation” scores, formatted in the form of Python lists. These scores measure the amount of “information revelation”, measured in terms of Kullback-Liebler divergence, for each subsequent section of the corresponding book. For details on how this measure was constructed, see https://ceur-ws.org/Vol-3558/paper6166.pdf


**Metadata Dataset:**

id: Unique book identifier.

title: Title of the book.

author: Author of the book.

language: Language of the book.

downloads: Total download count.

subjects: Book's subject categories.

type: Format of the book (text, sound, etc.).



**KLD Scores Dataset:**

id: Unique book identifier.

kld_values: KLD scores across narrative sections.



**Extra Controls Dataset:**

id: Unique book identifier.

subj2_war: Binary indicator for war genre.

subj2_adventure: Binary indicator for adventure genre.

subj2_comedy: Binary indicator for comedy genre.

subj2_biography: Binary indicator for biography genre.

subj2_romance: Binary indicator for romance genre.

subj2_drama: Binary indicator for drama genre.

subj2_fantasy: Binary indicator for fantasy genre.

subj2_family: Binary indicator for family genre.

subj2_sciencefiction: Binary indicator for science fiction genre.

subj2_action: Binary indicator for action genre.

subj2_thriller: Binary indicator for thriller genre.

subj2_western: Binary indicator for western genre.

subj2_horror: Binary indicator for horror genre.

subj2_mystery: Binary indicator for mystery genre.

subj2_crime: Binary indicator for crime genre.

subj2_history: Binary indicator for history genre.

subj2_periodicals: Binary indicator for periodicals.

subj2_others: Binary indicator for other genres.

speed: Narrative speed indicator.

sentiment_avg: Average sentiment score.

sentiment_vol: Sentiment score volatility.

wordcount: Total word count.

**Methodology**

1. **Data Processing**: Merging metadata, KLD scores, and genre information.

2. **KLD Measures**: Calculating book-level KLD characteristics such as average, variance, slope, and cumulative KLD.

3. **Regression Analysis**: Applying LASSO regression to identify key predictors of log-transformed download counts.

4. **Genre Impact**: Investigating heterogeneity of effects across genres and analyzing the influence of different genres on book popularity.

**Results**

The analysis reveals that certain genres, particularly mixed genres like horror, science fiction, and fantasy, significantly impact book downloads. The KLD measures, particularly average and cumulative KLD, show strong correlations with download counts, indicating that narrative structure plays a crucial role in attracting readers.

**Conclusion**

This project provides valuable insights into the factors driving book popularity, highlighting the importance of genre and narrative structure. The findings can help authors and publishers tailor their content to better meet reader preferences and maximize engagement.
