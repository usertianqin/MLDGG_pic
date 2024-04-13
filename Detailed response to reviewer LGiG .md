
Thank you very much for taking the time to review our paper. Your insights are invaluable in enhancing the quality and clarity of our research. We have carefully considered each of the points you raised：

**[W1]:** Thanks for your suggestions. We give a brief broader review of related meta-learning for domain generalization approaches.

"Meta-learning is acknowledged as a promising approach for domain generalization, as it enables models to transfer knowledge that can be effectively applied across various tasks and domains. Initially, Li et al. [a] introduced meta-learning in domain generalization by partitioning data from multiple source domains into non-overlapping meta-train and meta-test sets to emulate domain shifts during the training. Chen et al. [b] proposed Discriminative Adversarial Domain Generalization (DADG), which incorporates Discriminative Adversarial Learning to extract domain-invariant features, along with Meta-learning-based Cross Domain Validation for robust classifier training. Qiao et al. [c] presented a novel solution for single-domain generalization using Bayesian meta-learning, termed uncertainty-guided model generalization. The above methods are for Euclidean data (e.g., images). The methods for domain generalization utilizing meta-learning on graphs are provided in the first paragraph of the related work of our paper". We will discuss this in the updated version.

**[W2]:** Thank for your suggestions. We provide T-sne visualizations demonstrating the effectiveness of the representation learner at [[link](https://anonymous.4open.science/r/MLDGG_pic-DE35/tsne_graph.jpg)]. The domain-invariant semantic factors 𝑠 (middle) and domain-specific variation factors 𝑣 (right) are disentangled from the node representations 𝑟 (left) learned from GNNs. We can see that the samples represented by 𝑠 are more distinguished from the ones represented by 𝑟. The samples represented by 𝑣 are independent of classes. Our T-sne results demonstrate the effectiveness of the representation learner.

[a]Li et.al,. Learning to generalize: Meta-learning for domain generalization. AAAI 2018

[b]Chen et.al,. Discriminative adversarial domain generalization with meta-learning based cross-domain validation. Neurocomputing 2022

[c] Qiao et.al,. Uncertainty-guided model generalization to unseen domains. CVPR 2021
