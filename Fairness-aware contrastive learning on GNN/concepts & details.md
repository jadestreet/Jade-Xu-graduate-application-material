[Back to main page](https://github.com/jadestreet/Jade-Xu-graduate-application-material/tree/main/Fairness-aware%20contrastive%20learning%20on%20GNN)
## 1 What is Graph Neural Networks (GNN)? 
<!--Need literature.-->
In a nutshell, GNN is a type of Neural Network that takes in graph data as input. \
More specifically, 
## 2 What is fairness in GNN? 
Similar to the fairness notion in the real life, there is no general criterion for fairness in GNN. But based on past publishments and my understanding, fairness in GNN encompasses two primary dimensions.
### 2.1 Treatment-Focused Fairness:

This dimension aims to provide equitable opportunities to groups or individuals. It includes various types of fairness such as group fairness, individual fairness, and counterfactual fairness. 
- **Group Fairness**: Based on sensitive features, we classify the general population into different groups, and guarantee each group will get fair treat.[^1]
- **Individual Fairness**: Individuals with simimlar features should be treated equally.[^2]
- **Counterfactual Fairness**: The value of sensitive feature should not influence one's treatment. [^3] \
 \
*For convenience, I only list the most common fairness types. These surveys and tutorials provide further insights into fairness notions in machine learning and graph mining. [^4]*

### 2.2 Perference-Focused Fairness[^5]:
This dimension, though under-explored, revolves around managing resources to ensure every applicant secures their most ideal position. This approach introduces a theoretical perspective, emphasizing utility over equal opportunities. Notably, it raises challenges in real-world application, considering both applicant preferences and maximizing the interests of the company.
<!--WITH AN GRAPH EXAMPLE-->
For example, two positions X and Y in a company are recruiting. Two applicants, A and B, apply for this company with different preferences over this two positions. A prefers X to Y while B prefers in the opposite way. However, the company may evaluate A as being slightly better than B in earning position Y, and B being slightly better than A in earning position X. In this way, both applicants A and B get their less preferred position. However, to ensure fairness, we could respect their preference and arrange X and Y according to their preferences. 
![e1](/../Fairness-aware contrastive learning on GNN/pics/Hiring 1.jpg)
![e2](/Fairness-aware contrastive learning on GNN/pics/Hiring 2.jpg)
While this method sounds attractive, nonetheless, it more or less ignores the interest of the company side. From the applicants’ perspective, they both get what they want. But the company may want to maximize the possibility of hiring the most qualified applicants. If the abilities of A and B are almost the same, respecting their preferences will not be a problem. If not, more information deserves further consideration. 

### How to Define Fairness?/How to Select Sensitive Features?
While there was no general criterion for fairness in ML, we define fairness/select sensitive features based on social-cultural concept and empirical experiments. 
1. Draw features from the pool of disadvantaged groups: gender, race, region…
2. Conduct experiments to see if there are any differences in the output of the model between sensitive groups & insensitive groups.

## 3 Widely used fair methods at that time? 
As GNN takes in graph data as input, many fairness improvement methods focus on modifying the structure (nodes and edges) and features of input data under different settings. \
In the structure domain, the common methods include adding nodes/edges, and removing nodes/edges; In the features domain, the common methods include feature masking. \
However, the methods I explored at that that centered on the graph end. With time passed, there are fruitful directions such as optimization on the matrices where are the form we saved graphs, improvement through overall GNN structure like loss functions. 

<!--FIND THE PAPER I READ-->

<!-- ## 4 What is Contrastive Learning (CL)? 
[Graph of its structure] Emphasize structure.
The core element of CL is to make distances between similar pairs closer than dissimilar pairs. This structural emphasis aligns with the definition of individual fairness.
-->

## 4	Methods deserve further consideration
<!-- ### a) Fair Sampling:-->

### a) Correlation-based Fair Sampling: 
**Overview**: In addition to balancing sample ratios based on sensitive features, there are other features that may have a high correlation with sensitive features, in which way sensitive information would still influence the model output. Therefore, applying methods like feature masking is necessary to alleviate this problem. \
 \
Apart from balancing the ratio of sensitive and insensitive samples, I also realized that some other features may have a high correlation with the sensitive feature. However, we could not simply remove these features because apart from the correlation information it involves, these features may contain other information that influence the prediction result. Therefore, fairness methods such as feature masking is necessary to reduce the effect of correlation. 
<!--Problem: Not implemented given the priority.-->

### b) Making Pseudo-Examples: 
<!--[picture/formula of the inspiration paper]-->
**Overview**: Addressing imbalances in sensitive samples through the creation of pseudo-examples during model training. \
 \
During the experiments, we found that in some datasets, the number of sensitive samples and insensitive samples are very unbalanced. In which way we worried about whether the model could analyze the minority group thoroughly. Therefore, I borrowed the idea from one publication about producing pseudo-examples during training the model to alleviate this problem. 
<!--Problem: I was on the way to making pseudo-examples, but due to demanding schedule. I quitted the summer research.-->

### c) Applying Individual Fairness Loss Metric: [picture of CL structure & definition of individual fairness]
**Overview**: Exploring the incorporation of individual fairness loss metrics into the loss function, with considerations on structure alignment. \
 \
Current fairness metrics on GCA are all group fairness metrics. However, the structure of CL fits much better with the definition of individual fairness as they both emphasize individual samples. 
<!--Problem: we had a disagreement on the availability of this method. One mentor strongly supported me while the other did not consider it a good idea. Hence, I put this method into lower priority.-->

<!--
## 6 Datasets Used
Cora: citation network \
Credit: \
Pokec-c: region \
Pokec-z: region \
Bail: race
-->

[^1]: Dwork, Cynthia, et al. "Fairness through awareness." In ITCS 2012.
[^2]: Zeng, Ziqian, et al. Fair representation learning for heterogeneous information networks. In AAAI, 2021.
[^3]: Kusner, Matt J., et al. “Counterfactual fairness.” In NeurIPS, 2017.
[^4]: Yushun Dong, Oyku Deniz Kose, Yanning Shen, and Jundong Li. 2023. [Fairness in Graph Machine Learning: Recent Advances and Future Prospectives.](https://doi.org/10.1145/3580305.3599555) In Proceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD '23). Association for Computing Machinery, New York, NY, USA, 5794–5795. 
[^5]: 
