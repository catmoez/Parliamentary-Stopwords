# Parliamentary-Stopwords
Common words in parliamentary speech that are procedural formalities or otherwise not substantively meaningful



Methods:

A list of the top 100 most frequently appearing tokens (lowercased, apostrophes and other punctuation removed) was generated for each 2.5-year chunk of UK House of Commons text transcripts from Jan. 1, 1990, to Sept. 6, 2021. The lists were combined and duplicate tokens removed.

Next, words from the top parliamentary tokens were removed if they also appeared in the Quanteda package for R (Benoit et al. 2018)'s list of English stopwords. The remaining words make up the parliamentary stopword (parliamentary procedural word) 'longlist'.

Next, from the remaining top parliamentary words (everyday English stopwords now removed), any words appearing in the top 200 most common words from a reference newspaper corpus (The Guardian 2012-2016 corpus, also available from Quanteda) were also removed. The newspaper corpus was processed in the same way (lowercased, punctuation removed) and the justification for removing top newspaper words is that newspaper speech is a relatively good proxy for everyday English speech. This means that words appearing frequently in parliamentary transcripts but not in newspaper text (especially given that both cover public, political issues) are likely to be procedural formalities and not substantive words. The remaining words (top parliamentary words minus English stopwords and minus the top most common words from a generic news corpus) are saved as the parliamentary stopword 'shortlist'. 

The approach was also tested using the top 500 most common words from each parliamentary time period and top 500 from the newspaper corpus, but manual checks revealed many substantively meaningful words on the longer lists and therefore the 100 most common from Hansard and 200 most common from the news corpus were used.
