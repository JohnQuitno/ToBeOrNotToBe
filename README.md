To be or Not to be
==============================

Shakespeare Character Classification

Project Organization
------------


    ├── data
    │   └── raw   
    │        │── Shakespeare Classification Data                        
    │
    ├── notebooks          
    │   └── src.ipynb               


Data
----
The data set contained the play,  player line number, act.scene.Line, the text
of the PlayerLine, and the player. There are just over 100000 data points in 
this data set


Feature Engineering
-------------------
I did a couple things to make the given features more usefule. I used one hot encoding
to determine which act/scene we are in. We have one column for each play, and act/scene
pair. These are 1 when we are in the act/scene or play and 0 when we are not. I also used 
the player line to determine commonly spoken words and did something similar to the one hot 
encoding. I looked at the 500 most commonly spoken words in the play and made a column for 
each of them. These columns are 1 when the player speaks this word in their line and 0 when 
they don't

Classification Algorithms
-------------------------

I used the sklearn package to run both logisitic regression and Naive Bayes algorithms on 
the altered data. Logisitic regression performed much better than the Naive Bayes algorithm 
in this data set