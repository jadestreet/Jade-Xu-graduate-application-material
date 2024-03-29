# Fairness-aware Graph Neural Networks (GNN) at UIUC’s CS Department
## Project Overview
Conducted within the UIUC Computer Science department, this project involved students being filtered and matched with professors. My group's focus was on Graph Neural Networks (GNN), specifically addressing fairness concerns. The objective was to mitigate fairness issues prevalent in existing state-of-the-art models.
## Background and Learning
While I had prior knowledge of graph data, GNN models were relatively new to me. To bridge this gap, I immersed myself in relevant literature, particularly exploring applications of fairness in GNNs[^1].
## Identifying Fairness Issues
During this exploration, it became evident that fairness problems within GNNs were widely acknowledged. Existing mitigation methods predominantly centered around manipulating input graph data and modifying loss functions. After an extensive review, I chose to delve into the Graph Contrastive Learning with Adaptive Augmentation (GCA) model[^2]. 
## Action and Initial Results
My first step involved scrutinizing the fairness issues within GCA, drawing insights from existing literature and experimental results across various datasets. Implementing basic techniques, such as balancing data distribution between non-sensitive and sensitive groups, yielded promising results. The fairness metric improved significantly, rising from 25% to 40%.
## Further Analysis and Optimization
Building on these results, I conducted a more in-depth analysis to explore additional methods. This included introducing new metrics aligned with the structure of contrastive learning, processing data highly correlated with sensitive features, and generating pseudo-examples to address unbalanced number ratios between groups[^3].
## Conclusion
In conclusion, my exploration into fairness in GNNs not only highlighted the existing issues but also demonstrated tangible improvements through practical interventions. This experience deepened my understanding of fairness challenges in machine learning models and fostered a proactive approach to addressing them.

[^1]:Fairness notions and methods to alleviate fairness issues are introduced in the [concepts & details](https://github.com/jadestreet/Jade-Xu-graduate-application-material/blob/main/Fairness-aware%20contrastive%20learning%20on%20GNN/concepts%20%26%20details.md) file.
[^2]:Yanqiao Zhu, Yichen Xu, Feng Yu, Qiang Liu, Shu Wu, and Liang Wang. 2021. *Graph Contrastive Learning with Adaptive Augmentation*. In Proceedings of the Web Conference 2021 (WWW '21). Association for Computing Machinery, New York, NY, USA, 2069–2080. https://doi.org/10.1145/3442381.3449802.
<!--[^3]:Selected datasets and experiment results are introduced in the concepts & details file.-->
[^3]:Details about these advanced methods are introduced in the [concepts & details](https://github.com/jadestreet/Jade-Xu-graduate-application-material/blob/main/Fairness-aware%20contrastive%20learning%20on%20GNN/concepts%20%26%20details.md) file.
