### Team members
Vivekanandh Vel Rathinam (vvelrath@buffalo.edu)																				
Antony Jerry Ajay (jerryant@buffalo.edu)

### Introduction
This project deals with using Hadoop framework to analyze twitter data. Using Hadoop, the present trends in twitter is gathered. Some of the statistics we collected include the total count of hashtags, collection of users and their followers, and finally the most number of recurring words in a collection of tweets. Some of the fetched data is also visualized and interesting patterns are obtained in R.

### Project Objectives

 To understand the components and core technologies related to content retrieval, storage and data-intensive computing analysis.
 To explore designing and implementing data-intensive (Big-data) computing solutions using MapReduce (MR) programming model.
 Using Hadoop 2 for HDFS and MR infrastructure.
 To visualize the data using appropriate tools.
 Create a detailed documentation of the experience.

### Project Approach

We worked on the twitter4j API to fetch relevant statistics in-order to process them. The procedure of gathering the data extended over a period of days until we were satisfied that we had a collection of a small BIG DATA. Two types of data was collected in this approach. Firstly, a raw file containing around 200,000 tweets in English. Secondly, a file containing user names and the total number of followers for every user.

As the first step toward analyzing the tweets collected over a period of time, we sorted the tweets into three files where the files had a collection of all hash tags and the count, user names and the count, and finally the collection of words encountered while reading the tweets and their count. This process was accomplished using MR on Hadoop framework. This information is then used to identify the most trending hash tags, most active users and users with most followers respectively.

The second part of the project involves identifying co-occurring hash tags using pairs and stripes approach. The pairs approach was handled in MR by dividing the total number of occurrences of a pair to its marginal. The stripes approach involved aggregating the key value pairs and letting the MR engine to automatically sort the input and distribute the keys to the reducers internally.

The third part of the project involved developing K-means clusters to cluster users based on the total number of followers they had. The internal counters of Hadoop was used to compute the centroids. This process is repeated until convergence. The total number of centroids was assumed to be three and the iterations started with initial values of 50, 500 and 1000 respectively.

Finally, the fourth part of the project involved finding the shortest path of the most popular hash tag. This involved developing a connected network of sender -> receiver pattern and labelling the network for determining the shortest path between the nodes of this network. The job is given to an MR engine that finds the shortest path iteratively.

### Program execution:

1) Import all the TAR files into eclipse
2) Use /input and /output as the input and output paths respectively
3) No Command Line arguments are needed for any of the programs
