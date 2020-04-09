# ACI_BayesianNetwork

## Problem Statement

Ravichandran Ashwin is one of the most successful test bowlers from India claiming more than
350 international wickets. He has been spearheading the spin attack for the Indian test team since his
debut in November 2011 and is expected to make a dash to 400 wickets in the upcoming test series with
New Zealand. However, some exciting new spinning prospects have also staked their claim for the test
team.
As a selector you are aware about non subcontinent pitches being non-spin friendly which
reduces the number of slots for spinners in the team. Being an ex-player, you also know how important
toss is in test matches since it dictates whether a team will bat first or not. The decision to bat or bowl
first can have significant import on the final outcome of a match.
You have decided to construct a Bayesian Network to help you with your conundrum and help
you with your decision on Ashwin’s selection for the upcoming tour.
Attached excel contains information on all test matches played by India since Ashwin’s debut in
2011.

Implement Bayesian Networks and also learn to use the pomegranate library.

Create a bayesian network model which would help you predict the probability.

1) Create a function to calculate prior probability of any given variable. The function should read in
an array and output a dictionary of prior probability of each possible outcome.
e.g. {'A': 1/4, 'B': 1/2, 'C': 1/4}


2) Create a function to calculate conditional probability. The function should read in multiple
arrays and calculate the posterior probability of the last array wrt to previous arrays. For
example, if you pass arrays “Location” and “Ashwin Playing” the output should be
[[ 'home', 'Y', 0.xx ],
[ 'home', 'N', 0.xx ],
[ 'away', 'Y', 0.xx ],
[ 'away', 'N', 0.xx ]]


3) Use the functions created above and python’s pomegranate library to define conditionality
between variables to create Bayesian Network. Refer this excellent tutorial on how to use
pomegranate to create Bayesian Networks.
https://github.com/jmschrei/pomegranate/blob/master/tutorials/B_Model_Tutorial_4_Bayesian_Networks.ipynb


4) Use the Bayesian Network model created to calculate the probability of:
a. India winning, batting 2nd, Ashwin playing
b. India winning, batting 2nd, Ashwin not playing
c. India losing, batting 2nd, Ashwin playing
d. India losing, batting 2nd, Ashwin not playing


### What is a Bayesian Network ?

A Bayesian network, Bayes network, belief network, decision network, Bayes(ian) model or probabilistic directed acyclic graphical model is a probabilistic graphical model (a type of statistical model) that represents a set of variables and their conditional dependencies via a directed acyclic graph (DAG). 

Bayesian networks are ideal for taking an event that occurred and predicting the likelihood that any one of several possible known causes was the contributing factor. For example, a Bayesian network could represent the probabilistic relationships between diseases and symptoms. Given symptoms, the network can be used to compute the probabilities of the presence of various diseases. 

### Dataset

Dataset is attached in github. 

#### Dataset Description
##### Sample Tuple

Y	won	5wickets	lost	2nd	vWest_Indies	Home	6-Nov-11

##### Explanation
- The first column represents if Ashwin was in the playing 11 or not. 
- The second column represents the Result of the match . win indicates India won the match.
- The third column represents the Margin of victory / losss.
- The fourth column represents the results of the toss. won indicates India won the toss. 
- The fifth column represents the batting order. If India batted 1st or 2nd. 
- The sixth column represents the opponent.
- The seventh column represents the location of the match. If the match was held in Home(India) or away. 
- The last column represents the start date of the match.
