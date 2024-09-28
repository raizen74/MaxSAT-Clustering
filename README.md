# MaxSAT-Clustering
*CORRCLUSTERING &in; NP*

Given *V* = { *v*<sub>1</sub>, ..., *v*<sub>N</sub> } data points, a correlation function s: E → {0, 1} where *s*(*v*<sub>i</sub>, v<sub>j</sub>) = *s*(*v*<sub>j</sub>, v<sub>i</sub>) is applied to all pair of elements in *V* to obtain a symmetric correlation matrix *M*. Given an <em><strong>upper bound</strong></em> number of clusters *k*, <em>CORRCLUSTERING</em> determines whether there is a clustering *cl* of *V* where each pair of points in *cl* has intracluster correlation 1 and intercluster correlation 0 and |*cl*| &le; *k*.

In this project, I created an instance of the *CORRCLUSTERING* problem and performed a <em><strong>polynomial-time reduction</strong></em> to SAT. I obtained a propositional logic formula by reducing the problem to the HARD and SOFT clauses described in the paper published in 2013 by Jeremias Berg and Matti Järvisalo [Optimal Correlation Clustering via MaxSAT](https://www.cs.helsinki.fi/u/mjarvisa/papers/berg-jarvisalo.icdmw13.pdf) and applied a MaxSAT Solver to obtain a Maximum SATisfiability resulting clustering.

After obtaining the OPTIMAL resulting clustering *cl* it is very easy to extract from the model which SOFT clauses are violated. As the paper explains, the performance achieved by SAT Solvers to solve this task is much higher than its Integer programming counterparts, which can be prohibitive even for a relative small *V*.
