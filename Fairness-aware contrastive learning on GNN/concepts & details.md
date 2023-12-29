[Back to main page](https://github.com/jadestreet/Jade-Xu-graduate-application-material/tree/main/Fairness-aware%20contrastive%20learning%20on%20GNN)
## 1 What is Graph Neural Networks (GNN)? 
<!--Need literature.-->
In a nutshell, GNN is a type of Neural Network that takes in graph data as input.
## 2 What is fairness in GNN? Need literature.
Based on past publishment and my understanding, fairness in GNN encompasses two primary dimensions.
### 2.1 Equal Opportunity Fairness:
This dimension aims to provide equitable opportunities to groups or individuals. It includes various types of fairness such as group fairness, individual fairness, and counterfactual fairness. \
[definition & examples]

### 2.2 Utility-Focused Fairness:
This dimension, though under-explored, revolves around managing resources to ensure every applicant secures their most ideal position. This approach introduces a theoretical perspective, emphasizing utility over equal opportunities. Notably, it raises challenges in real-world application, considering both applicant preferences and maximizing the hiring potential of the company.

For example, two positions X and Y in a company are recruiting. Two applicants, A and B, apply for this company with different preferences over this two positions. A prefers X to Y while B prefers in the opposite way. However, the company may evaluate A as being slightly better than B in earning position Y, and B being slightly better than A in earning position X. In this way, both applicants A and B get their less preferred position. However, to ensure fairness, we could respect their preference and arrange X and Y according to their preferences. 

While this method sounds attractive, nonetheless, it more or less ignores the interest of the company side. From the applicants’ perspective, they both get what they want. But the company may want to maximize the possibility of hiring the most qualified applicants. If the abilities of A and B are almost the same, respecting their preferences will not be a problem. If not, more information deserves further consideration. 



## 3 Widely used fair methods at that time? sheet
This section explores fairness methods focusing on the structure and features of input data.

## 4 What is Contrastive Learning (CL)? [Graph of its structure]
Emphasize structure.
The core element of CL is to make distances between similar pairs closer than dissimilar pairs. This structural emphasis aligns with the definition of individual fairness.

## 5	Methods I have used and planned to use? Half Done. 
### a) Fair Sampling:

### b) Correlation-based Fair Sampling: 
In addition to balancing sample ratios, addressing high correlation with sensitive features using methods like feature masking. \
BG: Apart from balancing the ratio of sensitive and insensitive samples, I also realized that some other features may have a high correlation with the sensitive feature. However, we could not simply remove these features because apart from the correlation information it involves, these features may contain other information that influence the prediction result. Therefore, fairness methods such as feature masking is necessary to reduce the effect of correlation. \
Problem: Not implemented given the priority.
### c) Making Pseudo-Examples: [picture/formula of the inspiration paper]
Addressing imbalances in sensitive samples through the creation of pseudo-examples during model training. \
BG: During the experiments, we found that in some datasets, the number of sensitive samples and insensitive samples are very unbalanced. In which way we worried about whether the model could analyze the minority group thoroughly. Therefore, I borrowed the idea from one publication about producing pseudo-examples when training the model to alleviate this problem. \
Problem: I was on the way to making pseudo-examples, but due to demanding schedule. I quitted the summer research.
### d) Applying Individual Fairness Loss Metric: [picture of CL structure & definition of individual fairness]
Exploring the incorporation of individual fairness loss metrics into the loss function, with considerations on structure alignment. \
BG: Current fairness metrics on GCA are both group fairness metrics. However, the structure of CL corresponds much better to the definition of individual fairness as they both emphasize individual samples. \
Problem: we had a disagreement on the availability of this method. One mentor strongly supported me while the other did not consider it a good idea. Hence, I put this method into lower priority. 


## 5 How to Select Sensitive Features?
We select sensitive features based on social-cultural concept and empirical experiments. 
Draw features from the pool of disadvantaged groups: gender, race, region…
Conduct experiments to see if there are any differences between sensitive groups & insensitive groups.

## 6 Datasets Used
Cora: citation network \
Credit: \
Pokec-c: region \
Pokec-z: region \
Bail: race

