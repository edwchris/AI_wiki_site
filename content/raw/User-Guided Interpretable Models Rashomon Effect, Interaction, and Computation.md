---
title: "User-Guided Interpretable Models: Rashomon Effect, Interaction, and Computation"
source: "https://hdsr.mitpress.mit.edu/pub/m3fppgon/release/1"
author:
  - "[[Jiachang Liu]]"
  - "[[Cynthia Rudin]]"
published: 2025-10-17
created: 2026-06-27
description:
tags:
  - "clippings"
---
When moving from a simple univariate regression to a multivariate one, practitioners are often confronted with a frustrating phenomenon: the coefficient sign of a variable can flip, so that it disagrees with its (univariate) relationship with the outcome. An effect that is positive in isolation can appear negative in the context of other variables, or vice versa. This instability undermines the interpretability of the model, especially in high-stakes domains like health care where domain knowledge suggests a clear directional relationship. In “Univariate-Guided Sparse Regression,” Chatterjee et al. (2025) tackle this problem. They propose a method, uniLasso, that preserves the signs of univariate coefficients while leveraging the predictive strength of a sparse multivariate model. Their approach uses leave-one-datapoint-out univariate slopes as guides within an adaptive lasso framework. The result is a model that is sparser and more accurate than the standard lasso but also, by design, more aligned with the foundational insights gleaned from single-variable analysis. This commentary discusses their work in the context of a broader challenge: aligning models more generally with human intuition while keeping them sparse enough so that people can easily understand them.

## Background on Sparsity, Monotonicity, and General Interpretability

The problem Chatterjee et al. (2025) considers is a longstanding challenge in interpretable machine learning: how to create models that are sparse (since humans can handle a limited number of cognitive entities at once) and constrained to agree with natural relationships between variables and the outcome. This challenge is discussed in the review paper “10 Grand Challenges in Interpretable Machine Learning” (Rudin et al., 2022); specifically, Challenge 3 concerns generalized additive models that incorporate constraints like sparsity and monotonicity. (Chatterjee et al, 2025, tackles a special case of this challenge since the set of generalized additive models contains the set of linear models, and monotonicity constraints become sign constraints on the coefficients of linear models.) There has been a tremendous amount of work in this area, including much work by Chatterjee et al.'s (2025) authors over decades.

Monotonicity constraints are typically not difficult to incorporate because they are linear constraints, but sparsity is different: optimizing sparsity directly leads to a combinatorial optimization problem. Our own approach (among others) is to solve that optimization problem directly using

$$
\ell_0
$$

regularization (e.g., Liu, Zhong, Seltzer, & Rudin, 2022; Liu, Zhong, Li, et al., 2022; Liu, Rosen, et al., 2023; Liu, Zhang, & Rudin, 2024), which is plausible given the current speed of computers and modern algorithms. Chatterjee et al. (2025) pursue what could potentially be a computationally easier approach, which is to use

$$
\ell_1
$$

regularization to induce sparsity. However, the

$$
\ell_1
$$

term used as usual, as in lasso, also induces a bias that pulls the coefficients of all the terms downward, potentially reducing performance. This bias becomes stronger when the

$$
\ell_1
$$

regularization term is made large enough to send many coefficients to zero. Chatterjee et al. (2025) have found a clever way to combat this bias using a stacking technique (which the authors prove is equivalent to adaptive lasso) as well as a leave-one-datapoint-out technique that combines the predictions on validation data (the left-out data points). Further studies may investigate why this intriguing technique works, whether the computational expense of computing

$$
(n+1)\times p
$$

univariate models within their approach is worthwhile, and how uniLasso competes with or can be combined with

$$
\ell_0
$$

regularization. (Chatterjee et al., 2025, provides the explanation that non-useful features can have negative correlation with the leave-one-datapoint-out error, though they also imply that this is not necessarily the full explanation for the success of their algorithm, and we do not have a better explanation.)

While the question of which technique gives more accurate results for a given level of sparsity is intriguing, we no longer believe that this is generally the right scientific or modeling question to ask. The truth is that there are many algorithms that all work about equally well yet give totally different models. Chatterjee et al. (2025) note this phenomenon: “our belief is that in high dimensions there are likely to be a multitude of different models that have about the same MSE as the ‘optimal’ one chosen by the lasso. Hence it can make sense to choose one that is more interpretable and sparser than that of lasso.” This phenomenon of many equally good models is called the Rashomon effect (Breiman, 2001). The Rashomon effect implies that the data set cannot necessarily distinguish on its own which models are going to be the most useful. For instance, how do we know that linear models are even the right model class? Maybe a sparser generalized additive model or a sparse decision tree would be better. And among each function class, how do we really know that one set of variables should be chosen when there are many equally good choices? Because of uncertainties like these, we believe that understanding and exploiting the Rashomon effect is the key to a new user-centered way of creating models (Rudin et al., 2024). And, as described next, the Rashomon effect could be the key to unlocking the mystery of why accuracy/interpretability trade-offs often do not exist.

