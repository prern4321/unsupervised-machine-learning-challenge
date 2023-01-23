# unsupervised-machine-learning-challenge

We as a data science team of a medical research company have been assigned to find better ways to predict myopia, or nearsightedness. 
By using unsupervised learning, we would need to separate group of distinct patients that would be better to analyze. 
We've been provided with raw Data that would need to be processed to fit the machine learning models. 
We would use clustering models to explore whether the patients can be placed into distinct groups. 
The visualizations created would be shared with the team and other officials


Instructions
This activity is broken down into four parts:

Part 1: Prepare the Data

Part 2: Apply Dimensionality Reduction

Part 3: Perform a Cluster Analysis with K-means

Part 4: Make a Recommendation

Part 1: Prepare the Data
Read myopia.csv into a Pandas DataFrame.

Remove the "MYOPIC" column from the dataset.

Note: The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already!
Standardize the dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

Part 2: Apply Dimensionality Reduction
Perform dimensionality reduction with PCA. How did the number of the features change?
Hint: Rather than specify the number of principal components when you instantiate the PCA model, state the desired explained variance. For example, say that a dataset has 100 features. Using PCA(n_components=0.99) creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this assignment, preserve 90% of the explained variance in dimensionality reduction.
Further reduce the dataset dimensions with t-SNE and visually inspect the results. To do this, run t-SNE on the principal components, which is the output of the PCA transformation.

Create a scatter plot of the t-SNE output. Are there distinct clusters?

Part 3: Perform a Cluster Analysis with K-means
Create an elbow plot to identify the best number of clusters. Make sure to do the following:

Use a for loop to determine the inertia for each k between 1 through 10.

If possible, determine where the elbow of the plot is, and at which value of k it appears.

References
Reduced dataset from Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute

Analysis and Recommendation:
After taking all the steps as stated in the instructions, we yielded 10 principal components while preserving 90% of the explained variance. We also, plotted a scatter plot with the t-SNE model using the PCA data. We were not able to distinguish the clusters fairly using this model.Further more, we created a line plot performing a cluster analysis with K-Means. Observing the plot, the elbow of the curve seems to start at 3. Hence we did our predictions with k=3 and conclude that the patients can be clustered into 3 groups.
