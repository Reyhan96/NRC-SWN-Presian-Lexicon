# Presian Sentiment and Emotion Lexicon
In the Persian Language, there is no common library or project that gives the emotion of words. in this project, we want to obtain this information based on works done in this scope.

## SentiWordNet
SentiWordNet is a lexical resource for opinion mining that contains sentiment polarity of synsets. for more details you can visit [SentiWordNet](https://github.com/aesuli/SentiWordNet) 

This is a sample of rows here:
````
POS	ID	    PosScore  NegScore  SynsetTerms	      Gloss
a	00001740    0.125     0	        able#1	            (usually followed by `to') having the necessary means or skill or know-how or authority to do something; "able to swim"; "she was able to program her computer"; "we were at last able to buy a car"; "able to get a grant for the project"
a	00002098    0         0.75	unable#1	    (usually followed by `to') not having the necessary means or skill or know-how; "unable to get to town without a car"; "unable to obtain funds"
a	00002312    0         0	        dorsal#2 abaxial#1  facing away from the axis of an organ or organism; "the abaxial surface of a leaf is the underside or side facing away from the stem"

````

## [HesNegar: Persian Sentiment WordNet](https://github.com/Text-Mining/Persian-Sentiment-Resources)
HesNegar is a project that developed the Persian Sentiment WordNet. For more information, please visit [Their paper in the Signal and Data Processing Journal](http://jsdp.rcisp.ac.ir/article-1-554-en.html)

You can download csv version of this resource from : ["PersianSWN.csv"](https://github.com/Text-Mining/Persian-Sentiment-Resources/blob/master/PersianSWN.csv).

Each line (entry) has 5 fields :

  1.  Synset id (based on Princeton WordNet standard format): IdNumber-PosTag e.g. 00001740-a
  2.  Persian word.
  3.  Confidence value (based on FerdowsNet WordNet).
  4.  Positivity value.
  5.  Negativity value.

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
The NRC Emotion Intensity Lexicon (version 1) is a list of English words with real-valued intensity scores for eight basic emotions (anger, anticipation, disgust, fear, joy, sadness, surprise, and trust).

Here is a sample of this file:
````
word        emotion       emotion-intensity-score
outraged    anger               0.964
brutality   anger               0.959
hatred      anger               0.953
hateful     anger               0.940
terrorize   anger               0.939
infuriated  anger               0.938
````

## NRC and PersianSWN

In Persian Sentiment WordNet, we have the Persian translation of each synset_id which can be found in the [SentiWordNet](https://github.com/aesuli/SentiWordNet).
In this project, we first merge the SentiWordNet and Persian Sentiment WordNet to get the translation of each english word.
then we merge the result table with NRC emotion intensity to obtain the Persian Emotion Intensity.

The resulting table can be downloaded from : [PersianSWN-NRC-emotion-lexicon.csv](https://github.com/Reyhan96/NRC-SWN-Presian-Lexicon/blob/main/PersianSWN-NRC-emotion-lexicon.csv)

Sample rows of resulting table:

![Persian Emotion Intensity Lexicon](https://github.com/Reyhan96/NRC-SWN-Presian-Lexicon/blob/main/Persian%20emotion%20intensity%20lexicons.png)

