## NLP, Tabular data, Collaborative filtering, Embeddings

* We already looked at the range of vision application like classification, localization and image regression and we breifly touched on the NLP problems
* Today we dig deeper dive on the NLP and tabular data and Collaborative filtering
* Then we will start looking at the deeply into the collabrative filtering and start looking at the deep maths inside them
* From the last lecture, the **one hundred layers of Tiramisu** that some one pointed out the the exp should be run with the small subset of examples.


## NLP:
* Review: its just the natural language processing which is just taking some text and doing something with it
* Basically with text/document classification will prevent anything from SPAM or identifying the fake news
* Legal classification done by the How Khang et al legal text classification with universal language model fine turning
* *Task1* we will start about the movie review and we shall discuss if that positive or negative - basically the sentiment about the movie
* Our movie review contains roughly 25,000 peices and our task is to figure if thats positive or not
* Remember our **Neural nets is bunch of the matrix multiplies and simple non-linerties particulary replacing negatives with zeros**
* Those weight matrices start out random, if we start with random parameters and try to train those parmateres positive vs negative
movie reviews. Even if we have 25,000 movies review saying that I like this one and I dont like this one.
* Sometimes that could be nuanced beacause partculry like movie reviews -
* For long time until 2018 neural nets didnt do a great job at this kind of classifcation problems because not enough information available
* The trick is to use the **Transfer Learning**
* Its exactly like the computer vision model, use the pre-trained model which is trained to use something different
* FOr imageNet is originally used to predict the 1000 types of the photos and people fine tune them to use for all kind of predictions
* So using the same analogy we will start using the language model, use that as the pre-trained model.
* till [7.00] 
