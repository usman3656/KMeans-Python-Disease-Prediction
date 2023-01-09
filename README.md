# KMeans-Python-Disease-Prediction

1.	Kaggle Participation

As seen in the following pictures, the entries were submitted 70 times. Initially the values were quite low (except for one outlier) the accuracy was not very good, however as the entries progressed, the trend continued to increase as I learned new methods and applied new filters and learned from my mistakes.
This eventually led me to get my best entry at 0.84145.  



2.	Report

CRISP-DM
•	Business understanding: The business is from the medical domain that diagnoses the diseases based on the symptoms the patients show.

•	Data understanding: There are a lot of columns for symptoms for each patient in binary format on which eventually the disease will be diagnosed. The data consists of 133 columns and 2384 unique rows. There are no missing values and there are no duplicate entries. Each column shows a symptom except the first which is for the rowid.  

![image](https://user-images.githubusercontent.com/91872457/211271989-4e6ba466-ba6a-4cc4-992f-fd4835834444.png)


•	Data Preparation: In this data as this is binary, there was no normalizing as well as encoding for categorical values and no missing values. So data preparation was not needed a lot. The two main data preparation done were to remove the zero variance columns and remove highly corelated columns. Also removed low variance columns but that did not work out good for the accuracy. (picture attached)
 
![image](https://user-images.githubusercontent.com/91872457/211272028-e06f24c7-1e61-43ad-8de2-b3371ea8d11e.png)


•	Modelling: There were two major models that were implemented for this assignment. As this was a clustering-based dataset, so I had applied Kmean and Agglomerative clustering. The first half entries were Kmeans and then after that the most work was done on Agglomerative clustering. For kmeans a number of tools and features were used.

![image](https://user-images.githubusercontent.com/91872457/211272057-704fc428-8b9a-4ca9-86f5-27f1f82cd09b.png)


o	Elbow Curve: The elbow curve was used for checking the best value for the numbers of clusters that were to be used. I used 2 ways to make the elbow curve, one was through calculating distortion and the second one was through intertia. (pictures attached) However it was not of much use and the best value did not indeed come through there. The graph showed no straightforward answer so not a very useful tool for this dataset.
 

![image](https://user-images.githubusercontent.com/91872457/211272095-42d17845-977c-4527-b7ec-6bac49667a12.png)

 


o	Silhouette Coefficient and graphs: This was also used a lot to determine if the clusters were at the right positions or not. In addition it also was used to check the highest value I got from which cluster. However even for this tool even if I used a model with a high silhouette coefficient, the accuracy was not directly proportional to it. It helped a lot to understand the model but I could not estimate the accuracy based on the value of the silhouette coefficient.(pictures attached)
 
 
![image](https://user-images.githubusercontent.com/91872457/211272120-738944ed-7d3a-4797-bd76-71899f3e0f8b.png)

























•	Agglomerative Clustering: When I felt that I had done half my entries through kmeans and had reached a ceiling in terms of accuracy so I decide to change the model. Agglomerative is a hierarchical modeling method so its most popular tool is the dendrogram. 
o	Dendrogram: So in order to understand the dataset and the clusters, countless dendrograms were made. Using these diagrams I got close to the best value and made me increase my knowledge base on trees.(picture attached)
 





•	Evaluation: The best overall score was achieved through agglomerative clustering as well as some data preprocessing. The data preprocessing done was that the highly corelated features were removed whose value was more than 0.95 and all the zero variance columns were removed.For the agglomerative model the features I used were as follows.
 
At this implementation I scored my best accuracy of 0.84145
•	Deployment: at this stage not applicable but InshaAllah for future projects will be doing.

Which algorithm worked best for the given dataset and why? 
o	The agglomerative clustering performed the best. I tried all sorts of feature selection as well as data preprocessing with both the models but the agglomerative turned out the best in giving the max accuracy score. Using tools such as dendrogram also helped in fine tuning the features

What is the optimal number of clusters in the data as per your findings and why?
o	As per my findings and test and trial, the best cluster number was 11. The numbers 12 and 6 were also giving high score but 11 was the best. I believe it was due to the differences in data segregation and how the model divided the data into clusters.

What were the overall challenges that you faced while improving the score, and so on?
o	I tried a lot of things and the score had got stuck and I wasn’t getting any progress so was disheartened initially but eventually with a lot of effort and using methods and tools as well as tweaking features ultimately got me a decent score. 
o	
Some features used and played with?
o	KMeans, KMeans++, Linkage, Compute full tree, random state, number of clusters, algorithm= elkan, correlation, covariance, zero variance, dropping columns, Agglomerative, Affinity, manually changing csv etc


 
 
 
 
