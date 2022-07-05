# Presian Sentiment and Emotion Lexicon
In persian Language there is no common library or project that give the emotion of words. in this project we want to obtain this information based on works done in this scope.

## [HesNegar: Persian Sentiment WordNet](https://github.com/Text-Mining/Persian-Sentiment-Resources)
HesNegar is a project that developse the Persian Sentiment WordNet. For more information, please visit [Their paper in the Signal and Data Processing Journal](http://jsdp.rcisp.ac.ir/article-1-554-en.html)

You can download csv version of this resource from : ["PersianSWN.csv"](https://github.com/Text-Mining/Persian-Sentiment-Resources/blob/master/PersianSWN.csv).

This is a sample of rows here.
````
00001740-a	توانا	1.00	0.125	0.000
00051373-a	توانا	0.45	0.375	0.250
00001740-a	قادر	0.24	0.125	0.000
00002098-a	عاجز	1.00	0.000	0.750
00051696-a	عاجز	0.18	0.000	0.500
00002098-a	ناتوان	0.75	0.000	0.750
00051696-a	ناتوان	0.58	0.000	0.500
````

## [The NRC Emotion Intensity Lexicon (NRC-EIL)](http://www.saifmohammad.com/WebPages/AffectIntensity.htm)
The NRC Emotion Intensity Lexicon (version 1) is a list of English words with real-valued scores of intensity for eight basic emotions (anger, anticipation, disgust, fear, joy, sadness, surprise, and trust)

## NRC and PersianSWN

In Persian Sentiment WordNet we have the persian tranlsation of each synset_id that exist in the [Princetone SWN](https://wordnet.princeton.edu/).
In this project we merge the NRC Emotion Intensity Lexicon and Persian Sentiment WordNet to obtain the persian Emotion Intensity.

Sample rows of resulting table:

