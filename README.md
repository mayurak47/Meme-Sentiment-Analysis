# Meme-Sentiment-Analysis

Course project of BITS F312, Neural Networks and Fuzzy Logic

The project attempts to score internet memes on the basis of three measures, offensiveness, sentiment and expressed motivation.

<h3> Preprocessing </h3>
Images were all cropped to the same size, and standard NLP preprocessing techniques like stemming, lemmatization and hyperlink removal etc. were performed on the text.

<h3> Model </h3>
A pretrained ResNet is used to extract image features. The text is processed using pretrained GloVe vectors and a couple of stacked Bidirectional LSTM layers. The feature representations of both text and images are then combined. A few more fully connected layers are included to operate upon the combined representations. 

![Model]("https://raw.githubusercontent.com/mayurak47/Meme-Sentiment-Analysis/master/Model.png")

<h3> Metrics </h3>
Since the dataset is imbalanced, an F1 score is more meaningful than accuracy for the classification tasks. The offensiveness task was cast as a regression problem, and the mean square error was used as the loss metric.

