# Research Experience: Fairness-aware Graph Neural Networks (GNN) at UIUC’s CS Department
## Project Overview
Conducted within the UIUC Computer Science department, this project involved students being filtered and matched with professors. My group's focus was on Graph Neural Networks (GNN), specifically addressing fairness concerns. The objective was to mitigate fairness issues prevalent in existing state-of-the-art models.
## Background and Learning
While I had prior knowledge of graph data, GNN models were relatively new to me. To bridge this gap, I immersed myself in relevant literature, particularly exploring applications of fairness in GNNs.
## Identifying Fairness Issues
During this exploration, it became evident that fairness problems within GNNs were widely acknowledged. Existing mitigation methods predominantly centered around manipulating input graph data and modifying loss functions. After an extensive review, I chose to delve into the Graph Contrastive Learning with Adaptive Augmentation (GCA) model.
At that time, the fairness problem in GNN is widely discovered and accepted, and the methods to alleviate this problem mainly focused on processing the input graph data and modify the loss function. After several weeks’ publication review, I selected GCA model (Graph Contrastive /kənˈtræs.tɪv/ Learning with Adaptive Augmentation). 
Action and Initial Results
My first step involved scrutinizing the fairness issues within GCA, drawing insights from existing literature and experimental results across various datasets. Implementing basic techniques, such as balancing data distribution between non-sensitive and sensitive groups, yielded promising results. The fairness metric improved significantly, rising from 25% to 40%.

Building on these results, I conducted a more in-depth analysis to explore additional methods. This included introducing new metrics aligned with the structure of contrastive learning, processing data highly correlated with sensitive features, and generating pseudo-examples to address unbalanced number ratios between groups.

Then I made further analysis on it and worked to find other methods, such as applying new metrics which fit better with the structure of contrastive learning, processing data with high correlation with sensitive features, or making pseudo examples to leverage the unbalanced number ratios /ˈreɪ.ʃi.oʊ/ between two groups.
[all solutions presented in a why-guess] Done.
Conclusion
In conclusion, my exploration into fairness in GNNs not only highlighted the existing issues but also demonstrated tangible improvements through practical interventions. This experience deepened my understanding of fairness challenges in machine learning models and fostered a proactive approach to addressing them.
