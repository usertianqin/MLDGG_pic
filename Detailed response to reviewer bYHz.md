Thank you very much for taking the time to review our paper. Your insights are invaluable in enhancing the quality and clarity of our research. We have carefully considered each of the points you raised：

**[W1]:** It is feasible to learn $𝐴$. In practice, to reduce the time and space cost, following the simplification of [36], we convert the sampling of $𝐴^*$ in the structure learner to the product of the (𝑁𝑃)-dimensional matrix $𝐵$ and its transpose. So the complexity is reduced to $𝑁\times𝑃$ but the performance is the same, where $𝑃$ is the number of pivots nodes, where $P\ll N$. The complexity reduction details are as follows:

1. Randomly choose $𝑃$ nodes in the graph as pivots, where $𝑃$ is a hyperparameter.

2. The original $𝑁\times𝑁$ adjacency matrix 𝐴∗could be retrieved by: $𝐴^*=𝐵𝐵^T$.

3. The intermediate graph matrix (each element represents the similarity of the corresponding pair of nodes) corresponding to matrix $B$ is defined as $𝑇$. Then the message-passing process when the GNN is applied on $𝐴^*$​can be converted to:
   $$Z^{l+\frac{1}{2}}=RowNorm(T^T)r^{(l)}$$

   $$Z^{l+1}=RowNorm(T)r^{(l+\frac{1}{2})}$$

where $Z^{l+\frac{1}{2}}$ is an intermediate node representation and 𝑅𝑜𝑤𝑁𝑜𝑟𝑚 normalizes the values of each row. Then Eq.4 can be approximated to:
$$\mathcal{B} =-\alpha \sum _ {i.j} {E}^* _ {i,j} || \mathbf{r} _ {i}-\mathbf{r} _ {j} || _ 2^2 - \beta ||{E}^*|| _ {0}$$
where $𝐸=𝐵^T𝐵$ is the $𝑃\times 𝑃$ pivot-pivot adjacency matrix. Such a procedure can be efficiently conducted within $𝑂(𝑁𝑃)$ time and space complexity. We will emphasize this in the updated version.

**[W2]:** Thank you for your valuable feedback. Firstly, the theory considers the upper and lower bounds of the model generalization to the target domain with distribution shifts in topology structure (A) and attribute features (X). However [22] mainly focus on Euclidean data (e.g. image) and only considers the distribution shift on attribute features. Secondly, the primary emphasis of [22] lies in fairness and precision, topics that are unrelated to our work. Thirdly, all source domains discussed in [22] are generated through StarGAN or CycleGAN, which significantly differs from the source domain settings in our paper. Although the format may appear similar, the context and setup are entirely distinct.
