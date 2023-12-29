[Back to main page](https://github.com/jadestreet/Jade-Xu-graduate-application-material/tree/main/Fairness-aware%20contrastive%20learning%20on%20GNN)
## 1 What is GNN? Need literature.


## 2 What is fairness in GNN? Need literature.
From my perspective, there are two kinds of fairness.
The first kind of fairness focuses on offering equal opportunities to groups or individuals. Under this definition, there are several types of fairness: group fairness, individual fairness & counterfactual fairness.
[definition & examples]


The second kind of fairness is a bit under-explored, but I thought it is meaningful in terms of application. It focuses on utility, devoting to manage resources such that every applicant could get their most ideal position. However, this trend is rather theoretical and has not been applied to the real ML models. Before applying it to models, some details also need to be clarified.
For example, there are two positions X and Y in a company. Two applicants, A and B, apply for this company with different preferences over X and Y positions. A prefers X to Y while B prefers the opposite. However, the company may evaluate A is slightly better than B in earning position Y, and B is slightly better than A in earning position X. In this way, both applicants A and B get their less preferred position. However, to ensure fairness, we could respect their preference and arrange X and Y according to their preferences. 
While this method sounds attractive, nonetheless, it more or less ignores the interest of the company side. From the applicants’ perspective, they both get what they want. But the company may want to maximize the possibility of hiring the most qualified applicants. If the abilities of A and B are almost the same, respecting their preferences will not be a problem. If not, more information deserves further consideration. 



2.1 All fair methods at that time? sheet
It focuses on the structure and features of input data. 

## 3 What is CL? [Graph of its structure]
Emphasize structure.
The core element of CL is to make distances between similar pairs closer than dissimilar pairs. Therefore, I think its structure aligns with the definition of individual fairness.

## 4	Methods I have used and planned to use? Half Done. 
### a) Fair sampling:

### b) Correlation-based fair sampling: 
BG: Apart from balancing the ratio of sensitive and insensitive samples, we also realized that some other features may have a high correlation with the sensitive feature. Therefore, we also would like to apply fairness methods such as feature masking to reduce the effect of correlation. \
Problem: Not implemented and not sure which one is the best.
### c) Make pseudo-examples: [picture/formula of the inspiration paper]
BG: During the experiments, we found that in some datasets, the number of sensitive samples and insensitive samples are very unbalanced. In which way we worried about whether the model could analyze the minority group thoroughly. Therefore, I borrowed the idea from one publication about producing pseudo-examples when training the model to alleviate this problem. \
Problem: I was on the way to making pseudo-examples, but due to demanding schedule. I quitted the summer research.
### d) Apply individual fairness loss metric to loss function: [picture of CL structure & definition of individual fairness]
BG: Current fairness metrics on GCA are both group fairness metrics. However, the structure of CL corresponds much better to the definition of individual fairness as they both emphasize individual samples. \
Problem: we had a disagreement on the availability of this method. One mentor strongly supported me while the other did not consider it a good idea. Hence, I put this method into lower priority. 


## 5 How to select sensitive features? Done
We select sensitive features based on social-cultural concept and empirical experiments. 
Draw features from the pool of disadvantaged groups: gender, race, region…
Conduct experiments to see if there are any differences between sensitive groups & insensitive groups.

## 6 Datasets I have used? 
Cora: citation network \
Credit: \
Pokec-c: region \
Pokec-z: region \
Bail: race

