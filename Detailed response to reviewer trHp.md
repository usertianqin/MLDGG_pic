Thank you very much for taking the time to review our paper. Your insights are invaluable in enhancing the quality and clarity of our research. We have carefully considered each of the points you raised：

**[W1]** The paragraph "Shared Batch Normalization Bias" on page 6 of [a] (ICLR-18) highlights this assumption. It is reiterated in subsequent studies, including the 3-th paragraph of the introduction in [15] (AAAI-23). We will clarify it in the updated version.

**[W2]** The two challenges are (1) Distribution shifts across source and target domains lead to classifier generalization failure. (2) Specific to graphs, such shifts are characterized by variations in node features and topology. To this end, our framework consisting of a structure learner and a representation learner in the context of meta-learning facilitates knowledge transfer from source and target graphs. The structure learner aims to mitigate the adverse effects of task-unrelated edges, enhancing the comprehensiveness of representations learned by GNNs. Furthermore, the representation learner is to disentangle semantic and variation factors in each domain.

**[W3]** In our experiments followed by [42], the complexity of the structure learner is $𝑂(𝑁𝑃)$, where $𝑃$ is the number of pivot nodes. The complexity of GCNs is $O(|E|Dd)$, where $|𝐸|$ and $𝑑$ are the numbers of edges and classes, respectively, and $𝐷$ is the dimension of the node feature. The complexity of the representation learner is $𝑂(𝑁)$. Therefore, the complexity of our model is $𝑂(𝐾(𝑁𝑃+𝜂(|𝐸|𝐷𝑑+𝑁)))$, where $𝐾$ is the number of source domains and $𝐾,𝑃,𝜂 ≪ 𝑁$, $𝐷,𝑑≪|𝐸|$.

**[W4]** We have modified it accordingly.

**[W5]** We construct experiments within 3 scenarios on 3 datasets in Sec.6.1.3. Our experiment settings are designed based on distribution shifts (1) within the same dataset (Tab 2), as depicted on the left of Fig.1. (2) across different datasets with the single source domain (Tab 3), each with distinct distributions, as shown in the center of Fig.1, and (3) across different datasets with many source domains (Tabs 4-6), as depicted in the right of Fig.1. Our results demonstrate the proposed MLDGG can handle with different levels of distribution shifts.

**[W6]** Existing studies in graph domain generalization [16,36,42] solely focus on node classification. We follow their settings and use them as baselines in our experiments. Other tasks on graphs such as link prediction, graph-level classification, etc. require different settings. We will save the link prediction and graph classification as future work.

[a] Antoniou et al., How to train your MAML.ICLR 2018.
