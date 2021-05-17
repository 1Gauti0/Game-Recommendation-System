# Game-Recommendation-System
A Content-based recommender system using TF-IDF and Cosine Similarity 

The method used by us to recommend games to the user is by using Cosine Similarity to find the closest game with the keywords combined by using Tf-idf. 

The detailed method used is described below:
Content-based Filtering is a Machine Learning technique that uses similarities in features to make decisions. This technique is often used in recommender systems, which are algorithms designed to advertise or recommend things to users based on knowledge accumulated about the user.
A Content-Based Recommender works by the data that we take from the user, either explicitly (rating) or implicitly (clicking on a link). By the data we have about the user’s play-taste by which we suggest the user the games that they might like. As the user provides more input or take more actions on the recommendation, the engine becomes more accurate.

It relies on similarities between features of the items. It recommends items to a customer based on previously rated highest items by the same customer. List of features about these items needs to be generated.
•	Each item will have an item profile
•	A table structure will list these properties
•	Comparing what and how many features match and collect scores
•	Recommend highest scored item
•	Code will be based on an algorithm, by given some item, the most similar item will be found
•	Best scoring match will be provided to the user
•	This method relies on item features only, and not the user preferences.

Content-based evaluation item profile can be seen as vector. Measured 0 or 1, depends on YES or NO of containing a feature inside that item.

TF-IDF is a statistical measure that evaluates how relevant a word is to a document in a collection of documents. This is done by multiplying two metrics: how many times a word appears in a document, and the inverse document frequency of the word across a set of documents.
To pick important words, TF-IDF method was used. It will calculate the total words of the data frame column which we will process using Pandas Dataframe.  
We will use the Cosine Similarity from sklearn, as the metric to compute the similarity between two movies. Cosine similarity is a metric used to measure how similar two items are. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The output value ranges from 0–1.
0 means no similarity, whereas 1 means that both the items are 100% similar.

We have used two datasets in order to recommend games. The first dataset comprises of the Game Data which has all the Game related data including tags such as Genre, Publisher, Categories, etc.
The second dataset comprises of the User data which has all the user related data such as User ID, Games that he plays with its playtime and its playing behaviour.
First, we process the dataset by using Pandas Dataframes import the dataset for further processing.
After importing, we ask the user to enter their user_id so as to get the games that they play along with the playtime for that particular game. 
Then we categorised the resulting dataframe where the behaviour is ‘play’.
Then we get the game with the maximum playtime from the above dataframe
Now we use a combine function to combine the tags which will be necessary for recommending the games from the Game Dataset  
After this we find out the count matrix using Tf-idf Fit Transform
Then we find the cosine similarity for the count matrix and recommend the games having the closest distance from the list of enumerated cosine similarity. Then we display the 15 game recommendations that we get via the sorted list.  
