Unsupervised Learning, Recommenders, and Reinforcement Learning

These notes summarize key concepts from the third course of the Machine Learning Specialization by DeepLearning.AI and Stanford Online.

1. Unsupervised Learning

Unsupervised learning finds patterns or structure in data without relying on labeled target values.

Unlike supervised learning, the model is not given the correct output for every training example.

Common applications include customer segmentation, exploratory data analysis, and anomaly detection.

2. K-Means Clustering

K-means is a clustering algorithm that groups data points into a specified number of clusters.

How It Works

1. Initialize the cluster centroids.
2. Assign each data point to its nearest centroid.
3. Update each centroid using the mean of the points assigned to it.
4. Repeat the assignment and update steps until the algorithm converges or reaches a stopping condition.

Applications

- Customer segmentation
- Grouping similar products
- Exploring patterns in datasets

The number of clusters, (K), is selected before running the standard algorithm.

3. Anomaly Detection

Anomaly detection identifies examples that differ substantially from expected patterns.

For example, an unusual transaction may be flagged for further investigation.

One approach models the probability distribution of selected features. Examples with sufficiently low estimated probability may be flagged as potential anomalies.

Applications

- Fraud detection
- Equipment fault detection
- Network intrusion monitoring
- Unusual activity detection

An anomaly score is not proof that an event is fraudulent or harmful; additional investigation may be necessary.

4. Recommender Systems

Recommender systems suggest items that may be relevant to a user.

Examples include recommending movies, music, books, or products based on preferences and behavior.

Collaborative Filtering

Collaborative filtering uses patterns in user-item interactions, such as ratings, to generate recommendations.

The underlying idea is that users with similar preferences may enjoy some of the same items.

A model can learn user and item representations to estimate how much a user might like a particular item.

Content-Based Filtering

Content-based filtering recommends items using their characteristics and a user's known preferences.

For movies, features might include genres, descriptions, actors, or other available metadata.

Comparing the Approaches

- Collaborative filtering: Learns from patterns in interactions between users and items.
- Content-based filtering: Uses item features and user preference profiles.
- Hybrid systems: Combine multiple approaches.

New users and new items can present challenges when little interaction data is available. This is known as the cold-start problem.

5. Reinforcement Learning

Reinforcement learning studies how an agent can learn to make decisions by interacting with an environment.

The agent takes actions and receives rewards or penalties according to the environment's feedback.

Key Components

- Agent: The learner or decision-maker.
- Environment: The system the agent interacts with.
- State: The current situation.
- Action: A choice made by the agent.
- Reward: Feedback that evaluates an outcome.

The goal is to learn a policy that maximizes cumulative reward over time.

Exploration and Exploitation

- Exploration: Trying actions to discover their outcomes.
- Exploitation: Choosing actions based on what has already been learned.

Balancing the two helps an agent discover useful strategies while benefiting from its current knowledge.

6. Key Takeaways

- Unsupervised learning finds patterns without labeled targets.
- K-means groups data into clusters.
- Anomaly detection identifies unusual observations.
- Recommender systems personalize suggestions using interactions or item features.
- Collaborative filtering and content-based filtering use different sources of information.
- Reinforcement learning learns decision-making strategies from rewards and interaction.

7. Practical Applications

- Movie recommendation systems
- Customer segmentation
- Fraud and anomaly detection
- Personalized shopping recommendations
- Robotics and sequential decision-making

---

These notes are a personal learning summary. I will continue developing these concepts through independent implementations and projects.