## The Rashomon Effect Justifies the Existence of Interpretable Models

The fact that many methods, such as that of Chatterjee et al. (2025), can produce sparse, sign-constrained models without sacrificing predictive performance—as compared with least squares regression—might seem counterintuitive. Adding constraints could worsen the fit by preventing the algorithm from doing what it normally does unconstrained—but in reality, the constraints do not affect the accuracy. Our own work with generalized additive models (Liu, Zhong, Seltzer, & Rudin, 2022; Zhong et al., 2023), scoring systems (Liu, Zhong, Li, et al., 2022; Zhu et al., 2025), and decision trees (Babbar et al., 2025; Xin et al., 2022) has shown that imposing even complicated combinations of constraints often yields many models that are both sparse and accurate. This begs the question: Why do such models exist, and what does it mean for us modelers?

The answer, we believe, can be gleaned from the Rashomon effect (Boner et al., 2024; Rudin et al., 2024; Semenova, Rudin, & Parr, 2022; Semenova, Chen, et al., 2023): the existence of a multitude of different models that achieve near-optimal performance. The landscape of the loss function is not a sharp valley with a single point at the bottom, but a wide, flat basin. Within this ‘Rashomon set’ of well-performing models, there exist models with desirable properties—sparsity, preserved signs, a combination of both, fairness constraints, and even integer coefficients as in scoring systems (Liu, Zhong, Li, et al., 2022). See Figure 1 for an illustration. Chatterjee et al.'s (2025) experimental results simply reflect the Rashomon Effect at work.

