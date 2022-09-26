# German News Topic Sentiment Analysis Dataset (GerNTSA)


**GerNTSA** is a Dataset for Aspect-Based Sentiment Analysis on general German-language news articles. The main focus of this dataset is the recognition of one-sided representation and media bias, therefore the sentiment values are provided in relation to different news topics found in general online-newspaper articles.

This Dataset was created as part of my master's thesis *"Collective intelligence - generation of a dataset for sentiment analysis of German-language news texts" (OT: "Intelligenz im Kollektiv - Generierung eines Datensatzes zur Sentiment-Analyse deutschsprachiger Nachrichtentexte")* at the [FH Kufstein Tirol's](https://www.fh-kufstein.ac.at/eng/) [**Data Science & Intelligent Analytics**](https://www.fh-kufstein.ac.at/eng/Study/master/data-science-intelligent-analytics-pt) Program.

---
### Main Features

The Dataset consists of `3792` manually annotated Sentences extracted in the Timespan of one year between `1st August 2021` and `31st July 2022`. The news articles ìn this Dataset were collected from `15 different news providers` in the German-speaking region, consisting of `8 german`, `4 austrian` and `3 swiss` news outlets.
Contained sentiment values represent the sentiment polarity and classify `positive, neutral and negative` attitudes towards a news topic contained in the text.
In total, the corpus contains a mixture of 59.5% neutral 25.4% positive and 15.1% negative statements.

---

### Dataset Creation

The news articles used for this project were collected using the [news-please](https://github.com/fhamborg/news-please) Python Library. From the extracted news data, top keywords were automatically identified as news topics using the TF-IDF method. Selected sentences from the articles were annotated via crowdsourcing on the [Toloka](https://toloka.ai/) annotation platform using an overlap of five annotators per sentence. Valid results were consolidated using majority voting.

---

### Dataset Structure

The Dataset is availible in JSON-Format and contains the following values:

- `id`: Unique identifier of a tuple
- `opinion_snippet`: The annotated sentence
- `target`: The highlighted news topic in the text to which the opinion statement applies
- `target_anchor`: Position of the target in the opinion_snippet
    - `from`: Character number of the beginning of the target
    - `to`: Character number of the end of the target
- `sentiment`: Wrapper of the  sentiment-classification
    - `polarity`: Classification of the sentiment-polarity in the opinion_snippet against the target.  
      Representation in `positive`, `neutral` and `negative`. 
      
---

### Acknowledgements

The Raw Data for this project were collected using [news-please](https://github.com/fhamborg/news-please), sincere thanks to the news-please team for publishing such a wonderful piece of software.

---

### Licence

This Dataset is Licenced under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) Licence. 
Please consider mentioning this repository if you use this dataset.
