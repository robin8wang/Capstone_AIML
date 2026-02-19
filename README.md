### Optimal beam configuration and prediction in 5G wireless Channel State Information (CSI) using AI-powered time series analysis
**Prepared by Robin Wang**

#### Executive summary
This capstone project bridges advanced time series analysis + neural networking with practical wireless communication challenges, offering significant potential for performance improvements in next-generation networks while providing valuable insights into AI-driven network optimization methodologies

#### Rationale
In today’s fast-moving wireless networks—especially with the rollout of 5G and upcoming 6G—keeping a strong and stable signal for users on the move is a major challenge. Currently, networks spend a lot of time and resources constantly searching for the best signal direction, which slows down service and wastes capacity.
If this problem remains unsolved, users will experience more dropped calls, slower internet, and less reliable connections in crowded or dynamic environments like cities, stadiums, or highways. For telecom operators, this means higher operational costs, inefficient use of network resources, and difficulty supporting next-generation applications like autonomous vehicles or real-time augmented reality.


#### Research Question
Can AI-powered time series analysis of Channel State Information (CSI) and beam indices predict optimal beam configurations in real-time, thereby enhancing 5G/6G network performance through reduced latency and improved spectral efficiency?

#### Data Sources
DeepMIMO (https://www.deepmimo.net/), a publicly available massive MIMO channel dataset with realistic urban, rural, and indoor scenarios. Supplemental data from academic 5G-NR measurement campaigns and synthetic data generated using 3GPP-compliant channel models.

#### Methodology
1.	Seasonal AutoRegressive Integrated Moving Average with eXogenous Variables (SARIMAX) for modeling temporal dependencies and external factors.
2.	Long Short-Term Memory (LSTM) neural networks for capturing complex, non-linear patterns in high-dimensional CSI sequences.
3.	Pattern-based clustering with Markov Models to identify and predict common beam-switching scenarios(still in progress)

#### Results
A predictive beam management framework that reduces beam training overhead, lowers latency in beam establishment, and improves spectral efficiency compared to traditional exhaustive beam sweeping methods.

#### Next steps
Pattern-based Clustering with Markov Models
Behavioral Analysis: Identifies common beam switching scenarios (static, pedestrian, vehicular)
1. State Transition Modeling: Uses Markov chains for beam state predictions
2. Scenario-specific Optimization: Tailors beam management strategies to usage pattern
3. Methodology
  - Clustering Phase: Group similar beam transition patterns using K-means/DBSCAN
  - Markov Modeling: Build state transition matrices for each cluster
  - Real-time Classification: Match current pattern to historical clusters for prediction


#### Outline of project

- [capstone_aiml](#capstone_aiml.ipynb)


#### Contact and Further Information
Contact Robin Wang robin.888.wang@gmail.com  for further information