![](https://assets.pubpub.org/eegwk62z/RsetDefinition-31757979670372.png?width=800&fit=bounds)

Figure 1. Illustration of the Rashomon set.

The practical implication of the Rashomon effect is profound. It suggests that we need not be timid in our pursuit of interpretability. When working with high-dimensional data, we can be bold in imposing domain-specific constraints. The existence of a large Rashomon set makes it highly probable that a sparse, accurate, and interpretable model is not just a theoretical possibility, but a practical reality waiting to be discovered.

## Obtaining Interpretable Models as an Interactive Process

The motivation behind uniLasso is compelling. Chatterjee et al. (2025) say they were inspired to develop uniLasso after observing that on a cancer proteomics data set the signs of two key coefficients flipped when moving from univariate to multivariate models. This example highlights a crucial point: meaningful progress in interpretable machine learning is not often driven by rigid, predetermined rules of what we think is interpretable in advance (e.g., sparsity), but by the practical challenges that emerge in the midst of real-world data analysis. Creating a truly interpretable model generally requires a process, one that requires the model’s design to be guided by the user’s need to understand and trust its predictions. We do not want to get caught in the *interaction bottleneck* that arises when domain experts do not know in advance exactly what they are looking for, want to interact with the algorithm to improve the model, and find that they need to (painstakingly) reformulate the problem repeatedly and rerun the algorithm (Rudin et al., 2024). There is definitely a better way.

We have been working toward developing tools that facilitate interactive model design, breaking the interaction bottleneck. Specifically, instead of finding one ‘optimal’ model, our algorithms find many good models and visualize them, so that the user can interact with them to choose among them. We call this the *Rashomon set paradigm*. We have been developing algorithms for finding Rashomon sets and visualizing them. For instance, for decision trees, we developed an algorithm that finds all sparse good trees (Xin et al., 2022) and an interface for visualizing them that allows users to explore the models (Wang, Zhong, et al., 2022). For generalized additive models, Zhong et al. (2023) find an approximation of the Rashomon set, and Wang, Kale, et al. (2022) allow users to edit models within an [easy-to-use interface](https://interpret.ml/gam-changer). Liu, Zhong, Li, et al. (2022) also find a diverse set of scoring systems from the Rashomon set, and Oddo et al. (2024) provide an interactive visualization of it.

Chatterjee et al. (2025) discuss a pathological case where uniLasso might fail and propose a remedy by blending the uniLasso and lasso solutions. We see this as exemplifying an opportunity for deeper user involvement. An interactive modeling process in the Rashomon set paradigm would allow a user to do more than apply a universal sign-preservation constraint. Instead, they could selectively apply constraints, deciding on a feature-by-feature basis which signs to preserve, which to flip, and which to leave unconstrained. This iterative refinement, guided by domain expertise, offers a more flexible and powerful way to resolve such pathological cases. By embedding the user within the modeling loop, we transform model creation from a static optimization problem into a dynamic, collaborative dialogue between the data scientist and the domain expert, ultimately leading to models that are not only more accurate but are also ultimately more useful and better reflect knowledge of the domain.

## The Computational Challenge of User-Guided Modeling

Chatterjee et al.'s (2025) implementation is computationally efficient, thanks to their use of the highly optimized ‘glmnet’ package. Computational efficiency is an important step in ensuring that new methods can be readily adopted by the community. However, embracing the fully interactive, user-guided modeling process that we advocate introduces a broader computational challenge. Specifically, users may wish to impose a rich variety of domain-specific constraints—from sign preservation and feature budget limits to more complex logical or group-based rules, without necessarily knowing what those constraints are explicitly or in advance. While the adaptive lasso may induce more sparsity than lasso, it still produces single models, and its framework, even when implemented efficiently, is not easily extended to handle the arbitrary, often nonconvex, constraints that arise from deep-user interaction—without the user reformulating the problem—a task that is not realistically achievable for many users (e.g., physicians). How can we provide the users the flexibility to choose models that are optimized for complex criteria that may not even be known in advance?

If we switch back from

$$
\ell_1
$$

to

$$
\ell_0
$$

regularization, handling sparsity is more straightforward, as is sampling from a broader class of models to produce an approximation of the Rashomon set that the user can interact with. Even if users do not know the constraints or preferences in advance, they are able to use a visual interface to choose among a variety of models. We discussed how

$$
\ell_0
$$

is useful in that it does not distort the magnitudes of the nonzero coefficients. From a computational perspective, it is not as computationally demanding as one might think, given the speed of modern optimization algorithms. We can actually solve the

$$
\ell_0
$$

problem on many practical data sets despite the theoretical worst complexity. Modern solvers, leveraging techniques that use customized first-order methods, yield optimal and close-to-optimal solutions quickly (Liu, Zhong, Li, et al., 2022; Liu, Zhong, Seltzer, & Rudin, 2022; Liu, Rosen, et al., 2023; Liu, Zhang, & Rudin, 2024). We can also accelerate these first-order methods by running them on GPUs (Liu et al., 2025). Importantly, the new first-order methods permit efficient sampling from the Rashomon set, and these samples can be used for interactive tools. An interesting question is whether other approaches can be even more efficient or find a more complete representation of the Rashomon set.

## Our Interpretable Future

The work by Chatterjee et al. (2025) is more than just a new algorithm; it is a powerful reminder of the principles that should guide our pursuit of interpretable models. The existence of the Rashomon effect gives us the license to be creative in imposing constraints, the practice of user interaction provides the way to do that, and advances in computation provide the tools to do it. The path forward is exciting: we must build models not just from data, but with the domain experts who will use them. The question is no longer whether we can create interpretable models, but how we can best empower users to build them.

---

## Disclosure Statement

The authors have no financial or nonfinancial disclosures to share for this article.

---

## References

Babbar, V., McTavish, H., Rudin, C., & Seltzer, M. (2025). Near optimal decision trees in a SPLIT second*.* In *Proceedings of the 42nd International Conference on Machine Learning (ICML).*

Boner, Z., Chen, H., Semenova, L., Parr, R., & Rudin, C. (2024). Using noise to infer aspects of simplicity without learning. *Advances in Neural Information Processing Systems, 37,* 131824–131858.

Breiman, L. (2001). Statistical modeling: The two cultures (with comments and a rejoinder by the author). *Statistical Science*, *16* (3), 199–231. [https://doi.org/10.1214/ss/1009213726](https://doi.org/10.1214/ss/1009213726)

Chatterjee, S., Hastie, T., & Tibshirani, R. (2025). Univariate-guided sparse regression. *Harvard Data Science Review*, *7* (3). [https://doi.org/10.1162/99608f92.c79ff6db](https://doi.org/10.1162/99608f92.c79ff6db)

Liu, J., Rosen, S., Zhong, C., & Rudin, C. (2023). OKRidge: Scalable optimal k-sparse ridge regression. *Advances in Neural Information Processing Systems*, *36*, 41076–41258.

Liu, J., Shafiee, S., & Lodi, A. (2025). *Scalable first-order method for certifying optimal k-sparse GLMs.* In *Proceedings of the 42nd International Conference on Machine Learning (ICML).*

Liu, J., Zhang, R., & Rudin, C. (2024). FastSurvival: Hidden computational blessings in training Cox proportional hazards models. *Advances in Neural Information Processing Systems*, *37*, 87712–87765.

Liu, J., Zhong, C., Li, B., Seltzer, M., & Rudin, C. (2022). FasterRisk: Fast and accurate interpretable risk scores. *Advances in Neural Information Processing Systems*, *35*, 17760–17773.

Liu, J., Zhong, C., Seltzer, M., & Rudin, C. (2022). Fast sparse classification for generalized linear and additive models. In G. Camps-Valls, F. J. R. Ruiz, & I. Valera (Eds.), *Proceedings of the 25th International Conference on Artificial Intelligence and Statistics (AISTATS)* (pp. 9304–9333). PMLR.

Oddo, M., Liu, J., Munzner, T., Nguyen, F., Rudin, C., & Seltzer, M. (2024). *Riskomon: Card deck explorer for a FasterRisk Rashomon set*. Riskomon. [https://riskomon.netlify.app](https://riskomon.netlify.app/)

Rudin, C., Chen, C., Chen, Z., Huang, H., Semenova, L., & Zhong, C. (2022). Interpretable machine learning: Fundamental principles and 10 grand challenges. *Statistics Surveys*, *16*, 1–85. [https://doi.org/10.1214/21-SS133](https://doi.org/10.1214/21-SS133)

Rudin, C., Zhong, C., Semenova, L., Seltzer, M., Parr, R., Liu, J., Katta, S., Donnelly, J., Chen, H., & Boner, Z. (2024). Amazing things come from having many good models. In *Proceedings of the 41st International Conference on Machine Learning (ICML)* (pp. 42783–42795). PMLR.

Semenova, L., Chen, H., Parr, R., & Rudin, C. (2023). A path to simpler models starts with noise. *Advances in Neural Information Processing Systems, 36,* 3362–3401.

Semenova, L., Rudin, C., & Parr, R. (2022). On the existence of simpler machine learning models. In *Proceedings of the 2022 ACM conference on fairness, accountability, and transparency* (pp. 1827–1858). Association for Computing Machinery. [https://doi.org/10.1145/3531146.3533232](https://doi.org/10.1145/3531146.3533232)

Wang, Z. J., Kale, A., Nori, H., Stella, P., Nunnally, M. E., Chau, D. H., Vorvoreanu, M., Vaughan, J. W., & Caruana, R. (2022). Interpretability, then what? Editing machine learning models to reflect human knowledge and values. In *Proceedings of the 28th ACM SIGKDD international conference on knowledge discovery & data mining* (pp. 4132–4142). Association for Computing Machinery. [https://doi.org/10.1145/3534678.3539074](https://doi.org/10.1145/3534678.3539074)

Wang, Z. J., Zhong, C., Xin, R., Takagi, T., Chen, Z., Chau, D. H., Rudin, C., & Seltzer, M. (2022). TimberTrek: Exploring and curating sparse decision trees with interactive visualization. In *Proceedings of the IEEE visualization and visual analytics conference* (pp. 60–64). IEEE. [https://doi.org/10.1109/VIS54862.2022.00021](https://doi.org/10.1109/VIS54862.2022.00021)

Xin, R., Zhong, C., Chen, Z., Takagi, T., Seltzer, M., & Rudin, C. (2022). Exploring the whole Rashomon set of sparse decision trees. *Advances in Neural Information Processing Systems*, *35*, 14071–14084.

Zhong, C., Chen, Z., Liu, J., Seltzer, M., & Rudin, C. (2023). Exploring and interacting with the set of good sparse generalized additive models. *Advances in Neural Information Processing Systems, 36,* 56673–56699.

Zhu, C. Q., Tian, M., Semenova, L., Liu, J., Xu, J., Scarpa, J., & Rudin, C. (2025). Fast and interpretable mortality risk scores for critical care patients. *Journal of the American Medical Informatics Association*, *32* (4), 736–747. [https://doi.org/10.1093/jamia/ocae318](https://doi.org/10.1093/jamia/ocae318)

---